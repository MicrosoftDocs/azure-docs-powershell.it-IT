---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: af33bf23e6cd488f98e38c9bd2696029b5510aca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984506"
---
# <span data-ttu-id="4d64d-101">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="4d64d-101">Remove-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="4d64d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d64d-102">SYNOPSIS</span></span>
<span data-ttu-id="4d64d-103">eliminare l'ambito del collegamento privato</span><span class="sxs-lookup"><span data-stu-id="4d64d-103">delete private link scope</span></span>

## <span data-ttu-id="4d64d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d64d-104">SYNTAX</span></span>

### <span data-ttu-id="4d64d-105">ByResourceNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="4d64d-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d64d-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d64d-106">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d64d-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d64d-107">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d64d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4d64d-108">DESCRIPTION</span></span>
<span data-ttu-id="4d64d-109">eliminare l'ambito del collegamento privato</span><span class="sxs-lookup"><span data-stu-id="4d64d-109">delete private link scope</span></span>

## <span data-ttu-id="4d64d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d64d-110">EXAMPLES</span></span>

### <span data-ttu-id="4d64d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4d64d-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="4d64d-112">eliminare l'ambito del collegamento privato con il nome "scope_name" nel gruppo di risorse "rg_name"</span><span class="sxs-lookup"><span data-stu-id="4d64d-112">delete private link scope with name "scope_name" under resource group "rg_name"</span></span>

### <span data-ttu-id="4d64d-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4d64d-113">Example 2</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name"
```

<span data-ttu-id="4d64d-114">Eliminare l'ambito del collegamento privato con l'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="4d64d-114">delete private link scope with resource Id</span></span>

### <span data-ttu-id="4d64d-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="4d64d-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Remove-AzInsightsPrivateLinkScope
```

<span data-ttu-id="4d64d-116">Eliminare l'ambito del collegamento privato con l'oggetto ambito del collegamento privato di input</span><span class="sxs-lookup"><span data-stu-id="4d64d-116">delete private link scope with input private link scope object</span></span>

## <span data-ttu-id="4d64d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d64d-117">PARAMETERS</span></span>

### <span data-ttu-id="4d64d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d64d-118">-DefaultProfile</span></span>
<span data-ttu-id="4d64d-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4d64d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d64d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d64d-120">-InputObject</span></span>
<span data-ttu-id="4d64d-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="4d64d-121">PSMonitorPrivateLinkScope</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d64d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4d64d-122">-Name</span></span>
<span data-ttu-id="4d64d-123">Nome ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="4d64d-123">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d64d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d64d-124">-ResourceGroupName</span></span>
<span data-ttu-id="4d64d-125">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="4d64d-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d64d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d64d-126">-ResourceId</span></span>
<span data-ttu-id="4d64d-127">ID risorsa</span><span class="sxs-lookup"><span data-stu-id="4d64d-127">Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d64d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d64d-128">-Confirm</span></span>
<span data-ttu-id="4d64d-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d64d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d64d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d64d-130">-WhatIf</span></span>
<span data-ttu-id="4d64d-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d64d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d64d-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d64d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d64d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d64d-133">CommonParameters</span></span>
<span data-ttu-id="4d64d-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d64d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d64d-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4d64d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d64d-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="4d64d-136">INPUTS</span></span>

### <span data-ttu-id="4d64d-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="4d64d-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="4d64d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="4d64d-138">System.String</span></span>

## <span data-ttu-id="4d64d-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d64d-139">OUTPUTS</span></span>

### <span data-ttu-id="4d64d-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4d64d-140">System.Boolean</span></span>

## <span data-ttu-id="4d64d-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="4d64d-141">NOTES</span></span>

## <span data-ttu-id="4d64d-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d64d-142">RELATED LINKS</span></span>
