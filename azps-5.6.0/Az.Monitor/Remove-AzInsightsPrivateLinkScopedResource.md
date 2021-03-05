---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: 83f4fae326920b24d272ae87341c20702a2bf8fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003742"
---
# <span data-ttu-id="9e271-101">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="9e271-101">Remove-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="9e271-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e271-102">SYNOPSIS</span></span>
<span data-ttu-id="9e271-103">eliminare per la risorsa con ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="9e271-103">delete for private link scoped resource</span></span>

## <span data-ttu-id="9e271-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e271-104">SYNTAX</span></span>

### <span data-ttu-id="9e271-105">ByScopeParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9e271-105">ByScopeParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e271-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e271-106">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -Name <String> -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e271-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e271-107">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e271-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9e271-108">DESCRIPTION</span></span>
<span data-ttu-id="9e271-109">delete for private link scoped resource</span><span class="sxs-lookup"><span data-stu-id="9e271-109">delete for private link scoped resource</span></span>

## <span data-ttu-id="9e271-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e271-110">EXAMPLES</span></span>

### <span data-ttu-id="9e271-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9e271-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="9e271-112">eliminare una risorsa con ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="9e271-112">delete private link scoped resource</span></span>

## <span data-ttu-id="9e271-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e271-113">PARAMETERS</span></span>

### <span data-ttu-id="9e271-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e271-114">-DefaultProfile</span></span>
<span data-ttu-id="9e271-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9e271-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e271-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e271-116">-InputObject</span></span>
<span data-ttu-id="9e271-117">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="9e271-117">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="9e271-118">-Name</span><span class="sxs-lookup"><span data-stu-id="9e271-118">-Name</span></span>
<span data-ttu-id="9e271-119">Nome risorsa con ambito</span><span class="sxs-lookup"><span data-stu-id="9e271-119">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet, ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e271-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e271-120">-ResourceGroupName</span></span>
<span data-ttu-id="9e271-121">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="9e271-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e271-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e271-122">-ResourceId</span></span>
<span data-ttu-id="9e271-123">ID risorsa</span><span class="sxs-lookup"><span data-stu-id="9e271-123">Resource Id</span></span>

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

### <span data-ttu-id="9e271-124">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="9e271-124">-ScopeName</span></span>
<span data-ttu-id="9e271-125">Nome ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="9e271-125">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e271-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e271-126">-Confirm</span></span>
<span data-ttu-id="9e271-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e271-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e271-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e271-128">-WhatIf</span></span>
<span data-ttu-id="9e271-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e271-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e271-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e271-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e271-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e271-131">CommonParameters</span></span>
<span data-ttu-id="9e271-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e271-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e271-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9e271-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e271-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="9e271-134">INPUTS</span></span>

### <span data-ttu-id="9e271-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="9e271-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="9e271-136">System.String</span><span class="sxs-lookup"><span data-stu-id="9e271-136">System.String</span></span>

## <span data-ttu-id="9e271-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e271-137">OUTPUTS</span></span>

### <span data-ttu-id="9e271-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9e271-138">System.Boolean</span></span>

## <span data-ttu-id="9e271-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="9e271-139">NOTES</span></span>

## <span data-ttu-id="9e271-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e271-140">RELATED LINKS</span></span>
