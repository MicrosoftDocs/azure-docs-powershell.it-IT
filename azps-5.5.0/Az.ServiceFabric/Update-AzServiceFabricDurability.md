---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
ms.openlocfilehash: 1a0da9869ccfdc6b8344240a8367a4c8dfcd2350
ms.sourcegitcommit: 608289d079b819df2b8d1a2f7935cc500367a312
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "101684892"
---
# <span data-ttu-id="7786a-101">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="7786a-101">Update-AzServiceFabricDurability</span></span>

## <span data-ttu-id="7786a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7786a-102">SYNOPSIS</span></span>
<span data-ttu-id="7786a-103">Aggiornare il livello di durabilità o VmSKU di un tipo di nodo nel cluster.</span><span class="sxs-lookup"><span data-stu-id="7786a-103">Update the durability tier or VmSku of a node type in the cluster.</span></span> <span data-ttu-id="7786a-104">Inoltre aggiornerà il livello di durabilità nell'estensione Service Fabric VM nel set di scala delle macchine virtuali associato.</span><span class="sxs-lookup"><span data-stu-id="7786a-104">It will also update the durability tier in the Service Fabric VM extension on the associated Virtual Machine Scale Set.</span></span>

## <span data-ttu-id="7786a-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7786a-105">SYNTAX</span></span>

```
Update-AzServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7786a-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7786a-106">DESCRIPTION</span></span>
<span data-ttu-id="7786a-107">Usare **Update-AzServiceFabricDurability per** aggiornare la durabilità o SKU del cluster.</span><span class="sxs-lookup"><span data-stu-id="7786a-107">Use **Update-AzServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="7786a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7786a-108">EXAMPLES</span></span>

### <span data-ttu-id="7786a-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7786a-109">Example 1</span></span>
```
PS c:> Update-AzServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="7786a-110">Questo comando modifica il livello di durata del nodeType 'nt1' in silver.</span><span class="sxs-lookup"><span data-stu-id="7786a-110">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="7786a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7786a-111">PARAMETERS</span></span>

### <span data-ttu-id="7786a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7786a-112">-DefaultProfile</span></span>
<span data-ttu-id="7786a-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7786a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7786a-114">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="7786a-114">-DurabilityLevel</span></span>
<span data-ttu-id="7786a-115">Specificare il livello di durabilità.</span><span class="sxs-lookup"><span data-stu-id="7786a-115">Specify durability level.</span></span>

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

### <span data-ttu-id="7786a-116">-Name</span><span class="sxs-lookup"><span data-stu-id="7786a-116">-Name</span></span>
<span data-ttu-id="7786a-117">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="7786a-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="7786a-118">-NodeType</span><span class="sxs-lookup"><span data-stu-id="7786a-118">-NodeType</span></span>
<span data-ttu-id="7786a-119">Specificare il nome del tipo di nodo Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="7786a-119">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="7786a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7786a-120">-ResourceGroupName</span></span>
<span data-ttu-id="7786a-121">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7786a-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7786a-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="7786a-122">-Sku</span></span>
<span data-ttu-id="7786a-123">Specificare lo SKU del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="7786a-123">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="7786a-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7786a-124">-Confirm</span></span>
<span data-ttu-id="7786a-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7786a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7786a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7786a-126">-WhatIf</span></span>
<span data-ttu-id="7786a-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7786a-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7786a-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7786a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7786a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7786a-129">CommonParameters</span></span>
<span data-ttu-id="7786a-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7786a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7786a-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7786a-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7786a-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="7786a-132">INPUTS</span></span>

### <span data-ttu-id="7786a-133">System.String</span><span class="sxs-lookup"><span data-stu-id="7786a-133">System.String</span></span>

### <span data-ttu-id="7786a-134">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="7786a-134">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="7786a-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7786a-135">OUTPUTS</span></span>

### <span data-ttu-id="7786a-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="7786a-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="7786a-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="7786a-137">NOTES</span></span>

## <span data-ttu-id="7786a-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7786a-138">RELATED LINKS</span></span>
