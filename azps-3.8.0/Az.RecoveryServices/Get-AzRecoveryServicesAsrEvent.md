---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrEvent.md
ms.openlocfilehash: 8ed57766ba36607503994d331cec5381d9f43bbf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865169"
---
# <span data-ttu-id="4e408-101">Get-AzRecoveryServicesAsrEvent</span><span class="sxs-lookup"><span data-stu-id="4e408-101">Get-AzRecoveryServicesAsrEvent</span></span>

## <span data-ttu-id="4e408-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4e408-102">SYNOPSIS</span></span>
<span data-ttu-id="4e408-103">Ottiene i dettagli degli eventi di ripristino del sito di Azure nel Vault.</span><span class="sxs-lookup"><span data-stu-id="4e408-103">Gets details of Azure Site Recovery events in the vault.</span></span>

## <span data-ttu-id="4e408-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e408-104">SYNTAX</span></span>

### <span data-ttu-id="4e408-105">ByParam (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4e408-105">ByParam (Default)</span></span>
```
Get-AzRecoveryServicesAsrEvent [-AffectedObjectFriendlyName <String>] [-Fabric <ASRFabric>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e408-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4e408-106">ByResourceId</span></span>
```
Get-AzRecoveryServicesAsrEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e408-107">ByFabricId</span><span class="sxs-lookup"><span data-stu-id="4e408-107">ByFabricId</span></span>
```
Get-AzRecoveryServicesAsrEvent -FabricId <String> [-AffectedObjectFriendlyName <String>] [-Severity <String>]
 [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e408-108">ByName</span><span class="sxs-lookup"><span data-stu-id="4e408-108">ByName</span></span>
```
Get-AzRecoveryServicesAsrEvent -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e408-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e408-109">DESCRIPTION</span></span>
<span data-ttu-id="4e408-110">L'opzione **Get-AzRecoveryServicesAsrEvent** Ottiene l'elenco degli eventi nel Vault in base ai filtri di selezione specificati.</span><span class="sxs-lookup"><span data-stu-id="4e408-110">The **Get-AzRecoveryServicesAsrEvent** gets the list of events in the vault based on the specified selection filters.</span></span>

## <span data-ttu-id="4e408-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e408-111">EXAMPLES</span></span>

### <span data-ttu-id="4e408-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4e408-112">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent
```

<span data-ttu-id="4e408-113">Elenco di tutti gli eventi.</span><span class="sxs-lookup"><span data-stu-id="4e408-113">List of all events.</span></span>

### <span data-ttu-id="4e408-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4e408-114">Example 2</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -EventName "VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f"


AffectedObjectFriendlyName   : V2A-W2K12-400
Description                  : Virtual machine health is in Critical state.
EventCode                    : SRSVMHealthChanged
EventSpecificDetails         :
EventType                    : AgentHealth
FabricId                     : /Subscriptions/xxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxxxxxx/replicationFabrics/xxxxxxxxxxxx
HealthErrors                 : {}
Name                         : VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f
ProviderSpecificEventDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRInMageAzureV2EventDetails
Severity                     : Critical
TimeOfOccurence              : 8/17/2017 12:31:43 PM
```

<span data-ttu-id="4e408-115">Ottenere un evento per nome.</span><span class="sxs-lookup"><span data-stu-id="4e408-115">Get event by name.</span></span>

### <span data-ttu-id="4e408-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="4e408-116">Example 3</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxxx
```

<span data-ttu-id="4e408-117">Elenco di eventi per l'oggetto interessato.</span><span class="sxs-lookup"><span data-stu-id="4e408-117">List of event for affected Object.</span></span>

### <span data-ttu-id="4e408-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="4e408-118">Example 4</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxx -StartTime "8/17/2017 12:31:40 PM" -EndTime "8/17/2017 12:31:44 PM" -Severity Critical -EventType VmHealth
```

<span data-ttu-id="4e408-119">Elenco di eventi tra l'ora di inizio e l'ora di fine, la gravità critica e il tipo di integrità VmHealth.</span><span class="sxs-lookup"><span data-stu-id="4e408-119">List of event between time start time and end time , severity critical and health type VmHealth.</span></span>

## <span data-ttu-id="4e408-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4e408-120">PARAMETERS</span></span>

### <span data-ttu-id="4e408-121">-AffectedObjectFriendlyName</span><span class="sxs-lookup"><span data-stu-id="4e408-121">-AffectedObjectFriendlyName</span></span>
<span data-ttu-id="4e408-122">Specifica AffectedObject FriendlyName per la ricerca.</span><span class="sxs-lookup"><span data-stu-id="4e408-122">Specifies AffectedObject FriendlyName for the search.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e408-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e408-123">-DefaultProfile</span></span>
<span data-ttu-id="4e408-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4e408-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e408-125">-EndTime</span><span class="sxs-lookup"><span data-stu-id="4e408-125">-EndTime</span></span>
<span data-ttu-id="4e408-126">Specifica l'ora di fine della finestra di ricerca.</span><span class="sxs-lookup"><span data-stu-id="4e408-126">Specifies the end time of the search window.</span></span> <span data-ttu-id="4e408-127">Usa questo parametro per ottenere solo gli eventi che si sono verificati prima del tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="4e408-127">Use this parameter to get only those events that have occurred before the specified time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e408-128">-EventType</span><span class="sxs-lookup"><span data-stu-id="4e408-128">-EventType</span></span>
<span data-ttu-id="4e408-129">Filtrare gli eventi in base al tipo di evento.</span><span class="sxs-lookup"><span data-stu-id="4e408-129">Filter events by the event type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: VmHealth, ServerHealth, AgentHealth

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e408-130">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="4e408-130">-Fabric</span></span>
<span data-ttu-id="4e408-131">Filtrare gli eventi in base al tessuto specificato.</span><span class="sxs-lookup"><span data-stu-id="4e408-131">Filter events by the specified fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e408-132">-FabricId</span><span class="sxs-lookup"><span data-stu-id="4e408-132">-FabricId</span></span>
<span data-ttu-id="4e408-133">Specifica il fabricId da filtrare.</span><span class="sxs-lookup"><span data-stu-id="4e408-133">Specifies the fabricId to filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFabricId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e408-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="4e408-134">-Name</span></span>
<span data-ttu-id="4e408-135">Specifica il nome dell'evento per la ricerca.</span><span class="sxs-lookup"><span data-stu-id="4e408-135">Specifies name of the event for search.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e408-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e408-136">-ResourceId</span></span>
<span data-ttu-id="4e408-137">Specifica l'evento ResourceId dell'evento.</span><span class="sxs-lookup"><span data-stu-id="4e408-137">Specifies the event ResourceId of event.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e408-138">-Gravità</span><span class="sxs-lookup"><span data-stu-id="4e408-138">-Severity</span></span>
<span data-ttu-id="4e408-139">Gravità dell'evento su cui applicare il filtro.</span><span class="sxs-lookup"><span data-stu-id="4e408-139">Event severity to filter on.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: Critical, Warning, OK, Unknown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e408-140">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4e408-140">-StartTime</span></span>
<span data-ttu-id="4e408-141">Specifica l'ora di inizio della finestra di ricerca.</span><span class="sxs-lookup"><span data-stu-id="4e408-141">Specifies the start time of the search window.</span></span> <span data-ttu-id="4e408-142">Usa questo parametro per ottenere solo gli eventi che si sono verificati dopo il periodo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="4e408-142">Use this parameter to get only those events that have occurred after the specified time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e408-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e408-143">CommonParameters</span></span>
<span data-ttu-id="4e408-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e408-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e408-145">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e408-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e408-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4e408-146">INPUTS</span></span>

### <span data-ttu-id="4e408-147">System. String</span><span class="sxs-lookup"><span data-stu-id="4e408-147">System.String</span></span>

## <span data-ttu-id="4e408-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e408-148">OUTPUTS</span></span>

### <span data-ttu-id="4e408-149">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASREvent</span><span class="sxs-lookup"><span data-stu-id="4e408-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASREvent</span></span>

## <span data-ttu-id="4e408-150">Note</span><span class="sxs-lookup"><span data-stu-id="4e408-150">NOTES</span></span>

## <span data-ttu-id="4e408-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e408-151">RELATED LINKS</span></span>
