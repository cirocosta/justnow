justnow
=======

> Get stuff in realtime.

|    From    |           Scopes           |
| ---------- | -------------------------- |
| Twitter    | Public, User, Site         |
| Foursquare | User, Venue                |
| Instagram  | Users, Tags, Location, Geo |
| Facebook   | User, Place                |


## Realtime?

**/TODO** explain how realtime happens, what are the current docs around it (some guidelines, what people are doing, etc) and what people means by realtime in a lot of different cases.

**//TODO** Check [pubsubhubbub](http://pubsubhubbub.googlecode.com/svn/trunk/pubsubhubbub-core-0.3.html).

### Types of realtime

**/TODO** explain the different types of realtime APIs that we have.


## APIs

Here comes some description of the most famous public services APIs. Some of them quite sucks but it is worthwhile having them sometimes.

### [Twitter](https://dev.twitter.com)

The realtime twitter api is described on their documents section *[The Streaming APIs](https://dev.twitter.com/docs/api/streaming)*.

As they say:

> A proper implementation of a streaming client will be pushed messages indicating Tweets and other events have occurred, without any of the overhead associated with polling a REST endpoint

It separates in three categories: [Public](https://dev.twitter.com/docs/streaming-apis/streams/public), [User](https://dev.twitter.com/docs/streaming-apis/streams/user) and [Site](https://dev.twitter.com/docs/streaming-apis/streams/site) streams.

#### Public

This is the most interesting as it does not require any logging from a user.

| method |      endpoint     |
| ------ | ----------------- |
| POST   | statuses/filter   |
| GET    | statuses/sample   |
| GET    | statuses/firehose |

#### User

| method | endpoint |
| ------ | -------- |
| GET    | user     |



#### Site

| method | endpoint |
| ------ | -------- |
| GET    | site     |

### [Foursquare](https://developer.foursquare.com/overview/realtime)

#### User push API

#### Venue Push API

### [Instagram](http://instagram.com/developer/realtime/)

|    what   | desc |
| --------- | ---- |
| Users     |      |
| Tags      |      |
| Locations |      |
| Geo       |      |

### [Facebook](https://developers.facebook.com/docs/graph-api/real-time-updates/)

> The Graph API has a feature called 'Real Time Updates' that enables apps to subscribe to changes in certain pieces of data. When a change occurs, an HTTP 'POST' request will be sent to a callback URL belonging to that app. (...) real-time updates only indicate that a particular field has changed, they do not include the value of those fields.
