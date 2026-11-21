
- Allows the collection of data during runtime.
- Ref & Fn::GetATT = allows referencing of one logical resource or template within another
- Fn::Join & FN::Split - allows joining or splitting of strings (such as an IP4 and a web address so anyone can access)
- Fn::GetAZs & FN::Select - allows getting of list of az's in a region and select one from that list
- Conditions (Fn::IF, And, Equals, Not & Or) -used to provision resources on conditional checks (big instances on prod and small on dev )
- Fn::Base64 & Fn::Sub - accept non-encoded text and outputs base64 encoded texts to provide to resources. Sub allows substitutions within resources based on conditions
- Fn::Cidr - allows building of Cidr blocks within a network

Ref and Fn::GetAtt:
	- Using !Ref on template or pseudo parameters returns their value. When used with logical resources, the physical ID is usually returned
	- Using !GetAtt can be used to retrieve any attribute associated with the resource. Most logical resources return detailed configuration of the physical resource

Fn::GetAZs and Fn::Selection
	- GetAZs returns a list of AZs in the explicit region, or the current region
	- Fn::Select returns an object from a list of objects. Lists start at index 0 meaning the first object
	- These two make templates portable by not hard locking the region or objects

Fn::Join and Fn::Split
	- Split turns a string, ex. "roffle/truffles/penny/winke", into a list, "roffle, truffles, penny, winkie"
	- Join DOES THE OPPOSITE OF SPLIT

Fn::Base64 & Fn::Sub
	- FnBase64 takes not-encoded text and turns it into Base64 which is the necessary format of text within metadata
	- FnSub swaps out variables in the input, with their actual runtime values.

Fn::CIDR
	- can use to reference CIDR Range, tell how many subnets you want to allocate and their size. It will then output a list of CIDR ranges to use within subnets within a VPC. And use the Select function to allocate them to subnets individually. 