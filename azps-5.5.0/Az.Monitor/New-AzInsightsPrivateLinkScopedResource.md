---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: fd4dc0dd771029951da4ae375141cc526301de34
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192175"
---
# <span data-ttu-id="05293-101">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="05293-101">New-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="05293-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05293-102">SYNOPSIS</span></span>
<span data-ttu-id="05293-103">creare per una risorsa con ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="05293-103">create for private link scoped resource</span></span>

## <span data-ttu-id="05293-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05293-104">SYNTAX</span></span>

### <span data-ttu-id="05293-105">ByResourceNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="05293-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -ResourceGroupName <String>
 -ScopeName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="05293-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="05293-106">ByInputObjectParameterSet</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -Name <String>
 -InputObject <PSMonitorPrivateLinkScope> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="05293-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="05293-107">DESCRIPTION</span></span>
<span data-ttu-id="05293-108">creare per una risorsa con ambito collegamento privato, la risorsa con ambito può essere l'area di lavoro Analisi log o il componente Application Insights</span><span class="sxs-lookup"><span data-stu-id="05293-108">create for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="05293-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05293-109">EXAMPLES</span></span>

### <span data-ttu-id="05293-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="05293-110">Example 1</span></span>
```powershell
$ai = Get-AzApplicationInsights -ResourceGroupName "rg_name" -Name "ai_name"

New-AzInsightsPrivateLinkScopedResource -LinkedResourceId $ai.Id -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="05293-111">Create scoped resource "scoped_resource_name" linked to application insights component "ai_name"</span><span class="sxs-lookup"><span data-stu-id="05293-111">create scoped resource "scoped_resource_name" linked to application insights component "ai_name"</span></span>

## <span data-ttu-id="05293-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="05293-112">PARAMETERS</span></span>

### <span data-ttu-id="05293-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05293-113">-DefaultProfile</span></span>
<span data-ttu-id="05293-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="05293-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05293-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05293-115">-InputObject</span></span>
<span data-ttu-id="05293-116">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="05293-116">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="05293-117">-LinkedResourceId</span><span class="sxs-lookup"><span data-stu-id="05293-117">-LinkedResourceId</span></span>
<span data-ttu-id="05293-118">ID risorsa LA/AI per il collegamento</span><span class="sxs-lookup"><span data-stu-id="05293-118">LA/AI Resource Id to Link</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05293-119">-Name</span><span class="sxs-lookup"><span data-stu-id="05293-119">-Name</span></span>
<span data-ttu-id="05293-120">Nome risorsa con ambito</span><span class="sxs-lookup"><span data-stu-id="05293-120">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05293-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05293-121">-ResourceGroupName</span></span>
<span data-ttu-id="05293-122">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="05293-122">Resource Group Name</span></span>

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

### <span data-ttu-id="05293-123">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="05293-123">-ScopeName</span></span>
<span data-ttu-id="05293-124">Nome ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="05293-124">Private Link Scope Name</span></span>

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

### <span data-ttu-id="05293-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="05293-125">-Confirm</span></span>
<span data-ttu-id="05293-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05293-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05293-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05293-127">-WhatIf</span></span>
<span data-ttu-id="05293-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05293-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05293-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05293-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05293-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05293-130">CommonParameters</span></span>
<span data-ttu-id="05293-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05293-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05293-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="05293-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05293-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="05293-133">INPUTS</span></span>

### <span data-ttu-id="05293-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="05293-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="05293-135">System.String</span><span class="sxs-lookup"><span data-stu-id="05293-135">System.String</span></span>

## <span data-ttu-id="05293-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05293-136">OUTPUTS</span></span>

### <span data-ttu-id="05293-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="05293-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="05293-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="05293-138">NOTES</span></span>

## <span data-ttu-id="05293-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05293-139">RELATED LINKS</span></span>
