---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/restart-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 341684705b869c0a1b2b405b7f21f7fc84dcbf8d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183423"
---
# <span data-ttu-id="bfeb8-101">Restart-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="bfeb8-101">Restart-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="bfeb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfeb8-102">SYNOPSIS</span></span>
<span data-ttu-id="bfeb8-103">Riavviare nodi specifici dal tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="bfeb8-103">Restart specific nodes from the node type.</span></span>

## <span data-ttu-id="bfeb8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bfeb8-104">SYNTAX</span></span>

```
Restart-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRestart] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfeb8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bfeb8-105">DESCRIPTION</span></span>
<span data-ttu-id="bfeb8-106">Riavviare nodi specifici dal tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="bfeb8-106">Restart specific nodes from the node type.</span></span> <span data-ttu-id="bfeb8-107">I nodi dell'infrastruttura di servizio verranno disabilitati prima di riavviare le macchine virtuali e averli ri abilitati nuovamente una volta tornati.</span><span class="sxs-lookup"><span data-stu-id="bfeb8-107">It will disabled the service fabric nodes before restarting the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="bfeb8-108">Se questa operazione viene eseguita nei tipi di nodo primario, l'operazione potrebbe richiedere del tempo perché potrebbe non riavviare tutti i nodi contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="bfeb8-108">If this is done on primary node types it might take a while as it might not restart all the nodes at the same time.</span></span> <span data-ttu-id="bfeb8-109">Usare -ForceRestart forza l'operazione anche se l'infrastruttura del servizio non è in grado di disabilitare i nodi, ma con cautela, perché ciò potrebbe causare la perdita di dati se nel nodo sono in esecuzione carichi di lavoro con stato.</span><span class="sxs-lookup"><span data-stu-id="bfeb8-109">Use -ForceRestart force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="bfeb8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bfeb8-110">EXAMPLES</span></span>

### <span data-ttu-id="bfeb8-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bfeb8-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Restart-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="bfeb8-112">Riavviare il nodo 0 e 3 nel tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="bfeb8-112">Restart node 0 and 3 on the node type.</span></span>

## <span data-ttu-id="bfeb8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfeb8-113">PARAMETERS</span></span>

### <span data-ttu-id="bfeb8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bfeb8-114">-AsJob</span></span>
<span data-ttu-id="bfeb8-115">Eseguire il cmdlet in background e restituire un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="bfeb8-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="bfeb8-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="bfeb8-116">-ClusterName</span></span>
<span data-ttu-id="bfeb8-117">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="bfeb8-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="bfeb8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfeb8-118">-DefaultProfile</span></span>
<span data-ttu-id="bfeb8-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bfeb8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfeb8-120">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="bfeb8-120">-ForceRestart</span></span>
<span data-ttu-id="bfeb8-121">L'uso di questo flag forza il riavvio del nodo anche se non è possibile disabilitare i nodi.</span><span class="sxs-lookup"><span data-stu-id="bfeb8-121">Using this flag will force the node to restart even if service fabric is unable to disable the nodes.</span></span>

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

### <span data-ttu-id="bfeb8-122">-Name</span><span class="sxs-lookup"><span data-stu-id="bfeb8-122">-Name</span></span>
<span data-ttu-id="bfeb8-123">Specificare il nome del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="bfeb8-123">Specify the name of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NodeTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfeb8-124">-NodeName</span><span class="sxs-lookup"><span data-stu-id="bfeb8-124">-NodeName</span></span>
<span data-ttu-id="bfeb8-125">Elenco dei nomi dei nodi per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="bfeb8-125">List of node names for the operation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfeb8-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bfeb8-126">-PassThru</span></span>
<span data-ttu-id="bfeb8-127">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="bfeb8-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="bfeb8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfeb8-128">-ResourceGroupName</span></span>
<span data-ttu-id="bfeb8-129">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bfeb8-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="bfeb8-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bfeb8-130">-Confirm</span></span>
<span data-ttu-id="bfeb8-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfeb8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfeb8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfeb8-132">-WhatIf</span></span>
<span data-ttu-id="bfeb8-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bfeb8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfeb8-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bfeb8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfeb8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfeb8-135">CommonParameters</span></span>
<span data-ttu-id="bfeb8-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfeb8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfeb8-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bfeb8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfeb8-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="bfeb8-138">INPUTS</span></span>

### <span data-ttu-id="bfeb8-139">System.String</span><span class="sxs-lookup"><span data-stu-id="bfeb8-139">System.String</span></span>

## <span data-ttu-id="bfeb8-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bfeb8-140">OUTPUTS</span></span>

### <span data-ttu-id="bfeb8-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bfeb8-141">System.Boolean</span></span>

## <span data-ttu-id="bfeb8-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="bfeb8-142">NOTES</span></span>

## <span data-ttu-id="bfeb8-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bfeb8-143">RELATED LINKS</span></span>
