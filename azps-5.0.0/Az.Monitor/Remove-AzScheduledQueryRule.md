---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
ms.openlocfilehash: ea7679b2e3214c55463f9f6fd4ccaf2b22d32841
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203363"
---
# <span data-ttu-id="67b71-101">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="67b71-101">Remove-AzScheduledQueryRule</span></span>

## <span data-ttu-id="67b71-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="67b71-102">SYNOPSIS</span></span>
<span data-ttu-id="67b71-103">Rimuove una regola di avviso del log</span><span class="sxs-lookup"><span data-stu-id="67b71-103">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="67b71-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67b71-104">SYNTAX</span></span>

### <span data-ttu-id="67b71-105">ByRuleName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="67b71-105">ByRuleName (Default)</span></span>
```
Remove-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67b71-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="67b71-106">ByInputObject</span></span>
```
Remove-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67b71-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="67b71-107">ByResourceId</span></span>
```
Remove-AzScheduledQueryRule -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67b71-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67b71-108">DESCRIPTION</span></span>
<span data-ttu-id="67b71-109">Rimuove una regola di avviso del log</span><span class="sxs-lookup"><span data-stu-id="67b71-109">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="67b71-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67b71-110">EXAMPLES</span></span>

### <span data-ttu-id="67b71-111">Esempio 1: rimuovere il nome della regola</span><span class="sxs-lookup"><span data-stu-id="67b71-111">Example 1: Remove by rule name</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1"
```

### <span data-ttu-id="67b71-112">Esempio 2: Rimuovi per oggetto di input</span><span class="sxs-lookup"><span data-stu-id="67b71-112">Example 2: Remove by input object</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -InputObject $PSScheduledQueryRuleResource
```

### <span data-ttu-id="67b71-113">Esempio 3: Rimuovi dall'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="67b71-113">Example 3: Remove by resource Id</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledQueryRules/LogAlertRule1"
```

## <span data-ttu-id="67b71-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="67b71-114">PARAMETERS</span></span>

### <span data-ttu-id="67b71-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67b71-115">-DefaultProfile</span></span>
<span data-ttu-id="67b71-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67b71-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67b71-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67b71-117">-InputObject</span></span>
<span data-ttu-id="67b71-118">Risorsa della regola di query pianificata</span><span class="sxs-lookup"><span data-stu-id="67b71-118">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="67b71-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="67b71-119">-Name</span></span>
<span data-ttu-id="67b71-120">Nome avviso</span><span class="sxs-lookup"><span data-stu-id="67b71-120">The alert name</span></span>

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

### <span data-ttu-id="67b71-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67b71-121">-PassThru</span></span>
<span data-ttu-id="67b71-122">Restituisce un valore che indica l'esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="67b71-122">Return a value indicating success or failure.</span></span>
<span data-ttu-id="67b71-123">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="67b71-123">This cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="67b71-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67b71-124">-ResourceGroupName</span></span>
<span data-ttu-id="67b71-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="67b71-125">The resource group name</span></span>

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

### <span data-ttu-id="67b71-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67b71-126">-ResourceId</span></span>
<span data-ttu-id="67b71-127">ID risorsa</span><span class="sxs-lookup"><span data-stu-id="67b71-127">The resource Id</span></span>

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

### <span data-ttu-id="67b71-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="67b71-128">-Confirm</span></span>
<span data-ttu-id="67b71-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67b71-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67b71-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67b71-130">-WhatIf</span></span>
<span data-ttu-id="67b71-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67b71-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67b71-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67b71-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67b71-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67b71-133">CommonParameters</span></span>
<span data-ttu-id="67b71-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67b71-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67b71-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67b71-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67b71-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="67b71-136">INPUTS</span></span>

### <span data-ttu-id="67b71-137">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="67b71-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="67b71-138">System. String</span><span class="sxs-lookup"><span data-stu-id="67b71-138">System.String</span></span>

## <span data-ttu-id="67b71-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67b71-139">OUTPUTS</span></span>

### <span data-ttu-id="67b71-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="67b71-140">System.Boolean</span></span>

## <span data-ttu-id="67b71-141">Note</span><span class="sxs-lookup"><span data-stu-id="67b71-141">NOTES</span></span>

## <span data-ttu-id="67b71-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67b71-142">RELATED LINKS</span></span>
