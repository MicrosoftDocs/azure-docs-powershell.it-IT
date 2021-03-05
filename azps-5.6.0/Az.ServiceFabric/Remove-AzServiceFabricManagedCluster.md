---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
ms.openlocfilehash: a9e3f5f8305733329f7ff9e34eadde151d873c6b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005501"
---
# <span data-ttu-id="dce8f-101">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="dce8f-101">Remove-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="dce8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dce8f-102">SYNOPSIS</span></span>
<span data-ttu-id="dce8f-103">Rimuovere la risorsa cluster.</span><span class="sxs-lookup"><span data-stu-id="dce8f-103">Remove cluster resource.</span></span>

## <span data-ttu-id="dce8f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dce8f-104">SYNTAX</span></span>

### <span data-ttu-id="dce8f-105">ByObj (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dce8f-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dce8f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="dce8f-106">ByName</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dce8f-107">ById</span><span class="sxs-lookup"><span data-stu-id="dce8f-107">ById</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dce8f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dce8f-108">DESCRIPTION</span></span>
<span data-ttu-id="dce8f-109">Rimuovere il cluster rimuoverà anche i tipi di nodo nel cluster.</span><span class="sxs-lookup"><span data-stu-id="dce8f-109">Remove cluster this will remove the node types under the cluster too.</span></span>

## <span data-ttu-id="dce8f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dce8f-110">EXAMPLES</span></span>

### <span data-ttu-id="dce8f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dce8f-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedCluster -ResourceGroupName sfmcalsantamps -ClusterName sfmcalsantamps
```

<span data-ttu-id="dce8f-112">Rimuovere il cluster.</span><span class="sxs-lookup"><span data-stu-id="dce8f-112">Remove cluster.</span></span>

### <span data-ttu-id="dce8f-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="dce8f-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedCluster
```

<span data-ttu-id="dce8f-114">Rimuovere il cluster con l'opzione di piping.</span><span class="sxs-lookup"><span data-stu-id="dce8f-114">Remove cluster, with piping.</span></span>

## <span data-ttu-id="dce8f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dce8f-115">PARAMETERS</span></span>

### <span data-ttu-id="dce8f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dce8f-116">-AsJob</span></span>
<span data-ttu-id="dce8f-117">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="dce8f-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="dce8f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dce8f-118">-DefaultProfile</span></span>
<span data-ttu-id="dce8f-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dce8f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dce8f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dce8f-120">-InputObject</span></span>
<span data-ttu-id="dce8f-121">Risorsa cluster gestito</span><span class="sxs-lookup"><span data-stu-id="dce8f-121">Managed Cluster resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSManagedCluster
Parameter Sets: ByObj
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dce8f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="dce8f-122">-Name</span></span>
<span data-ttu-id="dce8f-123">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="dce8f-123">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dce8f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dce8f-124">-PassThru</span></span>
<span data-ttu-id="dce8f-125">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="dce8f-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="dce8f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dce8f-126">-ResourceGroupName</span></span>
<span data-ttu-id="dce8f-127">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dce8f-127">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dce8f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dce8f-128">-ResourceId</span></span>
<span data-ttu-id="dce8f-129">ID risorsa cluster gestito</span><span class="sxs-lookup"><span data-stu-id="dce8f-129">Managed Cluster resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dce8f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dce8f-130">-Confirm</span></span>
<span data-ttu-id="dce8f-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dce8f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dce8f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dce8f-132">-WhatIf</span></span>
<span data-ttu-id="dce8f-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dce8f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dce8f-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dce8f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dce8f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dce8f-135">CommonParameters</span></span>
<span data-ttu-id="dce8f-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dce8f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dce8f-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dce8f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dce8f-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="dce8f-138">INPUTS</span></span>

### <span data-ttu-id="dce8f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="dce8f-139">System.String</span></span>

## <span data-ttu-id="dce8f-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dce8f-140">OUTPUTS</span></span>

### <span data-ttu-id="dce8f-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dce8f-141">System.Boolean</span></span>

## <span data-ttu-id="dce8f-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="dce8f-142">NOTES</span></span>

## <span data-ttu-id="dce8f-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dce8f-143">RELATED LINKS</span></span>
