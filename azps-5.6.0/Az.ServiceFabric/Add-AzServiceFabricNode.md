---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/add-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
ms.openlocfilehash: 34b55a5da226a3985cb6fe3bede244ee1e054726
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984062"
---
# <span data-ttu-id="46ad2-101">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="46ad2-101">Add-AzServiceFabricNode</span></span>

## <span data-ttu-id="46ad2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46ad2-102">SYNOPSIS</span></span>
<span data-ttu-id="46ad2-103">Aggiungere i nodi al tipo di nodo specifico nel cluster.</span><span class="sxs-lookup"><span data-stu-id="46ad2-103">Add nodes to the specific node type in the cluster.</span></span>

## <span data-ttu-id="46ad2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="46ad2-104">SYNTAX</span></span>

```
Add-AzServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46ad2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="46ad2-105">DESCRIPTION</span></span>
<span data-ttu-id="46ad2-106">Usare **Add-AzServiceFabricNode** per aggiungere nodi al tipo di nodo specifico.</span><span class="sxs-lookup"><span data-stu-id="46ad2-106">Use **Add-AzServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="46ad2-107">È sufficiente specificare il numero di nodi da aggiungere a un tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="46ad2-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="46ad2-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="46ad2-108">EXAMPLES</span></span>

### <span data-ttu-id="46ad2-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="46ad2-109">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="46ad2-110">Questo comando aggiunge 2 nodi al tipo di nodo 'n1'.</span><span class="sxs-lookup"><span data-stu-id="46ad2-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="46ad2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46ad2-111">PARAMETERS</span></span>

### <span data-ttu-id="46ad2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46ad2-112">-DefaultProfile</span></span>
<span data-ttu-id="46ad2-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="46ad2-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46ad2-114">-Name</span><span class="sxs-lookup"><span data-stu-id="46ad2-114">-Name</span></span>
<span data-ttu-id="46ad2-115">Specificare il nome del cluster</span><span class="sxs-lookup"><span data-stu-id="46ad2-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="46ad2-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="46ad2-116">-NodeType</span></span>
<span data-ttu-id="46ad2-117">Nome del tipo di nodo</span><span class="sxs-lookup"><span data-stu-id="46ad2-117">Node type name</span></span>

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

### <span data-ttu-id="46ad2-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="46ad2-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="46ad2-119">Il numero di nodi da aggiungere</span><span class="sxs-lookup"><span data-stu-id="46ad2-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="46ad2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46ad2-120">-ResourceGroupName</span></span>
<span data-ttu-id="46ad2-121">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="46ad2-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="46ad2-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46ad2-122">-Confirm</span></span>
<span data-ttu-id="46ad2-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46ad2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46ad2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46ad2-124">-WhatIf</span></span>
<span data-ttu-id="46ad2-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="46ad2-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46ad2-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="46ad2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46ad2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46ad2-127">CommonParameters</span></span>
<span data-ttu-id="46ad2-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46ad2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46ad2-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="46ad2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46ad2-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="46ad2-130">INPUTS</span></span>

### <span data-ttu-id="46ad2-131">System.Int32</span><span class="sxs-lookup"><span data-stu-id="46ad2-131">System.Int32</span></span>

### <span data-ttu-id="46ad2-132">System.String</span><span class="sxs-lookup"><span data-stu-id="46ad2-132">System.String</span></span>

## <span data-ttu-id="46ad2-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="46ad2-133">OUTPUTS</span></span>

### <span data-ttu-id="46ad2-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="46ad2-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="46ad2-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="46ad2-135">NOTES</span></span>

## <span data-ttu-id="46ad2-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="46ad2-136">RELATED LINKS</span></span>

[<span data-ttu-id="46ad2-137">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="46ad2-137">Remove-AzServiceFabricNode</span></span>](./Remove-AzServiceFabricNode.md)
