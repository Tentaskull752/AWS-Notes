

- Streams record changes in data within a database. Stream must be enabled within each table
- Streams are operating 24 hours a dat
- Can be an addition, updating, or deletion of data.
- There are four perspectives to view these changes: Keys_only(PK and SK). New images, Old images, and New & Old images (before and after the change, lets you see the difference of the item without consulting the database)

- Database Triggers: performs actions based on changes of data.
- Item changes generate an event
- That EVENT contains the data which was changed
- An action is taken using that data
- AWS = Streams + Lambda
- Reporting & Analytics
- Aggregation, Messaging or Notifications 