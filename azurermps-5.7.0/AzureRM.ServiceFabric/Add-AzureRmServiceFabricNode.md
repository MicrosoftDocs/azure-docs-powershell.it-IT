---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
ms.openlocfilehash: af8f5d38777674d761b8b55c649b048c933f2c66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514107"
---
# <span data-ttu-id="da756-101">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="da756-101">Add-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="da756-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="da756-102">SYNOPSIS</span></span>
<span data-ttu-id="da756-103">Aggiungere nodi al tipo di nodo specifico nel cluster.</span><span class="sxs-lookup"><span data-stu-id="da756-103">Add nodes to the specific node type in the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da756-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da756-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da756-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da756-105">DESCRIPTION</span></span>
<span data-ttu-id="da756-106">USA **Add-AzureRmServiceFabricNode** per aggiungere nodi al tipo di nodo specifico.</span><span class="sxs-lookup"><span data-stu-id="da756-106">Use **Add-AzureRmServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="da756-107">Devi solo specificare il numero di nodi che vuoi aggiungere a un tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="da756-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="da756-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da756-108">EXAMPLES</span></span>

### <span data-ttu-id="da756-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="da756-109">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="da756-110">Questo comando aggiungerà 2 nodi al tipo di nodo "N1".</span><span class="sxs-lookup"><span data-stu-id="da756-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="da756-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="da756-111">PARAMETERS</span></span>

### <span data-ttu-id="da756-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da756-112">-DefaultProfile</span></span>
<span data-ttu-id="da756-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="da756-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da756-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="da756-114">-Name</span></span>
<span data-ttu-id="da756-115">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="da756-115">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da756-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="da756-116">-NodeType</span></span>
<span data-ttu-id="da756-117">Nome tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="da756-117">Node type name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da756-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="da756-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="da756-119">Numero di istanza VM.</span><span class="sxs-lookup"><span data-stu-id="da756-119">VM instance number.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Number

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da756-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da756-120">-ResourceGroupName</span></span>
<span data-ttu-id="da756-121">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="da756-121">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da756-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="da756-122">-Confirm</span></span>
<span data-ttu-id="da756-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da756-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da756-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da756-124">-WhatIf</span></span>
<span data-ttu-id="da756-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da756-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da756-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da756-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da756-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da756-127">CommonParameters</span></span>
<span data-ttu-id="da756-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da756-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da756-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da756-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da756-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="da756-130">INPUTS</span></span>

### <span data-ttu-id="da756-131">System. String</span><span class="sxs-lookup"><span data-stu-id="da756-131">System.String</span></span>

## <span data-ttu-id="da756-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da756-132">OUTPUTS</span></span>

### <span data-ttu-id="da756-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="da756-133">System.Object</span></span>

## <span data-ttu-id="da756-134">Note</span><span class="sxs-lookup"><span data-stu-id="da756-134">NOTES</span></span>

## <span data-ttu-id="da756-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da756-135">RELATED LINKS</span></span>

[<span data-ttu-id="da756-136">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="da756-136">Remove-AzureRmServiceFabricNode</span></span>](./Remove-AzureRmServiceFabricNode.md)