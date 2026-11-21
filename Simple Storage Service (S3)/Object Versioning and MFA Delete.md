
## Personal Notes

 Object Versions:
  - Controlled at the bucket level, starts off disabled and once enabled, it can NEVER be disabled. It can be suspended and then re-enabled. 
  - Without enabling, each object is identified by it's ID or name specifically. 
  - Versioning lets you store multiple versions of objects within a bucket. Operations which would modify objects generate a new version.
  - When versioning is disabled, the ID of an object is null, since it's the one of itself.
  - The newest version of any object within a bucket is known as the Latest Version or Current Version. Unless specified, the Latest Version will always be provided. 
  - If you ask to delete an object but don't specify which version; a Delete Marker is created that makes all the previous versions of the objects look deleted/hidden. Delete this and the objects appear again.
  - To properly delete an object, just specify the version by Name/ID to make it genuine.
  - If you delete the Current Version of an object, the original or next-sooner version then becomes the Current Version.
  - Space is consumed by all versions of an objects; only way to 0 costs - is to delete the bucket. 

MFA Delete:
   - Enabled within the versioning configuration of a bucket.
   - When enabled, MFA is required to change bucket versioning state. 
   - MFA is also required to delete versions.
   - To do any of the previous actions, you must provide the serial number + Code passed with API Calls.