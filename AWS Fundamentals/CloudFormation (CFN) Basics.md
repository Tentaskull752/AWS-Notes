
### Personal Summary

  - CloudFormation is a tool to create, delete, or update infrastructure templates within AWS.
  - All templates have a list of resources; if resources are added, deleted, or updated, then the template performs those actions. 
  - Description is a text field that gives the author of a space to let users know what resources do and how the template is formatted. 
  - IF YOU HAVE A DESCRIPTION AND AN AWS TEMPLATE FORMAT VERSION, THE DESCRIPTION NEEDS TO IMMEADIATELY FOLLOW THE TEMPLATE FORMAT VERSION.
  - Template Format Version: allows extending of standards over time. 
  - Meta-Data: controls how the items of the template are presented through the console U.I. 
  - Conditions: allow decision-making in the template, certain things won't happen in the template unless certain conditions are met. 

 - When a template is given to cloudformation, any resources within the template, are then labeled as "logical resources". For e.x, if there's a logical resource in the template, named instance, it will have a type (AWS), and a list of properties further telling of it's configuration. The purpose of cloudformation is to take this template of code and turn it into physical resources in your AWS console. Cloudformation will take all of the logical resources within the template and form a "Stack", a list of logical resources that will be converted into physical resources. And this stack can later be altered if a new template is introduced, in which it adds, deletes, or updates the configuration of the logical resources.
 


### Revealing Questions







### Insightful Links