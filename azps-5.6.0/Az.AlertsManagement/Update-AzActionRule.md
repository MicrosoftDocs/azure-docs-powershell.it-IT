---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/update-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
ms.openlocfilehash: 7dcbf947975719a30282037d592469a986990d50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993101"
---
# <span data-ttu-id="d7c0c-101">Update-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="d7c0c-101">Update-AzActionRule</span></span>

## <span data-ttu-id="d7c0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7c0c-102">SYNOPSIS</span></span>
<span data-ttu-id="d7c0c-103">Aggiorna le proprietà delle regole di azione.</span><span class="sxs-lookup"><span data-stu-id="d7c0c-103">Updates action rule properties.</span></span>

## <span data-ttu-id="d7c0c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d7c0c-104">SYNTAX</span></span>

### <span data-ttu-id="d7c0c-105">ByNameSimplifiedPatch (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d7c0c-105">ByNameSimplifiedPatch (Default)</span></span>
```
Update-AzActionRule -Name <String> -ResourceGroupName <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7c0c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d7c0c-106">ByResourceId</span></span>
```
Update-AzActionRule -ResourceId <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7c0c-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d7c0c-107">ByInputObject</span></span>
```
Update-AzActionRule -InputObject <PSActionRule> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7c0c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d7c0c-108">DESCRIPTION</span></span>
<span data-ttu-id="d7c0c-109">Il cmdlet **Update-AzActionRule** aggiorna le proprietà delle regole di azione, lo stato e i tag.</span><span class="sxs-lookup"><span data-stu-id="d7c0c-109">**Update-AzActionRule** cmdlet updates action rule properties - status and tags.</span></span>

## <span data-ttu-id="d7c0c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d7c0c-110">EXAMPLES</span></span>

### <span data-ttu-id="d7c0c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d7c0c-111">Example 1</span></span>
```powershell
PS C:\> Update-AzActionRule -ResourceGroupName "test-rg" -Name "Test-ActionRule" -Status "Disabled"
```

<span data-ttu-id="d7c0c-112">Questo cmdlet disabilita la regola di azione.</span><span class="sxs-lookup"><span data-stu-id="d7c0c-112">This cmdlet disables the action rule.</span></span> 

## <span data-ttu-id="d7c0c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7c0c-113">PARAMETERS</span></span>

### <span data-ttu-id="d7c0c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7c0c-114">-DefaultProfile</span></span>
<span data-ttu-id="d7c0c-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d7c0c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7c0c-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7c0c-116">-InputObject</span></span>
<span data-ttu-id="d7c0c-117">Risorsa regola azione</span><span class="sxs-lookup"><span data-stu-id="d7c0c-117">The action rule resource</span></span>

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

### <span data-ttu-id="d7c0c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d7c0c-118">-Name</span></span>
<span data-ttu-id="d7c0c-119">Nome regola azione</span><span class="sxs-lookup"><span data-stu-id="d7c0c-119">Action rule name</span></span>

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

### <span data-ttu-id="d7c0c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7c0c-120">-ResourceGroupName</span></span>
<span data-ttu-id="d7c0c-121">Nome regola azione</span><span class="sxs-lookup"><span data-stu-id="d7c0c-121">Action rule name</span></span>

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

### <span data-ttu-id="d7c0c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7c0c-122">-ResourceId</span></span>
<span data-ttu-id="d7c0c-123">ID risorsa della regola di azione</span><span class="sxs-lookup"><span data-stu-id="d7c0c-123">The resource id of action rule</span></span>

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

### <span data-ttu-id="d7c0c-124">-Stato</span><span class="sxs-lookup"><span data-stu-id="d7c0c-124">-Status</span></span>
<span data-ttu-id="d7c0c-125">Stato della regola di azione</span><span class="sxs-lookup"><span data-stu-id="d7c0c-125">Action rule status</span></span>

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

### <span data-ttu-id="d7c0c-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="d7c0c-126">-Tag</span></span>
<span data-ttu-id="d7c0c-127">Tag delle regole di azione</span><span class="sxs-lookup"><span data-stu-id="d7c0c-127">Action rule tags</span></span>

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

### <span data-ttu-id="d7c0c-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7c0c-128">-Confirm</span></span>
<span data-ttu-id="d7c0c-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7c0c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7c0c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7c0c-130">-WhatIf</span></span>
<span data-ttu-id="d7c0c-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d7c0c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7c0c-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d7c0c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7c0c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7c0c-133">CommonParameters</span></span>
<span data-ttu-id="d7c0c-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7c0c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7c0c-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d7c0c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7c0c-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="d7c0c-136">INPUTS</span></span>

### <span data-ttu-id="d7c0c-137">System.String</span><span class="sxs-lookup"><span data-stu-id="d7c0c-137">System.String</span></span>

### <span data-ttu-id="d7c0c-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="d7c0c-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="d7c0c-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d7c0c-139">OUTPUTS</span></span>

### <span data-ttu-id="d7c0c-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="d7c0c-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="d7c0c-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="d7c0c-141">NOTES</span></span>

## <span data-ttu-id="d7c0c-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d7c0c-142">RELATED LINKS</span></span>
