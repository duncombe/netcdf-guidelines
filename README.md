netcdf-guidelines
=================

Documentation and examples of IOOS compliant netCDF files.

TODO clarify this email into a coherent email that I can use to circulate for input. Include a task to create the gold standard data set and start with the nodc templates. What happens if we take that set of data and load it in to thredds now? Ncsos? Nciso? I think there are TDS endpoints on their page, look through the rubric scores to see how the are doing

Name, opendap-guide?

This repository provides documentation links and examples to encourage the IOOS community to more effectively use OPeNDAP, netCDF and related technologies to achieve interoperability.  [Hankin et al](http://www.oceanobs09.net/proceedings/cwp/cwp41/) provide an excellent summary of how the trio of standards evolved and arguments for continuing a path toward interoperability based largely on the standards. This document, and the accompanying repository of material provides specific guidance for IOOS data providers, specifically the 11 regional associations, shall implement the recommendations of Hankin et al. Additionally, this repository will provide examples of good data files and guidance for configuring OPeNDAP servers.  
The primary objective of this document is to ensure that the data published according to these guidelines fit into the larger DMAC system and enables the following capabilities.
1. Through the use of tools like nciso link, high quality discovery metadata can be harvested from IOOS data services which can be loaded into discovery portals like the IOOS Service Registry link at NGDC.
2. Ensure capabilities of supported client software (e.g. ensure that ncSOS link can generate valid SOS responses from the underlying netCDF-CF-OPeNDAP data set)
3. Integrate into supported delivery to operational systems like data assimilating ocean models, etc (need help here, do we have any of these?) UAF?
4. Ensure that any data published according to these guidelines is immediately acceptable as an archive submission to NODC.
5. Identify areas where the supporting technologies are insufficient and in need of further development, or alternatively, identify practices which are well tested in realistic systems from those that are new or experimental (e.g. do we have a best practice for serving collections of trajectories?)
# Scope
Is this primarily about netCDF files or should it extend to include guidance for TDS, ERDDAP etc?

Do we discuss the relationship to Archives?

Organization of the material??
By standard?
By platform?
By DSG?
By discipline?

* DSG
    * point
    * 
#Creating data files
* netCDF
   * CF
   * ACDD
   * Community specific conventions (IOOS Gliders, OceanSITES, Argo) ( don't describe each just mention that another level of profiling or constraining the more general conventions is common.)
   * UGrid (Gridspec?)
   
#Publishing data files using Data Access Services
* THREDDS Data Server
  * Example catalogs for common use cases

#Individual Components
##netCDF
Other than simple text file formats like CSV, netCDF is probably the most common file format used for exchanging oceanographic and meteorological information.
The emphasis of this document is on how netCDF is used in conjunction with other technologies to achieve interoperability within the network of web based data access services. For example data content standards apply to the DAP dataset accessed through an OPeNDAP server and not necessarily to the underlying netCDF files. 

**REQUIREMENT**: All IOOS data shall use the netcdf3 interface or the netcdf4-classic interface.

## Climate and Forecast and other netCDF Conventions
Do I include a complete description of each data type or platform type here?
Mention the compliance checker here or in the next higher section. Or, mention it in both. In troduce it in the next higher section and then show examples of how it can be run against some of the example data for a specific convention in the lower level section.

### Attribute Conventions for Dataset Discovery
Version x.y

Examples


Test data

Statement of requirements


#Setting within the larger system, archive package, ncsos, automated asset inventory, maximal use of discovery portals 

Example netcdf files for each in with platform, regular and irregular grids

#Relationship to other standards and a picture explaining the role each standard plays.

Example configurations for each server type, really just thredds and erddap

A similar repo for sos should include the templates, wsdd, and the list of tests we run.

How can you participate? Fork, pull request etc

#References
Hankin, S. & Co-Authors (2010). "NetCDF-CF-OPeNDAP: Standards for Ocean Data Interoperability and Object Lessons for Community Data Standards Processes" in Proceedings of OceanObs’09: Sustained Ocean Observations and Information for Society (Vol. 2), Venice, Italy, 21-25 September 2009, Hall, J., Harrison, D.E. & Stammer, D., Eds., ESA Publication WPP-306, doi:10.5270/OceanObs09.cwp.41
http://www.oceanobs09.net/proceedings/cwp/cwp41/

Paper written by rich and me
Thredds
Netcdf
Web site created by Matt Howard employee
ACDD
CF
Topics

http://erddap.marine.rutgers.edu/erddap/tabledap/allRutgersGliders.png?longitude,latitude,time&.draw=linesAndMarkers&.marker=2|5&.color=0xFFFFFF&.colorBar=Rainbow2|||||
