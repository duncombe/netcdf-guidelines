# Hierarchy of Data Dissemination

An attempt to organize concepts into a hierarchical framework. See also a
glossary of acronyms at [https://duncombe.github.io/glossary]

(metadata) - describes data    
  - included with data in the same file    
  - in a separate file in the same folder    
(data) <- is contained in a file

(data+metadata) <- is stored 
  - in real time     
    - QC according to QARTOD
    - delivered in NRT
  - recorded for later download and offline QC   
  
(QC data+metadata) <- is in a 
  - file <- has a format which can be 
    - binary (proprietary)
    - netCDF (formatted binary) <- has 
      - attributes 
        - non-conforming
        - ACDD conforming
        - CF Convention conforming
      - netCDF 
      - netCDF3 
      - netCDF4-classic
      - netCDF4 (contains HDF5)
    - HDF-4 (incompatible with HDF5)
    - HDF-5 (incompatible with HDF4)
    - ascii 
      - free format
      - CSV, comma separated values
      - TSV, tab separated values
    - 

WSDD provides guidance on dissemination of:    
- (data in files)  distributed by   
  - THREDDS: which has services   
    - ncSOS (adds OGC SOS service complies with IOOS SWE Milestone 1.0 and CF1.6 Discrete sampling Geometries)   
    - OPeNDAP (DAP2)   
    - ncWMS   
    - WCS Web Coverage Service   
    - ncISO   
    - NcML   
    - netCDF Subset Service   
  - ERDDAPP   
  - DODS
    - OPeNDAP
  
  
## Formats
- netCDF (origin UCAR)
- HDF4  incompatible with HDF5
- HDF5  incompatible with HDF4
- ascii 
- CSV/TSV
- CDF (origin NASA)


## Conventions or Standards
- ACDD 
- WSDD 
- CF Conventions
- QARTOD

## Data Servers
- THREDDS
- ERDDAPP   
- DODS

## Data Service Protocols
- ncSOS 
- OPeNDAP (DAP2)   
- ncWMS   
- WCS Web Coverage Service   
- ncISO   
- NcML   
- netCDF Subset Service   

## Institutions
- OGC 
- IOOS 

  
  
  
  
  
