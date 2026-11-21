

- Facial recognition
- Can monitor the contents (people, objects, animals) in video and images
- Can even manage live video and send it to Kinesis Stream for security
- Can analyze emotions on humans faces as well, can find identities
- Images are stored on S3, that counts as an event, Lambda is activated, it calls Rekognition, Rek. analyzes the object or video and keeps the meta data is DDB