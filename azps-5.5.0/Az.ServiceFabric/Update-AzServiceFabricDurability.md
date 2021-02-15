---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
ms.openlocfilehash: 1a406ad937a545c9b2599966909809c7552ad7db
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189063"
---
# <span data-ttu-id="5d4c1-101">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="5d4c1-101">Update-AzServiceFabricDurability</span></span>

## <span data-ttu-id="5d4c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d4c1-102">SYNOPSIS</span></span>
<span data-ttu-id="5d4c1-103">Aggiornare il livello di durabilità o VmSKU di un tipo di nodo nel cluster.</span><span class="sxs-lookup"><span data-stu-id="5d4c1-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

## <span data-ttu-id="5d4c1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5d4c1-104">SYNTAX</span></span>

```
Update-AzServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d4c1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5d4c1-105">DESCRIPTION</span></span>
<span data-ttu-id="5d4c1-106">Usare **Update-AzServiceFabricDurability per** aggiornare la durabilità o SKU del cluster.</span><span class="sxs-lookup"><span data-stu-id="5d4c1-106">Use **Update-AzServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="5d4c1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5d4c1-107">EXAMPLES</span></span>

### <span data-ttu-id="5d4c1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5d4c1-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="5d4c1-109">Questo comando modifica il livello di durabilità di NodeType 'nt1' in Silver.</span><span class="sxs-lookup"><span data-stu-id="5d4c1-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="5d4c1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d4c1-110">PARAMETERS</span></span>

### <span data-ttu-id="5d4c1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d4c1-111">-DefaultProfile</span></span>
<span data-ttu-id="5d4c1-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5d4c1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d4c1-113">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="5d4c1-113">-DurabilityLevel</span></span>
<span data-ttu-id="5d4c1-114">Specificare il livello di durabilità.</span><span class="sxs-lookup"><span data-stu-id="5d4c1-114">Specify durability level.</span></span>

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

### <span data-ttu-id="5d4c1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5d4c1-115">-Name</span></span>
<span data-ttu-id="5d4c1-116">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="5d4c1-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="5d4c1-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="5d4c1-117">-NodeType</span></span>
<span data-ttu-id="5d4c1-118">Specificare il nome del tipo di nodo Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="5d4c1-118">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="5d4c1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d4c1-119">-ResourceGroupName</span></span>
<span data-ttu-id="5d4c1-120">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5d4c1-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="5d4c1-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="5d4c1-121">-Sku</span></span>
<span data-ttu-id="5d4c1-122">Specificare lo SKU del tipo di nodo.</span><span class="sxs-lookup"><span data-stu-id="5d4c1-122">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="5d4c1-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d4c1-123">-Confirm</span></span>
<span data-ttu-id="5d4c1-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d4c1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d4c1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d4c1-125">-WhatIf</span></span>
<span data-ttu-id="5d4c1-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5d4c1-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5d4c1-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5d4c1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d4c1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d4c1-128">CommonParameters</span></span>
<span data-ttu-id="5d4c1-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d4c1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d4c1-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5d4c1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d4c1-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="5d4c1-131">INPUTS</span></span>

### <span data-ttu-id="5d4c1-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5d4c1-132">System.String</span></span>

### <span data-ttu-id="5d4c1-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="5d4c1-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="5d4c1-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5d4c1-134">OUTPUTS</span></span>

### <span data-ttu-id="5d4c1-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="5d4c1-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="5d4c1-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="5d4c1-136">NOTES</span></span>

## <span data-ttu-id="5d4c1-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5d4c1-137">RELATED LINKS</span></span>
