# A MongoDB-based store for Quartz.

This is a fork of a project originally started by MuleSoft. It supports all Quartz trigger types and
tries to be as feature complete as possible.


## Usage

To configure, set your Quartz properties to something like this:

    # Use the MongoDB store
    org.quartz.jobStore.class=com.mulesoft.quartz.mongo.MongoDBJobStore
    # comma separated list of mongodb hosts/replica set seeds
    org.quartz.jobStore.addresses=host1,host2
    # Mongo database name
    org.quartz.jobStore.dbName=quartz
    # Will be used to create collections like mycol_jobs, mycol_triggers, mycol_calendars, mycol_locks
    org.quartz.jobStore.collectionPrefix=mycol
    # not sure why Quartz requires this, but it does and we don't use it
    org.quartz.threadPool.threadCount=1


## License

[Apache Public License 2.0](http://www.apache.org/licenses/LICENSE-2.0.html)


## FAQ

### Why the Fork?

MuleSoft developers did not respond to attempts to submit pull requests for several months. As more and more
functionality was added, I decided to completely separate this fork form GitHub forks network because it is
very different. All changes were made with respect to the Apache Public License 2.0.