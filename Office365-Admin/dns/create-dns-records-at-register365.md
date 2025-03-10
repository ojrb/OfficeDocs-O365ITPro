---
title: "Create DNS records at Register365 for Office 365"
ms.author: pebaum
author: pebaum
manager: mnirkhe
audience: Admin
ms.topic: get-started-article
f1_keywords:
- 'O365P_DOM_Reg365'
- 'O365M_DOM_Reg365'
- 'O365E_DOM_Reg365'
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
ms.assetid: 004030b4-10ad-4026-96e7-011b6afc7e73
description: "Learn to verify your domain and set up DNS records for email, Skype for Business Online, and other services at Register365 for Office 365."
---

# Create DNS records at Register365 for Office 365

 **[Check the Domains FAQ](../setup/domains-faq.md)** if you don't find what you're looking for. 
  
If Register365 is your DNS hosting provider, follow the steps in this article to verify your domain and set up DNS records for email, Skype for Business Online, and so on. 
  
These are the main records to add.  
  
- [Add a TXT record for verification](#add-a-txt-record-for-verification)
    
- [Add an MX record so email for your domain will come to Office 365](#add-an-mx-record-so-email-for-your-domain-will-come-to-office-365)
    
- [Add the six CNAME records that are required for Office 365](#add-the-six-cname-records-that-are-required-for-office-365)
    
- [Add a TXT record for SPF to help prevent email spam](#add-a-txt-record-for-spf-to-help-prevent-email-spam)
    
- [Add the two SRV records that are required for Office 365](#add-the-two-srv-records-that-are-required-for-office-365)
    
After you add these records at Office 365, your domain will be set up to work with Office 365 services.
  
To learn about webhosting and DNS for websites with Office 365, see [Use a public website with Office 365](https://support.office.com/article/a8178510-501d-4bd8-9921-b04f2e9517a5.aspx).
  
> [!NOTE]
>  Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md). 
  
## Add a TXT record for verification
<a name="BKMK_verify"> </a>

Before you use your domain with Office 365, we have to make sure that you own it. Your ability to log in to your account at your domain registrar and create the DNS record proves to Office 365 that you own the domain.
  
> [!NOTE]
> This record is used only to verify that you own your domain; it doesn't affect anything else. You can delete it later, if you like. 
  
1. To get started, go to your domains page at Register365 by using [this link](https://admin.register365.com/dns/). You'll be prompted to log in first.
    
    ![The Control Panel log in page](../media/d7ec9791-d03f-45dd-b080-8aaae5d19ea6.png)
  
2. On the **Dashboard** page, find the name of the domain that you're updating, and then choose **DNS Settings** from the drop-down list. 
    
    (You may have to scroll down.)
    
    ![Clicking DNS Settings in the list](../media/57944802-3f6b-49bb-971a-b1d20936cba3.png)
  
3. On the **Add/Modify DNS Zone** page, in the **A, CNAME, AAAA, TXT and NS records** section, in the boxes for the new record, type or copy and paste the values from the following table. 
    
    (Select the **Type** value from the drop-down list.) 
    
    (If you need to add a row, choose **ADD A/CNAME RECORDS (+)**.)
    
    (You may have to scroll down.)
    
    |**Host name**|**Type**|**Result**|
    |:-----|:-----|:-----|
    |(Leave this field empty.)  <br/> |TXT  <br/> |MS=ms *XXXXXXXX*  <br/> **Note:** This is an example. Use your specific **Destination or Points to Address** value here, from the table in Office 365.           [How do I find this?](../get-help-with-domains/information-for-dns-records.md)          |
   
    ![Entering values on the Add/Modify DNS Zone page](../media/22326005-de95-464d-8e33-08ea31a89b2d.png)
  
4. Choose **Save**.
    
    (You may have to scroll down.)
    
    ![Click Save](../media/157cfb98-d5d0-48a3-8dd1-c4e759c2f8a8.png)
  
5. Wait a few minutes before you continue, so that the record you just created can update across the Internet.
    
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
>  Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md). 
  
## Add an MX record so email for your domain will come to Office 365
<a name="BKMK_add_MX"> </a>

1. To get started, go to your domains page at Register365 by using [this link](https://admin.register365.com/dns/). You'll be prompted to log in first.
    
    ![The Control Panel log in page](../media/d7ec9791-d03f-45dd-b080-8aaae5d19ea6.png)
  
2. On the **Dashboard** page, find the name of the domain that you're updating, and then choose **DNS Settings** from the drop-down list. 
    
    (You may have to scroll down.)
    
    ![Clicking DNS Settings in the list](../media/57944802-3f6b-49bb-971a-b1d20936cba3.png)
  
3. On the **Add/Modify DNS Zone** page, in the **Mail exchange records** section, in the boxes for the new record, type or copy and paste the values from the following table. 
    
    (You may have to scroll down.)
    
    |**Host name**|**Priority**|**Result**|
    |:-----|:-----|:-----|
    |(Leave this field empty.)  <br/> |1  <br/> For more information about priority, see [What is MX priority?](https://support.office.com/article/2784cc4d-95be-443d-b5f7-bb5dd867ba83.aspx) <br/> | *\<domain-key\>*  .mail.protection.outlook.com  <br/> **Note:** Get your  *\<domain-key\>*  from your Office 365 portal account.  [How do I find this?](../get-help-with-domains/information-for-dns-records.md)     |
   
    ![Entering values on the Add/Modify DNS Zone page](../media/2d3645a8-9cb8-435e-b895-5535b6b1fffd.png)
  
4. Choose **Save**.
    
    (You may have to scroll down.)
    
    ![Click Save](../media/0e565fb0-a126-4a48-8ff7-2c2d79d4af32.png)
  
5. If there are any other MX records in the **Mail exchange records** section, delete each one by selecting it and then pressing the **Delete** key on your keyboard. 
    
    ![Deleting records in the Mail exchange records section](../media/8cc37e4f-2e85-4242-af0e-78149434167f.png)
  
6. Choose **Save**.
    
    (You may have to scroll down.)
    
    ![Click Save](../media/1fb69bb5-b5df-4060-adf1-eb26cfaa6c4f.png)
  
## Add the six CNAME records that are required for Office 365
<a name="BKMK_add_CNAME"> </a>

1. To get started, go to your domains page at Register365 by using [this link](https://admin.register365.com/dns/). You'll be prompted to log in first.
    
    ![The Control Panel log in page](../media/d7ec9791-d03f-45dd-b080-8aaae5d19ea6.png)
  
2. On the **Dashboard** page, find the name of the domain that you're updating, and then choose **DNS Settings** from the drop-down list. 
    
    (You may have to scroll down.)
    
    ![Clicking DNS Settings in the list](../media/57944802-3f6b-49bb-971a-b1d20936cba3.png)
  
3. On the **Add/Modify DNS Zone** page, in the **A, CNAME, AAAA, TXT and NS records** section, in the boxes for the new records, type or copy and paste the values from the following table. 
    
    (Select the **Type** value from the drop-down list.) 
    
    (If you need to add a row, choose **ADD A/CNAME RECORDS (+)**.)
    
    (You may have to scroll down.)
    
    |****Host name****|****Type****|****Result****|
    |:-----|:-----|:-----|
    |autodiscover  <br/> |CNAME  <br/> |autodiscover.outlook.com  <br/> |
    |sip  <br/> |CNAME  <br/> |sipdir.online.lync.com  <br/> |
    |lyncdiscover  <br/> |CNAME  <br/> |webdir.online.lync.com  <br/> |
    |enterpriseregistration  <br/> |CNAME  <br/> |enterpriseregistration.windows.net  <br/> |
    |enterpriseenrollment  <br/> |CNAME  <br/> |enterpriseenrollment-s.manage.microsoft.com  <br/> |
   
    ![Entering values on the Add/Modify DNS Zone page](../media/3b79f0de-9cab-4c98-8fa8-c92b35241e8b.png)
  
4. Choose **Save**.
    
    ![Click Save](../media/8ded6428-af97-4fd8-9104-477fa22a5586.png)
  
## Add a TXT record for SPF to help prevent email spam
<a name="BKMK_add_TXT"> </a>

> [!IMPORTANT]
> You cannot have more than one TXT record for SPF for a domain. If your domain has more than one SPF record, you'll get email errors, as well as delivery and spam classification issues. If you already have an SPF record for your domain, don't create a new one for Office 365. Instead, add the required Office 365 values to the current record so that you have a  *single*  SPF record that includes both sets of values. 
  
1. To get started, go to your domains page at Register365 by using [this link](https://admin.register365.com/dns/). You'll be prompted to log in first.
    
    ![The Control Panel log in page](../media/d7ec9791-d03f-45dd-b080-8aaae5d19ea6.png)
  
2. On the **Dashboard** page, find the name of the domain that you're updating, and then choose **DNS Settings** from the drop-down list. 
    
    (You may have to scroll down.)
    
    ![Clicking DNS Settings in the list](../media/57944802-3f6b-49bb-971a-b1d20936cba3.png)
  
3. On the **Add/Modify DNS Zone** page, in the **A, CNAME, AAAA, TXT and NS records** section, in the boxes for the new record, type or copy and paste the values from the following table. 
    
    (Select the **Type** value from the drop-down list.) 
    
    (If you need to add a row, choose **ADD A/CNAME RECORDS (+)**.)
    
    (You may have to scroll down.)
    
    |**Host name**|**Type**|**Result**|
    |:-----|:-----|:-----|
    |(Leave this field empty.)  <br/> |TXT  <br/> |v=spf1 include:spf.protection.outlook.com -all  <br/>**Note:** We recommend copying and pasting this entry, so that all of the spacing stays correct.           |
   
    ![Entering values on the Add/Modify DNS Zone page](../media/33976398-da8a-439b-8e3d-534503b20ee0.png)
  
4. Choose **Save**.
    
    (You may have to scroll down.)
    
    ![Click Save](../media/1d8da122-4861-4ca3-bc9b-d01f18557d4c.png)
  
## Add the two SRV records that are required for Office 365
<a name="BKMK_add_SRV"> </a>

1. To get started, go to your domains page at Register365 by using [this link](https://admin.register365.com/dns/). You'll be prompted to log in first.
    
    ![The Control Panel log in page](../media/d7ec9791-d03f-45dd-b080-8aaae5d19ea6.png)
  
2. On the **Dashboard** page, find the name of the domain that you're updating, and then choose **DNS Settings** from the drop-down list. 
    
    (You may have to scroll down.)
    
    ![Clicking DNS Settings in the list](../media/57944802-3f6b-49bb-971a-b1d20936cba3.png)
  
3. On the **Add/Modify DNS Zone** page, in the **Service records** section, in the boxes for the new records, type or copy and paste the values from the following table. 
    
    (You may have to scroll down.)
    
    |**Name**|**Priority**|**Weight**|**Port**|**Result**|
    |:-----|:-----|:-----|:-----|:-----|
    |_sip._tls  <br/> |100  <br/> |1  <br/> |443  <br/> |sipdir.online.lync.com  <br/> |
    |_sipfederationtls._tcp  <br/> |100  <br/> |1  <br/> |5061  <br/> |sipfed.online.lync.com  <br/> |
   
    ![Entering values in the Service records section](../media/56bb1813-90e2-40c8-98bf-750e2dc3f8b6.png)
  
4. Choose **Save**.
    
    (You may have to scroll down.)
    
    ![Click Save](../media/3b80757c-01e1-492d-b2ce-f721d71f7235.png)
  
> [!NOTE]
>  Typically it takes about 15 minutes for DNS changes to take effect. However, it can occasionally take longer for a change you've made to update across the Internet's DNS system. If you're having trouble with mail flow or other issues after adding DNS records, see [Troubleshoot issues after changing your domain name or DNS records](../get-help-with-domains/find-and-fix-issues.md). 
  
