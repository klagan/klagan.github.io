---
published: true
tags: azure
---
* **Azure Scripting**
  * Basic scripting to achieve automation and used for ad-hoc configuration
* **Azure Desired State Configuration**
  * Ensure resource adheres to a baseline configuration
* **Azure Automation**
 * Schedule actions by time and/or triggers
* **Azure Deployment Templates**
 * Method to deploy a group of resources as a solution.  This is achieved through declarative configuration

###### So which one should I use? #####

There is no answer to this.  The should understand what each does and then choose what makes you feel more comfortable.

Scripting is the way it should be done.  But I come from a coding background.  That is what I would naturally say.

JSON is for declaring static information and the advantage of using a declarative construct like JSON would be that the functions that work on it would be in the control of Microsoft who could provide less breaking changes as they can manage their code to work around new declarative switches or schemas without the deployer ever knowing.

Microsoft probably got burnt with the whole ASM to ARM migration which personally, I didn't think was too bad.

JSON is being used as a programming tool which is **not** what it was designed for.  

Forcing things to do things they weren't designed for is never really a good place to start.  But on the other hand it is the weapon of choice for infrastructure behemoths like AWS so this would add familiarity to migrators.  

Who knows?

Todays hero is always tomorrows villian.
