---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: 40452c250b58edf4d1e45f54c953dee8c433c436
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181935"
---
# <span data-ttu-id="d1fe3-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="d1fe3-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="d1fe3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1fe3-102">SYNOPSIS</span></span>
<span data-ttu-id="d1fe3-103">Rimuovere un'assegnazione di progetto da una sottoscrizione o da un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="d1fe3-103">Remove a blueprint assignment from a subscription or a management group.</span></span>

## <span data-ttu-id="d1fe3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1fe3-104">SYNTAX</span></span>

### <span data-ttu-id="d1fe3-105">BySubscriptionAndName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d1fe3-105">BySubscriptionAndName (Default)</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [[-SubscriptionId] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1fe3-106">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="d1fe3-106">ByManagementGroupAndName</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [-ManagementGroupId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1fe3-107">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="d1fe3-107">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment -InputObject <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1fe3-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d1fe3-108">DESCRIPTION</span></span>
<span data-ttu-id="d1fe3-109">Rimuovere una progetto a cui è stata assegnata una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="d1fe3-109">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="d1fe3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1fe3-110">EXAMPLES</span></span>

### <span data-ttu-id="d1fe3-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d1fe3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="d1fe3-112">Rimuovere l'assegnazione di progetto specificata dal nome dalla sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="d1fe3-112">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="d1fe3-113">Il cmdlet richiederà conferma prima di eseguire il comando.</span><span class="sxs-lookup"><span data-stu-id="d1fe3-113">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="d1fe3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1fe3-114">PARAMETERS</span></span>

### <span data-ttu-id="d1fe3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1fe3-115">-DefaultProfile</span></span>
<span data-ttu-id="d1fe3-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d1fe3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1fe3-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1fe3-117">-InputObject</span></span>
<span data-ttu-id="d1fe3-118">Oggetto assegnazione progetto.</span><span class="sxs-lookup"><span data-stu-id="d1fe3-118">Blueprint assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1fe3-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="d1fe3-119">-ManagementGroupId</span></span>
<span data-ttu-id="d1fe3-120">ID del gruppo di gestione in cui viene salvata l'assegnazione del progetto.</span><span class="sxs-lookup"><span data-stu-id="d1fe3-120">The ID of the management group where the Blueprint assignment is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1fe3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d1fe3-121">-Name</span></span>
<span data-ttu-id="d1fe3-122">Nome dell'attività del progetto.</span><span class="sxs-lookup"><span data-stu-id="d1fe3-122">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, ByManagementGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1fe3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1fe3-123">-PassThru</span></span>
<span data-ttu-id="d1fe3-124">Quando è impostato, il cmdlet restituisce un oggetto che rappresenta l'assegnazione del progetto rimossa.</span><span class="sxs-lookup"><span data-stu-id="d1fe3-124">When set, the cmdlet will return an object representing the removed Blueprint assignment.</span></span> <span data-ttu-id="d1fe3-125">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="d1fe3-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d1fe3-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d1fe3-126">-SubscriptionId</span></span>
<span data-ttu-id="d1fe3-127">ID sottoscrizione a cui viene distribuita l'assegnazione della progetto.</span><span class="sxs-lookup"><span data-stu-id="d1fe3-127">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1fe3-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1fe3-128">-Confirm</span></span>
<span data-ttu-id="d1fe3-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1fe3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1fe3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1fe3-130">-WhatIf</span></span>
<span data-ttu-id="d1fe3-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d1fe3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1fe3-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d1fe3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1fe3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1fe3-133">CommonParameters</span></span>
<span data-ttu-id="d1fe3-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1fe3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1fe3-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d1fe3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1fe3-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="d1fe3-136">INPUTS</span></span>

### <span data-ttu-id="d1fe3-137">System.String</span><span class="sxs-lookup"><span data-stu-id="d1fe3-137">System.String</span></span>

### <span data-ttu-id="d1fe3-138">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span><span class="sxs-lookup"><span data-stu-id="d1fe3-138">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="d1fe3-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1fe3-139">OUTPUTS</span></span>

### <span data-ttu-id="d1fe3-140">System.Object</span><span class="sxs-lookup"><span data-stu-id="d1fe3-140">System.Object</span></span>
## <span data-ttu-id="d1fe3-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="d1fe3-141">NOTES</span></span>

## <span data-ttu-id="d1fe3-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1fe3-142">RELATED LINKS</span></span>
