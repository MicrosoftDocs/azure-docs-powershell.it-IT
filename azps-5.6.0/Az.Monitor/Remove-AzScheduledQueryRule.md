---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
ms.openlocfilehash: 24ad63f1422a829a0cef3ed0c4907ea5687b6151
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992653"
---
# <span data-ttu-id="a0ab5-101">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="a0ab5-101">Remove-AzScheduledQueryRule</span></span>

## <span data-ttu-id="a0ab5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0ab5-102">SYNOPSIS</span></span>
<span data-ttu-id="a0ab5-103">Rimuove una regola di avviso per il log</span><span class="sxs-lookup"><span data-stu-id="a0ab5-103">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="a0ab5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a0ab5-104">SYNTAX</span></span>

### <span data-ttu-id="a0ab5-105">ByRuleName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a0ab5-105">ByRuleName (Default)</span></span>
```
Remove-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0ab5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a0ab5-106">ByInputObject</span></span>
```
Remove-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0ab5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a0ab5-107">ByResourceId</span></span>
```
Remove-AzScheduledQueryRule -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0ab5-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a0ab5-108">DESCRIPTION</span></span>
<span data-ttu-id="a0ab5-109">Rimuove una regola di avviso per il log</span><span class="sxs-lookup"><span data-stu-id="a0ab5-109">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="a0ab5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a0ab5-110">EXAMPLES</span></span>

### <span data-ttu-id="a0ab5-111">Esempio 1: Rimuovere in base al nome della regola</span><span class="sxs-lookup"><span data-stu-id="a0ab5-111">Example 1: Remove by rule name</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1"
```

### <span data-ttu-id="a0ab5-112">Esempio 2: Rimuovere in base all'oggetto di input</span><span class="sxs-lookup"><span data-stu-id="a0ab5-112">Example 2: Remove by input object</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -InputObject $PSScheduledQueryRuleResource
```

### <span data-ttu-id="a0ab5-113">Esempio 3: Rimuovere in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="a0ab5-113">Example 3: Remove by resource Id</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledQueryRules/LogAlertRule1"
```

## <span data-ttu-id="a0ab5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0ab5-114">PARAMETERS</span></span>

### <span data-ttu-id="a0ab5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0ab5-115">-DefaultProfile</span></span>
<span data-ttu-id="a0ab5-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a0ab5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0ab5-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0ab5-117">-InputObject</span></span>
<span data-ttu-id="a0ab5-118">Risorsa Regola query programmata</span><span class="sxs-lookup"><span data-stu-id="a0ab5-118">The Scheduled Query Rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0ab5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a0ab5-119">-Name</span></span>
<span data-ttu-id="a0ab5-120">Nome dell'avviso</span><span class="sxs-lookup"><span data-stu-id="a0ab5-120">The alert name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0ab5-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0ab5-121">-PassThru</span></span>
<span data-ttu-id="a0ab5-122">Restituisce un valore che indica un'operazione riuscita o non riuscita.</span><span class="sxs-lookup"><span data-stu-id="a0ab5-122">Return a value indicating success or failure.</span></span>
<span data-ttu-id="a0ab5-123">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="a0ab5-123">This cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a0ab5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0ab5-124">-ResourceGroupName</span></span>
<span data-ttu-id="a0ab5-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a0ab5-125">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRuleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0ab5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0ab5-126">-ResourceId</span></span>
<span data-ttu-id="a0ab5-127">ID risorsa</span><span class="sxs-lookup"><span data-stu-id="a0ab5-127">The resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0ab5-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0ab5-128">-Confirm</span></span>
<span data-ttu-id="a0ab5-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0ab5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0ab5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0ab5-130">-WhatIf</span></span>
<span data-ttu-id="a0ab5-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0ab5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0ab5-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0ab5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0ab5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0ab5-133">CommonParameters</span></span>
<span data-ttu-id="a0ab5-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0ab5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0ab5-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a0ab5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0ab5-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="a0ab5-136">INPUTS</span></span>

### <span data-ttu-id="a0ab5-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="a0ab5-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="a0ab5-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a0ab5-138">System.String</span></span>

## <span data-ttu-id="a0ab5-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a0ab5-139">OUTPUTS</span></span>

### <span data-ttu-id="a0ab5-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a0ab5-140">System.Boolean</span></span>

## <span data-ttu-id="a0ab5-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="a0ab5-141">NOTES</span></span>

## <span data-ttu-id="a0ab5-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a0ab5-142">RELATED LINKS</span></span>
