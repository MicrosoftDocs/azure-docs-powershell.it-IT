---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/new-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
ms.openlocfilehash: 0d86d4e01c39170975901f5c9262bc2857883eec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972430"
---
# <span data-ttu-id="c0c13-101">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="c0c13-101">New-AzSupportTicket</span></span>

## <span data-ttu-id="c0c13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0c13-102">SYNOPSIS</span></span>
<span data-ttu-id="c0c13-103">Crea un ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="c0c13-103">Creates a support ticket.</span></span>

## <span data-ttu-id="c0c13-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c0c13-104">SYNTAX</span></span>

### <span data-ttu-id="c0c13-105">CreateSupportTicketWithContactDetailParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c0c13-105">CreateSupportTicketWithContactDetailParameterSet (Default)</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0c13-106">CreateSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0c13-106">CreateSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0c13-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0c13-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0c13-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0c13-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0c13-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0c13-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0c13-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0c13-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0c13-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c0c13-111">DESCRIPTION</span></span>
<span data-ttu-id="c0c13-112">Questo cmdlet può essere usato per creare un ticket di supporto per i problemi di fatturazione, gestione delle sottoscrizioni, quota o tecnici.</span><span class="sxs-lookup"><span data-stu-id="c0c13-112">This cmdlet can be used to create a support ticket for Billing, Subscription Management, Quota or Technical issues.</span></span> <span data-ttu-id="c0c13-113">Usare Get-AzSupportService cmdlet di Get-AzSupportProblemClassification per identificare il servizio Azure e le classificazioni di problemi corrispondenti, rispettivamente per cui si vuole richiedere supporto.</span><span class="sxs-lookup"><span data-stu-id="c0c13-113">Use Get-AzSupportService and Get-AzSupportProblemClassification cmdlets to identify the Azure service and it's corresponding problem classifications respectively for which you want to request support.</span></span> <span data-ttu-id="c0c13-114">È necessario specificare i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="c0c13-114">You must specify the following parameters:</span></span> 

    • Title
    • Description
    • Severity level
    • ProblemClassificationId
    • CustomerContactDetail (or individual customer contact parameters)

<span data-ttu-id="c0c13-115">È possibile usare New-AzSupportContactProfileObject helper per creare un oggetto CustomerContactDetail.</span><span class="sxs-lookup"><span data-stu-id="c0c13-115">You can use New-AzSupportContactProfileObject helper cmdlet to create CustomerContactDetail object.</span></span>

<span data-ttu-id="c0c13-116">Cloud Solution Provider può creare un ticket di supporto per le sottoscrizioni dei clienti accedendo al tenant del cliente e specificando l'ID tenant iniziale con il parametro *CSPHomeTenantId.*</span><span class="sxs-lookup"><span data-stu-id="c0c13-116">Cloud Solution Providers can create a support ticket for their customer's subscriptions by logging into their customer's tenant and specifying their home tenant id using *CSPHomeTenantId* parameter.</span></span>

<span data-ttu-id="c0c13-117">__Per i ticket tecnici:__</span><span class="sxs-lookup"><span data-stu-id="c0c13-117">__For technical tickets:__</span></span>

<span data-ttu-id="c0c13-118">Per specificare il nome della risorsa, ARM'ID risorsa della risorsa usando il *parametro TechnicalTicketResourceId.*</span><span class="sxs-lookup"><span data-stu-id="c0c13-118">To specify the resource name, specify the ARM resource ID of the resource by using *TechnicalTicketResourceId* parameter.</span></span> <span data-ttu-id="c0c13-119">Vedere un esempio di seguito.</span><span class="sxs-lookup"><span data-stu-id="c0c13-119">See an example below.</span></span> 

<span data-ttu-id="c0c13-120">__Per i ticket quota:__</span><span class="sxs-lookup"><span data-stu-id="c0c13-120">__For quota tickets:__</span></span>

<span data-ttu-id="c0c13-121">Per richiedere l'aumento della quota per **Compute VM Cores,** **Batch,** **SQL Database** e SQL **Data Warehouse,** fornisci ulteriori dettagli sotto *l'oggetto QuotaTicketDetail.*</span><span class="sxs-lookup"><span data-stu-id="c0c13-121">To request for quota increase for **Compute VM Cores**, **Batch**, **SQL Database** and **SQL Data Warehouse**, provide additional details under *QuotaTicketDetail* object.</span></span> <span data-ttu-id="c0c13-122">L'oggetto QuotaTicketDetail è costituito da 3 proprietà, come descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="c0c13-122">QuotaTicketDetail object consists of 3 properties as described below.</span></span> <span data-ttu-id="c0c13-123">Per la documentazione dettagliata, fare [clic qui.](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="c0c13-123">For detailed documentation, please [click here.](https://aka.ms/supportrpquotarequestpayload)</span></span>

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


<span data-ttu-id="c0c13-124">Per la documentazione dettagliata su come creare payload per vari tipi di quota, fare [clic qui](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="c0c13-124">For detailed documentation on how to construct Payload for various quota types, please [click here](https://aka.ms/supportrpquotarequestpayload)</span></span>

## <span data-ttu-id="c0c13-125">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c0c13-125">EXAMPLES</span></span>

### <span data-ttu-id="c0c13-126">Esempio 1: Creare un ticket di supporto per la fatturazione o la gestione delle sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="c0c13-126">Example 1: Create a Billing or Subscription Management support ticket.</span></span> <span data-ttu-id="c0c13-127">Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi di fatturazione o gestione delle sottoscrizioni per cui si vuole richiedere supporto</span><span class="sxs-lookup"><span data-stu-id="c0c13-127">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Billing or Subscription Management problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="c0c13-128">Esempio 2: Creare un ticket di supporto tecnico per una risorsa Macchina virtuale per Windows.</span><span class="sxs-lookup"><span data-stu-id="c0c13-128">Example 2: Create a technical support ticket for Virtual Machine for Windows resource.</span></span> <span data-ttu-id="c0c13-129">Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi di Macchine virtuali per Windows per cui si vuole richiedere supporto</span><span class="sxs-lookup"><span data-stu-id="c0c13-129">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Virtual Machine for Windows problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{vm_windows_service_guid}/problemClassifications/{problemClassification_guid}" -TechnicalTicketResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName              Status CreatedDate
----  ----- --------------- -------- ------------------              ------ -----------
test1 Test  150010521000317 Minimal  Virtual Machine running Windows Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="c0c13-130">Esempio 3: Creare un ticket di supporto per le quote per aumentare la quota per virtual machine core per una specifica famiglia di vm.</span><span class="sxs-lookup"><span data-stu-id="c0c13-130">Example 3: Create a quota support ticket to increase quota for Virtual Machine Cores for a specific VM family.</span></span> <span data-ttu-id="c0c13-131">Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi relativi ai core vm di quota di calcolo.</span><span class="sxs-lookup"><span data-stu-id="c0c13-131">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Compute VM Cores problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{cores_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":350}"}, @{Region = "eastus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":516}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="c0c13-132">Esempio 4: Creare un ticket di supporto della quota per aumentare la quota per core con priorità bassa per un account batch.</span><span class="sxs-lookup"><span data-stu-id="c0c13-132">Example 4: Create a quota support ticket to increase quota for Low-priority cores for a Batch account.</span></span> <span data-ttu-id="c0c13-133">Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi relativi ai batch quota.</span><span class="sxs-lookup"><span data-stu-id="c0c13-133">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":200,`"Type`":`"LowPriority`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="c0c13-134">Esempio 5: Creare un ticket di supporto della quota per aumentare la quota dei core vm per una specifica famiglia di vm per un account batch.</span><span class="sxs-lookup"><span data-stu-id="c0c13-134">Example 5: Create a quota support ticket to increase VM cores quota for a specific VM Family for a Batch account.</span></span> <span data-ttu-id="c0c13-135">Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi relativi ai batch quota.</span><span class="sxs-lookup"><span data-stu-id="c0c13-135">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"VMFamily`":`"standardA0_A7Family`",`"NewLimit`":200,`"Type`":`"Dedicated`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="c0c13-136">Esempio 6: Creare un ticket di supporto della quota per aumentare la quota di pool per un account batch.</span><span class="sxs-lookup"><span data-stu-id="c0c13-136">Example 6: Create a quota support ticket to increase Pools quota for a Batch account.</span></span> <span data-ttu-id="c0c13-137">Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi relativi ai batch quota.</span><span class="sxs-lookup"><span data-stu-id="c0c13-137">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Pools`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="c0c13-138">Esempio 7: Creare un ticket di supporto della quota per aumentare la quota per i processi attivi e le pianificazioni dei processi per un account batch.</span><span class="sxs-lookup"><span data-stu-id="c0c13-138">Example 7: Create a quota support ticket to increase active Jobs and job schedules quota for a Batch account.</span></span> <span data-ttu-id="c0c13-139">Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi relativi ai batch quota.</span><span class="sxs-lookup"><span data-stu-id="c0c13-139">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Jobs`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="c0c13-140">Esempio 8: Creare un ticket di supporto della quota per aumentare il numero di account Batch per una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="c0c13-140">Example 8: Create a quota support ticket to increase number of Batch accounts for a subscription.</span></span> <span data-ttu-id="c0c13-141">Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi relativi ai batch quota.</span><span class="sxs-lookup"><span data-stu-id="c0c13-141">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Subscription" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":120,`"Type`":`"Account`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="c0c13-142">Esempio 9: Creare un ticket di supporto della quota per aumentare la quota per le DKU per SQL database.</span><span class="sxs-lookup"><span data-stu-id="c0c13-142">Example 9: Create a quota support ticket to increase quota for DTUs for SQL Database.</span></span> <span data-ttu-id="c0c13-143">Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi di SQL database.</span><span class="sxs-lookup"><span data-stu-id="c0c13-143">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="c0c13-144">Esempio 10: Creare un ticket di supporto della quota per aumentare la quota per i server SQL database.</span><span class="sxs-lookup"><span data-stu-id="c0c13-144">Example 10: Create a quota support ticket to increase quota for Servers for SQL Database.</span></span> <span data-ttu-id="c0c13-145">Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi di SQL database.</span><span class="sxs-lookup"><span data-stu-id="c0c13-145">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="c0c13-146">Esempio 11: Creare un ticket di supporto della quota per aumentare la quota per le DKU per SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="c0c13-146">Example 11: Create a quota support ticket to increase quota for DTUs for SQL Data Warehouse.</span></span> <span data-ttu-id="c0c13-147">Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi SQL data warehouse.</span><span class="sxs-lookup"><span data-stu-id="c0c13-147">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Date Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="c0c13-148">Esempio 12: Creare un ticket di supporto della quota per aumentare la quota per i server per SQL Data Warehouse.</span><span class="sxs-lookup"><span data-stu-id="c0c13-148">Example 12: Create a quota support ticket to increase quota for Servers for SQL Data Warehouse.</span></span> <span data-ttu-id="c0c13-149">Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi di Quota SQL data warehouse.</span><span class="sxs-lookup"><span data-stu-id="c0c13-149">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Data Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="c0c13-150">Esempio 13: Creare un ticket di supporto della quota per aumentare la quota per i core con priorità bassa per il servizio di apprendimento automatico.</span><span class="sxs-lookup"><span data-stu-id="c0c13-150">Example 13: Create a quota support ticket to increase quota for Low-priority cores for Machine Learning service.</span></span> <span data-ttu-id="c0c13-151">Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi del servizio Quota Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="c0c13-151">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"LowPriority`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="c0c13-152">Esempio 14: Creare un ticket di supporto delle quote per aumentare la quota dei core VM per una specifica famiglia di vm per il servizio di apprendimento automatico.</span><span class="sxs-lookup"><span data-stu-id="c0c13-152">Example 14: Create a quota support ticket to increase VM cores quota for a specific VM Family for Machine Learning service.</span></span> <span data-ttu-id="c0c13-153">Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi del servizio Quota Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="c0c13-153">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"standardDFamily`",`"NewLimit`":200,`"Type`":`"Dedicated`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="c0c13-154">Esempio 15: Creare un ticket di supporto della quota per aumentare la quota per Azure SQL gestita.</span><span class="sxs-lookup"><span data-stu-id="c0c13-154">Example 15: Create a quota support ticket to increase quota for Azure SQL Managed Instance.</span></span> <span data-ttu-id="c0c13-155">Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi del servizio quota SQL servizio istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="c0c13-155">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Managed Instance service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_managed_instance_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "SQLMI" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"vCore`" }"}, @{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"Subnet`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="c0c13-156">Esempio 16: Creare un ticket di supporto specificando i singoli parametri di contatto del cliente invece dell'oggetto CustomerContactDetail.</span><span class="sxs-lookup"><span data-stu-id="c0c13-156">Example 16: Create a support ticket by specifying individual customer contact parameters instead of CustomerContactDetail object.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com"

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="c0c13-157">Esempio 17: Creare un ticket di supporto con richiesta di una risposta 24 ore su 24, 7 giorni su 7 da Azure.</span><span class="sxs-lookup"><span data-stu-id="c0c13-157">Example 17: Create a support ticket with request for 24 x 7 response from Azure.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "critical" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -Require24X7Response 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Critical  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="c0c13-158">Esempio 18: Creare un ticket di supporto per conto del cliente se si è un CSP (Cloud Solution Provider).</span><span class="sxs-lookup"><span data-stu-id="c0c13-158">Example 18: Create a support ticket on behalf of your customer if you are a Cloud Solution Provider (CSP).</span></span> <span data-ttu-id="c0c13-159">CSP deve prima accedere al proprio tenant e quindi al tenant del cliente, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="c0c13-159">CSP should first login into their tenant, and then login into customer's tenant as shown in the example below.</span></span> <span data-ttu-id="c0c13-160">Devono quindi usare il parametro -CSPHomeTenantId per specificare l'ID tenant della propria abitazione al momento della creazione di un ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="c0c13-160">They must then use -CSPHomeTenantId parameter to specify their home tenant id at the time of creating a support ticket.</span></span>  
```powershell

PS C:\> Login-AzAccount

PS C:\> Login-AzAccount -TenantId {customer_tenant_id}

PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -CSPHomeTenantId {csp_home_tenant_id} 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="c0c13-161">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0c13-161">PARAMETERS</span></span>

### <span data-ttu-id="c0c13-162">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="c0c13-162">-AdditionalEmailAddress</span></span>
<span data-ttu-id="c0c13-163">Altri indirizzi di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="c0c13-163">Additional email addresses.</span></span>
<span data-ttu-id="c0c13-164">Gli indirizzi e-mail qui elencati verranno copiati in qualsiasi corrispondenza del ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="c0c13-164">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

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

### <span data-ttu-id="c0c13-165">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0c13-165">-AsJob</span></span>
<span data-ttu-id="c0c13-166">Eseguire il cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="c0c13-166">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="c0c13-167">-CSPHomeTenantId</span><span class="sxs-lookup"><span data-stu-id="c0c13-167">-CSPHomeTenantId</span></span>
<span data-ttu-id="c0c13-168">ID tenant home dell'utente Cloud Solution Provider che ha cercato di creare un ticket di supporto per il cliente.</span><span class="sxs-lookup"><span data-stu-id="c0c13-168">This is the home tenant id of the Cloud Solution Provider user trying to create a support ticket for their customer.</span></span>

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

### <span data-ttu-id="c0c13-169">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="c0c13-169">-CustomerContactDetail</span></span>
<span data-ttu-id="c0c13-170">Dettagli di contatto del cliente associati alla risorsa SupportTicket.</span><span class="sxs-lookup"><span data-stu-id="c0c13-170">Customer contact details associated with SupportTicket resource.</span></span>

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

### <span data-ttu-id="c0c13-171">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="c0c13-171">-CustomerCountry</span></span>
<span data-ttu-id="c0c13-172">Paese del cliente.</span><span class="sxs-lookup"><span data-stu-id="c0c13-172">Customer country.</span></span>
<span data-ttu-id="c0c13-173">Deve essere un codice paese ISO Alfa-3 valido (ISO 3166).</span><span class="sxs-lookup"><span data-stu-id="c0c13-173">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="c0c13-174">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="c0c13-174">-CustomerFirstName</span></span>
<span data-ttu-id="c0c13-175">Nome del cliente.</span><span class="sxs-lookup"><span data-stu-id="c0c13-175">Customer first name.</span></span>

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

### <span data-ttu-id="c0c13-176">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="c0c13-176">-CustomerLastName</span></span>
<span data-ttu-id="c0c13-177">Cognome del cliente.</span><span class="sxs-lookup"><span data-stu-id="c0c13-177">Customer last name.</span></span>

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

### <span data-ttu-id="c0c13-178">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="c0c13-178">-CustomerPhoneNumber</span></span>
<span data-ttu-id="c0c13-179">Numero di telefono del cliente.</span><span class="sxs-lookup"><span data-stu-id="c0c13-179">Customer phone number.</span></span>
<span data-ttu-id="c0c13-180">È obbligatorio se il metodo di contatto preferito è il telefono.</span><span class="sxs-lookup"><span data-stu-id="c0c13-180">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="c0c13-181">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="c0c13-181">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="c0c13-182">Peferred language of the custom.</span><span class="sxs-lookup"><span data-stu-id="c0c13-182">Peferred language of the custom.</span></span>
<span data-ttu-id="c0c13-183">Deve essere un codice di lingua valido per una delle lingue supportate elencate https://azure.microsoft.com/en-us/support/faq/ qui.</span><span class="sxs-lookup"><span data-stu-id="c0c13-183">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/en-us/support/faq/.</span></span>

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

### <span data-ttu-id="c0c13-184">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="c0c13-184">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="c0c13-185">Fuso orario preferito del cliente.</span><span class="sxs-lookup"><span data-stu-id="c0c13-185">Customer preferred time zone.</span></span>
<span data-ttu-id="c0c13-186">Deve essere un valore System.TimeZoneInfo.Id valido.</span><span class="sxs-lookup"><span data-stu-id="c0c13-186">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="c0c13-187">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="c0c13-187">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="c0c13-188">Indirizzo di posta elettronica principale del cliente.</span><span class="sxs-lookup"><span data-stu-id="c0c13-188">Customer primary email address.</span></span>

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

### <span data-ttu-id="c0c13-189">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0c13-189">-DefaultProfile</span></span>
<span data-ttu-id="c0c13-190">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c0c13-190">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0c13-191">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0c13-191">-Description</span></span>
<span data-ttu-id="c0c13-192">Descrizione dettagliata della domanda o del problema.</span><span class="sxs-lookup"><span data-stu-id="c0c13-192">Detailed description of the question or issue.</span></span>

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

### <span data-ttu-id="c0c13-193">-Name</span><span class="sxs-lookup"><span data-stu-id="c0c13-193">-Name</span></span>
<span data-ttu-id="c0c13-194">Nome del ticket di supporto creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0c13-194">Name of support ticket that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c0c13-195">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="c0c13-195">-PreferredContactMethod</span></span>
<span data-ttu-id="c0c13-196">Metodo di contatto preferito.</span><span class="sxs-lookup"><span data-stu-id="c0c13-196">Preferred contact method.</span></span>

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

### <span data-ttu-id="c0c13-197">-ProblemClassificationId</span><span class="sxs-lookup"><span data-stu-id="c0c13-197">-ProblemClassificationId</span></span>
<span data-ttu-id="c0c13-198">Ogni servizio Azure ha un proprio set di categorie di problemi, denominato classificazione dei problemi, che corrisponde al tipo di problema riscontrato.</span><span class="sxs-lookup"><span data-stu-id="c0c13-198">Each Azure service has its own set of issue category called problem classification that corresponds to the type of problem you're experiencing.</span></span>
<span data-ttu-id="c0c13-199">Questo parametro è l'ARM ID risorsa della risorsa ProblemClassification.</span><span class="sxs-lookup"><span data-stu-id="c0c13-199">This parameter is the ARM resource id of ProblemClassification resource.</span></span>

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

### <span data-ttu-id="c0c13-200">-ProblemStartTime</span><span class="sxs-lookup"><span data-stu-id="c0c13-200">-ProblemStartTime</span></span>
<span data-ttu-id="c0c13-201">Data e ora di inizio del problema.</span><span class="sxs-lookup"><span data-stu-id="c0c13-201">Date and time when the problem started.</span></span>

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

### <span data-ttu-id="c0c13-202">-QuotaTicketDetail</span><span class="sxs-lookup"><span data-stu-id="c0c13-202">-QuotaTicketDetail</span></span>
<span data-ttu-id="c0c13-203">Altri dettagli per un ticket di supporto quota.</span><span class="sxs-lookup"><span data-stu-id="c0c13-203">Additional details for a Quota support ticket.</span></span>

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

### <span data-ttu-id="c0c13-204">-Require24X7Response</span><span class="sxs-lookup"><span data-stu-id="c0c13-204">-Require24X7Response</span></span>
<span data-ttu-id="c0c13-205">Indica se questo ticket di supporto richiede una risposta 24x7 da Azure.</span><span class="sxs-lookup"><span data-stu-id="c0c13-205">Indicates if this support ticket requires a 24x7 response from Azure.</span></span>

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

### <span data-ttu-id="c0c13-206">-Gravità</span><span class="sxs-lookup"><span data-stu-id="c0c13-206">-Severity</span></span>
<span data-ttu-id="c0c13-207">Gravità del ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="c0c13-207">Severity of the support ticket.</span></span>
<span data-ttu-id="c0c13-208">Ciò indica l'urgenza del caso, che a sua volta determina i tempi di risposta in base al contratto di servizio del piano di supporto tecnico in essere con Azure.</span><span class="sxs-lookup"><span data-stu-id="c0c13-208">This indicates the urgency of the case, which in turn determines the response time according to the service level agreement of the technical support plan you have with Azure.</span></span>

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

### <span data-ttu-id="c0c13-209">-TechnicalTicketResourceId</span><span class="sxs-lookup"><span data-stu-id="c0c13-209">-TechnicalTicketResourceId</span></span>
<span data-ttu-id="c0c13-210">ID della risorsa del servizio Azure (ad esempio: una risorsa di macchina virtuale o una risorsa HDInsight) per cui viene creato il ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="c0c13-210">This is the resource id of the Azure service resource (For example: A virtual machine resource or an HDInsight resource) for which the support ticket is created.</span></span>

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

### <span data-ttu-id="c0c13-211">-Title</span><span class="sxs-lookup"><span data-stu-id="c0c13-211">-Title</span></span>
<span data-ttu-id="c0c13-212">Titolo del ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="c0c13-212">Title of support ticket.</span></span>

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

### <span data-ttu-id="c0c13-213">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0c13-213">-Confirm</span></span>
<span data-ttu-id="c0c13-214">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0c13-214">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0c13-215">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0c13-215">-WhatIf</span></span>
<span data-ttu-id="c0c13-216">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c0c13-216">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0c13-217">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c0c13-217">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0c13-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0c13-218">CommonParameters</span></span>
<span data-ttu-id="c0c13-219">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0c13-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0c13-220">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c0c13-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0c13-221">INPUT</span><span class="sxs-lookup"><span data-stu-id="c0c13-221">INPUTS</span></span>

### <span data-ttu-id="c0c13-222">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c0c13-222">None</span></span>

## <span data-ttu-id="c0c13-223">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c0c13-223">OUTPUTS</span></span>

### <span data-ttu-id="c0c13-224">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="c0c13-224">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="c0c13-225">NOTE</span><span class="sxs-lookup"><span data-stu-id="c0c13-225">NOTES</span></span>

## <span data-ttu-id="c0c13-226">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c0c13-226">RELATED LINKS</span></span>
