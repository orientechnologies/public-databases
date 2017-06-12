public-databases
================

This repository contains the registry of OrientDB public databases. The file `config.json` is read by OrientDB Studio web tool when the user looks for a public database to download.

![](https://orientdb.com/images/install-db.png)

![](https://orientdb.com/images/import-public-db.png)

If you would like to see your database to appear here, please update the `config.json` file adding your database information and send a Pull Request. We'll review your database and if everything is ok it will be updated and available to everybody. Your database can be hosted by your own or at Orient Technologies servers.

This is the format of `config.json` file:

```json
{
  "<database name>" : {
    "description" : "<description will appear in Studio>",
    "license" : "<license type>",
    "versions": {
      "<version as 3 numbers separated by dots. Example 02.00.00>" : {
        "compatibleFrom" : "<OrientDB version compatible>",
        "releasedOn" : "<release date, in the format: yyyy-MM-dd. Example: 2014-08-30>",
        "url": "<url of .zip file containing the database>"
      }
    }
  }
}
```

Example:
```json
{
  "GratefulDeadConcerts" : {
    "description" : "Database containing the concerts of the Grateful Dead band",
    "license" : "Creative Commons",
      "versions": {
        "02.00.00" : {
        "compatibleFrom" : "02.00.00",
        "releasedOn" : "2014-08-30",
        "url": "http://www.orientechnologies.com/public-databases/GratefulDeadConcerts.zip"
      }
    }
  }
}
```

Databases must be released as zip file of the folder containing the OrientDB database. The folder must contains no sub-folders. No hidden or special files are allowed (example: .DS_Store).

