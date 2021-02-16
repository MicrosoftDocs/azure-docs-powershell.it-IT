---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHub.md
ms.openlocfilehash: eec7294a15217be85b4c2248dac6506d54c2e6aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204130"
---
# <span data-ttu-id="c800a-101">New-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="c800a-101">New-AzEventHub</span></span>

## <span data-ttu-id="c800a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c800a-102">SYNOPSIS</span></span>
<span data-ttu-id="c800a-103">Crea un nuovo hub eventi.</span><span class="sxs-lookup"><span data-stu-id="c800a-103">Creates a new Event Hub.</span></span>

## <span data-ttu-id="c800a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c800a-104">SYNTAX</span></span>

### <span data-ttu-id="c800a-105">EventhubPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c800a-105">EventhubPropertiesSet (Default)</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c800a-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c800a-106">EventhubInputObjectSet</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c800a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c800a-107">DESCRIPTION</span></span>
<span data-ttu-id="c800a-108">Il cmdlet New-AzEventHub crea un nuovo Hub eventi di Azure.</span><span class="sxs-lookup"><span data-stu-id="c800a-108">The New-AzEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="c800a-109">Per creare Eventhub con le proprietà descrittive di acquisizione, seguire la procedura seguente (esempi 2).</span><span class="sxs-lookup"><span data-stu-id="c800a-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 

## <span data-ttu-id="c800a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c800a-110">EXAMPLES</span></span>

### <span data-ttu-id="c800a-111">Esempio 1: Creare un nuovo EventoHub</span><span class="sxs-lookup"><span data-stu-id="c800a-111">Example 1: - Create new EventHub</span></span>
```powershell
PS C:\> New-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="c800a-112">Crea un hub eventi denominato MyEventHubName con un periodo di conservazione dei messaggi di 3 giorni e due partizioni, nella posizione WestUS, con il gruppo di risorse \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="c800a-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="c800a-113">Esempio 2: Aggiornare Eventhub con 'CaptureDescription'</span><span class="sxs-lookup"><span data-stu-id="c800a-113">Example 2: Update Eventhub with 'CaptureDescription'</span></span>
```powershell
PS C:\> New-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2

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

<span data-ttu-id="c800a-114">Crea un hub eventi denominato MyEventHubName con un periodo di conservazione dei messaggi di 3 giorni, 2 partizioni e proprietà CaptureDescription nel percorso WestUS, con il gruppo di risorse \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="c800a-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="c800a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c800a-115">PARAMETERS</span></span>

### <span data-ttu-id="c800a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c800a-116">-DefaultProfile</span></span>
<span data-ttu-id="c800a-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c800a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c800a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c800a-118">-InputObject</span></span>
<span data-ttu-id="c800a-119">Oggetto di input Di EventHub</span><span class="sxs-lookup"><span data-stu-id="c800a-119">EventHub Input object</span></span>

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

### <span data-ttu-id="c800a-120">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="c800a-120">-MessageRetentionInDays</span></span>
<span data-ttu-id="c800a-121">Conservazione dei messaggi di Eventhub in giorni</span><span class="sxs-lookup"><span data-stu-id="c800a-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="c800a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c800a-122">-Name</span></span>
<span data-ttu-id="c800a-123">Nome Eventhub</span><span class="sxs-lookup"><span data-stu-id="c800a-123">Eventhub Name</span></span>

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

### <span data-ttu-id="c800a-124">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c800a-124">-Namespace</span></span>
<span data-ttu-id="c800a-125">Nome spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c800a-125">Namespace Name</span></span>

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

### <span data-ttu-id="c800a-126">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="c800a-126">-PartitionCount</span></span>
<span data-ttu-id="c800a-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="c800a-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="c800a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c800a-128">-ResourceGroupName</span></span>
<span data-ttu-id="c800a-129">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="c800a-129">Resource Group Name</span></span>

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

### <span data-ttu-id="c800a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c800a-130">-Confirm</span></span>
<span data-ttu-id="c800a-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c800a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c800a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c800a-132">-WhatIf</span></span>
<span data-ttu-id="c800a-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c800a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c800a-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c800a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c800a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c800a-135">CommonParameters</span></span>
<span data-ttu-id="c800a-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c800a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c800a-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c800a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c800a-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="c800a-138">INPUTS</span></span>

### <span data-ttu-id="c800a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c800a-139">System.String</span></span>

### <span data-ttu-id="c800a-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="c800a-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="c800a-141">System.Nullable'1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c800a-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="c800a-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c800a-142">OUTPUTS</span></span>

### <span data-ttu-id="c800a-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="c800a-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="c800a-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="c800a-144">NOTES</span></span>

## <span data-ttu-id="c800a-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c800a-145">RELATED LINKS</span></span>
