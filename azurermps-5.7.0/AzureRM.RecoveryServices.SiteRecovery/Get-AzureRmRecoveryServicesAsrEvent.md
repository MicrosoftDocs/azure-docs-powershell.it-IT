---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrEvent.md
ms.openlocfilehash: e32f0b1d12b1cb0399ddef04623ac76557c809b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519388"
---
# <span data-ttu-id="5dbcf-101">Get-AzureRmRecoveryServicesAsrEvent</span><span class="sxs-lookup"><span data-stu-id="5dbcf-101">Get-AzureRmRecoveryServicesAsrEvent</span></span>

## <span data-ttu-id="5dbcf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5dbcf-102">SYNOPSIS</span></span>
<span data-ttu-id="5dbcf-103">Ottiene i dettagli degli eventi di ripristino del sito di Azure nel Vault.</span><span class="sxs-lookup"><span data-stu-id="5dbcf-103">Gets details of Azure Site Recovery events in the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5dbcf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5dbcf-104">SYNTAX</span></span>

### <span data-ttu-id="5dbcf-105">ByParam (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5dbcf-105">ByParam (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent [-AffectedObjectFriendlyName <String>] [-Fabric <ASRFabric>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5dbcf-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5dbcf-106">ByResourceId</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5dbcf-107">ByFabricId</span><span class="sxs-lookup"><span data-stu-id="5dbcf-107">ByFabricId</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent -FabricId <String> [-AffectedObjectFriendlyName <String>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5dbcf-108">ByName</span><span class="sxs-lookup"><span data-stu-id="5dbcf-108">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5dbcf-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5dbcf-109">DESCRIPTION</span></span>
<span data-ttu-id="5dbcf-110">L'opzione **Get-AzureRmRecoveryServicesAsrEvent** Ottiene l'elenco degli eventi nel Vault in base ai filtri di selezione specificati.</span><span class="sxs-lookup"><span data-stu-id="5dbcf-110">The **Get-AzureRmRecoveryServicesAsrEvent** gets the list of events in the vault based on the specified selection filters.</span></span>

## <span data-ttu-id="5dbcf-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5dbcf-111">EXAMPLES</span></span>

### <span data-ttu-id="5dbcf-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5dbcf-112">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent
```

<span data-ttu-id="5dbcf-113">Elenco di tutti gli eventi.</span><span class="sxs-lookup"><span data-stu-id="5dbcf-113">List of all events.</span></span>

### <span data-ttu-id="5dbcf-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5dbcf-114">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -EventName "VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f"


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

<span data-ttu-id="5dbcf-115">Ottenere un evento per nome.</span><span class="sxs-lookup"><span data-stu-id="5dbcf-115">Get event by name.</span></span>

### <span data-ttu-id="5dbcf-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="5dbcf-116">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxxx
```

<span data-ttu-id="5dbcf-117">Elenco di eventi per l'oggetto interessato.</span><span class="sxs-lookup"><span data-stu-id="5dbcf-117">List of event for affected Object.</span></span>

### <span data-ttu-id="5dbcf-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="5dbcf-118">Example 4</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxx -StartTime "8/17/2017 12:31:40 PM" -EndTime "8/17/2017 12:31:44 PM" -Severity Critical -EventType VmHealth
```

<span data-ttu-id="5dbcf-119">Elenco di eventi tra l'ora di inizio e l'ora di fine, la gravità critica e il tipo di integrità VmHealth.</span><span class="sxs-lookup"><span data-stu-id="5dbcf-119">List of event between time start time and end time , severity critical and health type VmHealth.</span></span>

## <span data-ttu-id="5dbcf-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5dbcf-120">PARAMETERS</span></span>

### <span data-ttu-id="5dbcf-121">-AffectedObjectFriendlyName</span><span class="sxs-lookup"><span data-stu-id="5dbcf-121">-AffectedObjectFriendlyName</span></span>
<span data-ttu-id="5dbcf-122">Specifica AffectedObject FriendlyName per la ricerca.</span><span class="sxs-lookup"><span data-stu-id="5dbcf-122">Specifies AffectedObject FriendlyName for the search.</span></span>

```yaml
Type: String
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dbcf-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dbcf-123">-DefaultProfile</span></span>
<span data-ttu-id="5dbcf-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5dbcf-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dbcf-125">-EndTime</span><span class="sxs-lookup"><span data-stu-id="5dbcf-125">-EndTime</span></span>
<span data-ttu-id="5dbcf-126">Specifica l'ora di fine della finestra di ricerca.</span><span class="sxs-lookup"><span data-stu-id="5dbcf-126">Specifies the end time of the search window.</span></span> <span data-ttu-id="5dbcf-127">Usa questo parametro per ottenere solo gli eventi che si sono verificati prima del tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="5dbcf-127">Use this parameter to get only those events that have occurred before the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dbcf-128">-EventType</span><span class="sxs-lookup"><span data-stu-id="5dbcf-128">-EventType</span></span>
<span data-ttu-id="5dbcf-129">Filtrare gli eventi in base al tipo di evento.</span><span class="sxs-lookup"><span data-stu-id="5dbcf-129">Filter events by the event type.</span></span>

```yaml
Type: String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: VmHealth, ServerHealth, AgentHealth

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dbcf-130">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="5dbcf-130">-Fabric</span></span>
<span data-ttu-id="5dbcf-131">Filtrare gli eventi in base al tessuto specificato.</span><span class="sxs-lookup"><span data-stu-id="5dbcf-131">Filter events by the specified fabric.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dbcf-132">-FabricId</span><span class="sxs-lookup"><span data-stu-id="5dbcf-132">-FabricId</span></span>
<span data-ttu-id="5dbcf-133">Specifica il fabricId da filtrare.</span><span class="sxs-lookup"><span data-stu-id="5dbcf-133">Specifies the fabricId to filter.</span></span>

```yaml
Type: String
Parameter Sets: ByFabricId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dbcf-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="5dbcf-134">-Name</span></span>
<span data-ttu-id="5dbcf-135">Specifica il nome dell'evento per la ricerca.</span><span class="sxs-lookup"><span data-stu-id="5dbcf-135">Specifies name of the event for search.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dbcf-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5dbcf-136">-ResourceId</span></span>
<span data-ttu-id="5dbcf-137">Specifica l'evento ReourceId dell'evento.</span><span class="sxs-lookup"><span data-stu-id="5dbcf-137">Specifes the event ReourceId of event.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dbcf-138">-Gravità</span><span class="sxs-lookup"><span data-stu-id="5dbcf-138">-Severity</span></span>
<span data-ttu-id="5dbcf-139">Gravità dell'evento su cui applicare il filtro.</span><span class="sxs-lookup"><span data-stu-id="5dbcf-139">Event severity to filter on.</span></span>

```yaml
Type: String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: Critical, Warning, OK, Unknown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dbcf-140">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5dbcf-140">-StartTime</span></span>
<span data-ttu-id="5dbcf-141">Specifica l'ora di inizio della finestra di ricerca.</span><span class="sxs-lookup"><span data-stu-id="5dbcf-141">Specifies the start time of the search window.</span></span> <span data-ttu-id="5dbcf-142">Usa questo parametro per ottenere solo gli eventi che si sono verificati dopo il periodo di tempo specificato.</span><span class="sxs-lookup"><span data-stu-id="5dbcf-142">Use this parameter to get only those events that have occurred after the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dbcf-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dbcf-143">CommonParameters</span></span>
<span data-ttu-id="5dbcf-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dbcf-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dbcf-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dbcf-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dbcf-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5dbcf-146">INPUTS</span></span>

### <span data-ttu-id="5dbcf-147">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="5dbcf-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="5dbcf-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5dbcf-148">OUTPUTS</span></span>

### <span data-ttu-id="5dbcf-149">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASREvent, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5dbcf-149">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASREvent, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="5dbcf-150">Note</span><span class="sxs-lookup"><span data-stu-id="5dbcf-150">NOTES</span></span>

## <span data-ttu-id="5dbcf-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5dbcf-151">RELATED LINKS</span></span>
