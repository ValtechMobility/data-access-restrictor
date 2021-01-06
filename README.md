# Data Access Restrictor

Simple and fast access restrictor for data.

## Motivation

In a connected world, it is sometimes better to restrict the data, which is accessible.
This could help to protect:
 * the data
 * the data sources
 * the business logic used to process the data.
But it mainly protects the data owner from being profiled.

In this repository you will find a working solution for such a data access restrictor. A simple nginx solution. It could be configured through an API and holds configuration and last access times in memory. So it's a perfect starting ground for further extensions.
## Usage

Place this data access restrictor in front of your HTTP Interface you want to protect.
Then configure the URIs you want to protect by `POST /rate_limit/PT10H/URI_TO_PROTECT`.
Now access to this URI will be restricted to be queried just once every 10 hours.
