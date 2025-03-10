---
title: "Create DNS records at name.com for Office 365"
ms.author: pebaum
author: pebaum
manager: mnirkhe
audience: Admin
ms.topic: get-started-article
f1_keywords:
- 'O365P_DOM_name'
- 'O365M_DOM_name'
- 'O365E_DOM_name'
ms.service: o365-administration
localization_priority: Normal
ms.collection: 
- M365-subscription-management
- Adm_O365
- Adm_NonTOC
- Adm_O365_Setup
search.appverid:
- BCS160
- MET150
- MOE150
ms.assetid: 9ddcc2fc-9433-4335-8192-6ffb1f541087
description: "Learn to verify your domain and set up DNS records for email, Skype for Business Online, and other services at name.com for Office 365."
---

# Create DNS records at name.com for Office 365

 **[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for. 
  
If name.com is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on.
  
After you add these records at name.com, your domain will be set up to work with Office 365 services.
  
To learn about webhosting and DNS for websites with Office 365, see [Use a public website with Office 365](https://support.office.com/article/a8178510-501d-4bd8-9921-b04f2e9517a5.aspx).
  
> [!NOTE]
> Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md). 
  
## Add a TXT record for verification
<a name="BKMK_verify"> </a>

Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.
  
> [!NOTE]
> This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like. 
  
1. To get started, go to your domains page at name.com by using [this link](https://www.name.com/account/domain). You'll be prompted to log in first.
    
    ![Name-BP-Configure-1-1](../media/1869b416-1d3f-4fb1-99c6-62b74ca7a4c7.png)
  
2. Under **My Domains**, choose the name of the domain that you want to modify.
    
    ![Name-BP-Configure-1-2](../media/c8b96e1e-aa35-4fb1-8209-450f587fec4d.png)
  
3. In the **Details** column, choose ** DNS Records **. 
    
    ![Name-BP-Configure-1-3](../media/c5da31e2-2f77-4d0c-b31d-189e6fb7b205.png)
  
4. In the boxes for the new record, type or copy and paste the values from the following table.
    
    (Select the **Type** value from the drop-down list.) 
    
    |||||
    |:-----|:-----|:-----|:-----|
    |**Type** <br/> |**Host** <br/> |**Answer** <br/> |**TTL** <br/> |
    |TXT  <br/> |(Leave this field empty.)  <br/> |MS=ms *XXXXXXXX*  <br/> **Note:** This is an example. Use your specific **Destination or Points to Address** value here, from the table in Office 365.           [How do I find this?](../get-help-with-domains/information-for-dns-records.md)          |Use the default value (300).  <br/> |
   
    ![Name-BP-Verify-1-1](../media/0c352fd3-cf84-439f-a481-0705e225cc54.png)
  
5. Choose **Add Record**.
    
    ![Name-BP-Verify-1-2](../media/816fc60b-17ab-4982-8849-6c3fcf3ca3d6.png)
  
6. Wait a few minutes before you continue, so that the record you just created can update across the Internet.
    
Now that you've added the record at your domain registrar's site, you'll go back to Office 365 and request Office 365 to look for the record.
  
When Office 365 finds the correct TXT record, your domain is verified.
  
1. Choose **Setup** \> **Domains**.
    
2. On the **Domains** page, choose the domain that you are verifying. 
    
    ![Domain name selected in Microsoft 365 admin center](../media/c61204f1-a025-448b-a2a1-c4d7abee7a06.png)
  
3. On the **Setup** page, choose **Start setup**.
    
    ![Start setup](../media/5f6578af-ae32-49e8-b283-ec2d080420da.png)
  
4. On the **Verify domain** page, choose **Verify**.
    
    ![Verify](../media/c256ab1d-03f2-498e-bb63-19e4d49a6b97.png)
  
> [!NOTE]
> Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md). 
  
## Add an MX record so email for your domain will come to Office 365
<a name="BKMK_add_MX"> </a>

1. To get started, go to your domains page at name.com by using [this link](https://www.name.com/account/domain). You'll be prompted to log in first.
    
    ![Name-BP-Configure-1-1](../media/1869b416-1d3f-4fb1-99c6-62b74ca7a4c7.png)
  
2. Under **My Domains**, choose the name of the domain that you want to modify.
    
    ![Name-BP-Configure-1-2](../media/c8b96e1e-aa35-4fb1-8209-450f587fec4d.png)
  
3. In the **Details** column, choose ** DNS Records **. 
    
    ![Name-BP-Configure-1-3](../media/c5da31e2-2f77-4d0c-b31d-189e6fb7b205.png)
  
4. In the boxes for the new record, type or copy and paste the values from the following table.
    
    (Select the **Type** value from the drop-down list.) 
    
    |**Type**|**Host**|**Answer**|**TTL**|**Prio**|
    |:-----|:-----|:-----|:-----|:-----|
    |MX  <br/> |(Leave this field empty.)  <br/> | *\<domain-key\>*  .mail.protection.outlook.com  <br/> **Note:** Get your  *\<domain-key\>*  from your Office 365 portal account.           [How do I find this?](../get-help-with-domains/information-for-dns-records.md)          |Use the default value (300).  <br/> |0  <br/> For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx) <br/> |
   
   ![Name-BP-Configure-2-1](../media/11ba2160-fc8e-4196-bb15-2b7c6d49c8fc.png)
  
5. Choose **Add Record**.
    
    ![Name-BP-Configure-2-2](../media/fd09f161-7cc4-4723-aec2-5fa801bd19e9.png)
  
6. If there are any other MX records, delete each of them by using the following two-step procedure:
    
    For each other MX record, choose **Delete** in the **Actions** column. 
    
    ![Name-BP-Configure-2-3](../media/16734a98-31c4-4023-a2a5-10b7c95bc58e.png)
  
    To confirm each deletion, choose **Delete** in the **Actions** column again. 
    
    ![Name-BP-Configure-2-4](../media/409c21c5-51f4-4244-bb84-5d32084224b2.png)
  
    Repeat this two-step procedure until you have deleted each of the other MX records.
    
## Add the CNAME records that are required for Office 365
<a name="BKMK_add_CNAME"> </a>

1. To get started, go to your domains page at name.com by using [this link](https://www.name.com/account/domain). You'll be prompted to log in first.
    
    ![Name-BP-Configure-1-1](../media/1869b416-1d3f-4fb1-99c6-62b74ca7a4c7.png)
  
2. Under **My Domains**, choose the name of the domain that you want to modify.
    
    ![Name-BP-Configure-1-2](../media/c8b96e1e-aa35-4fb1-8209-450f587fec4d.png)
  
3. In the **Details** column, choose ** DNS Records **. 
    
    ![Name-BP-Configure-1-3](../media/c5da31e2-2f77-4d0c-b31d-189e6fb7b205.png)
  
4. Add the first CNAME record.
    
    In the boxes for the new record, type or copy and paste the values from the first row of the following table.
    
    (Select the **Type** value from the drop-down list.) 
    
    |**Type**|**Host**|**Answer**|**TTL**|
    |:-----|:-----|:-----|:-----|
    |CNAME  <br/> |autodiscover  <br/> |autodiscover.outlook.com  <br/> |Use the default value (300).  <br/> |
    |CNAME  <br/> |sip  <br/> |sipdir.online.lync.com  <br/> |Use the default value (300).  <br/> |
    |CNAME  <br/> |lyncdiscover  <br/> |webdir.online.lync.com  <br/> |Use the default value (300).  <br/> |
    |CNAME  <br/> |enterpriseregistration  <br/> |enterpriseregistration.windows.net  <br/> |Use the default value (300).  <br/> |
    |CNAME  <br/> |enterpriseenrollment  <br/> |enterpriseenrollment-s.manage.microsoft.com  <br/> |Use the default value (300).  <br/> |
   
   ![Name-BP-Configure-3-1](../media/4e34caaf-b418-40ec-abfa-fe62175a87c2.png)
  
5. Choose **Add Record** to add the first record. 
    
    ![Name-BP-Configure-3-2](../media/1053c2a7-07c3-4c1b-b54a-1c02881fb0ec.png)
  
6. Add the second CNAME record.
    
    Use the values from the second row of the table above, and then choose **Add Record** to add the second record. 
    
    Add the remaining records in the same way, using the values from the third, fourth, fifth, and sixth rows of the table.
    
## Add a TXT record for SPF to help prevent email spam
<a name="BKMK_add_TXT"> </a>

> [!IMPORTANT]
> You cannot have more than one TXT record for SPF for a domain. If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues. If you already have an SPF record for your domain, don't create a new one for Office 365. Instead, add the required Office 365 values to the current record so that you have a  *single*  SPF record that includes both sets of values. 
  
1. To get started, go to your domains page at name.com by using [this link](https://www.name.com/account/domain). You'll be prompted to log in first.
    
    ![Name-BP-Configure-1-1](../media/1869b416-1d3f-4fb1-99c6-62b74ca7a4c7.png)
  
2. Under **My Domains**, choose the name of the domain that you want to modify.

    ![Name-BP-Configure-1-2](../media/c8b96e1e-aa35-4fb1-8209-450f587fec4d.png)
  
3. In the **Details** column, choose ** DNS Records **. 
    
    ![Name-BP-Configure-1-3](../media/c5da31e2-2f77-4d0c-b31d-189e6fb7b205.png)
  
4. In the boxes for the new record, type or copy and paste the values from the following table.
    
    (Select the **Type** value from the drop-down list.) 
    
    |**Type**|**Host**|**Answer**|**TTL**|
    |:-----|:-----|:-----|:-----|
    |TXT  <br/> |(Leave this field empty.)  <br/> |v=spf1 include:spf.protection.outlook.com -all  <br/> **Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.           |Use the default value (300).  <br/> |
   
   ![Name-BP-Configure-4-1](../media/cbbfc071-840a-4ffa-a59e-0dfce03063cc.png)
  
5. Choose **Add Record**.
    
    ![Name-BP-Configure-4-2](../media/db1e0e09-2b95-4fc1-88bd-e86da536921f.png)
  
## Add the two SRV records that are required for Office 365
<a name="BKMK_add_SRV"> </a>

1. To get started, go to your domains page at name.com by using [this link](https://www.name.com/account/domain). You'll be prompted to log in first.
    
    ![Name-BP-Configure-1-1](../media/1869b416-1d3f-4fb1-99c6-62b74ca7a4c7.png)
  
2. Under **My Domains**, choose the name of the domain that you want to modify.
    
    ![Name-BP-Configure-1-2](../media/c8b96e1e-aa35-4fb1-8209-450f587fec4d.png)
  
3. In the **Details** column, choose ** DNS Records **. 
    
    ![Name-BP-Configure-1-3](../media/c5da31e2-2f77-4d0c-b31d-189e6fb7b205.png)
  
4. Add the first SRV record:
    
    In the boxes for the new record, type or copy and paste the values from the first row of the following table.
    
    (Select the **Type** value from the drop-down list.) 
    
    |**Type**|**Service**|**Weight**|**TTL**|**Prio**|**Protocol**|**Port**|**Target**|
    |:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
    |SRV|sip|1|Use the default value (300).|100|tls|443|sipdir.online.lync.com <br> **Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.           |
    |SRV|sipfederationtls|1|Use the default value (300).|100|tcp|5061|sipfed.online.lync.com <br>**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.           |
   
   ![Name-BP-Configure-5-1](../media/d9a885fd-7300-45b6-ad4c-0b4bf1067560.png)
  
5. Choose **Add Record**.

    ![Name-BP-Configure-5-2](../media/a804d51d-8f57-4b0b-8bd6-a52eb1c87a97.png)
  
6. Add the second SRV record:

Use the values from the next row of the table above, and then choose **Add Record** to add the second record.

>[!NOTE]
>Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md).