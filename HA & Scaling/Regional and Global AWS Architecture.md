

Global Components:
 - Global Service Location & Discovery: Global DNS is used for service discovery and regional based health checks and request routing.
 - Content Delivery (CDN) and optimization: CDN's are used to cache content globally - as close to end users as possible to improve performance.
 - Global health checks & failover


Regional Components:
 - Scaling & Resilience
 - Application Services and components


 - Web-tier acts as an entry point for regional-based applications or application-components; a regional-based application service.
 - It draws customers away from the infrastructure, so these services could fail without any consequence in performance.
 - Compute-tier: comprised of EC2 and Lambda. Will consume storage services such as EBS, EFS, and S3. Cloudfront can cache data ex. movies, that are stored in S3. 
 - DB-tier: RDS, Aurora, DynamoDB, Redshift. A caching layer like Elasticache is used to access the DB instead of going directly to DB. This is to minimize reads to the DB; only when the cache doesn't have the wanted data, does a request go to the DB.