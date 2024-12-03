
# Adding new Tools to Shinkai 
![img](./shinkai-logo-brand.svg)

# Dev Repository 
[Reposity URL](https://raw.githubusercontent.com/acedward/shinkai-tool-deploy/main/dev-repository.json) 

# Guidelines
> This guide is intended for deveopers for testing & development of tools and agents for Shinkai.  

This is a repository for development purposes, **do not trust the code in this repository**

# Tool Programming

> 1. Keep it simple, a tool should resolve a single issue.  
> 2. Normally integrations should be keep in different tools, so they can be reused.  
> 3. Try to keep arguments as minimal as possible.  
> 4. OAuth is in the roadmap, for now they signed in a standalone page, and copy the keys.  
> 5. Prefer API Keys over OAuth when possible.  
> 6. Scrapping is ok, and even perefered over complex setups.   
 
1. Select your **programming language**
    * Typescript (Deno)
    * Python
2. Program your **tool**.
    * Some minor limitations my apply, the code will run in a sandbox.
    * At the time you may have only one implementation file.
    * Function signature cannot be modified.
3. Add **assets** if required.
4. **Test** your tool.
    * Check for good inputs, bad inputs, null, invalid, etc.
    * In case of error throw an exception.
6. Check if the **Metadata** is valid and matches the inputs, config and outputs 
7. **Improve** name, description and keywords if required.
8. **Save** the tool
9. Press **export**, and copy the tool-name-v1.zip to this repository at `./packages/`
10. **Add** the tool-name-v1.zip to the `dev-repository.json`


# Agent Programming
TODO

# dev-repository.json
```json
{
  "packages": [{
    "name": "Tool Name",
    "path": "https://raw.githubusercontent.com/acedward/shinkai-tool-deploy/main/packages/tool-name-v1.zip"
  }]
}
```
