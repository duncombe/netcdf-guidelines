# Hierarchy of Data Dissemination

(metadata) - describes data    
  - included with data in the same file    
  - in a separate file in the same folder    
(data) <- is contained in a file

(data+metadata) <- is stored 
  - in real time (QARTOD)
  - recorded for later download    
  
    - file <- has a format which can be 
      - binary (proprietary)
      - netCDF (formatted binary) <- has 
        - attributes 
          - non-conforming
          - conform to convention, e.g., ACDD 
      - HDF-4/HDF-5
      - ascii 
        - free format
        - CSV, comma separated values
        - TSV, tab separated values
      - 

WSDD provides guidance on dissemination of:    
(data in files) is distributed by 
  - THREDDS has services
    - ncSOS (adds OGC SOS service complies with IOOS SWE Milestone 1.0 and CF1.6 Discrete sampling Geometries)
    - OPeNDAP (DAP2)
    - ncWMS
    - WCS Web Coverage Service
    - ncISO
    - NcML
    - netCDF Subset Service
  - ERDDAPP
  - DODS


