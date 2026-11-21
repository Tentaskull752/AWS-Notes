
## Personal Notes

 - A way to retrieve parts of objects instead of their entirety.
 - S3 can store HUGE objects(up to 5TB), and an infinite number of objects.
 - When you download a 5TB item, all 5TB is used for this action, filtering the object at the client side does not reduce this used space and the price billed by S3.
 - S3/Glacier select let you use SQL-Like statements to select part of the object, pre-filtered by S3. 
 - FASTER AND CHEAPER
 - Can work on multiple on file formats: CSV< Jason, Parquet, BZIP2 compression
 - Filtering can be up to 400% faster an 80% cheaper. 
 - Selection of this feature can be selected at the S3 service.