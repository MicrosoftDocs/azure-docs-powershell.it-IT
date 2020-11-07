---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azscheduledqueryrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzScheduledQueryRule.md
ms.openlocfilehash: e1aa7381e7e0fa5042fc20af68864667a2a23910
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864236"
---
# <span data-ttu-id="9255f-101">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="9255f-101">Remove-AzScheduledQueryRule</span></span>

## <span data-ttu-id="9255f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9255f-102">SYNOPSIS</span></span>
<span data-ttu-id="9255f-103">Rimuove una regola di avviso del log</span><span class="sxs-lookup"><span data-stu-id="9255f-103">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="9255f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9255f-104">SYNTAX</span></span>

### <span data-ttu-id="9255f-105">ByRuleName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9255f-105">ByRuleName (Default)</span></span>
```
Remove-AzScheduledQueryRule -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9255f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9255f-106">ByInputObject</span></span>
```
Remove-AzScheduledQueryRule -InputObject <PSScheduledQueryRuleResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9255f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9255f-107">ByResourceId</span></span>
```
Remove-AzScheduledQueryRule -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9255f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9255f-108">DESCRIPTION</span></span>
<span data-ttu-id="9255f-109">Rimuove una regola di avviso del log</span><span class="sxs-lookup"><span data-stu-id="9255f-109">Removes a Log Alert Rule</span></span>

## <span data-ttu-id="9255f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9255f-110">EXAMPLES</span></span>

### <span data-ttu-id="9255f-111">Esempio 1-Rimuovi per nome regola</span><span class="sxs-lookup"><span data-stu-id="9255f-111">Example 1 - Remove by rule name</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceGroupName "MyResourceGroup" -Name "LogAlertRule1"
```

### <span data-ttu-id="9255f-112">Esempio 2-Rimuovi per oggetto di input</span><span class="sxs-lookup"><span data-stu-id="9255f-112">Example 2 - Remove by input object</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -InputObject $PSScheduledQueryRuleResource
```

### <span data-ttu-id="9255f-113">Esempio 3-Rimuovi per ID risorsa</span><span class="sxs-lookup"><span data-stu-id="9255f-113">Example 3 - Remove by resource Id</span></span>
```powershell
PS C:\> Remove-AzScheduledQueryRule -ResourceId "/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourceGroups/MyResourceGroup/providers/microsoft.insights/scheduledQueryRules/LogAlertRule1"
```

## <span data-ttu-id="9255f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9255f-114">PARAMETERS</span></span>

### <span data-ttu-id="9255f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9255f-115">-DefaultProfile</span></span>
<span data-ttu-id="9255f-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9255f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9255f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9255f-117">-InputObject</span></span>
<span data-ttu-id="9255f-118">Risorsa della regola di query pianificata</span><span class="sxs-lookup"><span data-stu-id="9255f-118">The Scheduled Query Rule resource</span></span>

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

### <span data-ttu-id="9255f-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="9255f-119">-Name</span></span>
<span data-ttu-id="9255f-120">Nome avviso</span><span class="sxs-lookup"><span data-stu-id="9255f-120">The alert name</span></span>

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

### <span data-ttu-id="9255f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9255f-121">-PassThru</span></span>
<span data-ttu-id="9255f-122">Restituisce un valore che indica l'esito positivo o negativo.</span><span class="sxs-lookup"><span data-stu-id="9255f-122">Return a value indicating success or failure.</span></span>
<span data-ttu-id="9255f-123">Questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="9255f-123">This cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9255f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9255f-124">-ResourceGroupName</span></span>
<span data-ttu-id="9255f-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="9255f-125">The resource group name</span></span>

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

### <span data-ttu-id="9255f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9255f-126">-ResourceId</span></span>
<span data-ttu-id="9255f-127">ID risorsa</span><span class="sxs-lookup"><span data-stu-id="9255f-127">The resource Id</span></span>

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

### <span data-ttu-id="9255f-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9255f-128">-Confirm</span></span>
<span data-ttu-id="9255f-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9255f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9255f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9255f-130">-WhatIf</span></span>
<span data-ttu-id="9255f-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9255f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9255f-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9255f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9255f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9255f-133">CommonParameters</span></span>
<span data-ttu-id="9255f-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9255f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9255f-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9255f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9255f-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9255f-136">INPUTS</span></span>

### <span data-ttu-id="9255f-137">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleResource</span><span class="sxs-lookup"><span data-stu-id="9255f-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleResource</span></span>

### <span data-ttu-id="9255f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9255f-138">System.String</span></span>

## <span data-ttu-id="9255f-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9255f-139">OUTPUTS</span></span>

### <span data-ttu-id="9255f-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9255f-140">System.Boolean</span></span>

## <span data-ttu-id="9255f-141">Note</span><span class="sxs-lookup"><span data-stu-id="9255f-141">NOTES</span></span>

## <span data-ttu-id="9255f-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9255f-142">RELATED LINKS</span></span>
