---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHub.md
ms.openlocfilehash: ad7d4a1cefaadf3f1c2f12b9ef3a1b516c3813fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678773"
---
# <span data-ttu-id="38ec9-101">Set-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="38ec9-101">Set-AzEventHub</span></span>

## <span data-ttu-id="38ec9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="38ec9-102">SYNOPSIS</span></span>
<span data-ttu-id="38ec9-103">Aggiorna l'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="38ec9-103">Updates the specified Event Hub.</span></span>

## <span data-ttu-id="38ec9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38ec9-104">SYNTAX</span></span>

### <span data-ttu-id="38ec9-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="38ec9-105">EventhubInputObjectSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38ec9-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="38ec9-106">EventhubPropertiesSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38ec9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38ec9-107">DESCRIPTION</span></span>
<span data-ttu-id="38ec9-108">Il cmdlet Set-AzEventHub aggiorna le proprietà dell'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="38ec9-108">The Set-AzEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="38ec9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38ec9-109">EXAMPLES</span></span>

### <span data-ttu-id="38ec9-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="38ec9-110">Example 1</span></span>
<span data-ttu-id="38ec9-111">Per aggiornare Eventhub con le proprietà della descrizione di acquisizione, seguire la procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="38ec9-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 

```
PS C:\> $CreatedEventHub = Get-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
PS C:\> $createdEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.PSCaptureDescriptionAttributes
PS C:\> $createdEventHub.CaptureDescription.Enabled = $true
PS C:\> $createdEventHub.CaptureDescription.IntervalInSeconds  = 120
PS C:\> $createdEventHub.CaptureDescription.Encoding  = "Avro"
PS C:\> $createdEventHub.CaptureDescription.SizeLimitInBytes = 10485763
PS C:\> $createdEventHub.CaptureDescription.Destination.Name = "EventHubArchive.AzureBlockBlob"
PS C:\> $createdEventHub.CaptureDescription.Destination.BlobContainer = "container"
PS C:\> $createdEventHub.CaptureDescription.Destination.ArchiveNameFormat = "{Namespace}/{EventHub}/{PartitionId}/{Year}/{Month}/{Day}/{Hour}/{Minute}/{Second}"
PS C:\> $createdEventHub.CaptureDescription.Destination.StorageAccountResourceId = "/subscriptions/{SubscriptionId}/resourceGroups/MyResourceGroupName/providers/Microsoft.ClassicStorage/storageAccounts/arjunteststorage"
PS C:\> Set-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="38ec9-112">Aggiorna l'MyEventHubName dell'hub eventi \` \` rappresentato dall' \` \` oggetto MyCreatedEventHub, impostando il periodo di conservazione dei messaggi su 4 giorni, il numero di partizioni in proprietà 2 e CaptureDescription</span><span class="sxs-lookup"><span data-stu-id="38ec9-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, the number of partitions to 2 and CaptureDescription properties</span></span>

### <span data-ttu-id="38ec9-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="38ec9-113">Example 2</span></span>
```
PS C:\> Set-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="38ec9-114">Aggiorna l'MyEventHubName dell'hub eventi \` \` rappresentato dall' \` \` oggetto MyCreatedEventHub, impostando il periodo di conservazione dei messaggi su 4 giorni e il numero di partizioni su 2.</span><span class="sxs-lookup"><span data-stu-id="38ec9-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="38ec9-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38ec9-115">PARAMETERS</span></span>

### <span data-ttu-id="38ec9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38ec9-116">-DefaultProfile</span></span>
<span data-ttu-id="38ec9-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38ec9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38ec9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38ec9-118">-InputObject</span></span>
<span data-ttu-id="38ec9-119">Oggetto EventHub</span><span class="sxs-lookup"><span data-stu-id="38ec9-119">EventHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases: EventHubObj

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38ec9-120">-messageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="38ec9-120">-messageRetentionInDays</span></span>
<span data-ttu-id="38ec9-121">Conservazione dei messaggi in Eventhub giorni</span><span class="sxs-lookup"><span data-stu-id="38ec9-121">Eventhub Message Retention In Days</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: EventhubPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38ec9-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="38ec9-122">-Name</span></span>
<span data-ttu-id="38ec9-123">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="38ec9-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38ec9-124">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="38ec9-124">-Namespace</span></span>
<span data-ttu-id="38ec9-125">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="38ec9-125">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38ec9-126">-partitionCount</span><span class="sxs-lookup"><span data-stu-id="38ec9-126">-partitionCount</span></span>
<span data-ttu-id="38ec9-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="38ec9-127">Eventhub PartitionCount</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: EventhubPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38ec9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38ec9-128">-ResourceGroupName</span></span>
<span data-ttu-id="38ec9-129">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="38ec9-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38ec9-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="38ec9-130">-Confirm</span></span>
<span data-ttu-id="38ec9-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38ec9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38ec9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38ec9-132">-WhatIf</span></span>
<span data-ttu-id="38ec9-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38ec9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38ec9-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38ec9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38ec9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38ec9-135">CommonParameters</span></span>
<span data-ttu-id="38ec9-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38ec9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38ec9-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38ec9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38ec9-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="38ec9-138">INPUTS</span></span>

### <span data-ttu-id="38ec9-139">System. String</span><span class="sxs-lookup"><span data-stu-id="38ec9-139">System.String</span></span>

### <span data-ttu-id="38ec9-140">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="38ec9-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="38ec9-141">System. Nullable ' 1 [[System. Int64, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="38ec9-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="38ec9-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38ec9-142">OUTPUTS</span></span>

### <span data-ttu-id="38ec9-143">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="38ec9-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="38ec9-144">Note</span><span class="sxs-lookup"><span data-stu-id="38ec9-144">NOTES</span></span>

## <span data-ttu-id="38ec9-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38ec9-145">RELATED LINKS</span></span>
