---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: cd71f1561525f166736b708caf4905fdefd443ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180110"
---
# <span data-ttu-id="a5ece-101">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="a5ece-101">Remove-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="a5ece-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5ece-102">SYNOPSIS</span></span>
<span data-ttu-id="a5ece-103">eliminare per la risorsa con ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="a5ece-103">delete for private link scoped resource</span></span>

## <span data-ttu-id="a5ece-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a5ece-104">SYNTAX</span></span>

### <span data-ttu-id="a5ece-105">ByScopeParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a5ece-105">ByScopeParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5ece-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5ece-106">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -Name <String> -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5ece-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5ece-107">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5ece-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a5ece-108">DESCRIPTION</span></span>
<span data-ttu-id="a5ece-109">eliminare per la risorsa con ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="a5ece-109">delete for private link scoped resource</span></span>

## <span data-ttu-id="a5ece-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a5ece-110">EXAMPLES</span></span>

### <span data-ttu-id="a5ece-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a5ece-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="a5ece-112">eliminare una risorsa con ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="a5ece-112">delete private link scoped resource</span></span>

## <span data-ttu-id="a5ece-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5ece-113">PARAMETERS</span></span>

### <span data-ttu-id="a5ece-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5ece-114">-DefaultProfile</span></span>
<span data-ttu-id="a5ece-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a5ece-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5ece-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5ece-116">-InputObject</span></span>
<span data-ttu-id="a5ece-117">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="a5ece-117">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="a5ece-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a5ece-118">-Name</span></span>
<span data-ttu-id="a5ece-119">Nome risorsa con ambito</span><span class="sxs-lookup"><span data-stu-id="a5ece-119">Scoped resource Name</span></span>

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

### <span data-ttu-id="a5ece-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5ece-120">-ResourceGroupName</span></span>
<span data-ttu-id="a5ece-121">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a5ece-121">Resource Group Name</span></span>

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

### <span data-ttu-id="a5ece-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5ece-122">-ResourceId</span></span>
<span data-ttu-id="a5ece-123">ID risorsa</span><span class="sxs-lookup"><span data-stu-id="a5ece-123">Resource Id</span></span>

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

### <span data-ttu-id="a5ece-124">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="a5ece-124">-ScopeName</span></span>
<span data-ttu-id="a5ece-125">Nome ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="a5ece-125">Private Link Scope Name</span></span>

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

### <span data-ttu-id="a5ece-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5ece-126">-Confirm</span></span>
<span data-ttu-id="a5ece-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5ece-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5ece-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5ece-128">-WhatIf</span></span>
<span data-ttu-id="a5ece-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5ece-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5ece-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5ece-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5ece-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5ece-131">CommonParameters</span></span>
<span data-ttu-id="a5ece-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5ece-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5ece-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a5ece-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5ece-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="a5ece-134">INPUTS</span></span>

### <span data-ttu-id="a5ece-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="a5ece-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="a5ece-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a5ece-136">System.String</span></span>

## <span data-ttu-id="a5ece-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a5ece-137">OUTPUTS</span></span>

### <span data-ttu-id="a5ece-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a5ece-138">System.Boolean</span></span>

## <span data-ttu-id="a5ece-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="a5ece-139">NOTES</span></span>

## <span data-ttu-id="a5ece-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a5ece-140">RELATED LINKS</span></span>
