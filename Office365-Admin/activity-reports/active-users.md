---
title: "Office 365 Reports in the Admin Center - Active Users"
ms.author: pebaum
author: pebaum
manager: mnirkhe
audience: Admin
ms.topic: overview
f1_keywords:
- 'O365E_ReportsLicensing'
ms.service: o365-administration
localization_priority: Normal
ms.collection: 
- M365-subscription-management 
- Adm_O365
- Adm_NonTOC
search.appverid:
- BCS160
- MET150
- MOE150
- GEA150
ms.assetid: fc1cf1d0-cd84-43fd-adb7-a4c4dfa8112d
description: "Learn how to get an Active Users report using the Office 365 Reports dashboard in the Microsoft 365 admin center and find out how many product licenses are being used."
---

# Office 365 Reports in the Admin Center - Active Users

The new Office 365 **Reports** dashboard shows you the activity overview across the Office 365 products in your organization. It enables you to drill in to individual product level reports to give you more granular insight about the activities within each product. Check out [the Reports overview topic](activity-reports.md).
  
For example, you can use the **Active Users** report to find out how many product licenses are being used by individuals in your organization, and drill down for information about which users are using what products. This report can help administrators identify underutilized products or users that might need additional training or information. 
  
> [!NOTE]
> You must be a global administrator in Office 365 or an Exchange, SharePoint, Skype for Business administrator, or reports reader to see Office 365 reports. 
  
## How to get to the Active Users report

1. Go to the Microsoft 365 admin center \> **Reports** \> and click **Usage**.
    
    ![In the admin center, click reports, then usage](../media/1e7dbaa2-155e-476a-b50a-7ae7a7393611.png)
  
2. On the Usage page, select **Active Users** from the drop down. 
    
    ![Select a report, and click Active users](../media/90c3229a-c2f8-41f4-83a9-c4d35228e205.png)
  
## Interpret the Active Users report

![Overview of the active users report](../media/cb9773a0-f13d-4f37-8dae-337ff20b77d9.png)
  
|||
|:-----|:-----|
|1.  <br/> |The **Active Users** report can be viewed for trends over the last 7 days, 30 days, 90 days, or 180 days. However, if you click into a particular day in the report, the table (7) will show data for up to 28 days from the current date (not the date the report was generated).  <br/> |
|2.  <br/> |Each report has a date for when this report was generated. The reports usually reflect a 24 to 48 hour latency from time of activity.  <br/> |
|3.  <br/> |The **Active Users** chart shows you daily active users in the reporting period separated by product.  <br/> The **Services** chart shows you count of users by activity type and Service.  <br/> |
|4.  <br/> | On the **Active Users** chart, the x axis shows the selected reporting time period and the y axis displays the daily active users separated and color coded by licence type.  <br/>  On the **Services** activity chart, the X axis displays the individual services your users are enabled for in the given time period and the Y axis is the Count of users by activity status, color coded by activity status.  <br/> |
|5.  <br/> |You can filter the series you see on the chart by clicking on an item in the legend. Changing this selection doesn't change the info in the grid table.  <br/> |
|6.  <br/> |You can also export the report data into an Excel .csv file, by clicking or tapping the **Export** ![Export your data to an Excel file](../media/816a224b-6ca7-4967-a135-4f6427f64dc8.JPG) link. This exports data of all users and enables you to do simple sorting and filtering for further analysis. If you have less than 2000 users, you can sort and filter within the table in the report itself. If you have more than 2000 users, in order to filter and sort, you will need to export the data.  <br/> |
|7.  <br/> |You can change what information is displayed in the grid table with column controls.  <br/> If your subscription is operated by 21Vianet, then you will not see Yammer. <br/> ![User level filter options](../media/af8f0a7a-171f-4a65-baae-960f0cb8a5bf.png) <br/> |
|||



If your organization's policies prevents you from viewing reports where user information is identifiable, you can change the privacy setting for all these reports. Check out the **How do I hide user level details?** section in [Activity Reports in the Microsoft 365 admin center](activity-reports.md).  
   

