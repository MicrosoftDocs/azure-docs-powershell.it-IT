---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/new-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
ms.openlocfilehash: 4a76d54e4c8a3abda87fb9fd6de1d4439b051112
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957133"
---
# <span data-ttu-id="32267-101">New-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="32267-101">New-AzEventHubCluster</span></span>

## <span data-ttu-id="32267-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32267-102">SYNOPSIS</span></span>
<span data-ttu-id="32267-103">Crea un nuovo cluster eventhub dedicato</span><span class="sxs-lookup"><span data-stu-id="32267-103">Creates a new dedicated eventhub cluster</span></span>

## <span data-ttu-id="32267-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32267-104">SYNTAX</span></span>

### <span data-ttu-id="32267-105">ClusterPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="32267-105">ClusterPropertiesSet (Default)</span></span>
```
New-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Capacity <Int32>]
 [-Tag <Hashtable>] [[-ResourceId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="32267-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="32267-106">ClusterResourceIdParameterSet</span></span>
```
New-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32267-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="32267-107">DESCRIPTION</span></span>
<span data-ttu-id="32267-108">Il cmdlet New-AzEventHubCluster crea il cluster eventhub dedicato nel gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="32267-108">The New-AzEventHubCluster cmdlet creates the dedicated eventhub cluster in the given resource group</span></span>

## <span data-ttu-id="32267-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32267-109">EXAMPLES</span></span>

### <span data-ttu-id="32267-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="32267-110">Example 1</span></span>
```powershell
PS C:\>  New-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557 -Location southcentralus -Capacity 1

Id        : /subscriptions/SubId/resourceGroups/RSG-Cluster27651/providers/Microsoft.EventHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/11/2020 01:31:18
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag1, Tag1], [ClusterTag2, Tag2]}

```

<span data-ttu-id="32267-111">Crea un cluster dedicato 'Eventhub-Cluster-5557' nel gruppo di risorse 'RSG-Cluster27651' con Location southcentralus e Capacity come 1</span><span class="sxs-lookup"><span data-stu-id="32267-111">Creates 'Eventhub-Cluster-5557' dedicated cluster in resourcegroup 'RSG-Cluster27651' with Location southcentralus and Capacity as 1</span></span>

## <span data-ttu-id="32267-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32267-112">PARAMETERS</span></span>

### <span data-ttu-id="32267-113">-Capacità</span><span class="sxs-lookup"><span data-stu-id="32267-113">-Capacity</span></span>
<span data-ttu-id="32267-114">Capacità cluster (CU), curarntrly, valore consentito = 1</span><span class="sxs-lookup"><span data-stu-id="32267-114">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32267-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32267-115">-DefaultProfile</span></span>
<span data-ttu-id="32267-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="32267-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32267-117">-Location</span><span class="sxs-lookup"><span data-stu-id="32267-117">-Location</span></span>
<span data-ttu-id="32267-118">Posizione del cluster</span><span class="sxs-lookup"><span data-stu-id="32267-118">Location of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32267-119">-Name</span><span class="sxs-lookup"><span data-stu-id="32267-119">-Name</span></span>
<span data-ttu-id="32267-120">Nome cluster</span><span class="sxs-lookup"><span data-stu-id="32267-120">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32267-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32267-121">-ResourceGroupName</span></span>
<span data-ttu-id="32267-122">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="32267-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32267-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32267-123">-ResourceId</span></span>
<span data-ttu-id="32267-124">ID risorsa del cluster</span><span class="sxs-lookup"><span data-stu-id="32267-124">Resource ID of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32267-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="32267-125">-Tag</span></span>
<span data-ttu-id="32267-126">Hashtables che rappresenta i tag di risorsa per i cluster</span><span class="sxs-lookup"><span data-stu-id="32267-126">Hashtables which represents resource Tags for Clusters</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32267-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32267-127">-Confirm</span></span>
<span data-ttu-id="32267-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32267-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32267-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32267-129">-WhatIf</span></span>
<span data-ttu-id="32267-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32267-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32267-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32267-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32267-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32267-132">CommonParameters</span></span>
<span data-ttu-id="32267-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32267-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32267-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="32267-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32267-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="32267-135">INPUTS</span></span>

### <span data-ttu-id="32267-136">System.String</span><span class="sxs-lookup"><span data-stu-id="32267-136">System.String</span></span>

### <span data-ttu-id="32267-137">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="32267-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="32267-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="32267-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="32267-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32267-139">OUTPUTS</span></span>

### <span data-ttu-id="32267-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="32267-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="32267-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="32267-141">NOTES</span></span>

## <span data-ttu-id="32267-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32267-142">RELATED LINKS</span></span>
