---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/get-azsupportproblemclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportProblemClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportProblemClassification.md
ms.openlocfilehash: 0c8bf7d7a8217ed63920495591f8ad061f1b0a8e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972494"
---
# <span data-ttu-id="52b35-101">Get-AzSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="52b35-101">Get-AzSupportProblemClassification</span></span>

## <span data-ttu-id="52b35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52b35-102">SYNOPSIS</span></span>
<span data-ttu-id="52b35-103">Ottenere le classificazioni dei problemi per il servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="52b35-103">Get problem classifications for the service specified.</span></span>

## <span data-ttu-id="52b35-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52b35-104">SYNTAX</span></span>

### <span data-ttu-id="52b35-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="52b35-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSupportProblemClassification -ServiceId <String> [-Id <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="52b35-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="52b35-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSupportProblemClassification [-Id <String>] -ServiceObject <PSSupportService>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52b35-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="52b35-107">DESCRIPTION</span></span>
<span data-ttu-id="52b35-108">Recupera l'elenco corrente di classificazione dei problemi per un servizio di Azure.</span><span class="sxs-lookup"><span data-stu-id="52b35-108">Gets the current list of problem classification for an Azure service.</span></span> <span data-ttu-id="52b35-109">È possibile usare il GUID per la classificazione del servizio e del problema per creare un nuovo ticket di supporto usando New-AzSupportTicket.</span><span class="sxs-lookup"><span data-stu-id="52b35-109">You can use the service and problem classification GUID to create a new support ticket using New-AzSupportTicket.</span></span>

<span data-ttu-id="52b35-110">Usare sempre i GUID della classificazione del servizio e dei problemi ottenuti a livello di programmazione.</span><span class="sxs-lookup"><span data-stu-id="52b35-110">Always use the service and problem classification GUIDs obtained programmatically.</span></span> <span data-ttu-id="52b35-111">Questa procedura assicura di avere il set più recente di GUID per la classificazione dei servizi e dei problemi per la creazione dei ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="52b35-111">This practice ensures that you have the most recent set of service and problem classification GUIDs for support ticket creation.</span></span>

## <span data-ttu-id="52b35-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52b35-112">EXAMPLES</span></span>

### <span data-ttu-id="52b35-113">Esempio 1: Ottenere tutte le classificazioni dei problemi per un servizio usando il parametro ID servizio.</span><span class="sxs-lookup"><span data-stu-id="52b35-113">Example 1: Get all problem classificaitons for a service using service id parameter.</span></span>
```powershell
PS C:\> Get-AzSupportProblemClassification -ServiceId "{vm_running_windows_service_guid}"

Name                                 DisplayName
----                                 -----------
4d78b174-3203-a3ac-9e08-41fb35de6354 Compute-VM (cores-vCPUs) subscription limit increases
923d6b56-d573-f943-b65d-d69ba79ea21a Cannot connect to my VM / My configuration change impacted connectivity
9e9faedb-7764-448b-244a-14eca26f5362 Cannot connect to my VM / Troubleshoot my network security group (NSG)
a0456e7c-3e84-2bd5-63e9-2fc8ba7cff73 Cannot connect to my VM / Troubleshoot my VM firewall
e5c307e3-50ff-5dc9-c8ae-7d35051f88c9 Cannot connect to my VM / I have an issue with my public IP
f325e249-4f10-e5bd-28f6-a466704826da Cannot connect to my VM / I need to reset my password
f44a2b74-6a5c-a93f-a259-81e756e8cc27 Cannot connect to my VM / I need guidance with serial console access
92c2396d-b703-973f-1bca-2eea9425b21a Cannot connect to my VM / Failure to connect using RDP or SSH port
d36eec9e-cab1-8d62-1ce5-3245a02e3bcf Cannot connect to my VM / My problem is not listed above
83e6afa6-4ecd-e1c6-ef63-de73e96d0842 Cannot start or stop my VM / My VM will not start after a configuration change
240605e1-1510-255d-b490-cb95f582b1dc Cannot start or stop my VM / I received a disk related error
f47d6b99-6f4b-d21a-feee-1800ad391e10 Cannot start or stop my VM / I received an allocation failure
```

### <span data-ttu-id="52b35-114">Esempio 2: Ottenere tutte le classificazioni di problemi per un servizio usando l'oggetto servizio padre</span><span class="sxs-lookup"><span data-stu-id="52b35-114">Example 2: Get all problem classificaitons for a service using parent service object</span></span>
```powershell
PS C:\> Get-AzSupportService -Id "{vm_running_windows_service_guid}" | Get-AzSupportProblemClassification 

Name                                 DisplayName
----                                 -----------
4d78b174-3203-a3ac-9e08-41fb35de6354 Compute-VM (cores-vCPUs) subscription limit increases
923d6b56-d573-f943-b65d-d69ba79ea21a Cannot connect to my VM / My configuration change impacted connectivity
9e9faedb-7764-448b-244a-14eca26f5362 Cannot connect to my VM / Troubleshoot my network security group (NSG)
a0456e7c-3e84-2bd5-63e9-2fc8ba7cff73 Cannot connect to my VM / Troubleshoot my VM firewall
e5c307e3-50ff-5dc9-c8ae-7d35051f88c9 Cannot connect to my VM / I have an issue with my public IP
f325e249-4f10-e5bd-28f6-a466704826da Cannot connect to my VM / I need to reset my password
f44a2b74-6a5c-a93f-a259-81e756e8cc27 Cannot connect to my VM / I need guidance with serial console access
92c2396d-b703-973f-1bca-2eea9425b21a Cannot connect to my VM / Failure to connect using RDP or SSH port
d36eec9e-cab1-8d62-1ce5-3245a02e3bcf Cannot connect to my VM / My problem is not listed above
83e6afa6-4ecd-e1c6-ef63-de73e96d0842 Cannot start or stop my VM / My VM will not start after a configuration change
240605e1-1510-255d-b490-cb95f582b1dc Cannot start or stop my VM / I received a disk related error
f47d6b99-6f4b-d21a-feee-1800ad391e10 Cannot start or stop my VM / I received an allocation failure
```

### <span data-ttu-id="52b35-115">Esempio 3: Ottenere i dettagli di un singolo problema classificati in base all'ID dall'oggetto servizio di piping</span><span class="sxs-lookup"><span data-stu-id="52b35-115">Example 3: Get details of a single problem classificaiton by id by piping service object</span></span>
```powershell
PS C:\> Get-AzSupportService -Id "{vm_running_windows_service_guid}" | Get-AzSupportProblemClassification -Id 923d6b56-d573-f943-b65d-d69ba79ea21a

Name                                 DisplayName
----                                 -----------
923d6b56-d573-f943-b65d-d69ba79ea21a Cannot connect to my VM / My configuration change impacted connectivity
```

## <span data-ttu-id="52b35-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52b35-116">PARAMETERS</span></span>

### <span data-ttu-id="52b35-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52b35-117">-DefaultProfile</span></span>
<span data-ttu-id="52b35-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="52b35-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52b35-119">-Id</span><span class="sxs-lookup"><span data-stu-id="52b35-119">-Id</span></span>
<span data-ttu-id="52b35-120">ID classificazione del problema.</span><span class="sxs-lookup"><span data-stu-id="52b35-120">Problem classification id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b35-121">-ServiceId</span><span class="sxs-lookup"><span data-stu-id="52b35-121">-ServiceId</span></span>
<span data-ttu-id="52b35-122">ID servizio per cui vengono recuperate tutte le classificazioni di problemi.</span><span class="sxs-lookup"><span data-stu-id="52b35-122">Service id for which all problem classifications are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b35-123">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="52b35-123">-ServiceObject</span></span>
<span data-ttu-id="52b35-124">Oggetto servizio per cui vengono recuperate le classificazioni di problemi.</span><span class="sxs-lookup"><span data-stu-id="52b35-124">Service object for which problem classifications are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportService
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52b35-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52b35-125">CommonParameters</span></span>
<span data-ttu-id="52b35-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52b35-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52b35-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="52b35-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52b35-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="52b35-128">INPUTS</span></span>

### <span data-ttu-id="52b35-129">Microsoft.Azure.Commands.Support.Models.PSSupportService</span><span class="sxs-lookup"><span data-stu-id="52b35-129">Microsoft.Azure.Commands.Support.Models.PSSupportService</span></span>

## <span data-ttu-id="52b35-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52b35-130">OUTPUTS</span></span>

### <span data-ttu-id="52b35-131">Microsoft.Azure.Commands.Support.Models.PSSupportProblemClassification</span><span class="sxs-lookup"><span data-stu-id="52b35-131">Microsoft.Azure.Commands.Support.Models.PSSupportProblemClassification</span></span>

## <span data-ttu-id="52b35-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="52b35-132">NOTES</span></span>

## <span data-ttu-id="52b35-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52b35-133">RELATED LINKS</span></span>
