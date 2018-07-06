# BookingBug Importer

A mechanism to easily push configuration such as *Companies*, *People (staff)*, *Resources* and *Users* into BookingBug from an external source.

![High level diagram](https://github.com/BookingBug/importer-specs/blob/master/visualisations/high-level-diagram.png)

## Why does the Importer exist?

There is a common need for clients/customer of BookingBug to sync their data with ours. Data such as branch/locations (companies) and People are required to allow BookingBug to correctly functionality and provide a Booking service.

## Who is it for?

The importer is aimed at large customers that want to automate the configuration of BookingBug. However, it can also be used do one-off uploaded for initial config.

### User cases:

#### One-off initial data/config load
**Usercase:** A small to medium size business/client provides a set of a dataset (maybe CSV).

**Action:** Transform them into the correct JSON schema and upload to the importer via the API

#### Continous Sync via HTTP endpoint
**Usercase:** A medium to large size business with an IT dept builds an application that does scheduled pushes into the API. Repeatly keeping data objects like Companies, People, etc up-to-date.

**Action:** Client builds to BB Importer JSON specification. Then uses credentials we provide to push JSON payloads into BB Importer API.

#### Continous Sync via SFTP site
**Usercase:** A medium to large size business with an IT dept builds a file feed to our JSON schema that they drop onto their SFTP site.

**Action:** A Importer FTP integration is set up to pull from this FTP site using credentials provided. The files are then pushed via HTTP into the BookingBug Importer API.

## Where does it live?
Currently its accessible via the BookingBug Admin API. Login credentials are required.
