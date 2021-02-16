---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 93e97906fc7e985d522f5af9d678392741a9022b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187383"
---
# <span data-ttu-id="dfab4-101">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="dfab4-101">Update-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="dfab4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfab4-102">SYNOPSIS</span></span>
<span data-ttu-id="dfab4-103">Aggiornamento per l'ambito del collegamento privato</span><span class="sxs-lookup"><span data-stu-id="dfab4-103">Update for private link scope</span></span>

## <span data-ttu-id="dfab4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dfab4-104">SYNTAX</span></span>

### <span data-ttu-id="dfab4-105">ByResourceNameParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="dfab4-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfab4-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfab4-106">ByResourceIdParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceId <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfab4-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dfab4-107">ByInputObjectParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfab4-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dfab4-108">DESCRIPTION</span></span>
<span data-ttu-id="dfab4-109">Aggiornamento per l'ambito del collegamento privato</span><span class="sxs-lookup"><span data-stu-id="dfab4-109">Update for private link scope</span></span>

## <span data-ttu-id="dfab4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dfab4-110">EXAMPLES</span></span>

### <span data-ttu-id="dfab4-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dfab4-111">Example 1</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" -Tags "key:value"
```

<span data-ttu-id="dfab4-112">aggiornare l'ambito del collegamento privato con il nome "scope_name" nel gruppo di risorse "rg_name" per usare il tag "chiave:valore"</span><span class="sxs-lookup"><span data-stu-id="dfab4-112">update private link scope with name "scope_name" under resource group "rg_name" to use tag "key:value"</span></span>

### <span data-ttu-id="dfab4-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="dfab4-113">Example 2</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name" -Tags "key:value"
```

<span data-ttu-id="dfab4-114">aggiornare l'ambito del collegamento privato con l'ID risorsa per usare il tag "chiave:valore"</span><span class="sxs-lookup"><span data-stu-id="dfab4-114">update private link scope with resource Id to use tag "key:value"</span></span>

### <span data-ttu-id="dfab4-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="dfab4-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Update-AzInsightsPrivateLinkScope -Tags "key:value"
```

<span data-ttu-id="dfab4-116">Aggiornare l'ambito del collegamento privato con l'oggetto ambito collegamento privato di input per usare il tag "chiave:valore"</span><span class="sxs-lookup"><span data-stu-id="dfab4-116">update private link scope with input private link scope object to use tag "key:value"</span></span>

## <span data-ttu-id="dfab4-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dfab4-117">PARAMETERS</span></span>

### <span data-ttu-id="dfab4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfab4-118">-DefaultProfile</span></span>
<span data-ttu-id="dfab4-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dfab4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfab4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfab4-120">-InputObject</span></span>
<span data-ttu-id="dfab4-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="dfab4-121">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="dfab4-122">-Name</span><span class="sxs-lookup"><span data-stu-id="dfab4-122">-Name</span></span>
<span data-ttu-id="dfab4-123">Nome ambito collegamento privato</span><span class="sxs-lookup"><span data-stu-id="dfab4-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="dfab4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfab4-124">-ResourceGroupName</span></span>
<span data-ttu-id="dfab4-125">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="dfab4-125">Resource Group Name</span></span>

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

### <span data-ttu-id="dfab4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dfab4-126">-ResourceId</span></span>
<span data-ttu-id="dfab4-127">ID risorsa</span><span class="sxs-lookup"><span data-stu-id="dfab4-127">Resource Id</span></span>

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

### <span data-ttu-id="dfab4-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="dfab4-128">-Tags</span></span>
<span data-ttu-id="dfab4-129">Tag</span><span class="sxs-lookup"><span data-stu-id="dfab4-129">Tags</span></span>

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

### <span data-ttu-id="dfab4-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dfab4-130">-Confirm</span></span>
<span data-ttu-id="dfab4-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfab4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfab4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfab4-132">-WhatIf</span></span>
<span data-ttu-id="dfab4-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dfab4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfab4-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dfab4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfab4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfab4-135">CommonParameters</span></span>
<span data-ttu-id="dfab4-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfab4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfab4-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dfab4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfab4-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="dfab4-138">INPUTS</span></span>

### <span data-ttu-id="dfab4-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="dfab4-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="dfab4-140">System.String</span><span class="sxs-lookup"><span data-stu-id="dfab4-140">System.String</span></span>

## <span data-ttu-id="dfab4-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dfab4-141">OUTPUTS</span></span>

### <span data-ttu-id="dfab4-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="dfab4-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="dfab4-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="dfab4-143">NOTES</span></span>

## <span data-ttu-id="dfab4-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dfab4-144">RELATED LINKS</span></span>
