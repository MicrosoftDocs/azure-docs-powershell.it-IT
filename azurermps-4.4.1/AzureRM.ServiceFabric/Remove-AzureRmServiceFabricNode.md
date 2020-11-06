---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
ms.openlocfilehash: cbf23af4c98e8174091b467e6e05ed5de6ae20c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512939"
---
# <span data-ttu-id="49d0c-101">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="49d0c-101">Remove-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="49d0c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="49d0c-102">SYNOPSIS</span></span>
<span data-ttu-id="49d0c-103">Rimuovere i nodi dal tipo di nodo specifico da un cluster.</span><span class="sxs-lookup"><span data-stu-id="49d0c-103">Remove nodes from the specific node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49d0c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49d0c-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNode [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -NumberOfNodesToRemove <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="49d0c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49d0c-105">DESCRIPTION</span></span>
<span data-ttu-id="49d0c-106">USA **Remove-AzureRmServiceFabricNode** per rimuovere i nodi da un tipo di nodo specifico da un cluster.</span><span class="sxs-lookup"><span data-stu-id="49d0c-106">Use **Remove-AzureRmServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="49d0c-107">La rimozione procede solo se soddisfa le metriche di integrità del cluster.</span><span class="sxs-lookup"><span data-stu-id="49d0c-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="49d0c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49d0c-108">EXAMPLES</span></span>

### <span data-ttu-id="49d0c-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="49d0c-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="49d0c-110">Questo comando consente di rimuovere 2 nodi da NodeType ' NT1'.</span><span class="sxs-lookup"><span data-stu-id="49d0c-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="49d0c-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="49d0c-111">PARAMETERS</span></span>

### <span data-ttu-id="49d0c-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="49d0c-112">-Name</span></span>
<span data-ttu-id="49d0c-113">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="49d0c-113">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="49d0c-114">-NodeType</span><span class="sxs-lookup"><span data-stu-id="49d0c-114">-NodeType</span></span>
<span data-ttu-id="49d0c-115">Nome tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="49d0c-115">Node type name.</span></span>

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

### <span data-ttu-id="49d0c-116">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="49d0c-116">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="49d0c-117">Numero di nodi da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="49d0c-117">Number of nodes to remove.</span></span>

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

### <span data-ttu-id="49d0c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49d0c-118">-ResourceGroupName</span></span>
<span data-ttu-id="49d0c-119">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="49d0c-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="49d0c-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="49d0c-120">-Confirm</span></span>
<span data-ttu-id="49d0c-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49d0c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49d0c-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49d0c-122">-WhatIf</span></span>
<span data-ttu-id="49d0c-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="49d0c-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49d0c-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="49d0c-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49d0c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49d0c-125">-DefaultProfile</span></span>
<span data-ttu-id="49d0c-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="49d0c-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49d0c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49d0c-127">CommonParameters</span></span>
<span data-ttu-id="49d0c-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49d0c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49d0c-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49d0c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49d0c-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="49d0c-130">INPUTS</span></span>

### <span data-ttu-id="49d0c-131">System. Int32</span><span class="sxs-lookup"><span data-stu-id="49d0c-131">System.Int32</span></span>
<span data-ttu-id="49d0c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="49d0c-132">System.String</span></span>

## <span data-ttu-id="49d0c-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49d0c-133">OUTPUTS</span></span>

### <span data-ttu-id="49d0c-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="49d0c-134">System.Object</span></span>

## <span data-ttu-id="49d0c-135">Note</span><span class="sxs-lookup"><span data-stu-id="49d0c-135">NOTES</span></span>

## <span data-ttu-id="49d0c-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49d0c-136">RELATED LINKS</span></span>

[<span data-ttu-id="49d0c-137">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="49d0c-137">Add-AzureRmServiceFabricNode</span></span>](./Add-AzureRmServiceFabricNode.md) 
