---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: f8a50a7e9686a3e40f517992e6c4de9912e8671b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965102"
---
# <span data-ttu-id="1651a-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="1651a-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="1651a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1651a-102">SYNOPSIS</span></span>
<span data-ttu-id="1651a-103">Rimuovere un'assegnazione di progetto da una sottoscrizione o da un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="1651a-103">Remove a blueprint assignment from a subscription or a management group.</span></span>

## <span data-ttu-id="1651a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1651a-104">SYNTAX</span></span>

### <span data-ttu-id="1651a-105">BySubscriptionAndName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1651a-105">BySubscriptionAndName (Default)</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [[-SubscriptionId] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1651a-106">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="1651a-106">ByManagementGroupAndName</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [-ManagementGroupId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1651a-107">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="1651a-107">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment -InputObject <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1651a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1651a-108">DESCRIPTION</span></span>
<span data-ttu-id="1651a-109">Rimuovi una progetto progetto che è stata assegnata a un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="1651a-109">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="1651a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1651a-110">EXAMPLES</span></span>

### <span data-ttu-id="1651a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1651a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="1651a-112">Rimuovere l'assegnazione di progetto specificata dal nome dalla sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="1651a-112">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="1651a-113">Il cmdlet richiederà conferma prima di eseguire il comando.</span><span class="sxs-lookup"><span data-stu-id="1651a-113">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="1651a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1651a-114">PARAMETERS</span></span>

### <span data-ttu-id="1651a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1651a-115">-DefaultProfile</span></span>
<span data-ttu-id="1651a-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1651a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1651a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1651a-117">-InputObject</span></span>
<span data-ttu-id="1651a-118">Oggetto assegnazione progetto.</span><span class="sxs-lookup"><span data-stu-id="1651a-118">Blueprint assignment object.</span></span>

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

### <span data-ttu-id="1651a-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="1651a-119">-ManagementGroupId</span></span>
<span data-ttu-id="1651a-120">ID del gruppo di gestione in cui viene salvata l'assegnazione del progetto.</span><span class="sxs-lookup"><span data-stu-id="1651a-120">The ID of the management group where the Blueprint assignment is saved.</span></span>

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

### <span data-ttu-id="1651a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1651a-121">-Name</span></span>
<span data-ttu-id="1651a-122">Nome dell'attività del progetto.</span><span class="sxs-lookup"><span data-stu-id="1651a-122">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="1651a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1651a-123">-PassThru</span></span>
<span data-ttu-id="1651a-124">Quando è impostato, il cmdlet restituisce un oggetto che rappresenta l'assegnazione del progetto rimossa.</span><span class="sxs-lookup"><span data-stu-id="1651a-124">When set, the cmdlet will return an object representing the removed Blueprint assignment.</span></span> <span data-ttu-id="1651a-125">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="1651a-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1651a-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1651a-126">-SubscriptionId</span></span>
<span data-ttu-id="1651a-127">ID sottoscrizione a cui viene distribuita l'assegnazione della progetto.</span><span class="sxs-lookup"><span data-stu-id="1651a-127">Subscription Id the blueprint assignment is deployed to.</span></span>

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

### <span data-ttu-id="1651a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1651a-128">-Confirm</span></span>
<span data-ttu-id="1651a-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1651a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1651a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1651a-130">-WhatIf</span></span>
<span data-ttu-id="1651a-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1651a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1651a-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1651a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1651a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1651a-133">CommonParameters</span></span>
<span data-ttu-id="1651a-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1651a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1651a-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1651a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1651a-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="1651a-136">INPUTS</span></span>

### <span data-ttu-id="1651a-137">System.String</span><span class="sxs-lookup"><span data-stu-id="1651a-137">System.String</span></span>

### <span data-ttu-id="1651a-138">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span><span class="sxs-lookup"><span data-stu-id="1651a-138">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="1651a-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1651a-139">OUTPUTS</span></span>

### <span data-ttu-id="1651a-140">System.Object</span><span class="sxs-lookup"><span data-stu-id="1651a-140">System.Object</span></span>
## <span data-ttu-id="1651a-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="1651a-141">NOTES</span></span>

## <span data-ttu-id="1651a-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1651a-142">RELATED LINKS</span></span>
