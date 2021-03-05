---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/update-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: ef53c93669faea2e9f952c0887e6cb0b105cf19b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965758"
---
# <span data-ttu-id="5c757-101">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="5c757-101">Update-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="5c757-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c757-102">SYNOPSIS</span></span>
<span data-ttu-id="5c757-103">Aggiornamento per l'ambito del collegamento privato</span><span class="sxs-lookup"><span data-stu-id="5c757-103">Update for private link scope</span></span>

## <span data-ttu-id="5c757-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5c757-104">SYNTAX</span></span>

### <span data-ttu-id="5c757-105">ByResourceNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="5c757-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c757-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c757-106">ByResourceIdParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceId <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c757-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c757-107">ByInputObjectParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c757-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5c757-108">DESCRIPTION</span></span>
<span data-ttu-id="5c757-109">Aggiornamento per l'ambito del collegamento privato</span><span class="sxs-lookup"><span data-stu-id="5c757-109">Update for private link scope</span></span>

## <span data-ttu-id="5c757-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5c757-110">EXAMPLES</span></span>

### <span data-ttu-id="5c757-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5c757-111">Example 1</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" -Tags "key:value"
```

<span data-ttu-id="5c757-112">aggiornare l'ambito del collegamento privato con il nome "scope_name" nel gruppo di risorse "rg_name" per usare il tag "chiave:valore"</span><span class="sxs-lookup"><span data-stu-id="5c757-112">update private link scope with name "scope_name" under resource group "rg_name" to use tag "key:value"</span></span>

### <span data-ttu-id="5c757-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5c757-113">Example 2</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name" -Tags "key:value"
```

<span data-ttu-id="5c757-114">Aggiornare l'ambito del collegamento privato con l'ID risorsa per usare il tag "key:value"</span><span class="sxs-lookup"><span data-stu-id="5c757-114">update private link scope with resource Id to use tag "key:value"</span></span>

### <span data-ttu-id="5c757-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="5c757-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Update-AzInsightsPrivateLinkScope -Tags "key:value"
```

<span data-ttu-id="5c757-116">Aggiornare l'ambito del collegamento privato con l'oggetto ambito collegamento privato di input per usare il tag "chiave:valore"</span><span class="sxs-lookup"><span data-stu-id="5c757-116">update private link scope with input private link scope object to use tag "key:value"</span></span>

## <span data-ttu-id="5c757-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c757-117">PARAMETERS</span></span>

### <span data-ttu-id="5c757-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c757-118">-DefaultProfile</span></span>
<span data-ttu-id="5c757-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5c757-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c757-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c757-120">-InputObject</span></span>
<span data-ttu-id="5c757-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="5c757-121">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="5c757-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5c757-122">-Name</span></span>
<span data-ttu-id="5c757-123">Nome ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="5c757-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="5c757-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c757-124">-ResourceGroupName</span></span>
<span data-ttu-id="5c757-125">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="5c757-125">Resource Group Name</span></span>

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

### <span data-ttu-id="5c757-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c757-126">-ResourceId</span></span>
<span data-ttu-id="5c757-127">ID risorsa</span><span class="sxs-lookup"><span data-stu-id="5c757-127">Resource Id</span></span>

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

### <span data-ttu-id="5c757-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="5c757-128">-Tags</span></span>
<span data-ttu-id="5c757-129">Tag</span><span class="sxs-lookup"><span data-stu-id="5c757-129">Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c757-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c757-130">-Confirm</span></span>
<span data-ttu-id="5c757-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c757-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c757-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c757-132">-WhatIf</span></span>
<span data-ttu-id="5c757-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5c757-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c757-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5c757-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c757-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c757-135">CommonParameters</span></span>
<span data-ttu-id="5c757-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c757-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c757-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5c757-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c757-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="5c757-138">INPUTS</span></span>

### <span data-ttu-id="5c757-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="5c757-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="5c757-140">System.String</span><span class="sxs-lookup"><span data-stu-id="5c757-140">System.String</span></span>

## <span data-ttu-id="5c757-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5c757-141">OUTPUTS</span></span>

### <span data-ttu-id="5c757-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="5c757-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="5c757-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="5c757-143">NOTES</span></span>

## <span data-ttu-id="5c757-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5c757-144">RELATED LINKS</span></span>
