---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/update-azurermservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
ms.openlocfilehash: aa53d34fcacca6515832eba9a6b302a4e56c7ccf
ms.sourcegitcommit: 608289d079b819df2b8d1a2f7935cc500367a312
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "101685010"
---
# <span data-ttu-id="20d99-101">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="20d99-101">Update-AzureRmServiceFabricDurability</span></span>

## <span data-ttu-id="20d99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20d99-102">SYNOPSIS</span></span>
<span data-ttu-id="20d99-103">Aggiornare il livello di durabilità o VmSKU di un tipo di nodo nel cluster.</span><span class="sxs-lookup"><span data-stu-id="20d99-103">Update the durability tier or VmSku of a node type in the cluster.</span></span> <span data-ttu-id="20d99-104">Inoltre aggiornerà il livello di durabilità nell'estensione Service Fabric VM nel set di scala delle macchine virtuali associato.</span><span class="sxs-lookup"><span data-stu-id="20d99-104">It will also update the durability tier in the Service Fabric VM extension on the associated Virtual Machine Scale Set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20d99-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="20d99-105">SYNTAX</span></span>

```
Update-AzureRmServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20d99-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="20d99-106">DESCRIPTION</span></span>
<span data-ttu-id="20d99-107">Usare **Update-AzureRmServiceFabricDurability per** aggiornare la durabilità o SKU del cluster.</span><span class="sxs-lookup"><span data-stu-id="20d99-107">Use **Update-AzureRmServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="20d99-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="20d99-108">EXAMPLES</span></span>

### <span data-ttu-id="20d99-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="20d99-109">Example 1</span></span>
```
PS c:> Update-AzureRmServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="20d99-110">Questo comando modifica il livello di durata del nodeType 'nt1' in silver.</span><span class="sxs-lookup"><span data-stu-id="20d99-110">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="20d99-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20d99-111">PARAMETERS</span></span>

### <span data-ttu-id="20d99-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20d99-112">-DefaultProfile</span></span>
<span data-ttu-id="20d99-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="20d99-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20d99-114">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="20d99-114">-DurabilityLevel</span></span>
<span data-ttu-id="20d99-115">Specificare il livello di durabilità.</span><span class="sxs-lookup"><span data-stu-id="20d99-115">Specify durability level.</span></span>

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

### <span data-ttu-id="20d99-116">-Name</span><span class="sxs-lookup"><span data-stu-id="20d99-116">-Name</span></span>
<span data-ttu-id="20d99-117">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="20d99-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="20d99-118">-NodeType</span><span class="sxs-lookup"><span data-stu-id="20d99-118">-NodeType</span></span>
<span data-ttu-id="20d99-119">Specificare il nome del tipo di nodo Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="20d99-119">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="20d99-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20d99-120">-ResourceGroupName</span></span>
<span data-ttu-id="20d99-121">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="20d99-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="20d99-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="20d99-122">-Sku</span></span>
<span data-ttu-id="20d99-123">Specificare lo SKU del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="20d99-123">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="20d99-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20d99-124">-Confirm</span></span>
<span data-ttu-id="20d99-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20d99-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20d99-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20d99-126">-WhatIf</span></span>
<span data-ttu-id="20d99-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="20d99-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20d99-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="20d99-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20d99-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20d99-129">CommonParameters</span></span>
<span data-ttu-id="20d99-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20d99-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20d99-131">Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20d99-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20d99-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="20d99-132">INPUTS</span></span>

### <span data-ttu-id="20d99-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="20d99-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>
<span data-ttu-id="20d99-134">System.String</span><span class="sxs-lookup"><span data-stu-id="20d99-134">System.String</span></span>

## <span data-ttu-id="20d99-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="20d99-135">OUTPUTS</span></span>

### <span data-ttu-id="20d99-136">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span><span class="sxs-lookup"><span data-stu-id="20d99-136">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="20d99-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="20d99-137">NOTES</span></span>

## <span data-ttu-id="20d99-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="20d99-138">RELATED LINKS</span></span>

