---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
ms.openlocfilehash: 578210490d92e272e3e4867fb7f96f40a1a39782
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520612"
---
# <span data-ttu-id="0d566-101">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="0d566-101">Remove-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="0d566-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0d566-102">SYNOPSIS</span></span>
<span data-ttu-id="0d566-103">Rimuovere i nodi dal tipo di nodo specifico da un cluster.</span><span class="sxs-lookup"><span data-stu-id="0d566-103">Remove nodes from the specific node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d566-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0d566-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d566-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d566-105">DESCRIPTION</span></span>
<span data-ttu-id="0d566-106">USA **Remove-AzureRmServiceFabricNode** per rimuovere i nodi da un tipo di nodo specifico da un cluster.</span><span class="sxs-lookup"><span data-stu-id="0d566-106">Use **Remove-AzureRmServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="0d566-107">La rimozione procede solo se soddisfa le metriche di integrità del cluster.</span><span class="sxs-lookup"><span data-stu-id="0d566-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="0d566-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0d566-108">EXAMPLES</span></span>

### <span data-ttu-id="0d566-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0d566-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="0d566-110">Questo comando consente di rimuovere 2 nodi da NodeType ' NT1'.</span><span class="sxs-lookup"><span data-stu-id="0d566-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="0d566-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0d566-111">PARAMETERS</span></span>

### <span data-ttu-id="0d566-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d566-112">-DefaultProfile</span></span>
<span data-ttu-id="0d566-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0d566-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d566-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="0d566-114">-Name</span></span>
<span data-ttu-id="0d566-115">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="0d566-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="0d566-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="0d566-116">-NodeType</span></span>
<span data-ttu-id="0d566-117">Nome tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="0d566-117">Node type name.</span></span>

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

### <span data-ttu-id="0d566-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="0d566-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="0d566-119">Numero di nodi da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="0d566-119">Number of nodes to remove.</span></span>

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

### <span data-ttu-id="0d566-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d566-120">-ResourceGroupName</span></span>
<span data-ttu-id="0d566-121">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0d566-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="0d566-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0d566-122">-Confirm</span></span>
<span data-ttu-id="0d566-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d566-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d566-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d566-124">-WhatIf</span></span>
<span data-ttu-id="0d566-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0d566-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d566-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0d566-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d566-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d566-127">CommonParameters</span></span>
<span data-ttu-id="0d566-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d566-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d566-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d566-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d566-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0d566-130">INPUTS</span></span>

### <span data-ttu-id="0d566-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="0d566-131">System.Int32</span></span>
<span data-ttu-id="0d566-132">Parametri: NumberOfNodesToRemove (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0d566-132">Parameters: NumberOfNodesToRemove (ByValue)</span></span>

### <span data-ttu-id="0d566-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0d566-133">System.String</span></span>
<span data-ttu-id="0d566-134">Parametri: NodeType (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0d566-134">Parameters: NodeType (ByValue)</span></span>

## <span data-ttu-id="0d566-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0d566-135">OUTPUTS</span></span>

### <span data-ttu-id="0d566-136">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="0d566-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="0d566-137">Note</span><span class="sxs-lookup"><span data-stu-id="0d566-137">NOTES</span></span>

## <span data-ttu-id="0d566-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0d566-138">RELATED LINKS</span></span>

[<span data-ttu-id="0d566-139">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="0d566-139">Add-AzureRmServiceFabricNode</span></span>](./Add-AzureRmServiceFabricNode.md) 
