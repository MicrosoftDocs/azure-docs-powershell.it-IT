---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
ms.openlocfilehash: 2af687a79255d5e5ab4b49135bf8a8f7b8f819f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205891"
---
# <span data-ttu-id="84170-101">Update-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="84170-101">Update-AzActionRule</span></span>

## <span data-ttu-id="84170-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84170-102">SYNOPSIS</span></span>
<span data-ttu-id="84170-103">Aggiorna le proprietà delle regole di azione.</span><span class="sxs-lookup"><span data-stu-id="84170-103">Updates action rule properties.</span></span>

## <span data-ttu-id="84170-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84170-104">SYNTAX</span></span>

### <span data-ttu-id="84170-105">ByNameSimplifiedPatch (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="84170-105">ByNameSimplifiedPatch (Default)</span></span>
```
Update-AzActionRule -Name <String> -ResourceGroupName <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84170-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="84170-106">ByResourceId</span></span>
```
Update-AzActionRule -ResourceId <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84170-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="84170-107">ByInputObject</span></span>
```
Update-AzActionRule -InputObject <PSActionRule> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84170-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="84170-108">DESCRIPTION</span></span>
<span data-ttu-id="84170-109">Il cmdlet **Update-AzActionRule** aggiorna le proprietà delle regole di azione, lo stato e i tag.</span><span class="sxs-lookup"><span data-stu-id="84170-109">**Update-AzActionRule** cmdlet updates action rule properties - status and tags.</span></span>

## <span data-ttu-id="84170-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84170-110">EXAMPLES</span></span>

### <span data-ttu-id="84170-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="84170-111">Example 1</span></span>
```powershell
PS C:\> Update-AzActionRule -ResourceGroupName "test-rg" -Name "Test-ActionRule" -Status "Disabled"
```

<span data-ttu-id="84170-112">Questo cmdlet disabilita la regola di azione.</span><span class="sxs-lookup"><span data-stu-id="84170-112">This cmdlet disables the action rule.</span></span> 

## <span data-ttu-id="84170-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84170-113">PARAMETERS</span></span>

### <span data-ttu-id="84170-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84170-114">-DefaultProfile</span></span>
<span data-ttu-id="84170-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="84170-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84170-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84170-116">-InputObject</span></span>
<span data-ttu-id="84170-117">Risorsa regola azione</span><span class="sxs-lookup"><span data-stu-id="84170-117">The action rule resource</span></span>

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

### <span data-ttu-id="84170-118">-Name</span><span class="sxs-lookup"><span data-stu-id="84170-118">-Name</span></span>
<span data-ttu-id="84170-119">Nome regola azione</span><span class="sxs-lookup"><span data-stu-id="84170-119">Action rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84170-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84170-120">-ResourceGroupName</span></span>
<span data-ttu-id="84170-121">Nome regola azione</span><span class="sxs-lookup"><span data-stu-id="84170-121">Action rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84170-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84170-122">-ResourceId</span></span>
<span data-ttu-id="84170-123">ID risorsa della regola di azione</span><span class="sxs-lookup"><span data-stu-id="84170-123">The resource id of action rule</span></span>

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

### <span data-ttu-id="84170-124">-Stato</span><span class="sxs-lookup"><span data-stu-id="84170-124">-Status</span></span>
<span data-ttu-id="84170-125">Stato della regola di azione</span><span class="sxs-lookup"><span data-stu-id="84170-125">Action rule status</span></span>

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

### <span data-ttu-id="84170-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="84170-126">-Tag</span></span>
<span data-ttu-id="84170-127">Tag delle regole di azione</span><span class="sxs-lookup"><span data-stu-id="84170-127">Action rule tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84170-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84170-128">-Confirm</span></span>
<span data-ttu-id="84170-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84170-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84170-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84170-130">-WhatIf</span></span>
<span data-ttu-id="84170-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84170-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84170-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84170-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84170-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84170-133">CommonParameters</span></span>
<span data-ttu-id="84170-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84170-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84170-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="84170-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84170-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="84170-136">INPUTS</span></span>

### <span data-ttu-id="84170-137">System.String</span><span class="sxs-lookup"><span data-stu-id="84170-137">System.String</span></span>

### <span data-ttu-id="84170-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="84170-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="84170-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84170-139">OUTPUTS</span></span>

### <span data-ttu-id="84170-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="84170-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="84170-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="84170-141">NOTES</span></span>

## <span data-ttu-id="84170-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84170-142">RELATED LINKS</span></span>
