# Fermi LAT Schema
GCN notices are machine-readable packets that are available in different formats; text, binary, and VOEvent. For each event and instrument-specific, different types of notices are available. Each type of notice contains different properties.

In this example, Fermi-LAT GCN notice is used as a text file, then schema and example are created as following steps:

* Extract the URL of the GCN notice text file from the HTML table at: https://gcn.gsfc.nasa.gov/fermi_lat_mon_trans.html using the BeautifulSoup library
* Convert the notice text into json example file, `fermi_lat_example.json`
* Generate the JSON schema as `fermi_lat_schema.json` using genson from the provided JSON example
* Validate the schema example against the JSON schema using Draft7Validator

## Kafka notices
> Typical Fermi LAT GCN notice contains the following information:

 Properties | Type | Value
 --------------- | ----------- |-------------------
 `TITLE` | string | `GCN/FERMI NOTICE`
 `NOTICE_DATE` | string | `Thu 23 Feb 23 15:49:32 UT`
 `NOTICE_TYPE` | string | `Fermi-LAT Monitor`
 `SOURCE_OBJ` | string | `BLLac_86400.png`
 `REF_NUM` | string | `1677167372`
 `RA` | string | `330.680d {+22h 02m 43s} (J2000),`
 `DEC` | string | `+42.278d {+42d 16\' 40"} (J2000),`
 `CURR_FLUX` | string | `1.70e-06 +- 6.50e-08 [ph/cm2/sec]`
 `BASE_FLUX` | string | `6.99e-07 +- 1.59e-07 [ph/cm2/sec]`
 `SIGNIFICANCE` | string | `5.59 [sigma]`
 `TIME_SCALE` | string | `0  {0=1day, 1=1week}`
 `ENERGY_BAND` | string | `0.1 - 300.0 [GeV]`
 `OUTBURST_DATE` | string | `19997 TJD;    53 DOY;   23/02/22 (yy/mm/dd)`
 `OUTBURST_TIME` | string | `43200.00 SOD {12:00:00.00} UT`
 `SOLN_STATUS` | string | `0x0`
 `LC_URL` | string | `http://fermi.gsfc.nasa.gov/FTP/glast/data/lat/catalogs/asp/current/lightcurves/BLLac_86400.png`
 `SUN_POSTN` | string | `336.62d {+22h 26m 28s}   -9.76d {-09d 45\' 42"}`
 `SUN_DIST` | string | `52.41 [deg]   Sun_angle= 0.4 [hr] (West of Sun)`
 `MOON_POSTN` | string | `19.50d {+01h 17m 59s}   +6.71d {+06d 42\' 18"}`
 `MOON_ILLUM` | string | `15 [%]`
 `GAL_COORDS` | string | `92.59,-10.44 [deg] galactic lon,lat of the burst (or transient)`
 `ECL_COORDS` | string | `354.26, 49.58 [deg] ecliptic lon,lat of the burst (or transient)`
 `COMMENTS` | string | ``
 
 
