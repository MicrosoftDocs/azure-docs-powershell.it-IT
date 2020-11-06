---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
ms.openlocfilehash: 2c5bf49245da7ecac0f9d4351f5a66a39a663b98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520448"
---
# <span data-ttu-id="14acf-101">New-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="14acf-101">New-AzureRmEventHub</span></span>

## <span data-ttu-id="14acf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="14acf-102">SYNOPSIS</span></span>
<span data-ttu-id="14acf-103">Crea un nuovo hub eventi.</span><span class="sxs-lookup"><span data-stu-id="14acf-103">Creates a new Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14acf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14acf-104">SYNTAX</span></span>

### <span data-ttu-id="14acf-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="14acf-105">EventhubInputObjectSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14acf-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="14acf-106">EventhubPropertiesSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14acf-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14acf-107">DESCRIPTION</span></span>
<span data-ttu-id="14acf-108">Il cmdlet New-AzureRmEventHub crea un nuovo hub di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="14acf-108">The New-AzureRmEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="14acf-109">Per creare Eventhub con le proprietà di descrizione di acquisizione, seguire i passaggi seguenti (esempi 2).</span><span class="sxs-lookup"><span data-stu-id="14acf-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 

## <span data-ttu-id="14acf-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14acf-110">EXAMPLES</span></span>

### <span data-ttu-id="14acf-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="14acf-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location WestUS -EventHubName MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2
```

<span data-ttu-id="14acf-112">Crea un hub eventi denominato \` MyEventHubName \` con un periodo di conservazione dei messaggi di 3 giorni e due partizioni, nella \` posizione westus \` , con il gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="14acf-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="14acf-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="14acf-113">Example 2</span></span>
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

<span data-ttu-id="14acf-114">Crea un hub eventi denominato \` MyEventHubName \` con un periodo di conservazione dei messaggi di 3 giorni, 2 partizioni e proprietà CaptureDescription nella \` posizione westus \` , con il gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="14acf-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="14acf-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="14acf-115">PARAMETERS</span></span>

### <span data-ttu-id="14acf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14acf-116">-DefaultProfile</span></span>
<span data-ttu-id="14acf-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="14acf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14acf-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14acf-118">-InputObject</span></span>
<span data-ttu-id="14acf-119">Oggetto di input EventHub</span><span class="sxs-lookup"><span data-stu-id="14acf-119">EventHub Input object</span></span>

```yaml
Type: PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases: EventHubObj

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14acf-120">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="14acf-120">-MessageRetentionInDays</span></span>
<span data-ttu-id="14acf-121">Conservazione dei messaggi in Eventhub giorni</span><span class="sxs-lookup"><span data-stu-id="14acf-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="14acf-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="14acf-122">-Name</span></span>
<span data-ttu-id="14acf-123">Nome Eventhub</span><span class="sxs-lookup"><span data-stu-id="14acf-123">Eventhub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14acf-124">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="14acf-124">-Namespace</span></span>
<span data-ttu-id="14acf-125">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="14acf-125">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14acf-126">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="14acf-126">-PartitionCount</span></span>
<span data-ttu-id="14acf-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="14acf-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="14acf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14acf-128">-ResourceGroupName</span></span>
<span data-ttu-id="14acf-129">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="14acf-129">Resource Group Name</span></span>

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

### <span data-ttu-id="14acf-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="14acf-130">-Confirm</span></span>
<span data-ttu-id="14acf-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14acf-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14acf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14acf-132">-WhatIf</span></span>
<span data-ttu-id="14acf-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14acf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14acf-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14acf-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14acf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14acf-135">CommonParameters</span></span>
<span data-ttu-id="14acf-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14acf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="14acf-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14acf-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14acf-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="14acf-138">INPUTS</span></span>

### <span data-ttu-id="14acf-139">System. String</span><span class="sxs-lookup"><span data-stu-id="14acf-139">System.String</span></span>
<span data-ttu-id="14acf-140">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes System. Nullable ' 1 [[System. Int64, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="14acf-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes System.Nullable\`1[[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>


## <span data-ttu-id="14acf-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14acf-141">OUTPUTS</span></span>

### <span data-ttu-id="14acf-142">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="14acf-142">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>


## <span data-ttu-id="14acf-143">Note</span><span class="sxs-lookup"><span data-stu-id="14acf-143">NOTES</span></span>

## <span data-ttu-id="14acf-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14acf-144">RELATED LINKS</span></span>
