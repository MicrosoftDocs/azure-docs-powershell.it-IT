---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
ms.openlocfilehash: 22aa963f772a87b97a0a64ccdaef5ad6ef004696
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677068"
---
# <span data-ttu-id="6fb30-101">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="6fb30-101">Remove-AzServiceFabricNode</span></span>

## <span data-ttu-id="6fb30-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6fb30-102">SYNOPSIS</span></span>
<span data-ttu-id="6fb30-103">Rimuovere i nodi dal tipo di nodo specifico da un cluster.</span><span class="sxs-lookup"><span data-stu-id="6fb30-103">Remove nodes from the specific node type from a cluster.</span></span>

## <span data-ttu-id="6fb30-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6fb30-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fb30-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6fb30-105">DESCRIPTION</span></span>
<span data-ttu-id="6fb30-106">USA **Remove-AzServiceFabricNode** per rimuovere i nodi da un tipo di nodo specifico da un cluster.</span><span class="sxs-lookup"><span data-stu-id="6fb30-106">Use **Remove-AzServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="6fb30-107">La rimozione procede solo se soddisfa le metriche di integrità del cluster.</span><span class="sxs-lookup"><span data-stu-id="6fb30-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="6fb30-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6fb30-108">EXAMPLES</span></span>

### <span data-ttu-id="6fb30-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6fb30-109">Example 1</span></span>
```
PS c:> Remove-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="6fb30-110">Questo comando consente di rimuovere 2 nodi da NodeType ' NT1'.</span><span class="sxs-lookup"><span data-stu-id="6fb30-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="6fb30-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6fb30-111">PARAMETERS</span></span>

### <span data-ttu-id="6fb30-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fb30-112">-DefaultProfile</span></span>
<span data-ttu-id="6fb30-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6fb30-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fb30-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="6fb30-114">-Name</span></span>
<span data-ttu-id="6fb30-115">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="6fb30-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="6fb30-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="6fb30-116">-NodeType</span></span>
<span data-ttu-id="6fb30-117">Nome tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="6fb30-117">Node type name.</span></span>

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

### <span data-ttu-id="6fb30-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="6fb30-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="6fb30-119">Numero di nodi da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6fb30-119">Number of nodes to remove.</span></span>

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

### <span data-ttu-id="6fb30-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fb30-120">-ResourceGroupName</span></span>
<span data-ttu-id="6fb30-121">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6fb30-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="6fb30-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6fb30-122">-Confirm</span></span>
<span data-ttu-id="6fb30-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fb30-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fb30-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fb30-124">-WhatIf</span></span>
<span data-ttu-id="6fb30-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6fb30-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6fb30-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6fb30-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fb30-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fb30-127">CommonParameters</span></span>
<span data-ttu-id="6fb30-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fb30-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fb30-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fb30-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fb30-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6fb30-130">INPUTS</span></span>

### <span data-ttu-id="6fb30-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="6fb30-131">System.Int32</span></span>

### <span data-ttu-id="6fb30-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6fb30-132">System.String</span></span>

## <span data-ttu-id="6fb30-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6fb30-133">OUTPUTS</span></span>

### <span data-ttu-id="6fb30-134">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="6fb30-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="6fb30-135">Note</span><span class="sxs-lookup"><span data-stu-id="6fb30-135">NOTES</span></span>

## <span data-ttu-id="6fb30-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6fb30-136">RELATED LINKS</span></span>

[<span data-ttu-id="6fb30-137">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="6fb30-137">Add-AzServiceFabricNode</span></span>](./Add-AzServiceFabricNode.md) 
