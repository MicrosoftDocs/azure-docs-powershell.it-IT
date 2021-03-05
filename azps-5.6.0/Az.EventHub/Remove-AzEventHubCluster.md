---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
ms.openlocfilehash: 7ba6a5f95c1cc37f7cdef7d8ead7a2514927e089
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992724"
---
# <span data-ttu-id="2772f-101">Remove-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="2772f-101">Remove-AzEventHubCluster</span></span>

## <span data-ttu-id="2772f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2772f-102">SYNOPSIS</span></span>
<span data-ttu-id="2772f-103">Elimina il cluster Dedicated Eventhub specificato dal Gruppo Risorse</span><span class="sxs-lookup"><span data-stu-id="2772f-103">Deletes the specified Dedicated Eventhub Cluster from the ResourceGroup</span></span>

## <span data-ttu-id="2772f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2772f-104">SYNTAX</span></span>

### <span data-ttu-id="2772f-105">ClusterPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2772f-105">ClusterPropertiesSet (Default)</span></span>
```
Remove-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2772f-106">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2772f-106">ClusterInputObjectSet</span></span>
```
Remove-AzEventHubCluster [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2772f-107">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2772f-107">ClusterResourceIdParameterSet</span></span>
```
Remove-AzEventHubCluster [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2772f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2772f-108">DESCRIPTION</span></span>
<span data-ttu-id="2772f-109">Il Remove-AzEventHubCluster cmdlet elimina il nome del cluster eventhub dedicato specificato dal gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="2772f-109">The Remove-AzEventHubCluster cmdlet deletes the given dedicated eventhub Cluster name from the given resourcegroup</span></span>

## <span data-ttu-id="2772f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2772f-110">EXAMPLES</span></span>

### <span data-ttu-id="2772f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2772f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557
```

<span data-ttu-id="2772f-112">Elimina il cluster Eventhub-Cluster-5557 RSG-Cluster27651 di risorse</span><span class="sxs-lookup"><span data-stu-id="2772f-112">Deletes Eventhub-Cluster-5557 Cluster from RSG-Cluster27651 resourcegroup</span></span>

## <span data-ttu-id="2772f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2772f-113">PARAMETERS</span></span>

### <span data-ttu-id="2772f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2772f-114">-AsJob</span></span>
<span data-ttu-id="2772f-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="2772f-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2772f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2772f-116">-DefaultProfile</span></span>
<span data-ttu-id="2772f-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2772f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2772f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2772f-118">-InputObject</span></span>
<span data-ttu-id="2772f-119">Oggetto Cluster</span><span class="sxs-lookup"><span data-stu-id="2772f-119">Cluster Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: ClusterInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2772f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2772f-120">-Name</span></span>
<span data-ttu-id="2772f-121">Nome cluster</span><span class="sxs-lookup"><span data-stu-id="2772f-121">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2772f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2772f-122">-PassThru</span></span>
<span data-ttu-id="2772f-123">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="2772f-123">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2772f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2772f-124">-ResourceGroupName</span></span>
<span data-ttu-id="2772f-125">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="2772f-125">Resource Group Name</span></span>

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

### <span data-ttu-id="2772f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2772f-126">-ResourceId</span></span>
<span data-ttu-id="2772f-127">ID risorsa cluster</span><span class="sxs-lookup"><span data-stu-id="2772f-127">Cluster Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2772f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2772f-128">-Confirm</span></span>
<span data-ttu-id="2772f-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2772f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2772f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2772f-130">-WhatIf</span></span>
<span data-ttu-id="2772f-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2772f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2772f-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2772f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2772f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2772f-133">CommonParameters</span></span>
<span data-ttu-id="2772f-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2772f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2772f-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2772f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2772f-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="2772f-136">INPUTS</span></span>

### <span data-ttu-id="2772f-137">System.String</span><span class="sxs-lookup"><span data-stu-id="2772f-137">System.String</span></span>

### <span data-ttu-id="2772f-138">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="2772f-138">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="2772f-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2772f-139">OUTPUTS</span></span>

### <span data-ttu-id="2772f-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2772f-140">System.Boolean</span></span>

## <span data-ttu-id="2772f-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="2772f-141">NOTES</span></span>

## <span data-ttu-id="2772f-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2772f-142">RELATED LINKS</span></span>
