---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksNodePool.md
ms.openlocfilehash: 13bc647a0b2cbbc415c12aabb9e14016e3d34149
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188641"
---
# <span data-ttu-id="4febb-101">Remove-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="4febb-101">Remove-AzAksNodePool</span></span>

## <span data-ttu-id="4febb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4febb-102">SYNOPSIS</span></span>
<span data-ttu-id="4febb-103">Eliminare il pool di nodi da un cluster gestito.</span><span class="sxs-lookup"><span data-stu-id="4febb-103">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="4febb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4febb-104">SYNTAX</span></span>

### <span data-ttu-id="4febb-105">GroupNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4febb-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksNodePool [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4febb-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4febb-106">InputObjectParameterSet</span></span>
```
Remove-AzAksNodePool -InputObject <PSNodePool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4febb-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4febb-107">IdParameterSet</span></span>
```
Remove-AzAksNodePool [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4febb-108">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4febb-108">ParentObjectParameterSet</span></span>
```
Remove-AzAksNodePool [-Name] <String> -ClusterObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4febb-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4febb-109">DESCRIPTION</span></span>
<span data-ttu-id="4febb-110">Eliminare il pool di nodi da un cluster gestito.</span><span class="sxs-lookup"><span data-stu-id="4febb-110">Delete node pool from managed cluster.</span></span>

## <span data-ttu-id="4febb-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4febb-111">EXAMPLES</span></span>

### <span data-ttu-id="4febb-112">Eliminare il pool di nodi specificato</span><span class="sxs-lookup"><span data-stu-id="4febb-112">Delete specified node pool</span></span>
```powershell
PS C:\> Remove-AzAksNodePool -ResourceGroupName myResourceGroup -CulsterName myCluster -Name winpool
```

## <span data-ttu-id="4febb-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4febb-113">PARAMETERS</span></span>

### <span data-ttu-id="4febb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4febb-114">-AsJob</span></span>
<span data-ttu-id="4febb-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4febb-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4febb-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="4febb-116">-ClusterName</span></span>
<span data-ttu-id="4febb-117">Nome del cluster di Kubernetes gestito</span><span class="sxs-lookup"><span data-stu-id="4febb-117">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4febb-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="4febb-118">-ClusterObject</span></span>
<span data-ttu-id="4febb-119">Oggetto cluster.</span><span class="sxs-lookup"><span data-stu-id="4febb-119">The cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4febb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4febb-120">-DefaultProfile</span></span>
<span data-ttu-id="4febb-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4febb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4febb-122">-Force</span><span class="sxs-lookup"><span data-stu-id="4febb-122">-Force</span></span>
<span data-ttu-id="4febb-123">Rimuovere il pool di nodi senza richiesta</span><span class="sxs-lookup"><span data-stu-id="4febb-123">Remove node pool without prompt</span></span>

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

### <span data-ttu-id="4febb-124">-ID</span><span class="sxs-lookup"><span data-stu-id="4febb-124">-Id</span></span>
<span data-ttu-id="4febb-125">ID di un pool di nodi nel cluster managed Kubernetes</span><span class="sxs-lookup"><span data-stu-id="4febb-125">Id of an node pool in managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4febb-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4febb-126">-InputObject</span></span>
<span data-ttu-id="4febb-127">Un oggetto PSAgentPool, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="4febb-127">A PSAgentPool object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSNodePool
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4febb-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="4febb-128">-Name</span></span>
<span data-ttu-id="4febb-129">Nome del pool di nodi</span><span class="sxs-lookup"><span data-stu-id="4febb-129">Name of your node pool</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4febb-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4febb-130">-PassThru</span></span>
<span data-ttu-id="4febb-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="4febb-131">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="4febb-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4febb-132">-ResourceGroupName</span></span>
<span data-ttu-id="4febb-133">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="4febb-133">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4febb-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4febb-134">-Confirm</span></span>
<span data-ttu-id="4febb-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4febb-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4febb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4febb-136">-WhatIf</span></span>
<span data-ttu-id="4febb-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4febb-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4febb-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4febb-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4febb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4febb-139">CommonParameters</span></span>
<span data-ttu-id="4febb-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4febb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4febb-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4febb-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4febb-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4febb-142">INPUTS</span></span>

### <span data-ttu-id="4febb-143">Microsoft. Azure. Commands. AKS. Models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="4febb-143">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="4febb-144">System. String</span><span class="sxs-lookup"><span data-stu-id="4febb-144">System.String</span></span>

## <span data-ttu-id="4febb-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4febb-145">OUTPUTS</span></span>

### <span data-ttu-id="4febb-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4febb-146">System.Boolean</span></span>

## <span data-ttu-id="4febb-147">Note</span><span class="sxs-lookup"><span data-stu-id="4febb-147">NOTES</span></span>

## <span data-ttu-id="4febb-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4febb-148">RELATED LINKS</span></span>
