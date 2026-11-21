
### Personal Summary

 - S3 is a Global Storage Platform; when not used, it's stored at a specific region and won't leave if you originally assigned it there.
 - It's a public service (accessed from anywhere with a wifi connection), has unlimited data and multi-user
 - Movies, Audio, Photos, Text, Large Data sets
 - S3 delivers Objects and Buckets:
	 - Objects: the data that S3 sends. There's the Object and the Key that identifies the object within a bucket. The value(size) of an object can range from 0 bytes to 5 Terabytes. 
	 - Value: Content being stored within the data.
	 - Buckets: containers for data/objects. Creating a bucket within a region creates a private container; nothing leaves unless the owner wants. Blast radius of a disaster is region-sized. Bucket names must be globally-unique. Buckets can hold an unlimited number of objects, 0 - infinite bytes of data.
	 - All objects within the bucket are within the same level, everything stored in the bucket is at the same level. It's a flat hierarchy. Folders are represented in the bucket when objects have the object key structure of (ex.) /old/Koala3.jpg.

EXAM POWERUP:
 - Buckets are globally unique
 - 3-63 characters, all lowercase, no underscores
 - Start with a lowercase letter or number
 - Can't be formatted e.g. 1.1.1.1
 - Buckets - 100 soft limit, 1000 hard per account. You can split up a bucket of multiple objects belonging to more than 1 clients.

 - You CAN'T MOUNT an S3 bucket as (k:\ or /images)
 - S3 is great for large data storage, distribution or upload
 - Great for 'offload'
 - Input and or Output to MANY AWS products


### Revealing Questions







### Insightful Links