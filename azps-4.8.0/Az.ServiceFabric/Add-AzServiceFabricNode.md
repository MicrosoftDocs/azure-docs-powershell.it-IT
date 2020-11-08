---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
ms.openlocfilehash: 41c78b659a39d3df52185eeb2b67e4c921f22b45
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189344"
---
# <span data-ttu-id="3bc97-101">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="3bc97-101">Add-AzServiceFabricNode</span></span>

## <span data-ttu-id="3bc97-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3bc97-102">SYNOPSIS</span></span>
<span data-ttu-id="3bc97-103">Aggiungere nodi al tipo di nodo specifico nel cluster.</span><span class="sxs-lookup"><span data-stu-id="3bc97-103">Add nodes to the specific node type in the cluster.</span></span>

## <span data-ttu-id="3bc97-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3bc97-104">SYNTAX</span></span>

```
Add-AzServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3bc97-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3bc97-105">DESCRIPTION</span></span>
<span data-ttu-id="3bc97-106">USA **Add-AzServiceFabricNode** per aggiungere nodi al tipo di nodo specifico.</span><span class="sxs-lookup"><span data-stu-id="3bc97-106">Use **Add-AzServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="3bc97-107">Devi solo specificare il numero di nodi che vuoi aggiungere a un tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="3bc97-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="3bc97-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3bc97-108">EXAMPLES</span></span>

### <span data-ttu-id="3bc97-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3bc97-109">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="3bc97-110">Questo comando aggiungerà 2 nodi al tipo di nodo "N1".</span><span class="sxs-lookup"><span data-stu-id="3bc97-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="3bc97-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3bc97-111">PARAMETERS</span></span>

### <span data-ttu-id="3bc97-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bc97-112">-DefaultProfile</span></span>
<span data-ttu-id="3bc97-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3bc97-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bc97-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="3bc97-114">-Name</span></span>
<span data-ttu-id="3bc97-115">Specificare il nome del cluster</span><span class="sxs-lookup"><span data-stu-id="3bc97-115">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc97-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="3bc97-116">-NodeType</span></span>
<span data-ttu-id="3bc97-117">Nome tipo di nodo</span><span class="sxs-lookup"><span data-stu-id="3bc97-117">Node type name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc97-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="3bc97-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="3bc97-119">Numero di nodi da aggiungere</span><span class="sxs-lookup"><span data-stu-id="3bc97-119">The number of nodes to add</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Number

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3bc97-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bc97-120">-ResourceGroupName</span></span>
<span data-ttu-id="3bc97-121">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3bc97-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="3bc97-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3bc97-122">-Confirm</span></span>
<span data-ttu-id="3bc97-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bc97-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bc97-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bc97-124">-WhatIf</span></span>
<span data-ttu-id="3bc97-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3bc97-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bc97-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3bc97-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bc97-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bc97-127">CommonParameters</span></span>
<span data-ttu-id="3bc97-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bc97-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bc97-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3bc97-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bc97-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3bc97-130">INPUTS</span></span>

### <span data-ttu-id="3bc97-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="3bc97-131">System.Int32</span></span>

### <span data-ttu-id="3bc97-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3bc97-132">System.String</span></span>

## <span data-ttu-id="3bc97-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3bc97-133">OUTPUTS</span></span>

### <span data-ttu-id="3bc97-134">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="3bc97-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="3bc97-135">Note</span><span class="sxs-lookup"><span data-stu-id="3bc97-135">NOTES</span></span>

## <span data-ttu-id="3bc97-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3bc97-136">RELATED LINKS</span></span>

[<span data-ttu-id="3bc97-137">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="3bc97-137">Remove-AzServiceFabricNode</span></span>](./Remove-AzServiceFabricNode.md)
