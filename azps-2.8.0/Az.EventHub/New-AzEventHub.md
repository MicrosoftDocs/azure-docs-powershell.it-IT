---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHub.md
ms.openlocfilehash: ac61b1f0bec6ea6b76fcc2b0ea4cf1438359197b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674443"
---
# <span data-ttu-id="d6ceb-101">New-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="d6ceb-101">New-AzEventHub</span></span>

## <span data-ttu-id="d6ceb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d6ceb-102">SYNOPSIS</span></span>
<span data-ttu-id="d6ceb-103">Crea un nuovo hub eventi.</span><span class="sxs-lookup"><span data-stu-id="d6ceb-103">Creates a new Event Hub.</span></span>

## <span data-ttu-id="d6ceb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d6ceb-104">SYNTAX</span></span>

### <span data-ttu-id="d6ceb-105">EventhubPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d6ceb-105">EventhubPropertiesSet (Default)</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6ceb-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d6ceb-106">EventhubInputObjectSet</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d6ceb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6ceb-107">DESCRIPTION</span></span>
<span data-ttu-id="d6ceb-108">Il cmdlet New-AzEventHub crea un nuovo hub di eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="d6ceb-108">The New-AzEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="d6ceb-109">Per creare Eventhub con le proprietà di descrizione di acquisizione, seguire i passaggi seguenti (esempi 2).</span><span class="sxs-lookup"><span data-stu-id="d6ceb-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 

## <span data-ttu-id="d6ceb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d6ceb-110">EXAMPLES</span></span>

### <span data-ttu-id="d6ceb-111">Esempio 1-creare nuovi EventHub</span><span class="sxs-lookup"><span data-stu-id="d6ceb-111">Example 1  - Create new EventHub</span></span>
```
PS C:\> New-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="d6ceb-112">Crea un hub eventi denominato \` MyEventHubName \` con un periodo di conservazione dei messaggi di 3 giorni e due partizioni, nella \` posizione westus \` , con il gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="d6ceb-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="d6ceb-113">Esempio 2 aggiornamento di Eventhub con "CaptureDescription"</span><span class="sxs-lookup"><span data-stu-id="d6ceb-113">Example 2 Update Eventhub with 'CaptureDescription'</span></span>
```
PS C:\> New-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2

PS C:\> $CreatedEventHub = Get-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName

PS C:\> $createdEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.CaptureDescriptionAttributes

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

<span data-ttu-id="d6ceb-114">Crea un hub eventi denominato \` MyEventHubName \` con un periodo di conservazione dei messaggi di 3 giorni, 2 partizioni e proprietà CaptureDescription nella \` posizione westus \` , con il gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="d6ceb-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="d6ceb-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d6ceb-115">PARAMETERS</span></span>

### <span data-ttu-id="d6ceb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6ceb-116">-DefaultProfile</span></span>
<span data-ttu-id="d6ceb-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d6ceb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6ceb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6ceb-118">-InputObject</span></span>
<span data-ttu-id="d6ceb-119">Oggetto di input EventHub</span><span class="sxs-lookup"><span data-stu-id="d6ceb-119">EventHub Input object</span></span>

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

### <span data-ttu-id="d6ceb-120">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="d6ceb-120">-MessageRetentionInDays</span></span>
<span data-ttu-id="d6ceb-121">Conservazione dei messaggi in Eventhub giorni</span><span class="sxs-lookup"><span data-stu-id="d6ceb-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="d6ceb-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="d6ceb-122">-Name</span></span>
<span data-ttu-id="d6ceb-123">Nome Eventhub</span><span class="sxs-lookup"><span data-stu-id="d6ceb-123">Eventhub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6ceb-124">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d6ceb-124">-Namespace</span></span>
<span data-ttu-id="d6ceb-125">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="d6ceb-125">Namespace Name</span></span>

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

### <span data-ttu-id="d6ceb-126">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="d6ceb-126">-PartitionCount</span></span>
<span data-ttu-id="d6ceb-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="d6ceb-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="d6ceb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6ceb-128">-ResourceGroupName</span></span>
<span data-ttu-id="d6ceb-129">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="d6ceb-129">Resource Group Name</span></span>

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

### <span data-ttu-id="d6ceb-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d6ceb-130">-Confirm</span></span>
<span data-ttu-id="d6ceb-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6ceb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6ceb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6ceb-132">-WhatIf</span></span>
<span data-ttu-id="d6ceb-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6ceb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6ceb-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6ceb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6ceb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6ceb-135">CommonParameters</span></span>
<span data-ttu-id="d6ceb-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6ceb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6ceb-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6ceb-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6ceb-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d6ceb-138">INPUTS</span></span>

### <span data-ttu-id="d6ceb-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d6ceb-139">System.String</span></span>

### <span data-ttu-id="d6ceb-140">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="d6ceb-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="d6ceb-141">System. Nullable ' 1 [[System. Int64, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d6ceb-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d6ceb-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d6ceb-142">OUTPUTS</span></span>

### <span data-ttu-id="d6ceb-143">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="d6ceb-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="d6ceb-144">Note</span><span class="sxs-lookup"><span data-stu-id="d6ceb-144">NOTES</span></span>

## <span data-ttu-id="d6ceb-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d6ceb-145">RELATED LINKS</span></span>
