# O365BronzeStack
This is a sample Azure ARM template that will deploy a Demo POC IaaS for o365 needs, the servers include, ADFS, WAP, ADDC, AAD Connect. This is a template to test drive Azure ARM Templates.

v1 of this ARM one click deployment is the beginning to get as much as possible to a light touch deployment for ADDC,ADFS,WAP,AADCONNET servers for Azure AD \ Office 365. This can provide a load balanced solution for single sign on for your Azure AD \ Office 365 deployment. This should eliminate time spent on setting up and designing this solution. Click and head to lunch, return and the components are there and ready to be configured after some additional steps. There will be further development on my part to add automation through the ARM template and DSC for the servers in the next iteration.


Please post or send comments and suggestions to nate.swift@live.com





After Deployment:

From Azure (ARM Portal)


Create NSG on Subnet 2 for Web Application Proxy servers(See Below Appendix A) (Future Automation)



On Servers: (Partial Future Automation)


Install ADDS Role on ADDC01

Configure ADDC01 to add a domain forest to existing domain

Join ADFS01,SYN01 to domain

on DSYN01 Install and configure directory sync using Azure AD Connect

Install ADFS Role on ADFS01

Configure ADFS

Install WAP Role on ADFS01

Configure WAP

From Azure (ARM Portal)


Remove PIP1-4 addresses once S2S is up and hybrid connectivity established

Change VNET for Azure ADDC01 as AD DNS servers


Appendix A:

Create a .csv file for your NSG needs a sample and ps script can be found: https://onedrive.live.com/redir?resid=B3BD82E4293DFD9E!103296&authkey=!AA31KIYnaah-JME&ithint=folder%2ccsv 

