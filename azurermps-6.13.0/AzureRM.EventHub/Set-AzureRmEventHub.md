---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHub.md
ms.openlocfilehash: e5f3041038c79a12a6e9fb92937679f538ce22b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515355"
---
# <span data-ttu-id="2be57-101">Set-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="2be57-101">Set-AzureRmEventHub</span></span>

## <span data-ttu-id="2be57-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2be57-102">SYNOPSIS</span></span>
<span data-ttu-id="2be57-103">Aggiorna l'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="2be57-103">Updates the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2be57-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2be57-104">SYNTAX</span></span>

### <span data-ttu-id="2be57-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2be57-105">EventhubInputObjectSet</span></span>
```
Set-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2be57-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="2be57-106">EventhubPropertiesSet</span></span>
```
Set-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2be57-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2be57-107">DESCRIPTION</span></span>
<span data-ttu-id="2be57-108">Il cmdlet Set-AzureRmEventHub aggiorna le proprietà dell'hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="2be57-108">The Set-AzureRmEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="2be57-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2be57-109">EXAMPLES</span></span>

### <span data-ttu-id="2be57-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2be57-110">Example 1</span></span>
<span data-ttu-id="2be57-111">Per aggiornare Eventhub con le proprietà della descrizione di acquisizione, seguire la procedura seguente.</span><span class="sxs-lookup"><span data-stu-id="2be57-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 

```
PS C:\> $CreatedEventHub = Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName
PS C:\> $createdEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.PSCaptureDescriptionAttributes
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

<span data-ttu-id="2be57-112">Aggiorna l'MyEventHubName dell'hub eventi \` \` rappresentato dall' \` \` oggetto MyCreatedEventHub, impostando il periodo di conservazione dei messaggi su 4 giorni, il numero di partizioni in proprietà 2 e CaptureDescription</span><span class="sxs-lookup"><span data-stu-id="2be57-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, the number of partitions to 2 and CaptureDescription properties</span></span>

### <span data-ttu-id="2be57-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2be57-113">Example 2</span></span>
```
PS C:\> Set-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="2be57-114">Aggiorna l'MyEventHubName dell'hub eventi \` \` rappresentato dall' \` \` oggetto MyCreatedEventHub, impostando il periodo di conservazione dei messaggi su 4 giorni e il numero di partizioni su 2.</span><span class="sxs-lookup"><span data-stu-id="2be57-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="2be57-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2be57-115">PARAMETERS</span></span>

### <span data-ttu-id="2be57-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2be57-116">-DefaultProfile</span></span>
<span data-ttu-id="2be57-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2be57-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2be57-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2be57-118">-InputObject</span></span>
<span data-ttu-id="2be57-119">Oggetto EventHub</span><span class="sxs-lookup"><span data-stu-id="2be57-119">EventHub object</span></span>

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

### <span data-ttu-id="2be57-120">-messageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="2be57-120">-messageRetentionInDays</span></span>
<span data-ttu-id="2be57-121">Conservazione dei messaggi in Eventhub giorni</span><span class="sxs-lookup"><span data-stu-id="2be57-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="2be57-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="2be57-122">-Name</span></span>
<span data-ttu-id="2be57-123">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2be57-123">Namespace Name</span></span>

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

### <span data-ttu-id="2be57-124">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2be57-124">-Namespace</span></span>
<span data-ttu-id="2be57-125">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="2be57-125">Namespace Name</span></span>

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

### <span data-ttu-id="2be57-126">-partitionCount</span><span class="sxs-lookup"><span data-stu-id="2be57-126">-partitionCount</span></span>
<span data-ttu-id="2be57-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="2be57-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="2be57-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2be57-128">-ResourceGroupName</span></span>
<span data-ttu-id="2be57-129">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="2be57-129">Resource Group Name</span></span>

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

### <span data-ttu-id="2be57-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2be57-130">-Confirm</span></span>
<span data-ttu-id="2be57-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2be57-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2be57-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2be57-132">-WhatIf</span></span>
<span data-ttu-id="2be57-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2be57-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2be57-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2be57-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2be57-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2be57-135">CommonParameters</span></span>
<span data-ttu-id="2be57-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2be57-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2be57-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2be57-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2be57-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2be57-138">INPUTS</span></span>

### <span data-ttu-id="2be57-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2be57-139">System.String</span></span>

### <span data-ttu-id="2be57-140">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="2be57-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="2be57-141">System. Nullable ' 1 [[System. Int64, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="2be57-141">System.Nullable\`1[[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="2be57-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2be57-142">OUTPUTS</span></span>

### <span data-ttu-id="2be57-143">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="2be57-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="2be57-144">Note</span><span class="sxs-lookup"><span data-stu-id="2be57-144">NOTES</span></span>

## <span data-ttu-id="2be57-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2be57-145">RELATED LINKS</span></span>