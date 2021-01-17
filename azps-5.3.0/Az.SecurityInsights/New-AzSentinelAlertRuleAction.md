---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 57b1f21aae43bd8b52d6bd4f23a15a7f41c15495
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486204"
---
# <span data-ttu-id="2bd8a-101">New-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="2bd8a-101">New-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="2bd8a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2bd8a-102">SYNOPSIS</span></span>
<span data-ttu-id="2bd8a-103">Aggiungere una risposta automatica a un Analatic.</span><span class="sxs-lookup"><span data-stu-id="2bd8a-103">Add an Automated Response to an Analatic.</span></span>

## <span data-ttu-id="2bd8a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2bd8a-104">SYNTAX</span></span>

```
New-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-ActionId <String>] -LogicAppResourceId <String> -TriggerUri <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bd8a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2bd8a-105">DESCRIPTION</span></span>
<span data-ttu-id="2bd8a-106">Il cmdlet **New-AzSentinelAlertRuleAction** crea una risposta automatica per una regola di avviso nell'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="2bd8a-106">The **New-AzSentinelAlertRuleAction** cmdlet creates an Automated Response for an Alert Rule in the specified workspace.</span></span>
<span data-ttu-id="2bd8a-107">Devi specificare l'ID resorce dell'app logica e l'URI trigger che puoi trovare usando il modulo app Logic.</span><span class="sxs-lookup"><span data-stu-id="2bd8a-107">You must provide the Logic App Resorce Id and Trigger Uri which can be found using the Logic App module.</span></span>
<span data-ttu-id="2bd8a-108">Puoi usare il parametro *Confirm* e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="2bd8a-108">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="2bd8a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2bd8a-109">EXAMPLES</span></span>

### <span data-ttu-id="2bd8a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2bd8a-110">Example 1</span></span>
```powershell
PS C:\>$LogicAppResourceId = Get-AzLogicApp -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword"
PS C:\>$LogicAppTriggerUri = Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "MyResourceGroup" -Name "Reset-AADPassword" -TriggerName "When_a_response_to_an_Azure_Sentinel_alert_is_triggered"
PS C:\>$AlertRuleAction = New-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -LogicAppResourceId ($LogicAppResourceId.Id) -TriggerUri ($LogicAppTriggerUri.Value)
```

<span data-ttu-id="2bd8a-111">Questo esempio crea un **AlertRuleAction** per la regola di avviso specificata usando le proprietà dell'app logica e lo archivia nella variabile $AlertRuleAction.</span><span class="sxs-lookup"><span data-stu-id="2bd8a-111">This example creates an **AlertRuleAction** for the specified Alert Rule using properties of the Logic App, and then stores it in the $AlertRuleAction variable.</span></span>

## <span data-ttu-id="2bd8a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2bd8a-112">PARAMETERS</span></span>

### <span data-ttu-id="2bd8a-113">-ActionId</span><span class="sxs-lookup"><span data-stu-id="2bd8a-113">-ActionId</span></span>
<span data-ttu-id="2bd8a-114">ID azione.</span><span class="sxs-lookup"><span data-stu-id="2bd8a-114">Action Id.</span></span>

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

### <span data-ttu-id="2bd8a-115">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="2bd8a-115">-AlertRuleId</span></span>
<span data-ttu-id="2bd8a-116">ID regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="2bd8a-116">Alert Rule Id.</span></span>

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

### <span data-ttu-id="2bd8a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bd8a-117">-DefaultProfile</span></span>
<span data-ttu-id="2bd8a-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2bd8a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bd8a-119">-LogicAppResourceId</span><span class="sxs-lookup"><span data-stu-id="2bd8a-119">-LogicAppResourceId</span></span>
<span data-ttu-id="2bd8a-120">ID risorsa delle app logiche di azione.</span><span class="sxs-lookup"><span data-stu-id="2bd8a-120">Action Logic App Resource Id.</span></span>

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

### <span data-ttu-id="2bd8a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bd8a-121">-ResourceGroupName</span></span>
<span data-ttu-id="2bd8a-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2bd8a-122">Resource group name.</span></span>

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

### <span data-ttu-id="2bd8a-123">-TriggerUri</span><span class="sxs-lookup"><span data-stu-id="2bd8a-123">-TriggerUri</span></span>
<span data-ttu-id="2bd8a-124">URI trigger dell'app logica di azione.</span><span class="sxs-lookup"><span data-stu-id="2bd8a-124">Action Logic App Trigger Uri.</span></span>

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

### <span data-ttu-id="2bd8a-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2bd8a-125">-WorkspaceName</span></span>
<span data-ttu-id="2bd8a-126">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="2bd8a-126">Workspace Name.</span></span>

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

### <span data-ttu-id="2bd8a-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2bd8a-127">-Confirm</span></span>
<span data-ttu-id="2bd8a-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bd8a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bd8a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bd8a-129">-WhatIf</span></span>
<span data-ttu-id="2bd8a-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2bd8a-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2bd8a-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2bd8a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bd8a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bd8a-132">CommonParameters</span></span>
<span data-ttu-id="2bd8a-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bd8a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bd8a-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2bd8a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bd8a-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2bd8a-135">INPUTS</span></span>

### <span data-ttu-id="2bd8a-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2bd8a-136">None</span></span>
## <span data-ttu-id="2bd8a-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2bd8a-137">OUTPUTS</span></span>

### <span data-ttu-id="2bd8a-138">Microsoft. Azure. Commands. SecurityInsights. Models. Actions. PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="2bd8a-138">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="2bd8a-139">Note</span><span class="sxs-lookup"><span data-stu-id="2bd8a-139">NOTES</span></span>

## <span data-ttu-id="2bd8a-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2bd8a-140">RELATED LINKS</span></span>
