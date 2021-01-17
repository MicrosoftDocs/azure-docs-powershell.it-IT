---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicket.md
ms.openlocfilehash: 31e529ce30be608c5bd3167044b82f8094c1d248
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335092"
---
# <span data-ttu-id="7d8d9-101">New-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="7d8d9-101">New-AzSupportTicket</span></span>

## <span data-ttu-id="7d8d9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7d8d9-102">SYNOPSIS</span></span>
<span data-ttu-id="7d8d9-103">Crea un ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-103">Creates a support ticket.</span></span>

## <span data-ttu-id="7d8d9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d8d9-104">SYNTAX</span></span>

### <span data-ttu-id="7d8d9-105">CreateSupportTicketWithContactDetailParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7d8d9-105">CreateSupportTicketWithContactDetailParameterSet (Default)</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d8d9-106">CreateSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d8d9-106">CreateSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d8d9-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d8d9-107">CreateTechnicalSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d8d9-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d8d9-108">CreateQuotaSupportTicketWithContactObjectParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerContactDetail <PSContactProfile> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d8d9-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d8d9-109">CreateTechnicalSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -TechnicalTicketResourceId <String> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d8d9-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d8d9-110">CreateQuotaSupportTicketWithContactDetailParameterSet</span></span>
```
New-AzSupportTicket -Name <String> -Title <String> -Description <String> -ProblemClassificationId <String>
 -Severity <Severity> -CustomerFirstName <String> -CustomerLastName <String>
 -PreferredContactMethod <ContactMethod> -CustomerPrimaryEmailAddress <String>
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] -CustomerPreferredTimeZone <String>
 -CustomerCountry <String> -CustomerPreferredSupportLanguage <String> [-ProblemStartTime <DateTime>]
 -QuotaTicketDetail <PSQuotaTicketDetail> [-CSPHomeTenantId <String>] [-Require24X7Response] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d8d9-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d8d9-111">DESCRIPTION</span></span>
<span data-ttu-id="7d8d9-112">Questo cmdlet può essere usato per creare un ticket di supporto per la fatturazione, la gestione degli abbonamenti, le quote o i problemi tecnici.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-112">This cmdlet can be used to create a support ticket for Billing, Subscription Management, Quota or Technical issues.</span></span> <span data-ttu-id="7d8d9-113">USA i cmdlet Get-AzSupportService e Get-AzSupportProblemClassification per identificare il servizio Azure e le corrispondenti classificazioni dei problemi rispettivamente per cui vuoi richiedere il supporto.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-113">Use Get-AzSupportService and Get-AzSupportProblemClassification cmdlets to identify the Azure service and it's corresponding problem classifications respectively for which you want to request support.</span></span> <span data-ttu-id="7d8d9-114">Devi specificare i parametri seguenti:</span><span class="sxs-lookup"><span data-stu-id="7d8d9-114">You must specify the following parameters:</span></span> 

    • Title
    • Description
    • Severity level
    • ProblemClassificationId
    • CustomerContactDetail (or individual customer contact parameters)

<span data-ttu-id="7d8d9-115">Puoi usare New-AzSupportContactProfileObject cmdlet helper per creare un oggetto CustomerContactDetail.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-115">You can use New-AzSupportContactProfileObject helper cmdlet to create CustomerContactDetail object.</span></span>

<span data-ttu-id="7d8d9-116">I provider di soluzioni cloud possono creare un ticket di supporto per gli abbonamenti del cliente accedendo al tenant del cliente e specificando l'ID del tenant domestico usando il parametro *CSPHomeTenantId* .</span><span class="sxs-lookup"><span data-stu-id="7d8d9-116">Cloud Solution Providers can create a support ticket for their customer's subscriptions by logging into their customer's tenant and specifying their home tenant id using *CSPHomeTenantId* parameter.</span></span>

<span data-ttu-id="7d8d9-117">__Per i ticket tecnici:__</span><span class="sxs-lookup"><span data-stu-id="7d8d9-117">__For technical tickets:__</span></span>

<span data-ttu-id="7d8d9-118">Per specificare il nome della risorsa, specificare l'ID di risorsa ARM della risorsa usando il parametro *TechnicalTicketResourceId* .</span><span class="sxs-lookup"><span data-stu-id="7d8d9-118">To specify the resource name, specify the ARM resource ID of the resource by using *TechnicalTicketResourceId* parameter.</span></span> <span data-ttu-id="7d8d9-119">Vedere un esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-119">See an example below.</span></span> 

<span data-ttu-id="7d8d9-120">__Per i ticket di quota:__</span><span class="sxs-lookup"><span data-stu-id="7d8d9-120">__For quota tickets:__</span></span>

<span data-ttu-id="7d8d9-121">Per richiedere un aumento delle quote per il **calcolo di core VM**, **batch**, **database SQL** e **data warehouse SQL**, fornisci dettagli aggiuntivi in oggetto *QuotaTicketDetail* .</span><span class="sxs-lookup"><span data-stu-id="7d8d9-121">To request for quota increase for **Compute VM Cores**, **Batch**, **SQL Database** and **SQL Data Warehouse**, provide additional details under *QuotaTicketDetail* object.</span></span> <span data-ttu-id="7d8d9-122">L'oggetto QuotaTicketDetail è costituito da 3 proprietà come descritto di seguito.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-122">QuotaTicketDetail object consists of 3 properties as described below.</span></span> <span data-ttu-id="7d8d9-123">Per una documentazione dettagliata, [fare clic qui.](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="7d8d9-123">For detailed documentation, please [click here.](https://aka.ms/supportrpquotarequestpayload)</span></span>

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


<span data-ttu-id="7d8d9-124">Per informazioni dettagliate su come creare payload per vari tipi di quote, [fare clic qui](https://aka.ms/supportrpquotarequestpayload)</span><span class="sxs-lookup"><span data-stu-id="7d8d9-124">For detailed documentation on how to construct Payload for various quota types, please [click here](https://aka.ms/supportrpquotarequestpayload)</span></span>

## <span data-ttu-id="7d8d9-125">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d8d9-125">EXAMPLES</span></span>

### <span data-ttu-id="7d8d9-126">Esempio 1: creare un ticket di supporto per la gestione delle fatture o degli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-126">Example 1: Create a Billing or Subscription Management support ticket.</span></span> <span data-ttu-id="7d8d9-127">Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi di gestione della fatturazione o dell'abbonamento per cui si vuole richiedere il supporto</span><span class="sxs-lookup"><span data-stu-id="7d8d9-127">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Billing or Subscription Management problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7d8d9-128">Esempio 2: creare un ticket di supporto tecnico per la risorsa macchina virtuale per Windows.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-128">Example 2: Create a technical support ticket for Virtual Machine for Windows resource.</span></span> <span data-ttu-id="7d8d9-129">Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi della macchina virtuale per Windows per cui si vuole richiedere il supporto</span><span class="sxs-lookup"><span data-stu-id="7d8d9-129">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Virtual Machine for Windows problem classification for which you want to request support</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{vm_windows_service_guid}/problemClassifications/{problemClassification_guid}" -TechnicalTicketResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM" -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName              Status CreatedDate
----  ----- --------------- -------- ------------------              ------ -----------
test1 Test  150010521000317 Minimal  Virtual Machine running Windows Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7d8d9-130">Esempio 3: creare un ticket di supporto delle quote per aumentare la quota per i core della macchina virtuale per una famiglia di VM specifica.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-130">Example 3: Create a quota support ticket to increase quota for Virtual Machine Cores for a specific VM family.</span></span> <span data-ttu-id="7d8d9-131">Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi di calcolo delle quote di VM Core.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-131">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Compute VM Cores problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{cores_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":350}"}, @{Region = "eastus"; Payload = "{`"VMFamily`":`"Dv2 Series`",`"NewLimit`":516}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7d8d9-132">Esempio 4: creare un ticket di supporto delle quote per aumentare la quota per i core con priorità bassa per un account batch.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-132">Example 4: Create a quota support ticket to increase quota for Low-priority cores for a Batch account.</span></span> <span data-ttu-id="7d8d9-133">Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi del batch di quote.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-133">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":200,`"Type`":`"LowPriority`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7d8d9-134">Esempio 5: creare un ticket di supporto delle quote per aumentare la quota di VM Core per una famiglia di VM specifica per un account batch.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-134">Example 5: Create a quota support ticket to increase VM cores quota for a specific VM Family for a Batch account.</span></span> <span data-ttu-id="7d8d9-135">Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi del batch di quote.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-135">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"VMFamily`":`"standardA0_A7Family`",`"NewLimit`":200,`"Type`":`"Dedicated`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7d8d9-136">Esempio 6: creare un ticket di supporto delle quote per aumentare la quota di pool per un account batch.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-136">Example 6: Create a quota support ticket to increase Pools quota for a Batch account.</span></span> <span data-ttu-id="7d8d9-137">Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi del batch di quote.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-137">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Pools`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7d8d9-138">Esempio 7: creare un ticket di supporto delle quote per aumentare i processi attivi e pianificare la quota di lavoro per un account batch.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-138">Example 7: Create a quota support ticket to increase active Jobs and job schedules quota for a Batch account.</span></span> <span data-ttu-id="7d8d9-139">Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi del batch di quote.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-139">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Account" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"AccountName`":`"test`",`"NewLimit`":120,`"Type`":`"Jobs`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7d8d9-140">Esempio 8: creare un ticket di supporto per la quota per aumentare il numero di account batch per un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-140">Example 8: Create a quota support ticket to increase number of Batch accounts for a subscription.</span></span> <span data-ttu-id="7d8d9-141">Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi del batch di quote.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-141">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Batch problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{batch_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Subscription" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":120,`"Type`":`"Account`"}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7d8d9-142">Esempio 9: creare un ticket di supporto delle quote per aumentare la quota per DTU per database SQL.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-142">Example 9: Create a quota support ticket to increase quota for DTUs for SQL Database.</span></span> <span data-ttu-id="7d8d9-143">Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi di database SQL quota.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-143">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7d8d9-144">Esempio 10: creare un ticket di supporto delle quote per aumentare la quota per i server per database SQL.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-144">Example 10: Create a quota support ticket to increase quota for Servers for SQL Database.</span></span> <span data-ttu-id="7d8d9-145">Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi di database SQL quota.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-145">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Database problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_database_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7d8d9-146">Esempio 11: creare un ticket di supporto delle quote per aumentare la quota per DTU per il data warehouse SQL.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-146">Example 11: Create a quota support ticket to increase quota for DTUs for SQL Data Warehouse.</span></span> <span data-ttu-id="7d8d9-147">Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi di data warehouse SQL quota.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-147">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Date Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "DTUs" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"ServerName`":`"testserver`",`"NewLimit`":54000}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7d8d9-148">Esempio 12: creare un ticket di supporto delle quote per aumentare la quota per i server per il data warehouse SQL.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-148">Example 12: Create a quota support ticket to increase quota for Servers for SQL Data Warehouse.</span></span> <span data-ttu-id="7d8d9-149">Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi del data warehouse SQL quota.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-149">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Data Warehouse problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_datawarehouse_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "Servers" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200}"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7d8d9-150">Esempio 13: creare un ticket di supporto delle quote per aumentare la quota per i core a bassa priorità per il servizio di apprendimento automatico.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-150">Example 13: Create a quota support ticket to increase quota for Low-priority cores for Machine Learning service.</span></span> <span data-ttu-id="7d8d9-151">Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi del servizio di apprendimento delle quote.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-151">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"LowPriority`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7d8d9-152">Esempio 14: creare un ticket di supporto delle quote per aumentare la quota di VM Core per una specifica famiglia di VM per il servizio di apprendimento automatico.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-152">Example 14: Create a quota support ticket to increase VM cores quota for a specific VM Family for Machine Learning service.</span></span> <span data-ttu-id="7d8d9-153">Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi del servizio di apprendimento delle quote.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-153">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota Machine Learning service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{machine_learning_service_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "BatchAml" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"VMFamily`":`"standardDFamily`",`"NewLimit`":200,`"Type`":`"Dedicated`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7d8d9-154">Esempio 15: creare un ticket di supporto delle quote per aumentare la quota per l'istanza gestita di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-154">Example 15: Create a quota support ticket to increase quota for Azure SQL Managed Instance.</span></span> <span data-ttu-id="7d8d9-155">Usare Get-AzSupportService e Get-AzSupportProblemClassification per recuperare i GUID corretti per la classificazione dei problemi del servizio di istanza gestita da SQL di quota.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-155">Use Get-AzSupportService and Get-AzSupportProblemClassification to retrieve correct GUIDs for Quota SQL Managed Instance service problem classification.</span></span>
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{quota_service_guid}/problemClassifications/{sql_managed_instance_problemClassification_guid}" -QuotaTicketDetail @{QuotaChangeRequestVersion = "1.0" ; QuotaChangeRequestSubType = "SQLMI" ; QuotaChangeRequests = (@{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"vCore`" }"}, @{Region = "westus"; Payload = "{`"NewLimit`":200,`"Type`":`"Subnet`" }"})} -CustomerContactDetail @{FirstName = "first" ; LastName = "last" ; PreferredTimeZone = "pacific standard time" ; PreferredSupportLanguage = "en-us" ; Country = "USA" ; PreferredContactMethod = "Email" ; PrimaryEmailAddress = "user@contoso.com"}

Name  Title SupportTicketId Severity ServiceDisplayName                       Status CreatedDate
----  ----- --------------- -------- ------------------                       ------ -----------
test1 Test  150010521000317 Minimal  Service and subscription limits (quotas) Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7d8d9-156">Esempio 16: creare un ticket di supporto specificando i singoli parametri di contatto del cliente anziché l'oggetto CustomerContactDetail.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-156">Example 16: Create a support ticket by specifying individual customer contact parameters instead of CustomerContactDetail object.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com"

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7d8d9-157">Esempio 17: creare un ticket di supporto con la richiesta di risposta 24 x 7 da Azure.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-157">Example 17: Create a support ticket with request for 24 x 7 response from Azure.</span></span> 
```powershell
PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "critical" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -Require24X7Response 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Critical  Billing            Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="7d8d9-158">Esempio 18: creare un ticket di supporto per conto del cliente se si è un provider di soluzioni cloud (CSP).</span><span class="sxs-lookup"><span data-stu-id="7d8d9-158">Example 18: Create a support ticket on behalf of your customer if you are a Cloud Solution Provider (CSP).</span></span> <span data-ttu-id="7d8d9-159">Il CSP deve prima eseguire l'accesso al tenant e quindi effettuare l'accesso al tenant del cliente, come illustrato nell'esempio seguente.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-159">CSP should first login into their tenant, and then login into customer's tenant as shown in the example below.</span></span> <span data-ttu-id="7d8d9-160">Devono quindi usare il parametro-CSPHomeTenantId per specificare l'ID del tenant Home al momento della creazione di un ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-160">They must then use -CSPHomeTenantId parameter to specify their home tenant id at the time of creating a support ticket.</span></span>  
```powershell

PS C:\> Login-AzAccount

PS C:\> Login-AzAccount -TenantId {customer_tenant_id}

PS C:\> New-AzSupportTicket -Name "test1" -Title "Test" -Description "Test" -Severity "minimal" -ProblemClassificationId "/providers/Microsoft.Support/services/{billing_service_guid}/problemClassifications/{problemClassification_guid}" -CustomerFirstName "first" -CustomerLastName "last" -CustomerPreferredTimeZone "pacific standard time" -CustomerPreferredSupportLanguage "en-us" -CustomerCountry = "USA" -PreferredContactMethod "Email" -CustomerPrimaryEmailAddress "user@contoso.com" -CSPHomeTenantId {csp_home_tenant_id} 

Name  Title SupportTicketId Severity ServiceDisplayName Status CreatedDate
----  ----- --------------- -------- ------------------ ------ -----------
test1 Test  150010521000317 Minimal  Billing            Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="7d8d9-161">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7d8d9-161">PARAMETERS</span></span>

### <span data-ttu-id="7d8d9-162">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="7d8d9-162">-AdditionalEmailAddress</span></span>
<span data-ttu-id="7d8d9-163">Altri indirizzi di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-163">Additional email addresses.</span></span>
<span data-ttu-id="7d8d9-164">Gli indirizzi di posta elettronica elencati qui verranno copiati in corrispondenza del ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-164">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

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

### <span data-ttu-id="7d8d9-165">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d8d9-165">-AsJob</span></span>
<span data-ttu-id="7d8d9-166">Esegui cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-166">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="7d8d9-167">-CSPHomeTenantId</span><span class="sxs-lookup"><span data-stu-id="7d8d9-167">-CSPHomeTenantId</span></span>
<span data-ttu-id="7d8d9-168">Questo è l'ID tenant Home dell'utente del provider di soluzioni cloud che prova a creare un ticket di supporto per il cliente.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-168">This is the home tenant id of the Cloud Solution Provider user trying to create a support ticket for their customer.</span></span>

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

### <span data-ttu-id="7d8d9-169">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="7d8d9-169">-CustomerContactDetail</span></span>
<span data-ttu-id="7d8d9-170">Dettagli di contatto del cliente associati alla risorsa SupportTicket.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-170">Customer contact details associated with SupportTicket resource.</span></span>

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

### <span data-ttu-id="7d8d9-171">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="7d8d9-171">-CustomerCountry</span></span>
<span data-ttu-id="7d8d9-172">Paese del cliente.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-172">Customer country.</span></span>
<span data-ttu-id="7d8d9-173">Questo deve essere un codice di paese ISO alfa-3 valido (ISO 3166).</span><span class="sxs-lookup"><span data-stu-id="7d8d9-173">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="7d8d9-174">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="7d8d9-174">-CustomerFirstName</span></span>
<span data-ttu-id="7d8d9-175">Nome cliente.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-175">Customer first name.</span></span>

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

### <span data-ttu-id="7d8d9-176">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="7d8d9-176">-CustomerLastName</span></span>
<span data-ttu-id="7d8d9-177">Cognome del cliente.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-177">Customer last name.</span></span>

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

### <span data-ttu-id="7d8d9-178">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="7d8d9-178">-CustomerPhoneNumber</span></span>
<span data-ttu-id="7d8d9-179">Numero di telefono del cliente.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-179">Customer phone number.</span></span>
<span data-ttu-id="7d8d9-180">Questo è obbligatorio se il metodo di contatto preferito è Phone.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-180">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="7d8d9-181">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="7d8d9-181">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="7d8d9-182">Lingua peferred dell'usanza.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-182">Peferred language of the custom.</span></span>
<span data-ttu-id="7d8d9-183">Questo deve essere un codice contabile della lingua valido per una delle lingue supportate elencate qui https://azure.microsoft.com/en-us/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="7d8d9-183">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/en-us/support/faq/.</span></span>

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

### <span data-ttu-id="7d8d9-184">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="7d8d9-184">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="7d8d9-185">Fuso orario preferito dal cliente.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-185">Customer preferred time zone.</span></span>
<span data-ttu-id="7d8d9-186">Deve essere un valore System.TimeZoneInfo.Id valido.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-186">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="7d8d9-187">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="7d8d9-187">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="7d8d9-188">Indirizzo di posta elettronica principale del cliente.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-188">Customer primary email address.</span></span>

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

### <span data-ttu-id="7d8d9-189">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d8d9-189">-DefaultProfile</span></span>
<span data-ttu-id="7d8d9-190">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-190">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d8d9-191">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d8d9-191">-Description</span></span>
<span data-ttu-id="7d8d9-192">Descrizione dettagliata della domanda o del problema.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-192">Detailed description of the question or issue.</span></span>

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

### <span data-ttu-id="7d8d9-193">-Nome</span><span class="sxs-lookup"><span data-stu-id="7d8d9-193">-Name</span></span>
<span data-ttu-id="7d8d9-194">Nome del ticket di supporto creato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-194">Name of support ticket that this cmdlet creates.</span></span>

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

### <span data-ttu-id="7d8d9-195">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="7d8d9-195">-PreferredContactMethod</span></span>
<span data-ttu-id="7d8d9-196">Metodo di contatto preferito.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-196">Preferred contact method.</span></span>

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

### <span data-ttu-id="7d8d9-197">-ProblemClassificationId</span><span class="sxs-lookup"><span data-stu-id="7d8d9-197">-ProblemClassificationId</span></span>
<span data-ttu-id="7d8d9-198">Ogni servizio Azure ha un proprio set di categorie di problemi denominato classificazione del problema che corrisponde al tipo di problema che si sta verificando.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-198">Each Azure service has its own set of issue category called problem classification that corresponds to the type of problem you're experiencing.</span></span>
<span data-ttu-id="7d8d9-199">Questo parametro è l'ID delle risorse ARM della risorsa ProblemClassification.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-199">This parameter is the ARM resource id of ProblemClassification resource.</span></span>

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

### <span data-ttu-id="7d8d9-200">-ProblemStartTime</span><span class="sxs-lookup"><span data-stu-id="7d8d9-200">-ProblemStartTime</span></span>
<span data-ttu-id="7d8d9-201">Data e ora di inizio del problema.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-201">Date and time when the problem started.</span></span>

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

### <span data-ttu-id="7d8d9-202">-QuotaTicketDetail</span><span class="sxs-lookup"><span data-stu-id="7d8d9-202">-QuotaTicketDetail</span></span>
<span data-ttu-id="7d8d9-203">Dettagli aggiuntivi per un ticket di supporto delle quote.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-203">Additional details for a Quota support ticket.</span></span>

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

### <span data-ttu-id="7d8d9-204">-Require24X7Response</span><span class="sxs-lookup"><span data-stu-id="7d8d9-204">-Require24X7Response</span></span>
<span data-ttu-id="7d8d9-205">Indica se questo ticket di supporto richiede una risposta 24x7 da Azure.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-205">Indicates if this support ticket requires a 24x7 response from Azure.</span></span>

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

### <span data-ttu-id="7d8d9-206">-Gravità</span><span class="sxs-lookup"><span data-stu-id="7d8d9-206">-Severity</span></span>
<span data-ttu-id="7d8d9-207">Gravità del ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-207">Severity of the support ticket.</span></span>
<span data-ttu-id="7d8d9-208">Questo indica l'urgenza del caso, che a sua volta determina il tempo di risposta in base al contratto del livello di servizio del piano di supporto tecnico in Azure.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-208">This indicates the urgency of the case, which in turn determines the response time according to the service level agreement of the technical support plan you have with Azure.</span></span>

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

### <span data-ttu-id="7d8d9-209">-TechnicalTicketResourceId</span><span class="sxs-lookup"><span data-stu-id="7d8d9-209">-TechnicalTicketResourceId</span></span>
<span data-ttu-id="7d8d9-210">Questo è l'ID risorsa della risorsa di Azure Service, ad esempio una risorsa macchina virtuale o una risorsa HDInsight, per cui viene creato il ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-210">This is the resource id of the Azure service resource (For example: A virtual machine resource or an HDInsight resource) for which the support ticket is created.</span></span>

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

### <span data-ttu-id="7d8d9-211">-Titolo</span><span class="sxs-lookup"><span data-stu-id="7d8d9-211">-Title</span></span>
<span data-ttu-id="7d8d9-212">Titolo del ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-212">Title of support ticket.</span></span>

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

### <span data-ttu-id="7d8d9-213">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7d8d9-213">-Confirm</span></span>
<span data-ttu-id="7d8d9-214">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-214">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d8d9-215">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d8d9-215">-WhatIf</span></span>
<span data-ttu-id="7d8d9-216">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-216">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d8d9-217">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-217">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d8d9-218">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d8d9-218">CommonParameters</span></span>
<span data-ttu-id="7d8d9-219">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d8d9-219">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d8d9-220">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d8d9-220">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d8d9-221">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7d8d9-221">INPUTS</span></span>

### <span data-ttu-id="7d8d9-222">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7d8d9-222">None</span></span>

## <span data-ttu-id="7d8d9-223">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d8d9-223">OUTPUTS</span></span>

### <span data-ttu-id="7d8d9-224">Microsoft. Azure. Commands. support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="7d8d9-224">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="7d8d9-225">Note</span><span class="sxs-lookup"><span data-stu-id="7d8d9-225">NOTES</span></span>

## <span data-ttu-id="7d8d9-226">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d8d9-226">RELATED LINKS</span></span>
