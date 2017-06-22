---
layout: page
title: REST API
permalink: /rest-api/
---

This [Time Series Database][tsdb] is designed with the Web in mind
and it use the [REST][rest] architectural style. It is implemented
targeting the highest level (3) of the [Richardson Maturity Model][rmm]

Bellow you will find a comprehensive list of all the kind of resources
exposed as part of the [Time Series Database][tsdb] API, the supported
operations over those resources and the relations established between
them.

    Note for developers:
        Do not hardcode path to resources exposed by the Time Series
        Database API. This could render your client useless if a
        resource is relocated for any reason. Use the relations
        described below to drive your client interactions with the
        Time Series Database.

# Root Resource

The Root Resource is the only publicly known entry point into the
[Time Series Database][tsdb] API. It offers information about the
implementation of the [Time Series Database][tsdb] (such as version,
capacity, etc.) and provide links to other [Time Series Database][tsdb]
resources that are part of its API.

Links on the Root Resource are identified by the following possible
relations:

 - **https://tsdb.org/relations/has-ts-collection**: Is used to mark
   the link on the Root Resource leading to the Time Series collection.

[rest]: https://en.wikipedia.org/wiki/Representational_state_transfer
[rmm]: http://martinfowler.com/articles/richardsonMaturityModel.html
[tsdb]: https://en.wikipedia.org/wiki/Time_series_database