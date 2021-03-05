---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/remove-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
ms.openlocfilehash: 7e34a37e0375c90fb5d36ce37c821c3b2c2fd69a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960942"
---
# <span data-ttu-id="17e61-101">Remove-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="17e61-101">Remove-AzActionRule</span></span>

## <span data-ttu-id="17e61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17e61-102">SYNOPSIS</span></span>
<span data-ttu-id="17e61-103">Elimina una regola di azione</span><span class="sxs-lookup"><span data-stu-id="17e61-103">Deletes a action rule</span></span>

## <span data-ttu-id="17e61-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="17e61-104">SYNTAX</span></span>

### <span data-ttu-id="17e61-105">ByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="17e61-105">ByName (Default)</span></span>
```
Remove-AzActionRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17e61-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="17e61-106">ByResourceId</span></span>
```
Remove-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17e61-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="17e61-107">ByInputObject</span></span>
```
Remove-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17e61-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="17e61-108">DESCRIPTION</span></span>
<span data-ttu-id="17e61-109">Il cmdlet **Remove-AzActionRule** elimina una regola di azione.</span><span class="sxs-lookup"><span data-stu-id="17e61-109">**Remove-AzActionRule** cmdlet deletes a action rule.</span></span>

## <span data-ttu-id="17e61-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="17e61-110">EXAMPLES</span></span>

### <span data-ttu-id="17e61-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="17e61-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzActionRule -ResourceGroupName "test-rg" -Name "ActionRuleName"
```

<span data-ttu-id="17e61-112">Questo cmdlet elimina la regola di azione con nome ActionRuleName nel gruppo di risorse test-rg</span><span class="sxs-lookup"><span data-stu-id="17e61-112">This cmdlet deletes the action rule with name ActionRuleName in resource group test-rg</span></span>

## <span data-ttu-id="17e61-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17e61-113">PARAMETERS</span></span>

### <span data-ttu-id="17e61-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17e61-114">-DefaultProfile</span></span>
<span data-ttu-id="17e61-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="17e61-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17e61-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17e61-116">-InputObject</span></span>
<span data-ttu-id="17e61-117">Risorsa regola azione</span><span class="sxs-lookup"><span data-stu-id="17e61-117">The action rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17e61-118">-Name</span><span class="sxs-lookup"><span data-stu-id="17e61-118">-Name</span></span>
<span data-ttu-id="17e61-119">Nome della regola di azione</span><span class="sxs-lookup"><span data-stu-id="17e61-119">Name of action rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e61-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="17e61-120">-PassThru</span></span>
<span data-ttu-id="17e61-121">PassThru restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="17e61-121">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="17e61-122">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="17e61-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="17e61-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17e61-123">-ResourceGroupName</span></span>
<span data-ttu-id="17e61-124">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="17e61-124">Resource Group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e61-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17e61-125">-ResourceId</span></span>
<span data-ttu-id="17e61-126">Ottenere la regola Azione in base all'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="17e61-126">Get Action rule by resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17e61-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17e61-127">-Confirm</span></span>
<span data-ttu-id="17e61-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17e61-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17e61-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17e61-129">-WhatIf</span></span>
<span data-ttu-id="17e61-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="17e61-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17e61-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="17e61-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17e61-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17e61-132">CommonParameters</span></span>
<span data-ttu-id="17e61-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17e61-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17e61-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="17e61-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17e61-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="17e61-135">INPUTS</span></span>

### <span data-ttu-id="17e61-136">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="17e61-136">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="17e61-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="17e61-137">OUTPUTS</span></span>

### <span data-ttu-id="17e61-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="17e61-138">System.Boolean</span></span>

## <span data-ttu-id="17e61-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="17e61-139">NOTES</span></span>

## <span data-ttu-id="17e61-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="17e61-140">RELATED LINKS</span></span>
