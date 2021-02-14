---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 57b1f21aae43bd8b52d6bd4f23a15a7f41c15495
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201743"
---
# <span data-ttu-id="c61ea-101">New-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="c61ea-101">New-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="c61ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c61ea-102">SYNOPSIS</span></span>
<span data-ttu-id="c61ea-103">Aggiungere una risposta automatica a un analatico.</span><span class="sxs-lookup"><span data-stu-id="c61ea-103">Add an Automated Response to an Analatic.</span></span>

## <span data-ttu-id="c61ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c61ea-104">SYNTAX</span></span>

```
New-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-ActionId <String>] -LogicAppResourceId <String> -TriggerUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c61ea-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c61ea-105">DESCRIPTION</span></span>
<span data-ttu-id="c61ea-106">Il cmdlet **New-AzSentinelAlertRuleAction** crea una risposta automatica per una regola di avviso nell'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="c61ea-106">The **New-AzSentinelAlertRuleAction** cmdlet creates an Automated Response for an Alert Rule in the specified workspace.</span></span>
<span data-ttu-id="c61ea-107">È necessario specificare l'ID resorce dell'app logica e l'URI trigger, disponibili nel modulo dell'app logica.</span><span class="sxs-lookup"><span data-stu-id="c61ea-107">You must provide the Logic App Resorce Id and Trigger Uri which can be found using the Logic App module.</span></span>
<span data-ttu-id="c61ea-108">È possibile usare il *parametro Confirm* $ConfirmPreference Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="c61ea-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="c61ea-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c61ea-109">EXAMPLES</span></span>

### <span data-ttu-id="c61ea-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c61ea-110">Example 1</span></span>
```powershell
PS C:\>$LogicAppResourceId = Get-AzLogicApp -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword"
PS C:\>$LogicAppTriggerUri = Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword" -TriggerName "When_a_response_to_an_Azure_Sentinel_alert_is_triggered"
PS C:\>$AlertRuleAction = New-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="c61ea-111">Questo esempio crea **un'azione AlertRuleAction** per la regola di avviso specificata usando le proprietà dell'app logica e quindi la archivia nella $AlertRuleAction variabile.</span><span class="sxs-lookup"><span data-stu-id="c61ea-111">This example creates an **AlertRuleAction** for the specified Alert Rule using properties of the Logic App, and then stores it in the $AlertRuleAction variable.</span></span>

## <span data-ttu-id="c61ea-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c61ea-112">PARAMETERS</span></span>

### <span data-ttu-id="c61ea-113">-ActionId</span><span class="sxs-lookup"><span data-stu-id="c61ea-113">-ActionId</span></span>
<span data-ttu-id="c61ea-114">ID azione.</span><span class="sxs-lookup"><span data-stu-id="c61ea-114">Action Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c61ea-115">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="c61ea-115">-AlertRuleId</span></span>
<span data-ttu-id="c61ea-116">ID regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="c61ea-116">Alert Rule Id.</span></span>

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

### <span data-ttu-id="c61ea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c61ea-117">-DefaultProfile</span></span>
<span data-ttu-id="c61ea-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c61ea-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c61ea-119">-LogicAppResourceId</span><span class="sxs-lookup"><span data-stu-id="c61ea-119">-LogicAppResourceId</span></span>
<span data-ttu-id="c61ea-120">ID risorsa app logica azione.</span><span class="sxs-lookup"><span data-stu-id="c61ea-120">Action Logic App Resource Id.</span></span>

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

### <span data-ttu-id="c61ea-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c61ea-121">-ResourceGroupName</span></span>
<span data-ttu-id="c61ea-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c61ea-122">Resource group name.</span></span>

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

### <span data-ttu-id="c61ea-123">-TriggerUri</span><span class="sxs-lookup"><span data-stu-id="c61ea-123">-TriggerUri</span></span>
<span data-ttu-id="c61ea-124">Uri del trigger dell'app per la logica di azione.</span><span class="sxs-lookup"><span data-stu-id="c61ea-124">Action Logic App Trigger Uri.</span></span>

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

### <span data-ttu-id="c61ea-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c61ea-125">-WorkspaceName</span></span>
<span data-ttu-id="c61ea-126">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c61ea-126">Workspace Name.</span></span>

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

### <span data-ttu-id="c61ea-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c61ea-127">-Confirm</span></span>
<span data-ttu-id="c61ea-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c61ea-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c61ea-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c61ea-129">-WhatIf</span></span>
<span data-ttu-id="c61ea-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c61ea-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c61ea-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c61ea-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c61ea-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c61ea-132">CommonParameters</span></span>
<span data-ttu-id="c61ea-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c61ea-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c61ea-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c61ea-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c61ea-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="c61ea-135">INPUTS</span></span>

### <span data-ttu-id="c61ea-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c61ea-136">None</span></span>
## <span data-ttu-id="c61ea-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c61ea-137">OUTPUTS</span></span>

### <span data-ttu-id="c61ea-138">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="c61ea-138">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="c61ea-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="c61ea-139">NOTES</span></span>

## <span data-ttu-id="c61ea-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c61ea-140">RELATED LINKS</span></span>
