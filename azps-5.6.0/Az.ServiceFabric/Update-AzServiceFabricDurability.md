---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/update-azservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
ms.openlocfilehash: 40ac27339faf2915ccc88c3bbd5f0a39581af743
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955549"
---
# <span data-ttu-id="c5ecc-101">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="c5ecc-101">Update-AzServiceFabricDurability</span></span>

## <span data-ttu-id="c5ecc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5ecc-102">SYNOPSIS</span></span>
<span data-ttu-id="c5ecc-103">Aggiornare il livello di durabilità o VmSKU di un tipo di nodo nel cluster.</span><span class="sxs-lookup"><span data-stu-id="c5ecc-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

## <span data-ttu-id="c5ecc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5ecc-104">SYNTAX</span></span>

```
Update-AzServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5ecc-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c5ecc-105">DESCRIPTION</span></span>
<span data-ttu-id="c5ecc-106">Usare **Update-AzServiceFabricDurability per** aggiornare la durabilità o SKU del cluster.</span><span class="sxs-lookup"><span data-stu-id="c5ecc-106">Use **Update-AzServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="c5ecc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5ecc-107">EXAMPLES</span></span>

### <span data-ttu-id="c5ecc-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c5ecc-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="c5ecc-109">Questo comando modifica il livello di durabilità di NodeType 'nt1' in Silver.</span><span class="sxs-lookup"><span data-stu-id="c5ecc-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="c5ecc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5ecc-110">PARAMETERS</span></span>

### <span data-ttu-id="c5ecc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5ecc-111">-DefaultProfile</span></span>
<span data-ttu-id="c5ecc-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c5ecc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5ecc-113">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="c5ecc-113">-DurabilityLevel</span></span>
<span data-ttu-id="c5ecc-114">Specificare il livello di durabilità.</span><span class="sxs-lookup"><span data-stu-id="c5ecc-114">Specify durability level.</span></span>

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

### <span data-ttu-id="c5ecc-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c5ecc-115">-Name</span></span>
<span data-ttu-id="c5ecc-116">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="c5ecc-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c5ecc-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="c5ecc-117">-NodeType</span></span>
<span data-ttu-id="c5ecc-118">Specificare il nome del tipo di nodo Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="c5ecc-118">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="c5ecc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5ecc-119">-ResourceGroupName</span></span>
<span data-ttu-id="c5ecc-120">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c5ecc-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c5ecc-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="c5ecc-121">-Sku</span></span>
<span data-ttu-id="c5ecc-122">Specificare lo SKU del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="c5ecc-122">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="c5ecc-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5ecc-123">-Confirm</span></span>
<span data-ttu-id="c5ecc-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5ecc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5ecc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5ecc-125">-WhatIf</span></span>
<span data-ttu-id="c5ecc-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5ecc-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c5ecc-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5ecc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5ecc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5ecc-128">CommonParameters</span></span>
<span data-ttu-id="c5ecc-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5ecc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5ecc-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c5ecc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5ecc-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="c5ecc-131">INPUTS</span></span>

### <span data-ttu-id="c5ecc-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c5ecc-132">System.String</span></span>

### <span data-ttu-id="c5ecc-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="c5ecc-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="c5ecc-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5ecc-134">OUTPUTS</span></span>

### <span data-ttu-id="c5ecc-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="c5ecc-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="c5ecc-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="c5ecc-136">NOTES</span></span>

## <span data-ttu-id="c5ecc-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5ecc-137">RELATED LINKS</span></span>
