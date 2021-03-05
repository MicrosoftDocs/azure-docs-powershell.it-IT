---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/set-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
ms.openlocfilehash: 3fb0030d6475ab3fb41f78ab1dc1a54870ed2f8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998324"
---
# <span data-ttu-id="2bf55-101">Set-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="2bf55-101">Set-AzEventHubCluster</span></span>

## <span data-ttu-id="2bf55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bf55-102">SYNOPSIS</span></span>
<span data-ttu-id="2bf55-103">Aggiorna il tag per il cluster specificato</span><span class="sxs-lookup"><span data-stu-id="2bf55-103">Updates the Tag for the given Cluster</span></span>

## <span data-ttu-id="2bf55-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2bf55-104">SYNTAX</span></span>

### <span data-ttu-id="2bf55-105">ClusterPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2bf55-105">ClusterPropertiesSet (Default)</span></span>
```
Set-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-Capacity <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bf55-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2bf55-106">ClusterResourceIdParameterSet</span></span>
```
Set-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bf55-107">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2bf55-107">ClusterInputObjectSet</span></span>
```
Set-AzEventHubCluster [-InputObject] <PSEventHubClusterAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bf55-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2bf55-108">DESCRIPTION</span></span>
<span data-ttu-id="2bf55-109">Il cmdlet Set-AzEventHubCluster aggiorna i tag del cluster specificato</span><span class="sxs-lookup"><span data-stu-id="2bf55-109">The Set-AzEventHubCluster cmdlet updates tags of the given cluster</span></span>

## <span data-ttu-id="2bf55-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2bf55-110">EXAMPLES</span></span>

### <span data-ttu-id="2bf55-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2bf55-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557 -Tag @{"ClusterTag3" = "Tag3"; "ClusterTag4" = "Tag4";}

Id        : /subscriptions/{SubID}/resourceGroups/RSG-Cluster27651/providers/Microsoft.EventHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/11/2020 01:31:18
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag3, Tag3], [ClusterTag4, Tag4]}
```

<span data-ttu-id="2bf55-112">Aggiorna i tag del cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="2bf55-112">Updates tags of the given cluster.</span></span> 

## <span data-ttu-id="2bf55-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2bf55-113">PARAMETERS</span></span>

### <span data-ttu-id="2bf55-114">-Capacità</span><span class="sxs-lookup"><span data-stu-id="2bf55-114">-Capacity</span></span>
<span data-ttu-id="2bf55-115">Capacità cluster (CU), curarntrly, valore consentito = 1</span><span class="sxs-lookup"><span data-stu-id="2bf55-115">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

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

### <span data-ttu-id="2bf55-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bf55-116">-DefaultProfile</span></span>
<span data-ttu-id="2bf55-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2bf55-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bf55-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2bf55-118">-InputObject</span></span>
<span data-ttu-id="2bf55-119">Nome cluster</span><span class="sxs-lookup"><span data-stu-id="2bf55-119">Cluster Name</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes
Parameter Sets: ClusterInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bf55-120">-Location</span><span class="sxs-lookup"><span data-stu-id="2bf55-120">-Location</span></span>
<span data-ttu-id="2bf55-121">Posizione del cluster</span><span class="sxs-lookup"><span data-stu-id="2bf55-121">Location of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bf55-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2bf55-122">-Name</span></span>
<span data-ttu-id="2bf55-123">Nome cluster</span><span class="sxs-lookup"><span data-stu-id="2bf55-123">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet, ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bf55-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bf55-124">-ResourceGroupName</span></span>
<span data-ttu-id="2bf55-125">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="2bf55-125">Resource Group Name</span></span>

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

### <span data-ttu-id="2bf55-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2bf55-126">-ResourceId</span></span>
<span data-ttu-id="2bf55-127">ID risorsa del cluster</span><span class="sxs-lookup"><span data-stu-id="2bf55-127">Resource ID of Cluster</span></span>

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

### <span data-ttu-id="2bf55-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="2bf55-128">-Tag</span></span>
<span data-ttu-id="2bf55-129">Hashtables che rappresenta il tag di risorsa per i cluster</span><span class="sxs-lookup"><span data-stu-id="2bf55-129">Hashtables which represents resource Tag for Clusters</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ClusterPropertiesSet, ClusterResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2bf55-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2bf55-130">-Confirm</span></span>
<span data-ttu-id="2bf55-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bf55-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bf55-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bf55-132">-WhatIf</span></span>
<span data-ttu-id="2bf55-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2bf55-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bf55-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2bf55-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bf55-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bf55-135">CommonParameters</span></span>
<span data-ttu-id="2bf55-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bf55-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bf55-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2bf55-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bf55-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="2bf55-138">INPUTS</span></span>

### <span data-ttu-id="2bf55-139">System.String</span><span class="sxs-lookup"><span data-stu-id="2bf55-139">System.String</span></span>

### <span data-ttu-id="2bf55-140">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="2bf55-140">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="2bf55-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="2bf55-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

### <span data-ttu-id="2bf55-142">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2bf55-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2bf55-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2bf55-143">OUTPUTS</span></span>

### <span data-ttu-id="2bf55-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="2bf55-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="2bf55-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="2bf55-145">NOTES</span></span>

## <span data-ttu-id="2bf55-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2bf55-146">RELATED LINKS</span></span>
