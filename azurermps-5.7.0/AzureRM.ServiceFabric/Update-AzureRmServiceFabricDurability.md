---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/update-azurermservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
ms.openlocfilehash: 9c82f0aab38fb5479f5344166a409b9b32f7447c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519357"
---
# <span data-ttu-id="7c2cb-101">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="7c2cb-101">Update-AzureRmServiceFabricDurability</span></span>

## <span data-ttu-id="7c2cb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7c2cb-102">SYNOPSIS</span></span>
<span data-ttu-id="7c2cb-103">Aggiornare il livello di durabilità o VmSku di un tipo di nodo nel cluster.</span><span class="sxs-lookup"><span data-stu-id="7c2cb-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c2cb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c2cb-104">SYNTAX</span></span>

```
Update-AzureRmServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c2cb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c2cb-105">DESCRIPTION</span></span>
<span data-ttu-id="7c2cb-106">Usare **Update-AzureRmServiceFabricDurability** per aggiornare la durabilità o il SKU del cluster.</span><span class="sxs-lookup"><span data-stu-id="7c2cb-106">Use **Update-AzureRmServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="7c2cb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c2cb-107">EXAMPLES</span></span>

### <span data-ttu-id="7c2cb-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7c2cb-108">Example 1</span></span>
```
PS c:> Update-AzureRmServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="7c2cb-109">Questo comando modifica il livello di durabilità di NodeType ' NT1' in Silver.</span><span class="sxs-lookup"><span data-stu-id="7c2cb-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="7c2cb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7c2cb-110">PARAMETERS</span></span>

### <span data-ttu-id="7c2cb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c2cb-111">-DefaultProfile</span></span>
<span data-ttu-id="7c2cb-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c2cb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c2cb-113">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="7c2cb-113">-DurabilityLevel</span></span>
<span data-ttu-id="7c2cb-114">Specificare il livello di durabilità.</span><span class="sxs-lookup"><span data-stu-id="7c2cb-114">Specify durability level.</span></span>

```yaml
Type: DurabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: Bronze, Silver, Gold

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c2cb-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="7c2cb-115">-Name</span></span>
<span data-ttu-id="7c2cb-116">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="7c2cb-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="7c2cb-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="7c2cb-117">-NodeType</span></span>
<span data-ttu-id="7c2cb-118">Specificare il nome del tipo di nodo Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="7c2cb-118">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="7c2cb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c2cb-119">-ResourceGroupName</span></span>
<span data-ttu-id="7c2cb-120">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7c2cb-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7c2cb-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="7c2cb-121">-Sku</span></span>
<span data-ttu-id="7c2cb-122">Specificare l'USK del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="7c2cb-122">Specify the SKU of the node type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c2cb-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7c2cb-123">-Confirm</span></span>
<span data-ttu-id="7c2cb-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c2cb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c2cb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c2cb-125">-WhatIf</span></span>
<span data-ttu-id="7c2cb-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c2cb-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c2cb-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c2cb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c2cb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c2cb-128">CommonParameters</span></span>
<span data-ttu-id="7c2cb-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c2cb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c2cb-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c2cb-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c2cb-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7c2cb-131">INPUTS</span></span>

### <span data-ttu-id="7c2cb-132">Microsoft. Azure. Commands. ServiceFabric. Models. DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="7c2cb-132">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>
<span data-ttu-id="7c2cb-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7c2cb-133">System.String</span></span>

## <span data-ttu-id="7c2cb-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c2cb-134">OUTPUTS</span></span>

### <span data-ttu-id="7c2cb-135">Microsoft. Azure. Commands. ServiceFabric. Models. PsCluster</span><span class="sxs-lookup"><span data-stu-id="7c2cb-135">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="7c2cb-136">Note</span><span class="sxs-lookup"><span data-stu-id="7c2cb-136">NOTES</span></span>

## <span data-ttu-id="7c2cb-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c2cb-137">RELATED LINKS</span></span>

