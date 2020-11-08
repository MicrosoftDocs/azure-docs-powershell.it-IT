---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
ms.openlocfilehash: 3580315755792aaaddf3b10e185413254784a3d7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191908"
---
# <span data-ttu-id="d3fc1-101">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="d3fc1-101">Remove-AzServiceFabricNode</span></span>

## <span data-ttu-id="d3fc1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3fc1-102">SYNOPSIS</span></span>
<span data-ttu-id="d3fc1-103">Rimuovere i nodi dal tipo di nodo specifico da un cluster.</span><span class="sxs-lookup"><span data-stu-id="d3fc1-103">Remove nodes from the specific node type from a cluster.</span></span>

## <span data-ttu-id="d3fc1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3fc1-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3fc1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3fc1-105">DESCRIPTION</span></span>
<span data-ttu-id="d3fc1-106">USA **Remove-AzServiceFabricNode** per rimuovere i nodi da un tipo di nodo specifico da un cluster.</span><span class="sxs-lookup"><span data-stu-id="d3fc1-106">Use **Remove-AzServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="d3fc1-107">La rimozione procede solo se soddisfa le metriche di integrità del cluster.</span><span class="sxs-lookup"><span data-stu-id="d3fc1-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="d3fc1-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3fc1-108">EXAMPLES</span></span>

### <span data-ttu-id="d3fc1-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d3fc1-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="d3fc1-110">Questo comando consente di rimuovere 2 nodi da NodeType ' NT1'.</span><span class="sxs-lookup"><span data-stu-id="d3fc1-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="d3fc1-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3fc1-111">PARAMETERS</span></span>

### <span data-ttu-id="d3fc1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3fc1-112">-DefaultProfile</span></span>
<span data-ttu-id="d3fc1-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3fc1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3fc1-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="d3fc1-114">-Name</span></span>
<span data-ttu-id="d3fc1-115">Specificare il nome del cluster</span><span class="sxs-lookup"><span data-stu-id="d3fc1-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="d3fc1-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="d3fc1-116">-NodeType</span></span>
<span data-ttu-id="d3fc1-117">Nome tipo di nodo</span><span class="sxs-lookup"><span data-stu-id="d3fc1-117">Node type name</span></span>

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

### <span data-ttu-id="d3fc1-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="d3fc1-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="d3fc1-119">Numero di nodi da aggiungere</span><span class="sxs-lookup"><span data-stu-id="d3fc1-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="d3fc1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3fc1-120">-ResourceGroupName</span></span>
<span data-ttu-id="d3fc1-121">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d3fc1-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="d3fc1-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d3fc1-122">-Confirm</span></span>
<span data-ttu-id="d3fc1-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3fc1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3fc1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3fc1-124">-WhatIf</span></span>
<span data-ttu-id="d3fc1-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3fc1-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3fc1-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3fc1-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3fc1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3fc1-127">CommonParameters</span></span>
<span data-ttu-id="d3fc1-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3fc1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3fc1-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3fc1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3fc1-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3fc1-130">INPUTS</span></span>

### <span data-ttu-id="d3fc1-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d3fc1-131">System.Int32</span></span>

### <span data-ttu-id="d3fc1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d3fc1-132">System.String</span></span>

## <span data-ttu-id="d3fc1-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3fc1-133">OUTPUTS</span></span>

### <span data-ttu-id="d3fc1-134">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="d3fc1-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="d3fc1-135">Note</span><span class="sxs-lookup"><span data-stu-id="d3fc1-135">NOTES</span></span>

## <span data-ttu-id="d3fc1-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3fc1-136">RELATED LINKS</span></span>

[<span data-ttu-id="d3fc1-137">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="d3fc1-137">Add-AzServiceFabricNode</span></span>](./Add-AzServiceFabricNode.md)
