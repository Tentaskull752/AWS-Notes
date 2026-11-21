
- Mappings object contain many mapping logical resources.
- Which map keys to values, allowing lookup; ex. provide a key and get a value back
- Can have one key, or Top & Second level
- Mappings use the !FindInMap intrinsic function
- Common use....retrieve AMI for given region & architecture
- Improve Template Portability
- !FindInMap ["RegionMap", Ref 'AWS::Region', "HVM64"] and in the example, the AMI ID is returned after searching for these qualificaitons