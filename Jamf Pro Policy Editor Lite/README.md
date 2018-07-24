# Jamf Pro Policy Editor Lite
## Edit a policy's version number via the API

---

## About

Since Jamf Pro PI-005903, I’ve been thinking of a faster way to update policies.

Last week, Adobe released six updates which — outside of building new packages via Adobe's admin console — effectively required only incrementing a version number **four** places in each policy (please don't tell @talkingmoose):
- Adobe After Effects CC _15.1.1_ was update to: Adobe After Effects CC _15.1.2_
- Adobe Media Encoder CC _12.1.1_ was update to: Adobe Media Encoder CC _12.1.2_
- Adobe Bridge CC _8.0.1_ was update to: Adobe Bridge CC _8.1_
- Adobe Premiere Pro CC _12.1.1_ was update to: Adobe Premiere Pro CC _12.1.2_
- Adobe Prelude CC _7.1_ was update to: Adobe Prelude CC _7.1.1_
- Adobe XD CC _9.1.12_ was updated to: Adobe XD CC _10.0.12_

With inspiration from @mm2270 [API scripts](https://github.com/mm2270/Casper-API/blob/master/Convert-SG-Search-Search-SG.sh), Jamf Pro Policy Editor Lite was born.

---

## Requirements

### API
To utilize this script, the API account must have the following privileges:  
- Policies: CREATE, READ, UPDATE
- Because of the need to use API credentials with Create privileges, the script allows you to interactively enter the credentials so they don't need to be stored within the script. (Thanks, mm2270)
- The script performs only minor error checking; please ensure proper API credentials or you will encounter errors

### Packages
The updated package must be present **before** running this script.

---

## Usage  

This script was designed to be run _interactively_ in Terminal and allows you to use the API (along with valid API credentials) to update a policy's version number.  

This script uses some **BASH** specific items; please first make the script executable:  
`chmod +x /path/to/Jamf\ Pro\ Policy\ Editor\ Lite.sh`  

To use the script:
`/path/to/path/to/Jamf\ Pro\ Policy\ Editor\ Lite.sh`  

---

## Warning

While the script does backup a policy's XML before performing updates, please thoroughly test before using in production.

---

## Special Thanks
- @mm2270
- @BIG-RAT