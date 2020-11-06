---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: f825d1ba1621a00be6196219d99dc188496ea5da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509612"
---
# <span data-ttu-id="9eb9d-101">Remove-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="9eb9d-101">Remove-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="9eb9d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9eb9d-102">SYNOPSIS</span></span>
<span data-ttu-id="9eb9d-103">Rimuovere un tipo di nodo completo da un cluster.</span><span class="sxs-lookup"><span data-stu-id="9eb9d-103">Remove a complete node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9eb9d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9eb9d-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9eb9d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9eb9d-105">DESCRIPTION</span></span>
<span data-ttu-id="9eb9d-106">Usa il **Remove-AzureRmServiceFabricNodeType** per rimuovere tutti i nodi da un tipo di nodo specifico e il tipo di nodo da un cluster.</span><span class="sxs-lookup"><span data-stu-id="9eb9d-106">Use the **Remove-AzureRmServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="9eb9d-107">Questo comando non può essere usato per eliminare il tipo di nodo primario.</span><span class="sxs-lookup"><span data-stu-id="9eb9d-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="9eb9d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9eb9d-108">EXAMPLES</span></span>

### <span data-ttu-id="9eb9d-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9eb9d-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="9eb9d-110">Questo comando consente di rimuovere NodeType ' NT1' dal cluster.</span><span class="sxs-lookup"><span data-stu-id="9eb9d-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="9eb9d-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9eb9d-111">PARAMETERS</span></span>

### <span data-ttu-id="9eb9d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eb9d-112">-DefaultProfile</span></span>
<span data-ttu-id="9eb9d-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9eb9d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9eb9d-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="9eb9d-114">-Name</span></span>
<span data-ttu-id="9eb9d-115">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="9eb9d-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="9eb9d-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="9eb9d-116">-NodeType</span></span>
<span data-ttu-id="9eb9d-117">Nome del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="9eb9d-117">The node type name.</span></span>

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

### <span data-ttu-id="9eb9d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eb9d-118">-ResourceGroupName</span></span>
<span data-ttu-id="9eb9d-119">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9eb9d-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="9eb9d-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9eb9d-120">-Confirm</span></span>
<span data-ttu-id="9eb9d-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9eb9d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9eb9d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9eb9d-122">-WhatIf</span></span>
<span data-ttu-id="9eb9d-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9eb9d-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9eb9d-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9eb9d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9eb9d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eb9d-125">CommonParameters</span></span>
<span data-ttu-id="9eb9d-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9eb9d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eb9d-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9eb9d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eb9d-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9eb9d-128">INPUTS</span></span>

### <span data-ttu-id="9eb9d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9eb9d-129">System.String</span></span>

## <span data-ttu-id="9eb9d-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9eb9d-130">OUTPUTS</span></span>

### <span data-ttu-id="9eb9d-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="9eb9d-131">System.Object</span></span>

## <span data-ttu-id="9eb9d-132">Note</span><span class="sxs-lookup"><span data-stu-id="9eb9d-132">NOTES</span></span>

## <span data-ttu-id="9eb9d-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9eb9d-133">RELATED LINKS</span></span>
