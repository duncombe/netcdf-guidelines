netcdf-guidelines
=================

Notes: 

1. Suggestion of an alternate name: opendap-guide?       
   _OPeNDAP_ - Open-source Project for a Network Data Access Protocol. OPeNDAP is both the name of a non-profit organization and the commonly-used name of a protocol which the OPeNDAP organization has developed.     
   _netCDF_ -  Network Common Data Format -- a set of software libraries and self-describing, machine-independent data formats that support the creation, access, and sharing of array-oriented scientific data.   
NetCDF describes a file format. OPeNDAP is a network protocol to describe how to fetch a file?   
     
2. This document will serve to formulate a coherent email to circulate for input. 
     
3. Need to set up a task to create the gold standard data set.      
   What happens if we take that set of data and load it into:
      - THREDDS? 
      - ncSOS? 
      - ncISO?    
    
      

4. Draft of the document starts below:

# netCDF Guidelines
## Documentation and examples of IOOS compliant netCDF files.

TODO: 
   - 
   - start with the [NODC templates](http://www.nodc.noaa.gov/data/formats/netcdf/v1.1/). *Since IOOS channels data to NODC we should reiterate NODC's hope that providers will see the benefits in structuring data to the template conventions.*
   
   I think there are TDS endpoints on their page, look through the rubric scores to see how they are doing.

This repository provides documentation links and examples to encourage the IOOS community to more effectively use OPeNDAP, netCDF and related technologies to achieve interoperability.  [Hankin, et al](http://www.oceanobs09.net/proceedings/cwp/cwp41/), provide an excellent summary of how the trio of standards evolved and arguments for continuing a path toward interoperability based largely on the standards. This document, and the accompanying repository of material provides specific guidance for IOOS data providers, especially the 11 regional associations, shall implement the recommendations of [Hankin, et al](http://www.oceanobs09.net/proceedings/cwp/cwp41/). Additionally, this repository will provide examples of good data files and guidance for configuring OPeNDAP servers. 

Information abouut netCDF [here](http://www.unidata.ucar.edu/software/netcdf/docs/faq.html).

The primary objective of this document is to ensure that the data published according to these guidelines fit into the larger DMAC system and enables the following capabilities.

1. Through the use of tools like [ncISO](http://www.ngdc.noaa.gov/eds/tds/), high quality discovery metadata can be harvested from IOOS data services which can be loaded into discovery portals like the [IOOS Service Registry](https://geo-ide.noaa.gov/wiki/index.php?title=ESRI_Geoportal#IOOS_WAFs) at NGDC.
2. Ensure capabilities of supported client software (e.g. ensure that [ncSOS](https://github.com/asascience-open/ncSOS/wiki) can generate valid SOS responses from the underlying netCDF-CF-OPeNDAP data set)
3. Integrate into supported delivery to operational systems like data assimilating ocean models, etc., *(need help here, do we have any of these?) UAF?*
4. Ensure that any data published according to these guidelines is immediately acceptable as an archive submission to NODC.
5. Identify areas where the supporting technologies are insufficient and in need of further development, or alternatively, identify practices which are well tested in realistic systems from those that are new or experimental (e.g. do we have a best practice for serving collections of trajectories?)

## Scope
Is this primarily about netCDF files or should it extend to include guidance for TDS, ERDDAP etc?

Do we discuss the relationship to Archives?

Organization of the material??
- By standard?
- By platform?
- By DSG?
- By discipline?

* DSG
    * point

##Creating data files
* netCDF: NODC provides templates for the production of preservable, discoverable accessible and interoperable data. 
Since IOOS channels data to NODC we reiterate NODC's hope that providers will see the benefits in structuring data to the template conventions.

   - The NOAA National Oceanographic Data Center (NODC) has developed netCDF templates based on what are called "feature types" by Unidata and CF. These templates conform to Unidata's netCDF Attribute Convention for Dataset Discovery (ACDD) and netCDF Climate and Forecast (CF) conventions. Adding to these established conventions, NODC also provides several recommendations for both netCDF variables and attributes. These best practices capture NODC's experience in providing long-term preservation, scientific quality control, product development, and multiple data re-use beyond its original intent.
These templates are intended as a service to our community of Data Producers, and are also being used internally at NODC in our own data development efforts. We hope the templates will serve as good starting points for Data Producers who wish to create preservable, discoverable, accessible, and interoperable data. It is important to note that these templates do not represent an attempt to create a new standard, and they are not absolutely required for archiving data at NODC. However, we do hope that you will see the benefits in structuring your data following these conventions and NODC stands ready to assist you in doing so.
We have published Version 1.0 of these templates at: http://www.nodc.noaa.gov/data/formats/netcdf/ Please see that page for more information, including access to the templates, a decision tree, and real-world examples following the templates. -- [NODC NetCDF Templates page](http://www.nodc.noaa.gov/data/formats/netcdf/v1.1/) page.  

   * CF (Climate and Forecast)
      
   * ACDD
   * Community specific conventions (IOOS Gliders, OceanSITES, Argo) 
   ( don't describe each just mention that another level of profiling or constraining the more general conventions is common.)
   * UGrid (Gridspec?)
   
##Publishing data files using Data Access Services
* THREDDS Data Server
  * Example catalogs for common use cases

##Individual Components
###netCDF
Other than simple text file formats like CSV, netCDF is probably the most common file format used for exchanging oceanographic and meteorological information.
The emphasis of this document is on how netCDF is used in conjunction with other technologies to achieve interoperability within the network of web based data access services. For example data content standards apply to the DAP dataset accessed through an OPeNDAP server and not necessarily to the underlying netCDF files. 

**REQUIREMENT**: All IOOS data shall use the netcdf3 interface or the netcdf4-classic interface.

### Climate and Forecast and other netCDF Conventions
Do I include a complete description of each data type or platform type here?
Mention the compliance checker here or in the next higher section. Or, mention it in both. Introduce it in the next higher section and then show examples of how it can be run against some of the example data for a specific convention in the lower level section.

### Attribute Conventions for Dataset Discovery
####Version x.y

####Examples


####Test data

####Statement of requirements


###Setting within the larger system, archive package, ncsos, automated asset inventory, maximal use of discovery portals 

Example netcdf files for each in with platform, regular and irregular grids

###Relationship to other standards and a picture explaining the role each standard plays.

Example configurations for each server type, really just thredds and erddap

A similar repo for sos should include the templates, wsdd, and the list of tests we run.

How can you participate? Fork, pull request etc

## Resources

[NGDAC-NetCDF-File-Format-Version-2](https://github.com/ioos/ioosngdac/wiki/NGDAC-NetCDF-File-Format-Version-2)


##References

Hankin, S. & Co-Authors (2010). "NetCDF-CF-OPeNDAP: Standards for Ocean Data Interoperability and Object Lessons for Community Data Standards Processes" in Proceedings of OceanObs’09: Sustained Ocean Observations and Information for Society (Vol. 2), Venice, Italy, 21-25 September 2009, Hall, J., Harrison, D.E. & Stammer, D., Eds., ESA Publication WPP-306, doi:10.5270/OceanObs09.cwp.41
http://www.oceanobs09.net/proceedings/cwp/cwp41/

Paper written by R. Signell and D. Snowden.

Thredds

Netcdf

Web site created by Matt Howard employee

ACDD

CF

Topics

http://erddap.marine.rutgers.edu/erddap/tabledap/allRutgersGliders.png?longitude,latitude,time&.draw=linesAndMarkers&.marker=2|5&.color=0xFFFFFF&.colorBar=Rainbow2




