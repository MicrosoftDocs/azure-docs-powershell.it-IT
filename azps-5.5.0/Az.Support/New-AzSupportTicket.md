---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
ms.openlocfilehash: 31e529ce30be608c5bd3167044b82f8094c1d248
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182822"
---
# New-AzSupportTicket

## SYNOPSIS
Crea un ticket di supporto.

## SINTASSI

### CreateSupportTicketWithContactDetailParameterSet (impostazione predefinita)
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateSupportTicketWithContactObjectParameterSet
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateTechnicalSupportTicketWithContactObjectParameterSet
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateQuotaSupportTicketWithContactObjectParameterSet
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateTechnicalSupportTicketWithContactDetailParameterSet
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CreateQuotaSupportTicketWithContactDetailParameterSet
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIZIONE
Questo cmdlet può essere usato per creare un ticket di supporto per i problemi di fatturazione, gestione delle sottoscrizioni, quota o tecnici. Usare Get-AzSupportService cmdlet di Get-AzSupportProblemClassification per identificare il servizio Azure e le classificazioni di problemi corrispondenti, rispettivamente per cui si vuole richiedere supporto. È necessario specificare i parametri seguenti: 

    • Title
    • Description
    • Severity level
    • ProblemClassificationId
    • CustomerContactDetail (or individual customer contact parameters)

È possibile usare New-AzSupportContactProfileObject helper per creare un oggetto CustomerContactDetail.

Cloud Solution Provider può creare un ticket di supporto per le sottoscrizioni dei clienti accedendo al tenant del cliente e specificando l'ID tenant iniziale con il parametro *CSPHomeTenantId.*

__Per i ticket tecnici:__

Per specificare il nome della risorsa, ARM ID risorsa della risorsa usando il *parametro TechnicalTicketResourceId.* Vedere un esempio di seguito. 

__Per i ticket quota:__

Per richiedere l'aumento della quota per **Compute VM Cores,** **Batch,** **SQL Database** e SQL **Data Warehouse,** fornisci ulteriori dettagli sotto *l'oggetto QuotaTicketDetail.* L'oggetto QuotaTicketDetail è costituito da 3 proprietà, come descritto di seguito. Per la documentazione dettagliata, fare [clic qui.](https://aka.ms/supportrpquotarequestpayload)

    • QuotaChangeRequestSubType

        This is required for certain quota types when there is a sub type that you are requesting quota increase for. Example: Batch, SQL Database and SQL Data Warehouse have a sub type.

    • QuotaChangeRequestVersion

        This is required and indicates the version of the quota change request payload.

    • QuotaChangeRequests

        This is required and is a list of PSQuotaChangeRequest objects. PSQuotaChangeRequest object has 2 required properties.

        ○ Region

            This is the Azure location or region for which you are requesting quota increase. This is the Location property of Get-AzLocation cmdlet.
        
        ○ Payload

            This is where you specify the new limits for the selected quota type.


Per la documentazione dettagliata su come creare payload per vari tipi di quota, fare [clic qui](https://aka.ms/supportrpquotarequestpayload)

## ESEMPI

### Esempio 1: Creare un ticket di supporto per la fatturazione o la gestione delle sottoscrizioni. Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi di fatturazione o gestione delle sottoscrizioni per cui si vuole richiedere supporto 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### Esempio 2: Creare un ticket di supporto tecnico per una risorsa Macchina virtuale per Windows. Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi di Macchine virtuali per Windows per cui si vuole richiedere supporto 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{vm_windows_service_guid}/problemClassifications/{problemClassification_guid}" -TechnicalTicketResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName              Status CreatedDate
----  ----- --------------- -------- ------------------              ------ -----------
test1 Test  150010521000317 Minimal  Virtual Machine running Windows Open   2/5/2020 1:33:53 AM
```

### Esempio 3: Creare un ticket di supporto per le quote per aumentare la quota per virtual machine core per una specifica famiglia di vm. Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi relativi ai core vm di calcolo quota.
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{cores_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":350}"}, @{Region = "eastus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":516}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### Esempio 4: Creare un ticket di supporto della quota per aumentare la quota per core con priorità bassa per un account batch. Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi relativi ai batch quota.
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":200,`"Type`":`"LowPriority`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### Esempio 5: Creare un ticket di supporto della quota per aumentare la quota dei core vm per una specifica famiglia di vm per un account batch. Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi relativi ai batch quota.
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"VMFamily`":`"standardA0_A7Family`",`"NewLimit`":200,`"Type`":`"Dedicated`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### Esempio 6: Creare un ticket di supporto della quota per aumentare la quota di pool per un account batch. Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi relativi ai batch quota.
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Pools`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### Esempio 7: Creare un ticket di supporto della quota per aumentare la quota per i processi attivi e le pianificazioni dei processi per un account batch. Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi relativi ai batch quota.
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Jobs`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### Esempio 8: Creare un ticket di supporto della quota per aumentare il numero di account Batch per una sottoscrizione. Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi relativi ai batch quota.
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Subscription" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":120,`"Type`":`"Account`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### Esempio 9: Creare un ticket di supporto della quota per aumentare la quota per le DKU per SQL database. Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi di SQL database.
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### Esempio 10: Creare un ticket di supporto della quota per aumentare la quota per i server SQL database. Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi di SQL database.
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### Esempio 11: Creare un ticket di supporto quota per aumentare la quota per le DKU per SQL Data Warehouse. Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi SQL data warehouse.
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### Esempio 12: Creare un ticket di supporto della quota per aumentare la quota per i server per SQL Data Warehouse. Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi di Quota SQL data warehouse.
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### Esempio 13: Creare un ticket di supporto della quota per aumentare la quota per i core con priorità bassa per il servizio di apprendimento automatico. Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi del servizio Quota Machine Learning.
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"LowPriority`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### Esempio 14: Creare un ticket di supporto delle quote per aumentare la quota dei core VM per una specifica famiglia di vm per il servizio di apprendimento automatico. Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi del servizio Quota Machine Learning.
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"standardDFamily`",`"NewLimit`":200,`"Type`":`"Dedicated`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### Esempio 15: Creare un ticket di supporto della quota per aumentare la quota per Azure SQL gestita. Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi del SQL servizio istanza gestita.
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_managed_instance_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "SQLMI" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"vCore`" }"}, @{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"Subnet`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### Esempio 16: Creare un ticket di supporto specificando i singoli parametri di contatto del cliente invece dell'oggetto CustomerContactDetail. 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com"

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### Esempio 17: Creare un ticket di supporto con richiesta di una risposta 24 ore su 24, 7 giorni su 7 da Azure. 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "critical" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -Require24X7Response 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Critical  Billing            Open   2/5/2020 1:33:53 AM
```

### Esempio 18: Creare un ticket di supporto per conto del cliente se si è un CSP (Cloud Solution Provider). CSP deve prima accedere al proprio tenant e quindi al tenant del cliente, come illustrato nell'esempio seguente. Devono quindi usare il parametro -CSPHomeTenantId per specificare l'ID tenant della propria abitazione al momento della creazione di un ticket di supporto.  
```powershell

PS C:\> Login-AzAccount

PS C:\> Login-AzAccount -TenantId {customer_tenant_id}

PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -CSPHomeTenantId {csp_home_tenant_id} 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

## PARAMETERS

### -AdditionalEmailAddress
Altri indirizzi di posta elettronica.
Gli indirizzi e-mail qui elencati verranno copiati in qualsiasi corrispondenza del ticket di supporto.

```yaml
Type: System.String[]
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
Eseguire il cmdlet in background.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CSPHomeTenantId
ID tenant home dell'utente Cloud Solution Provider che ha cercato di creare un ticket di supporto per il cliente.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomerContactDetail
Dettagli di contatto del cliente associati alla risorsa SupportTicket.

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSContactProfile
Parameter Sets: CreateSupportTicketWithContactObjectParameterSet, CreateTechnicalSupportTicketWithContactObjectParameterSet, CreateQuotaSupportTicketWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomerCountry
Paese del cliente.
Deve essere un codice paese ISO Alfa 3 valido (ISO 3166).

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomerFirstName
Nome del cliente.

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomerLastName
Cognome del cliente.

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomerPhoneNumber
Numero di telefono del cliente.
È obbligatorio se il metodo di contatto preferito è il telefono.

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomerPreferredSupportLanguage
Peferred language of the custom.
Deve essere un codice di lingua valido per una delle lingue supportate elencate https://azure.microsoft.com/en-us/support/faq/ qui.

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomerPreferredTimeZone
Fuso orario preferito del cliente.
Deve essere un valore System.TimeZoneInfo.Id valido.

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomerPrimaryEmailAddress
Indirizzo e-mail principale del cliente.

```yaml
Type: System.String
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Descrizione
Descrizione dettagliata della domanda o del problema.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Nome del ticket di supporto creato da questo cmdlet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreferredContactMethod
Metodo di contatto preferito.

```yaml
Type: Microsoft.Azure.Commands.Support.Models.ContactMethod
Parameter Sets: CreateSupportTicketWithContactDetailParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:
Accepted values: Email, Phone

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProblemClassificationId
Ogni servizio Azure ha un proprio set di categorie di problemi, denominato classificazione dei problemi, che corrisponde al tipo di problema riscontrato.
Questo parametro è l'ARM ID risorsa della risorsa ProblemClassification.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProblemStartTime
Data e ora di inizio del problema.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -QuotaTicketDetail
Altri dettagli per un ticket di supporto quota.

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSQuotaTicketDetail
Parameter Sets: CreateQuotaSupportTicketWithContactObjectParameterSet, CreateQuotaSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Require24X7Response
Indica se questo ticket di supporto richiede una risposta 24x7 da Azure.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Gravità
Gravità del ticket di supporto.
Questo indica l'urgenza del caso, che a sua volta determina i tempi di risposta in base al contratto di servizio del piano di supporto tecnico in essere con Azure.

```yaml
Type: Microsoft.Azure.Commands.Support.Models.Severity
Parameter Sets: (All)
Aliases:
Accepted values: Minimal, Moderate, Critical, HighestCriticalImpact

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TechnicalTicketResourceId
ID risorsa della risorsa del servizio Azure (ad esempio: una risorsa di macchina virtuale o una risorsa HDInsight) per cui viene creato il ticket di supporto.

```yaml
Type: System.String
Parameter Sets: CreateTechnicalSupportTicketWithContactObjectParameterSet, CreateTechnicalSupportTicketWithContactDetailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Title
Titolo del ticket di supporto.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Chiede conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa accadrebbe se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Nessuno

## OUTPUT

### Microsoft.Azure.Commands.Support.Models.PSSupportTicket

## NOTE

## COLLEGAMENTI CORRELATI
