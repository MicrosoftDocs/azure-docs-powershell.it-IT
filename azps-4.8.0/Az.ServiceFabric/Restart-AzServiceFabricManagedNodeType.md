---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/restart-azservicefabricmanagednodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Restart-AzServiceFabricManagedNodeType.md
ms.openlocfilehash: 341684705b869c0a1b2b405b7f21f7fc84dcbf8d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190104"
---
# <span data-ttu-id="cebb3-101">Restart-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="cebb3-101">Restart-AzServiceFabricManagedNodeType</span></span>

## <span data-ttu-id="cebb3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cebb3-102">SYNOPSIS</span></span>
<span data-ttu-id="cebb3-103">Riavviare nodi specifici dal tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="cebb3-103">Restart specific nodes from the node type.</span></span>

## <span data-ttu-id="cebb3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cebb3-104">SYNTAX</span></span>

```
Restart-AzServiceFabricManagedNodeType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 -NodeName <String[]> [-ForceRestart] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cebb3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cebb3-105">DESCRIPTION</span></span>
<span data-ttu-id="cebb3-106">Riavviare nodi specifici dal tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="cebb3-106">Restart specific nodes from the node type.</span></span> <span data-ttu-id="cebb3-107">I nodi del tessuto del servizio verranno disabilitati prima di riavviare le VM e riabilitati quando torneranno.</span><span class="sxs-lookup"><span data-stu-id="cebb3-107">It will disabled the service fabric nodes before restarting the vms and enabled them back again once they come back.</span></span> <span data-ttu-id="cebb3-108">Se l'operazione viene eseguita nei tipi di nodi primari, potrebbe essere necessario un po' di tempo perché potrebbe non riavviare tutti i nodi contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="cebb3-108">If this is done on primary node types it might take a while as it might not restart all the nodes at the same time.</span></span> <span data-ttu-id="cebb3-109">Use-ForceRestart forza l'operazione anche se il tessuto di servizio non è in grado di disabilitare i nodi, ma può essere usato con cautela perché potrebbe causare perdite di dati se nel nodo sono in esecuzione carichi di lavoro con stato.</span><span class="sxs-lookup"><span data-stu-id="cebb3-109">Use -ForceRestart force the operation even if service fabric is unable to disable the nodes but use with caution as this might cause data loss if stateful workloads are running on the node.</span></span>

## <span data-ttu-id="cebb3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cebb3-110">EXAMPLES</span></span>

### <span data-ttu-id="cebb3-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cebb3-111">Example 1</span></span>
```powershell
$rgName = "testRG"
$clusterName = "testCluster"
$NodeTypeName = "nt1"
Restart-AzServiceFabricManagedNodeType -ResourceGroupName $rgName -ClusterName $clusterName  -Name $NodeTypeName -NodeName nt1_0, nt1_3
```

<span data-ttu-id="cebb3-112">Riavviare il nodo 0 e 3 nel tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="cebb3-112">Restart node 0 and 3 on the node type.</span></span>

## <span data-ttu-id="cebb3-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cebb3-113">PARAMETERS</span></span>

### <span data-ttu-id="cebb3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cebb3-114">-AsJob</span></span>
<span data-ttu-id="cebb3-115">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="cebb3-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="cebb3-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="cebb3-116">-ClusterName</span></span>
<span data-ttu-id="cebb3-117">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="cebb3-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="cebb3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cebb3-118">-DefaultProfile</span></span>
<span data-ttu-id="cebb3-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cebb3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cebb3-120">-ForceRestart</span><span class="sxs-lookup"><span data-stu-id="cebb3-120">-ForceRestart</span></span>
<span data-ttu-id="cebb3-121">L'uso di questo contrassegno forza il riavvio del nodo anche se il tessuto di servizio non è in grado di disabilitare i nodi.</span><span class="sxs-lookup"><span data-stu-id="cebb3-121">Using this flag will force the node to restart even if service fabric is unable to disable the nodes.</span></span>

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

### <span data-ttu-id="cebb3-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="cebb3-122">-Name</span></span>
<span data-ttu-id="cebb3-123">Specificare il nome del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="cebb3-123">Specify the name of the node type.</span></span>

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

### <span data-ttu-id="cebb3-124">-NodeName</span><span class="sxs-lookup"><span data-stu-id="cebb3-124">-NodeName</span></span>
<span data-ttu-id="cebb3-125">Elenco di nomi di nodo per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="cebb3-125">List of node names for the operation.</span></span>

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

### <span data-ttu-id="cebb3-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cebb3-126">-PassThru</span></span>
<span data-ttu-id="cebb3-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="cebb3-127">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="cebb3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cebb3-128">-ResourceGroupName</span></span>
<span data-ttu-id="cebb3-129">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cebb3-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="cebb3-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cebb3-130">-Confirm</span></span>
<span data-ttu-id="cebb3-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cebb3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cebb3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cebb3-132">-WhatIf</span></span>
<span data-ttu-id="cebb3-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cebb3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cebb3-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cebb3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cebb3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cebb3-135">CommonParameters</span></span>
<span data-ttu-id="cebb3-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cebb3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cebb3-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cebb3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cebb3-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cebb3-138">INPUTS</span></span>

### <span data-ttu-id="cebb3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="cebb3-139">System.String</span></span>

## <span data-ttu-id="cebb3-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cebb3-140">OUTPUTS</span></span>

### <span data-ttu-id="cebb3-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cebb3-141">System.Boolean</span></span>

## <span data-ttu-id="cebb3-142">Note</span><span class="sxs-lookup"><span data-stu-id="cebb3-142">NOTES</span></span>

## <span data-ttu-id="cebb3-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cebb3-143">RELATED LINKS</span></span>