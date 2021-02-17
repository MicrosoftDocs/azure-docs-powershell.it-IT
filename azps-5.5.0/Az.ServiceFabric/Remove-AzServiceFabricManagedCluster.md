---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricmanagedcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricManagedCluster.md
ms.openlocfilehash: d676958948b9197a64a08646e837287299107bfa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191158"
---
# <span data-ttu-id="2a986-101">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="2a986-101">Remove-AzServiceFabricManagedCluster</span></span>

## <span data-ttu-id="2a986-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a986-102">SYNOPSIS</span></span>
<span data-ttu-id="2a986-103">Rimuovere la risorsa cluster.</span><span class="sxs-lookup"><span data-stu-id="2a986-103">Remove cluster resource.</span></span>

## <span data-ttu-id="2a986-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2a986-104">SYNTAX</span></span>

### <span data-ttu-id="2a986-105">ByObj (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2a986-105">ByObj (Default)</span></span>
```
Remove-AzServiceFabricManagedCluster [-InputObject] <PSManagedCluster> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a986-106">ByName</span><span class="sxs-lookup"><span data-stu-id="2a986-106">ByName</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a986-107">ById</span><span class="sxs-lookup"><span data-stu-id="2a986-107">ById</span></span>
```
Remove-AzServiceFabricManagedCluster [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a986-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2a986-108">DESCRIPTION</span></span>
<span data-ttu-id="2a986-109">Rimuovere il cluster rimuoverà anche i tipi di nodo nel cluster.</span><span class="sxs-lookup"><span data-stu-id="2a986-109">Remove cluster this will remove the node types under the cluster too.</span></span>

## <span data-ttu-id="2a986-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2a986-110">EXAMPLES</span></span>

### <span data-ttu-id="2a986-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2a986-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
Remove-AzServiceFabricManagedCluster -ResourceGroupName sfmcalsantamps -ClusterName sfmcalsantamps
```

<span data-ttu-id="2a986-112">Rimuovere il cluster.</span><span class="sxs-lookup"><span data-stu-id="2a986-112">Remove cluster.</span></span>

### <span data-ttu-id="2a986-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2a986-113">Example 2</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$cluster = Get-AzServiceFabricManagedCluster -ResourceGroupName $rgName -Name $clusterName

$cluster | Remove-AzServiceFabricManagedCluster
```

<span data-ttu-id="2a986-114">Rimuovere il cluster, con le tubature.</span><span class="sxs-lookup"><span data-stu-id="2a986-114">Remove cluster, with piping.</span></span>

## <span data-ttu-id="2a986-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a986-115">PARAMETERS</span></span>

### <span data-ttu-id="2a986-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a986-116">-AsJob</span></span>
<span data-ttu-id="2a986-117">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="2a986-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="2a986-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a986-118">-DefaultProfile</span></span>
<span data-ttu-id="2a986-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2a986-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a986-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a986-120">-InputObject</span></span>
<span data-ttu-id="2a986-121">Risorsa cluster gestito</span><span class="sxs-lookup"><span data-stu-id="2a986-121">Managed Cluster resource</span></span>

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

### <span data-ttu-id="2a986-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2a986-122">-Name</span></span>
<span data-ttu-id="2a986-123">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="2a986-123">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="2a986-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a986-124">-PassThru</span></span>
<span data-ttu-id="2a986-125">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="2a986-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="2a986-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a986-126">-ResourceGroupName</span></span>
<span data-ttu-id="2a986-127">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2a986-127">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="2a986-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a986-128">-ResourceId</span></span>
<span data-ttu-id="2a986-129">ID risorsa cluster gestito</span><span class="sxs-lookup"><span data-stu-id="2a986-129">Managed Cluster resource id</span></span>

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

### <span data-ttu-id="2a986-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a986-130">-Confirm</span></span>
<span data-ttu-id="2a986-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a986-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a986-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a986-132">-WhatIf</span></span>
<span data-ttu-id="2a986-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2a986-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a986-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2a986-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a986-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a986-135">CommonParameters</span></span>
<span data-ttu-id="2a986-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a986-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a986-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2a986-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a986-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="2a986-138">INPUTS</span></span>

### <span data-ttu-id="2a986-139">System.String</span><span class="sxs-lookup"><span data-stu-id="2a986-139">System.String</span></span>

## <span data-ttu-id="2a986-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2a986-140">OUTPUTS</span></span>

### <span data-ttu-id="2a986-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2a986-141">System.Boolean</span></span>

## <span data-ttu-id="2a986-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="2a986-142">NOTES</span></span>

## <span data-ttu-id="2a986-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2a986-143">RELATED LINKS</span></span>
