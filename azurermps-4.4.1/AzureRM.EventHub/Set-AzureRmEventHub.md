---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 2ff36708ba9b8303c8b8763146c81ee4e4d8b209
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519183"
---
# <span data-ttu-id="1d265-101">Set-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="1d265-101">Set-AzureRmEventHub</span></span>

## <span data-ttu-id="1d265-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1d265-102">SYNOPSIS</span></span>
<span data-ttu-id="1d265-103">Aggiorna l'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="1d265-103">Updates the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d265-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1d265-104">SYNTAX</span></span>

### <span data-ttu-id="1d265-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1d265-105">EventhubInputObjectSet</span></span>
```
Set-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-InputObject <EventHubAttributes>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="1d265-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="1d265-106">EventhubPropertiesSet</span></span>
```
Set-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="1d265-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d265-107">DESCRIPTION</span></span>
<span data-ttu-id="1d265-108">Il cmdlet Set-AzureRmEventHub aggiorna le proprietà dell'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="1d265-108">The Set-AzureRmEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="1d265-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1d265-109">EXAMPLES</span></span>

### <span data-ttu-id="1d265-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1d265-110">Example 1</span></span>
<span data-ttu-id="1d265-111">Per aggiornare Eventhub con le proprietà della descrizione di acquisizione, seguire la procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="1d265-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 

```
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

<span data-ttu-id="1d265-112">Aggiorna l'MyEventHubName dell'hub eventi \` \` rappresentato dall' \` \` oggetto MyCreatedEventHub, impostando il periodo di conservazione dei messaggi su 4 giorni, il numero di partizioni in proprietà 2 e CaptureDescription</span><span class="sxs-lookup"><span data-stu-id="1d265-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, the number of partitions to 2 and CaptureDescription properties</span></span>

### <span data-ttu-id="1d265-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1d265-113">Example 2</span></span>

```
PS C:\> Set-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="1d265-114">Aggiorna l'MyEventHubName dell'hub eventi \` \` rappresentato dall' \` \` oggetto MyCreatedEventHub, impostando il periodo di conservazione dei messaggi su 4 giorni e il numero di partizioni su 2.</span><span class="sxs-lookup"><span data-stu-id="1d265-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="1d265-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1d265-115">PARAMETERS</span></span>

### <span data-ttu-id="1d265-116">-messageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="1d265-116">-messageRetentionInDays</span></span>
<span data-ttu-id="1d265-117">Periodo di conservazione dei messaggi dell'hub eventi, in giorni.</span><span class="sxs-lookup"><span data-stu-id="1d265-117">Event Hub message retention period, in days.</span></span>

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

### <span data-ttu-id="1d265-118">-partitionCount</span><span class="sxs-lookup"><span data-stu-id="1d265-118">-partitionCount</span></span>
<span data-ttu-id="1d265-119">Numero di partizioni nell'hub dell'evento.</span><span class="sxs-lookup"><span data-stu-id="1d265-119">Number of partitions on this Event Hub.</span></span>

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

### <span data-ttu-id="1d265-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d265-120">-ResourceGroupName</span></span>
<span data-ttu-id="1d265-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1d265-121">Resource group name.</span></span>

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

### <span data-ttu-id="1d265-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1d265-122">-Confirm</span></span>
<span data-ttu-id="1d265-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d265-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d265-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d265-124">-WhatIf</span></span>
<span data-ttu-id="1d265-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d265-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d265-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d265-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d265-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d265-127">-InputObject</span></span>
<span data-ttu-id="1d265-128">Oggetto EventHub.</span><span class="sxs-lookup"><span data-stu-id="1d265-128">EventHub object.</span></span>

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

### <span data-ttu-id="1d265-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="1d265-129">-Name</span></span>
<span data-ttu-id="1d265-130">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="1d265-130">Namespace Name.</span></span>

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

### <span data-ttu-id="1d265-131">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1d265-131">-Namespace</span></span>
<span data-ttu-id="1d265-132">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="1d265-132">Namespace Name.</span></span>

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

## <span data-ttu-id="1d265-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1d265-133">INPUTS</span></span>

### <span data-ttu-id="1d265-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1d265-134">System.String</span></span>

## <span data-ttu-id="1d265-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1d265-135">OUTPUTS</span></span>

### <span data-ttu-id="1d265-136">Microsoft. Azure. Commands. EventHub. Models. EventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="1d265-136">Microsoft.Azure.Commands.EventHub.Models.EventHubAttributes</span></span>

## <span data-ttu-id="1d265-137">Note</span><span class="sxs-lookup"><span data-stu-id="1d265-137">NOTES</span></span>

## <span data-ttu-id="1d265-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1d265-138">RELATED LINKS</span></span>

