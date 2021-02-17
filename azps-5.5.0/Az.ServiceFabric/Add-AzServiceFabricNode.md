---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
ms.openlocfilehash: 41c78b659a39d3df52185eeb2b67e4c921f22b45
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208091"
---
# <span data-ttu-id="b229b-101">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="b229b-101">Add-AzServiceFabricNode</span></span>

## <span data-ttu-id="b229b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b229b-102">SYNOPSIS</span></span>
<span data-ttu-id="b229b-103">Aggiungere i nodi al tipo di nodo specifico nel cluster.</span><span class="sxs-lookup"><span data-stu-id="b229b-103">Add nodes to the specific node type in the cluster.</span></span>

## <span data-ttu-id="b229b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b229b-104">SYNTAX</span></span>

```
Add-AzServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b229b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b229b-105">DESCRIPTION</span></span>
<span data-ttu-id="b229b-106">Usare **Add-AzServiceFabricNode** per aggiungere nodi al tipo di nodo specifico.</span><span class="sxs-lookup"><span data-stu-id="b229b-106">Use **Add-AzServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="b229b-107">È sufficiente specificare il numero di nodi da aggiungere a un tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="b229b-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="b229b-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b229b-108">EXAMPLES</span></span>

### <span data-ttu-id="b229b-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b229b-109">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="b229b-110">Questo comando aggiunge 2 nodi al tipo di nodo 'n1'.</span><span class="sxs-lookup"><span data-stu-id="b229b-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="b229b-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b229b-111">PARAMETERS</span></span>

### <span data-ttu-id="b229b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b229b-112">-DefaultProfile</span></span>
<span data-ttu-id="b229b-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b229b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b229b-114">-Name</span><span class="sxs-lookup"><span data-stu-id="b229b-114">-Name</span></span>
<span data-ttu-id="b229b-115">Specificare il nome del cluster</span><span class="sxs-lookup"><span data-stu-id="b229b-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="b229b-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="b229b-116">-NodeType</span></span>
<span data-ttu-id="b229b-117">Nome del tipo di nodo</span><span class="sxs-lookup"><span data-stu-id="b229b-117">Node type name</span></span>

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

### <span data-ttu-id="b229b-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="b229b-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="b229b-119">Il numero di nodi da aggiungere</span><span class="sxs-lookup"><span data-stu-id="b229b-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="b229b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b229b-120">-ResourceGroupName</span></span>
<span data-ttu-id="b229b-121">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b229b-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="b229b-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b229b-122">-Confirm</span></span>
<span data-ttu-id="b229b-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b229b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b229b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b229b-124">-WhatIf</span></span>
<span data-ttu-id="b229b-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b229b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b229b-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b229b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b229b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b229b-127">CommonParameters</span></span>
<span data-ttu-id="b229b-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b229b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b229b-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b229b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b229b-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="b229b-130">INPUTS</span></span>

### <span data-ttu-id="b229b-131">System.Int32</span><span class="sxs-lookup"><span data-stu-id="b229b-131">System.Int32</span></span>

### <span data-ttu-id="b229b-132">System.String</span><span class="sxs-lookup"><span data-stu-id="b229b-132">System.String</span></span>

## <span data-ttu-id="b229b-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b229b-133">OUTPUTS</span></span>

### <span data-ttu-id="b229b-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="b229b-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="b229b-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="b229b-135">NOTES</span></span>

## <span data-ttu-id="b229b-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b229b-136">RELATED LINKS</span></span>

[<span data-ttu-id="b229b-137">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="b229b-137">Remove-AzServiceFabricNode</span></span>](./Remove-AzServiceFabricNode.md)
