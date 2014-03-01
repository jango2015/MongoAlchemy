Release Notes
=======================

All #xxx numbers are the github issues.  All releases 0.14 and before were added retroactively, so appologies for anything that isn't quite right.

0.14.3 -- 2013-11-28 10:43
-----------------------------
* [BUG] The elem match projection being used caused that field to be inaccessible on the object returned from the database


0.14 -- 2013-02-25 00:04
-----------------------------
* [FEATURE] #108: Add default_f, to allow a function to be used for default values
* [FEATURE] #107: Add normal pymongo sorting to query.sort and a new config, config_default_sort
* [FEATURE] #99: Schema migration via transform_incoming. This is a hook which allows schema migrations by allowing transforms of a document before MA touches it
* [BUG] #91: Saving a partial document raises FieldNotRetrieved

0.13.3 -- 2012-10-02 12:12
-----------------------------

* 0.13.2 and 0.13.1 had build issues
* [BREAKING] [FEATURE] #95: Check integrity on setting attributes, not on save
* [BREAKING] [FEATURE] #88: Support for transactions. The session with statement now opens and closes sessions.  Also added a caching mechanism.
* [FEATURE] #85: Timezone support. Pass a timezone into the session to enable. Times are always saved as UTC in the database.
* [BREAKING] The timezone feature also adds the requirement that unwrap functions on custom types to need take a session object (because the current session timezone needs to be accessible)
* [FEATURE] #28: Delegate to subclass. This allows subclasses with the same collection name
* [FEATURE] #7: Support for DBRefs. Check out RefField and SRefField in the fields documentation


0.12.2 -- 2012-09-10 01:32
-----------------------------
* [FEATURE] #92: Support for $exists. Thanks silversupreme!


0.12.1 -- 2012-05-20 18:13
-----------------------------
* [BUG] Use FloatField in GeoField


0.12 -- 2012-05-10 12:46
-----------------------------
* [FEATURE] geo index support


0.11.1 -- 2011-12-08 15:00
-----------------------------

* [BUG] Use pymongo 2.2 package re-ordering