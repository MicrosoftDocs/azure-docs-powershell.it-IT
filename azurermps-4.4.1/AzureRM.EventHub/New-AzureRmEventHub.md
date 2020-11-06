---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 656e010a05ce1272355f689be8513ecadd330e7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521671"
---
# <span data-ttu-id="414ac-101">New-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="414ac-101">New-AzureRmEventHub</span></span>

## <span data-ttu-id="414ac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="414ac-102">SYNOPSIS</span></span>
<span data-ttu-id="414ac-103">Crea un nuovo hub eventi.</span><span class="sxs-lookup"><span data-stu-id="414ac-103">Creates a new Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="414ac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="414ac-104">SYNTAX</span></span>

### <span data-ttu-id="414ac-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="414ac-105">EventhubInputObjectSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> [[-Location] <String>] -Name <String>
 [-InputObject <EventHubAttributes>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="414ac-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="414ac-106">EventhubPropertiesSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> [[-Location] <String>] -Name <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="414ac-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="414ac-107">DESCRIPTION</span></span>
<span data-ttu-id="414ac-108">Il cmdlet New-AzureRmEventHub crea un nuovo hub di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="414ac-108">The New-AzureRmEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="414ac-109">Per creare Eventhub con le proprietà di descrizione di acquisizione, seguire i passaggi seguenti (esempi 2).</span><span class="sxs-lookup"><span data-stu-id="414ac-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 


## <span data-ttu-id="414ac-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="414ac-110">EXAMPLES</span></span>

### <span data-ttu-id="414ac-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="414ac-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location WestUS -EventHubName MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2
```

<span data-ttu-id="414ac-112">Crea un hub eventi denominato \` MyEventHubName \` con un periodo di conservazione dei messaggi di 3 giorni e due partizioni, nella \` posizione westus \` , con il gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="414ac-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="414ac-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="414ac-113">Example 2</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location WestUS -EventHubName MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2

PS C:\> $CreatedEventHub = Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName

PS C:\> $createdEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.CaptureDescriptionAttributes

PS C:\> $createdEventHub.CaptureDescription.Enabled = $true
PS C:\> $createdEventHub.CaptureDescription.IntervalInSeconds  = 120
PS C:\> $createdEventHub.CaptureDescription.Encoding  = "Avro"
PS C:\> $createdEventHub.CaptureDescription.SizeLimitInBytes = 10485763
PS C:\> $createdEventHub.CaptureDescription.Destination.Name = "EventHubArchive.AzureBlockBlob"
PS C:\> $createdEventHub.CaptureDescription.Destination.BlobContainer = "container"
PS C:\> $createdEventHub.CaptureDescription.Destination.ArchiveNameFormat = "{Namespace}/{EventHub}/{PartitionId}/{Year}/{Month}/{Day}/{Hour}/{Minute}/{Second}"
PS C:\> $createdEventHub.CaptureDescription.Destination.StorageAccountResourceId = "/subscriptions/{SubscriptionId}/resourceGroups/MyResourceGroupName/providers/Microsoft.ClassicStorage/storageAccounts/arjunteststorage"
PS C:\> Set-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="414ac-114">Crea un hub eventi denominato \` MyEventHubName \` con un periodo di conservazione dei messaggi di 3 giorni, 2 partizioni e proprietà CaptureDescription nella \` posizione westus \` , con il gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="414ac-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="414ac-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="414ac-115">PARAMETERS</span></span>

### <span data-ttu-id="414ac-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="414ac-116">-Location</span></span>
<span data-ttu-id="414ac-117">Posizione geografica dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="414ac-117">Namespace geographic location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="414ac-118">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="414ac-118">-MessageRetentionInDays</span></span>
<span data-ttu-id="414ac-119">Tempo di conservazione dei messaggi degli hub eventi in giorni.</span><span class="sxs-lookup"><span data-stu-id="414ac-119">Event Hubs message retention time in days.</span></span>

```yaml
Type: Int64
Parameter Sets: EventhubPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="414ac-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="414ac-120">-PartitionCount</span></span>
<span data-ttu-id="414ac-121">Numero di partizioni nell'hub eventi.</span><span class="sxs-lookup"><span data-stu-id="414ac-121">Number of partitions in the Event Hub.</span></span>

```yaml
Type: Int64
Parameter Sets: EventhubPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="414ac-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="414ac-122">-ResourceGroupName</span></span>
<span data-ttu-id="414ac-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="414ac-123">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="414ac-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="414ac-124">-Confirm</span></span>
<span data-ttu-id="414ac-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="414ac-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="414ac-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="414ac-126">-WhatIf</span></span>
<span data-ttu-id="414ac-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="414ac-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="414ac-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="414ac-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="414ac-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="414ac-129">-InputObject</span></span>
<span data-ttu-id="414ac-130">Oggetto di input EventHub.</span><span class="sxs-lookup"><span data-stu-id="414ac-130">EventHub Input object.</span></span>

```yaml
Type: EventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases: EventHubObj

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="414ac-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="414ac-131">-Name</span></span>
<span data-ttu-id="414ac-132">Nome Eventhub.</span><span class="sxs-lookup"><span data-stu-id="414ac-132">Eventhub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="414ac-133">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="414ac-133">-Namespace</span></span>
<span data-ttu-id="414ac-134">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="414ac-134">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="414ac-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="414ac-135">INPUTS</span></span>

### <span data-ttu-id="414ac-136">System. String</span><span class="sxs-lookup"><span data-stu-id="414ac-136">System.String</span></span>

## <span data-ttu-id="414ac-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="414ac-137">OUTPUTS</span></span>

### <span data-ttu-id="414ac-138">Microsoft. Azure. Commands. EventHub. Models. EventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="414ac-138">Microsoft.Azure.Commands.EventHub.Models.EventHubAttributes</span></span>

## <span data-ttu-id="414ac-139">Note</span><span class="sxs-lookup"><span data-stu-id="414ac-139">NOTES</span></span>

## <span data-ttu-id="414ac-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="414ac-140">RELATED LINKS</span></span>

