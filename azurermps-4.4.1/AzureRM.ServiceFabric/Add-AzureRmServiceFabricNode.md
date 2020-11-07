---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
ms.openlocfilehash: aca27be11fde78df8abad1d7cdcfeff4232b60d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687077"
---
# <span data-ttu-id="4d557-101">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="4d557-101">Add-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="4d557-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4d557-102">SYNOPSIS</span></span>
<span data-ttu-id="4d557-103">Aggiungere nodi al tipo di nodo specifico nel cluster.</span><span class="sxs-lookup"><span data-stu-id="4d557-103">Add nodes to the specific node type in the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d557-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d557-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNode [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -NumberOfNodesToAdd <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d557-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d557-105">DESCRIPTION</span></span>
<span data-ttu-id="4d557-106">USA **Add-AzureRmServiceFabricNode** per aggiungere nodi al tipo di nodo specifico.</span><span class="sxs-lookup"><span data-stu-id="4d557-106">Use **Add-AzureRmServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="4d557-107">Devi solo specificare il numero di nodi che vuoi aggiungere a un tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="4d557-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="4d557-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d557-108">EXAMPLES</span></span>

### <span data-ttu-id="4d557-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4d557-109">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="4d557-110">Questo comando aggiungerà 2 nodi al tipo di nodo "N1".</span><span class="sxs-lookup"><span data-stu-id="4d557-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="4d557-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4d557-111">PARAMETERS</span></span>

### <span data-ttu-id="4d557-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="4d557-112">-Name</span></span>
<span data-ttu-id="4d557-113">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="4d557-113">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="4d557-114">-NodeType</span><span class="sxs-lookup"><span data-stu-id="4d557-114">-NodeType</span></span>
<span data-ttu-id="4d557-115">Nome tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="4d557-115">Node type name.</span></span>

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

### <span data-ttu-id="4d557-116">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="4d557-116">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="4d557-117">Numero di istanza VM.</span><span class="sxs-lookup"><span data-stu-id="4d557-117">VM instance number.</span></span>

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

### <span data-ttu-id="4d557-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d557-118">-ResourceGroupName</span></span>
<span data-ttu-id="4d557-119">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4d557-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="4d557-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4d557-120">-Confirm</span></span>
<span data-ttu-id="4d557-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d557-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d557-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d557-122">-WhatIf</span></span>
<span data-ttu-id="4d557-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d557-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d557-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d557-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d557-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d557-125">-DefaultProfile</span></span>
<span data-ttu-id="4d557-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4d557-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d557-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d557-127">CommonParameters</span></span>
<span data-ttu-id="4d557-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d557-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d557-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d557-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d557-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4d557-130">INPUTS</span></span>

### <span data-ttu-id="4d557-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4d557-131">System.String</span></span>

## <span data-ttu-id="4d557-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d557-132">OUTPUTS</span></span>

### <span data-ttu-id="4d557-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="4d557-133">System.Object</span></span>

## <span data-ttu-id="4d557-134">Note</span><span class="sxs-lookup"><span data-stu-id="4d557-134">NOTES</span></span>

## <span data-ttu-id="4d557-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d557-135">RELATED LINKS</span></span>

[<span data-ttu-id="4d557-136">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="4d557-136">Remove-AzureRmServiceFabricNode</span></span>](./Remove-AzureRmServiceFabricNode.md)
