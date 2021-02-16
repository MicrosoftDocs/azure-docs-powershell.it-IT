---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
ms.openlocfilehash: 7a81ce555ed99de1504dc0625c0c83cdab6ab881
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189614"
---
# <span data-ttu-id="304c8-101">Remove-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="304c8-101">Remove-AzIpAllocation</span></span>

## <span data-ttu-id="304c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="304c8-102">SYNOPSIS</span></span>
<span data-ttu-id="304c8-103">Elimina una ipAllocation di Azure.</span><span class="sxs-lookup"><span data-stu-id="304c8-103">Deletes an Azure IpAllocation.</span></span>

## <span data-ttu-id="304c8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="304c8-104">SYNTAX</span></span>

### <span data-ttu-id="304c8-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="304c8-105">DeleteByNameParameterSet</span></span>
```
Remove-AzIpAllocation [-Name] <String> [-ResourceGroupName] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="304c8-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="304c8-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzIpAllocation [-InputObject] <PSTopLevelResource> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="304c8-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="304c8-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzIpAllocation [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="304c8-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="304c8-108">DESCRIPTION</span></span>
<span data-ttu-id="304c8-109">Il cmdlet **Remove-AzIpAllocation** elimina una ipAllocation di Azure</span><span class="sxs-lookup"><span data-stu-id="304c8-109">The **Remove-AzIpAllocation** cmdlet deletes an Azure IpAllocation</span></span>

## <span data-ttu-id="304c8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="304c8-110">EXAMPLES</span></span>

### <span data-ttu-id="304c8-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="304c8-111">Example 1</span></span>
```powershell
Remove-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="304c8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="304c8-112">PARAMETERS</span></span>

### <span data-ttu-id="304c8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="304c8-113">-AsJob</span></span>
<span data-ttu-id="304c8-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="304c8-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="304c8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="304c8-115">-DefaultProfile</span></span>
<span data-ttu-id="304c8-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="304c8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="304c8-117">-Force</span><span class="sxs-lookup"><span data-stu-id="304c8-117">-Force</span></span>
<span data-ttu-id="304c8-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="304c8-118">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="304c8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="304c8-119">-InputObject</span></span>
<span data-ttu-id="304c8-120">{{ Fill InputObject Description }}</span><span class="sxs-lookup"><span data-stu-id="304c8-120">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTopLevelResource
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="304c8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="304c8-121">-Name</span></span>
<span data-ttu-id="304c8-122">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="304c8-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="304c8-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="304c8-123">-PassThru</span></span>
<span data-ttu-id="304c8-124">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="304c8-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="304c8-125">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="304c8-125">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="304c8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="304c8-126">-ResourceGroupName</span></span>
<span data-ttu-id="304c8-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="304c8-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="304c8-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="304c8-128">-ResourceId</span></span>
<span data-ttu-id="304c8-129">ID risorsa IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="304c8-129">IpAllocation resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="304c8-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="304c8-130">-Confirm</span></span>
<span data-ttu-id="304c8-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="304c8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="304c8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="304c8-132">-WhatIf</span></span>
<span data-ttu-id="304c8-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="304c8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="304c8-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="304c8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="304c8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="304c8-135">CommonParameters</span></span>
<span data-ttu-id="304c8-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="304c8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="304c8-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="304c8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="304c8-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="304c8-138">INPUTS</span></span>

### <span data-ttu-id="304c8-139">System.String</span><span class="sxs-lookup"><span data-stu-id="304c8-139">System.String</span></span>

## <span data-ttu-id="304c8-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="304c8-140">OUTPUTS</span></span>

### <span data-ttu-id="304c8-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="304c8-141">System.Boolean</span></span>

## <span data-ttu-id="304c8-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="304c8-142">NOTES</span></span>

## <span data-ttu-id="304c8-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="304c8-143">RELATED LINKS</span></span>
