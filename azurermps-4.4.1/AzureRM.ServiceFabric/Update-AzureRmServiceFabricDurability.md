---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
ms.openlocfilehash: b056e5328c24270df6a95e33b079e7b907f29fa3
ms.sourcegitcommit: 608289d079b819df2b8d1a2f7935cc500367a312
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "101685021"
---
# <span data-ttu-id="b60e8-101">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="b60e8-101">Update-AzureRmServiceFabricDurability</span></span>

## <span data-ttu-id="b60e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b60e8-102">SYNOPSIS</span></span>
<span data-ttu-id="b60e8-103">Aggiornare il livello di durabilità o VmSKU di un tipo di nodo nel cluster.</span><span class="sxs-lookup"><span data-stu-id="b60e8-103">Update the durability tier or VmSku of a node type in the cluster.</span></span> <span data-ttu-id="b60e8-104">Inoltre aggiornerà il livello di durabilità nell'estensione Service Fabric VM nel set di scala delle macchine virtuali associato.</span><span class="sxs-lookup"><span data-stu-id="b60e8-104">It will also update the durability tier in the Service Fabric VM extension on the associated Virtual Machine Scale Set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b60e8-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b60e8-105">SYNTAX</span></span>

```
Update-AzureRmServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b60e8-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b60e8-106">DESCRIPTION</span></span>
<span data-ttu-id="b60e8-107">Usare **Update-AzureRmServiceFabricDurability per** aggiornare la durabilità o SKU del cluster.</span><span class="sxs-lookup"><span data-stu-id="b60e8-107">Use **Update-AzureRmServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="b60e8-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b60e8-108">EXAMPLES</span></span>

### <span data-ttu-id="b60e8-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b60e8-109">Example 1</span></span>
```
PS c:> Update-AzureRmServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="b60e8-110">Questo comando modifica il livello di durata del nodeType 'nt1' in silver.</span><span class="sxs-lookup"><span data-stu-id="b60e8-110">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="b60e8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b60e8-111">PARAMETERS</span></span>

### <span data-ttu-id="b60e8-112">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="b60e8-112">-DurabilityLevel</span></span>
<span data-ttu-id="b60e8-113">Specificare il livello di durabilità.</span><span class="sxs-lookup"><span data-stu-id="b60e8-113">Specify durability level.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: Bronze, Silver, Gold

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b60e8-114">-Name</span><span class="sxs-lookup"><span data-stu-id="b60e8-114">-Name</span></span>
<span data-ttu-id="b60e8-115">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="b60e8-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="b60e8-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="b60e8-116">-NodeType</span></span>
<span data-ttu-id="b60e8-117">Specificare il nome del tipo di nodo Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="b60e8-117">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="b60e8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b60e8-118">-ResourceGroupName</span></span>
<span data-ttu-id="b60e8-119">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b60e8-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b60e8-120">-SKU</span><span class="sxs-lookup"><span data-stu-id="b60e8-120">-Sku</span></span>
<span data-ttu-id="b60e8-121">Specificare lo SKU del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="b60e8-121">Specify the SKU of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b60e8-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b60e8-122">-Confirm</span></span>
<span data-ttu-id="b60e8-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b60e8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b60e8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b60e8-124">-WhatIf</span></span>
<span data-ttu-id="b60e8-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b60e8-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b60e8-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b60e8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b60e8-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b60e8-127">-DefaultProfile</span></span>
<span data-ttu-id="b60e8-128">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b60e8-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b60e8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b60e8-129">CommonParameters</span></span>
<span data-ttu-id="b60e8-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b60e8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b60e8-131">Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b60e8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b60e8-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="b60e8-132">INPUTS</span></span>

### <span data-ttu-id="b60e8-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="b60e8-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>
<span data-ttu-id="b60e8-134">System.String</span><span class="sxs-lookup"><span data-stu-id="b60e8-134">System.String</span></span>

## <span data-ttu-id="b60e8-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b60e8-135">OUTPUTS</span></span>

### <span data-ttu-id="b60e8-136">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span><span class="sxs-lookup"><span data-stu-id="b60e8-136">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="b60e8-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="b60e8-137">NOTES</span></span>

## <span data-ttu-id="b60e8-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b60e8-138">RELATED LINKS</span></span>

