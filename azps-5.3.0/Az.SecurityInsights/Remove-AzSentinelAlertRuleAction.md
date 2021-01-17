---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 48566fde735deb5693783f9e71f047f73d5f9336
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486172"
---
# <span data-ttu-id="df8a6-101">Remove-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="df8a6-101">Remove-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="df8a6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="df8a6-102">SYNOPSIS</span></span>
<span data-ttu-id="df8a6-103">Rimuovere una risposta automatica da una analitica.</span><span class="sxs-lookup"><span data-stu-id="df8a6-103">Remove an Automated Response from an Analytic.</span></span>

## <span data-ttu-id="df8a6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="df8a6-104">SYNTAX</span></span>

### <span data-ttu-id="df8a6-105">ActionId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="df8a6-105">ActionId (Default)</span></span>
```
Remove-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df8a6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="df8a6-106">InputObject</span></span>
```
Remove-AzSentinelAlertRuleAction -InputObject <PSSentinelActionResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df8a6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df8a6-107">DESCRIPTION</span></span>
<span data-ttu-id="df8a6-108">Il cmdlet **Remove-AzSentinelAlertRuleAction** Elimina definitivamente una risposta automatica dalla regola di avviso in un'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="df8a6-108">The **Remove-AzSentinelAlertRuleAction** cmdlet permanently deletes an Automated Response from the Alert Rule in a specified workspace.</span></span>
<span data-ttu-id="df8a6-109">Puoi passare un oggetto **AlertRuleAction** usando l'operatore pipeline o in alternativa puoi specificare i parametri obbligatori.</span><span class="sxs-lookup"><span data-stu-id="df8a6-109">You can pass an **AlertRuleAction** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="df8a6-110">Puoi usare il parametro Confirm e $ConfirmPreference variabile di Windows PowerShell per controllare se il cmdlet richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="df8a6-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="df8a6-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="df8a6-111">EXAMPLES</span></span>

### <span data-ttu-id="df8a6-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="df8a6-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
```

<span data-ttu-id="df8a6-113">Questo comando rimuove la regola di avviso dall'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="df8a6-113">This command removes the Alert Rule from the workspace.</span></span>

## <span data-ttu-id="df8a6-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="df8a6-114">PARAMETERS</span></span>

### <span data-ttu-id="df8a6-115">-ActionId</span><span class="sxs-lookup"><span data-stu-id="df8a6-115">-ActionId</span></span>
<span data-ttu-id="df8a6-116">ID azione.</span><span class="sxs-lookup"><span data-stu-id="df8a6-116">Action Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df8a6-117">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="df8a6-117">-AlertRuleId</span></span>
<span data-ttu-id="df8a6-118">ID regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="df8a6-118">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df8a6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df8a6-119">-DefaultProfile</span></span>
<span data-ttu-id="df8a6-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="df8a6-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df8a6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df8a6-121">-InputObject</span></span>
<span data-ttu-id="df8a6-122">InputObject.</span><span class="sxs-lookup"><span data-stu-id="df8a6-122">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df8a6-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df8a6-123">-PassThru</span></span>
<span data-ttu-id="df8a6-124">PassThru</span><span class="sxs-lookup"><span data-stu-id="df8a6-124">PassThru</span></span>

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

### <span data-ttu-id="df8a6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df8a6-125">-ResourceGroupName</span></span>
<span data-ttu-id="df8a6-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="df8a6-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df8a6-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="df8a6-127">-WorkspaceName</span></span>
<span data-ttu-id="df8a6-128">Nome area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="df8a6-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df8a6-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="df8a6-129">-Confirm</span></span>
<span data-ttu-id="df8a6-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df8a6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df8a6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df8a6-131">-WhatIf</span></span>
<span data-ttu-id="df8a6-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="df8a6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df8a6-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="df8a6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df8a6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df8a6-134">CommonParameters</span></span>
<span data-ttu-id="df8a6-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df8a6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df8a6-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df8a6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df8a6-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="df8a6-137">INPUTS</span></span>

### <span data-ttu-id="df8a6-138">System. String</span><span class="sxs-lookup"><span data-stu-id="df8a6-138">System.String</span></span>
### <span data-ttu-id="df8a6-139">Microsoft. Azure. Commands. SecurityInsights. Models. Actions. PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="df8a6-139">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="df8a6-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="df8a6-140">OUTPUTS</span></span>

### <span data-ttu-id="df8a6-141">Microsoft. Azure. Commands. SecurityInsights. Models. Actions. PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="df8a6-141">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="df8a6-142">Note</span><span class="sxs-lookup"><span data-stu-id="df8a6-142">NOTES</span></span>

## <span data-ttu-id="df8a6-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="df8a6-143">RELATED LINKS</span></span>
