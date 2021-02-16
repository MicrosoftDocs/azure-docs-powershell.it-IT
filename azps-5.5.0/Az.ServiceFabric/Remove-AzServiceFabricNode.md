---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
ms.openlocfilehash: fd38b68c8133cbc498bbc50ffea84b48e58198a9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183454"
---
# <span data-ttu-id="5897c-101">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="5897c-101">Remove-AzServiceFabricNode</span></span>

## <span data-ttu-id="5897c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5897c-102">SYNOPSIS</span></span>
<span data-ttu-id="5897c-103">Rimuovere i nodi dal tipo di nodo specifico da un cluster.</span><span class="sxs-lookup"><span data-stu-id="5897c-103">Remove nodes from the specific node type from a cluster.</span></span>

## <span data-ttu-id="5897c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5897c-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5897c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5897c-105">DESCRIPTION</span></span>
<span data-ttu-id="5897c-106">Usare **Remove-AzServiceFabricNode** per rimuovere i nodi da un tipo di nodo specifico da un cluster.</span><span class="sxs-lookup"><span data-stu-id="5897c-106">Use **Remove-AzServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="5897c-107">La rimozione procede solo se soddisfa le metriche di integrità dei cluster.</span><span class="sxs-lookup"><span data-stu-id="5897c-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="5897c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5897c-108">EXAMPLES</span></span>

### <span data-ttu-id="5897c-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5897c-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="5897c-110">Questo comando rimuove 2 nodi da NodeType 'nt1'.</span><span class="sxs-lookup"><span data-stu-id="5897c-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="5897c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5897c-111">PARAMETERS</span></span>

### <span data-ttu-id="5897c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5897c-112">-DefaultProfile</span></span>
<span data-ttu-id="5897c-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5897c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5897c-114">-Name</span><span class="sxs-lookup"><span data-stu-id="5897c-114">-Name</span></span>
<span data-ttu-id="5897c-115">Specificare il nome del cluster</span><span class="sxs-lookup"><span data-stu-id="5897c-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="5897c-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="5897c-116">-NodeType</span></span>
<span data-ttu-id="5897c-117">Nome del tipo di nodo</span><span class="sxs-lookup"><span data-stu-id="5897c-117">Node type name</span></span>

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

### <span data-ttu-id="5897c-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="5897c-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="5897c-119">Il numero di nodi da aggiungere</span><span class="sxs-lookup"><span data-stu-id="5897c-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="5897c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5897c-120">-ResourceGroupName</span></span>
<span data-ttu-id="5897c-121">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5897c-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="5897c-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5897c-122">-Confirm</span></span>
<span data-ttu-id="5897c-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5897c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5897c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5897c-124">-WhatIf</span></span>
<span data-ttu-id="5897c-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5897c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5897c-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5897c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5897c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5897c-127">CommonParameters</span></span>
<span data-ttu-id="5897c-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5897c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5897c-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5897c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5897c-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="5897c-130">INPUTS</span></span>

### <span data-ttu-id="5897c-131">System.Int32</span><span class="sxs-lookup"><span data-stu-id="5897c-131">System.Int32</span></span>

### <span data-ttu-id="5897c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5897c-132">System.String</span></span>

## <span data-ttu-id="5897c-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5897c-133">OUTPUTS</span></span>

### <span data-ttu-id="5897c-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="5897c-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="5897c-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="5897c-135">NOTES</span></span>

## <span data-ttu-id="5897c-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5897c-136">RELATED LINKS</span></span>

[<span data-ttu-id="5897c-137">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="5897c-137">Add-AzServiceFabricNode</span></span>](./Add-AzServiceFabricNode.md)
