
 -   Monolithic architecture 
	 - has multiple stages of process to create a video within an application. It's done in one place, one code base, one component; but failure of one of these processes means the failure of the whole operation.
	 - Everything within the monolithic architecture scales together as well; need to scale vertically, bc everything is running on the same compute hardware. 
	 - All components are always running and so, always incur charges. Least cost effective way to architect systems. 

 - Tiered Architecture
	 - There are tiers, each with it's own function, it's bringing specialization to the architecture. 
	 - Individual tiers can be vertically scaled independently.
	 - Each tier, instead of being connected directly, internal load balancers can be filled within the tiers. THEY ARE NO LONGER COMMUNICATING WITH EACH OTHER. This allows horizontal scaling since the increase of function does not affect the other tiers.
	 - Though there is still the need of ALL the tiers functioning or else they collapse one by one, until complete failure.
	 - Each tier has to be running something for the app to function. 
	