---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/remove-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
ms.openlocfilehash: 4462434bcda1045afcc8478bbd9c4b7a1718d478
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199783"
---
# <span data-ttu-id="ee183-101">Remove-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="ee183-101">Remove-AzActionRule</span></span>

## <span data-ttu-id="ee183-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee183-102">SYNOPSIS</span></span>
<span data-ttu-id="ee183-103">Elimina una regola di azione</span><span class="sxs-lookup"><span data-stu-id="ee183-103">Deletes a action rule</span></span>

## <span data-ttu-id="ee183-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee183-104">SYNTAX</span></span>

### <span data-ttu-id="ee183-105">ByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ee183-105">ByName (Default)</span></span>
```
Remove-AzActionRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee183-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ee183-106">ByResourceId</span></span>
```
Remove-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee183-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ee183-107">ByInputObject</span></span>
```
Remove-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee183-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ee183-108">DESCRIPTION</span></span>
<span data-ttu-id="ee183-109">Il cmdlet **Remove-AzActionRule** elimina una regola di azione.</span><span class="sxs-lookup"><span data-stu-id="ee183-109">**Remove-AzActionRule** cmdlet deletes a action rule.</span></span>

## <span data-ttu-id="ee183-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee183-110">EXAMPLES</span></span>

### <span data-ttu-id="ee183-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ee183-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzActionRule -ResourceGroupName "test-rg" -Name "ActionRuleName"
```

<span data-ttu-id="ee183-112">Questo cmdlet elimina la regola di azione con nome ActionRuleName nel gruppo di risorse test-rg</span><span class="sxs-lookup"><span data-stu-id="ee183-112">This cmdlet deletes the action rule with name ActionRuleName in resource group test-rg</span></span>

## <span data-ttu-id="ee183-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee183-113">PARAMETERS</span></span>

### <span data-ttu-id="ee183-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee183-114">-DefaultProfile</span></span>
<span data-ttu-id="ee183-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ee183-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee183-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee183-116">-InputObject</span></span>
<span data-ttu-id="ee183-117">Risorsa regola azione</span><span class="sxs-lookup"><span data-stu-id="ee183-117">The action rule resource</span></span>

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

### <span data-ttu-id="ee183-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ee183-118">-Name</span></span>
<span data-ttu-id="ee183-119">Nome della regola di azione</span><span class="sxs-lookup"><span data-stu-id="ee183-119">Name of action rule</span></span>

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

### <span data-ttu-id="ee183-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee183-120">-PassThru</span></span>
<span data-ttu-id="ee183-121">PassThru restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="ee183-121">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="ee183-122">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="ee183-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ee183-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee183-123">-ResourceGroupName</span></span>
<span data-ttu-id="ee183-124">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ee183-124">Resource Group name</span></span>

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

### <span data-ttu-id="ee183-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee183-125">-ResourceId</span></span>
<span data-ttu-id="ee183-126">Ottenere la regola Azione in base all'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="ee183-126">Get Action rule by resource id.</span></span>

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

### <span data-ttu-id="ee183-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee183-127">-Confirm</span></span>
<span data-ttu-id="ee183-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee183-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee183-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee183-129">-WhatIf</span></span>
<span data-ttu-id="ee183-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee183-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee183-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee183-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee183-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee183-132">CommonParameters</span></span>
<span data-ttu-id="ee183-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee183-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee183-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ee183-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee183-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="ee183-135">INPUTS</span></span>

### <span data-ttu-id="ee183-136">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="ee183-136">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="ee183-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee183-137">OUTPUTS</span></span>

### <span data-ttu-id="ee183-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ee183-138">System.Boolean</span></span>

## <span data-ttu-id="ee183-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="ee183-139">NOTES</span></span>

## <span data-ttu-id="ee183-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee183-140">RELATED LINKS</span></span>
