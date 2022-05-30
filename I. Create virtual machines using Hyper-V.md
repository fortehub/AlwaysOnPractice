# AlwaysOnPractice
<br/>

**I. Create virtual machines using Hyper-V**
<br/>

**Resources**
------------------------------------------------------------------------------------------------------------------------------------
**1.** [Create Virtual Machine with Hyper-V on Windows 10](https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/quick-start/create-virtual-machine)<br/>
**2.** Use my provided PowerShell Script to create Virtual Machines. File name "hyperv-createvm.ps1"

I'm going to use the PowerShell I've created to create the following virtual machines:	<br/> 
**a.** **hjc-adprod** -- The Domain controller server.	  <br/>
**b.** **hjc-sqlprod** -- The Primary SQL Server Instance. <br/>
**c.** **hjc-sqldr01** -- The Seconday SQL Server Instance. <br/>

Time for some action.
<br/>

**Create Virtual Machines using a PowerShell Script**
------------------------------------------------------------------------------------------------------------------------------------
1. Open PowerShell ISE (run as administrator). Set the execution policy to "Unrestricted" to CurrentUser scope. <br/>
```PowerShell
Set-ExecutionPolicy Unrestricted -Scope CurrentUser -Force
Get-ExecutionPolicy -List
```

![image](https://user-images.githubusercontent.com/95063830/170930540-17097346-7794-4ac8-9b8b-73da9dcf28ec.png)

2. At the PowerShell ISE, navigate to **File**, click **Open** then select the provided PowerShell script (hyperv-createvm.ps1).

![image](https://user-images.githubusercontent.com/95063830/170930889-f0a47dcf-13ed-4283-a1b1-f4789ffd8ed4.png)

3. Click the Run Script button or Press F5.  <br/>
4. Type in the name of the virtual machine, size of Disk C & D, and the Memory of the Virtual Machines. I've created first the "**hjc-adprod**" virtual machines, set the size of Disk C & D to 32 GB & 10GB, and Memory to 4096 MB or 4GB, respectively. Press enter and wait till the process complete.

![image](https://user-images.githubusercontent.com/95063830/170931579-749c8c24-3c90-47af-9832-77a017f41e9e.png)

5. Process complete!

![image](https://user-images.githubusercontent.com/95063830/170932266-88e05ea5-1dc5-4ac1-9736-81026892beac.png)


 To verify, type the following in the PowerShell ISE. <br/>
```PowerShell
Get-VM
```
Here's the result:  <br/>
![image](https://user-images.githubusercontent.com/95063830/170932350-1ff00ace-1c13-44f3-98c3-c5e7692a9180.png)

Or open the Hyper-V Manager to see the newly created Virtual Machines. <br/>
![image](https://user-images.githubusercontent.com/95063830/170932499-f1e39385-a040-4936-8302-370b255c48fb.png)

6. Now create the 2 remaining virtual machines. To create a new PowerShell ISE Session/TAB, press **CTRL+T**. Run the PowerShell Script again. <br/>
7. All virtual machines created successfully! 

![image](https://user-images.githubusercontent.com/95063830/170933392-84dbd84e-ef65-4e32-8ead-962bd34c094d.png)

![image](https://user-images.githubusercontent.com/95063830/170933483-31e01c81-abac-4200-bd4a-9e050138dcfc.png)


**Next Stage**
------------------------------------------------------------------------------------------------------------------------------------

[II. Install OS and OS features such as Active Directory Domain Services, and so on]
