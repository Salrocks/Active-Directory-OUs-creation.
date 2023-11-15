# Active-Directory-OUs-modifications.
Managing Organizational Units (OUs) in Active Directory, including their creation and deletion.

<h1>Description</h1>
The project involves the management of Organization Units (OUs) in Active Directory, encompassing tasks such as adding and removing OUs, as well as navigating through Active Directory's accidental protection features.



<h2>Languages and Utilities Used</h2>
- <b>Active Directory</b> <br>
- <b>Windows OS</b> 


<h2>Program walk-through:</h2>

<p align="center">

Active Directory is a crucial element in network security. To access it, you need to sign in as an administrator, granting access to powerful actions unavailable to regular users. Once opened, Active Directory appears as follows: <br/>
<img src="https://i.imgur.com/9T1O4m5.png" height="80%" width="80%" alt="OU modification"/>
<br />
<br />
On the left side, you'll find various folders called Organizational Units (OUs), serving as containers for categorizing users and machines. Opening any OU reveals its contained users, which can be edited. Administrators have the authority to create, delete, and modify users within OUs. For instance, let's explore the THM and IT OUs. On the right side, you'll see the users linked to the IT group.<br/>
<img src="https://i.imgur.com/bwrXQQO.png" height="80%" width="80%" alt="OU modification"/>
<br />
<br />
As a side note, Windows creates some default OUs on the left side, including Builtin, Computers, Domain Controllers, Users, and Managed Service Accounts. These OUs serve specific purposes:

- Builtin: Contains default groups for any Windows host. <br>
- Computers: Where new network machines are initially placed, but you can move them as needed.<br>
- Domain Controllers: Houses the default OUs for domain controllers. <br>
- Users: Contains default users and groups that apply domain-wide. <br>
- Managed Service Accounts: Holds accounts used by Windows domain services. <br/>
<img src="https://i.imgur.com/fF0zntS.png" height="80%" width="80%" alt="OU modification"/>
<br />
<br />
Returning to the OUs on the left side, creating a new OU is a straightforward process. You can do this by right-clicking, selecting "New," and then choosing "Organizational Unit" from the available options, as illustrated below. <br/> 
<img src="https://i.imgur.com/3J0Zild.png" height="80%" width="80%" alt="OU modification"/>
<br />
<br />

Following this, we will be prompt with a new screen as below. 
  <br/>
<img src="https://i.imgur.com/RwShUrH.png" height="80%" width="80%" alt="OU modification"/>
<br />
<br />
In the new window, this is where you specify the name for your new OU. As an example, let's create a new OU named "Help Desk" and ensure it has been successfully added to the Active Directory. <br/>
<img src="https://i.imgur.com/r5vwf2j.png" height="80%" width="80%" alt="OU modification"/>
<br />
<br />
Having covered the creation of new OUs, let's now explore the reverse process: how to delete an OU. If you right-click on an OU, you'll be presented with the option to delete, as depicted below. This will be followed by a confirmation prompt.  <br/>
<img src="https://i.imgur.com/863lXQL.png" height="80%" width="80%" alt="OU modification"/>
<img src="https://i.imgur.com/qvA0eXZ.png" height="80%" width="80%" alt="OU modification"/>
</p>
However, upon confirming the deletion of the OU by clicking "Yes," an error message will be encountered: <br/>
<img src="https://i.imgur.com/FQR8WJ5.png" height="80%" width="80%" alt="OU modification"/>
</p>
The error occurs due to Active Directory's accidental deletion protection feature, which prevents inadvertent deletions when working with numerous OUs and users. To address this, start by clicking the "View" tab in Active Directory, which opens a list of options as depicted below.  <br/>
<img src="https://i.imgur.com/1682Nug.png" height="80%" width="80%" alt="OU modification"/>
</p>
From the list, click on "Advanced Properties." This reveals additional containers and allows you to disable accidental deletion protection in the properties tab.  <br/>
<img src="https://i.imgur.com/4ZaYUL2.png" height="80%" width="80%" alt="DOU modification"/>
</p>

Now that we've enabled Advanced Properties, return to the OU, right-click, and select "Properties." In this example, we'll delete the "Research and Development" OU. <br/>
<img src="https://i.imgur.com/8EEbfda.png" height="80%" width="80%" alt="OU modification"/>
</p>

After clicking on properties, a new tab will be opened as shown below:
 <br/>
<img src="https://i.imgur.com/ZxEiW6k.png" height="80%" width="80%" alt="OU modification"/>
</p>

In the new tab, go to the "Object" tab at the top. At the bottom, you'll find the "Protect object from accidental deletion" option. Ensure that this option is unchecked, as this will allow you to delete the OU.  <br/>
<img src="https://i.imgur.com/Eg0i66d.png" height="80%" width="80%" alt="OU modification"/>
</p>
Returning to the OU you wish to delete, follow the same procedure: right-click, select "Delete," and confirm by clicking "Yes." <br/>
<img src="https://i.imgur.com/Cq89uuh.png" height="80%" width="80%" alt="DOU modification"/>
</p>
After clicking "Yes," you'll encounter a warning prompt. After a thorough review, proceed by clicking "Yes" to confirm the deletion of the OU. <br/>
<img src="https://i.imgur.com/7NvkPCg.png" height="80%" width="80%" alt="OU modification"/>
</p>
To confirm, check the left-hand side, and you'll notice that the "Research and Development" OU is no longer present. <br/>
<br />
<img src="https://i.imgur.com/oArbuji.png" height="80%" width="80%" alt="OU modification"/>
</p>


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
