---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/update-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Update-AzAksNodePool.md
ms.openlocfilehash: a3849a07f83cda8876acdf87015e8f2fc9fe81b5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348856"
---
# <span data-ttu-id="d275f-101">Update-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="d275f-101">Update-AzAksNodePool</span></span>

## <span data-ttu-id="d275f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d275f-102">SYNOPSIS</span></span>
<span data-ttu-id="d275f-103">Aggiornare il pool di nodi in un cluster gestito.</span><span class="sxs-lookup"><span data-stu-id="d275f-103">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="d275f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d275f-104">SYNTAX</span></span>

### <span data-ttu-id="d275f-105">defaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d275f-105">defaultParameterSet (Default)</span></span>
```
Update-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> -Name <String> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d275f-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d275f-106">ParentObjectParameterSet</span></span>
```
Update-AzAksNodePool -Name <String> -ClusterObject <PSKubernetesCluster> [-AsJob] [-Force]
 [-KubernetesVersion <String>] [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d275f-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d275f-107">InputObjectParameterSet</span></span>
```
Update-AzAksNodePool -InputObject <PSNodePool> [-AsJob] [-Force] [-KubernetesVersion <String>]
 [-MinCount <Int32>] [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d275f-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d275f-108">IdParameterSet</span></span>
```
Update-AzAksNodePool -Id <String> [-AsJob] [-Force] [-KubernetesVersion <String>] [-MinCount <Int32>]
 [-MaxCount <Int32>] [-EnableAutoScaling] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d275f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d275f-109">DESCRIPTION</span></span>
<span data-ttu-id="d275f-110">Aggiornare il pool di nodi in un cluster gestito.</span><span class="sxs-lookup"><span data-stu-id="d275f-110">Update node pool in a managed cluster.</span></span>

## <span data-ttu-id="d275f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d275f-111">EXAMPLES</span></span>

### <span data-ttu-id="d275f-112">Modificare il numero minimo fino a 5 per il pool di nodi specificato</span><span class="sxs-lookup"><span data-stu-id="d275f-112">Change minimun count to 5 for specified node pool</span></span>
```powershell
PS C:\> Update-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster -Name linuxpool -MinCount 5
```

## <span data-ttu-id="d275f-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d275f-113">PARAMETERS</span></span>

### <span data-ttu-id="d275f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d275f-114">-AsJob</span></span>
<span data-ttu-id="d275f-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d275f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d275f-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="d275f-116">-ClusterName</span></span>
<span data-ttu-id="d275f-117">Nome della risorsa del cluster gestito.</span><span class="sxs-lookup"><span data-stu-id="d275f-117">The name of the managed cluster resource.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d275f-118">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="d275f-118">-ClusterObject</span></span>
<span data-ttu-id="d275f-119">Oggetto cluster</span><span class="sxs-lookup"><span data-stu-id="d275f-119">The cluster object</span></span>

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

### <span data-ttu-id="d275f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d275f-120">-DefaultProfile</span></span>
<span data-ttu-id="d275f-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d275f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d275f-122">-EnableAutoScaling</span><span class="sxs-lookup"><span data-stu-id="d275f-122">-EnableAutoScaling</span></span>
<span data-ttu-id="d275f-123">Se abilitare il ridimensionamento automatico</span><span class="sxs-lookup"><span data-stu-id="d275f-123">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="d275f-124">-Force</span><span class="sxs-lookup"><span data-stu-id="d275f-124">-Force</span></span>
<span data-ttu-id="d275f-125">Aggiornare il pool di nodi senza richiesta</span><span class="sxs-lookup"><span data-stu-id="d275f-125">Update node pool without prompt</span></span>

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

### <span data-ttu-id="d275f-126">-ID</span><span class="sxs-lookup"><span data-stu-id="d275f-126">-Id</span></span>
<span data-ttu-id="d275f-127">ID di un pool di nodi nel cluster managed Kubernetes</span><span class="sxs-lookup"><span data-stu-id="d275f-127">Id of an node pool in managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d275f-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d275f-128">-InputObject</span></span>
<span data-ttu-id="d275f-129">Un oggetto PSAgentPool, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="d275f-129">A PSAgentPool object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="d275f-130">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="d275f-130">-KubernetesVersion</span></span>
<span data-ttu-id="d275f-131">La versione di Kubernetes da usare per creare il cluster.</span><span class="sxs-lookup"><span data-stu-id="d275f-131">The version of Kubernetes to use for creating the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d275f-132">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="d275f-132">-MaxCount</span></span>
<span data-ttu-id="d275f-133">Numero massimo di nodi per il ridimensionamento automatico</span><span class="sxs-lookup"><span data-stu-id="d275f-133">Maximum number of nodes for auto-scaling</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d275f-134">-MinCount</span><span class="sxs-lookup"><span data-stu-id="d275f-134">-MinCount</span></span>
<span data-ttu-id="d275f-135">Numero minimo di nodi per il ridimensionamento automatico.</span><span class="sxs-lookup"><span data-stu-id="d275f-135">Minimum number of nodes for auto-scaling.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d275f-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="d275f-136">-Name</span></span>
<span data-ttu-id="d275f-137">Nome del pool di nodi.</span><span class="sxs-lookup"><span data-stu-id="d275f-137">The name of the node pool.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d275f-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d275f-138">-ResourceGroupName</span></span>
<span data-ttu-id="d275f-139">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d275f-139">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d275f-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d275f-140">-Confirm</span></span>
<span data-ttu-id="d275f-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d275f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d275f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d275f-142">-WhatIf</span></span>
<span data-ttu-id="d275f-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d275f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d275f-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d275f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d275f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d275f-145">CommonParameters</span></span>
<span data-ttu-id="d275f-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d275f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d275f-147">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d275f-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d275f-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d275f-148">INPUTS</span></span>

### <span data-ttu-id="d275f-149">Microsoft. Azure. Commands. AKS. Models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="d275f-149">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

### <span data-ttu-id="d275f-150">System. String</span><span class="sxs-lookup"><span data-stu-id="d275f-150">System.String</span></span>

## <span data-ttu-id="d275f-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d275f-151">OUTPUTS</span></span>

### <span data-ttu-id="d275f-152">Microsoft. Azure. Commands. AKS. Models. PSNodePool</span><span class="sxs-lookup"><span data-stu-id="d275f-152">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="d275f-153">Note</span><span class="sxs-lookup"><span data-stu-id="d275f-153">NOTES</span></span>

## <span data-ttu-id="d275f-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d275f-154">RELATED LINKS</span></span>
