---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: 40452c250b58edf4d1e45f54c953dee8c433c436
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478072"
---
# <span data-ttu-id="6ff41-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="6ff41-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="6ff41-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6ff41-102">SYNOPSIS</span></span>
<span data-ttu-id="6ff41-103">Rimuovere un'assegnazione Blueprint da un abbonamento o da un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="6ff41-103">Remove a blueprint assignment from a subscription or a management group.</span></span>

## <span data-ttu-id="6ff41-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ff41-104">SYNTAX</span></span>

### <span data-ttu-id="6ff41-105">BySubscriptionAndName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6ff41-105">BySubscriptionAndName (Default)</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [[-SubscriptionId] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ff41-106">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="6ff41-106">ByManagementGroupAndName</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [-ManagementGroupId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ff41-107">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="6ff41-107">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment -InputObject <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ff41-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ff41-108">DESCRIPTION</span></span>
<span data-ttu-id="6ff41-109">Rimuovere un modello assegnato a un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6ff41-109">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="6ff41-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ff41-110">EXAMPLES</span></span>

### <span data-ttu-id="6ff41-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6ff41-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="6ff41-112">Rimuovere l'assegnazione Blueprint specificata per nome dall'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="6ff41-112">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="6ff41-113">Il cmdlet richiederà la conferma prima di eseguire il comando.</span><span class="sxs-lookup"><span data-stu-id="6ff41-113">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="6ff41-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6ff41-114">PARAMETERS</span></span>

### <span data-ttu-id="6ff41-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ff41-115">-DefaultProfile</span></span>
<span data-ttu-id="6ff41-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6ff41-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ff41-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ff41-117">-InputObject</span></span>
<span data-ttu-id="6ff41-118">Oggetto assegnazione Blueprint.</span><span class="sxs-lookup"><span data-stu-id="6ff41-118">Blueprint assignment object.</span></span>

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

### <span data-ttu-id="6ff41-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="6ff41-119">-ManagementGroupId</span></span>
<span data-ttu-id="6ff41-120">ID del gruppo di gestione in cui viene salvata l'assegnazione Blueprint.</span><span class="sxs-lookup"><span data-stu-id="6ff41-120">The ID of the management group where the Blueprint assignment is saved.</span></span>

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

### <span data-ttu-id="6ff41-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="6ff41-121">-Name</span></span>
<span data-ttu-id="6ff41-122">Nome assegnazione modello.</span><span class="sxs-lookup"><span data-stu-id="6ff41-122">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="6ff41-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ff41-123">-PassThru</span></span>
<span data-ttu-id="6ff41-124">Quando viene impostato, il cmdlet restituirà un oggetto che rappresenta l'assegnazione del modello rimosso.</span><span class="sxs-lookup"><span data-stu-id="6ff41-124">When set, the cmdlet will return an object representing the removed Blueprint assignment.</span></span> <span data-ttu-id="6ff41-125">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="6ff41-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6ff41-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6ff41-126">-SubscriptionId</span></span>
<span data-ttu-id="6ff41-127">ID abbonamento a cui è distribuita l'assegnazione Blueprint.</span><span class="sxs-lookup"><span data-stu-id="6ff41-127">Subscription Id the blueprint assignment is deployed to.</span></span>

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

### <span data-ttu-id="6ff41-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6ff41-128">-Confirm</span></span>
<span data-ttu-id="6ff41-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ff41-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ff41-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ff41-130">-WhatIf</span></span>
<span data-ttu-id="6ff41-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ff41-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ff41-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ff41-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ff41-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ff41-133">CommonParameters</span></span>
<span data-ttu-id="6ff41-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ff41-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ff41-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ff41-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ff41-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6ff41-136">INPUTS</span></span>

### <span data-ttu-id="6ff41-137">System. String</span><span class="sxs-lookup"><span data-stu-id="6ff41-137">System.String</span></span>

### <span data-ttu-id="6ff41-138">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintAssignment []</span><span class="sxs-lookup"><span data-stu-id="6ff41-138">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="6ff41-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ff41-139">OUTPUTS</span></span>

### <span data-ttu-id="6ff41-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="6ff41-140">System.Object</span></span>
## <span data-ttu-id="6ff41-141">Note</span><span class="sxs-lookup"><span data-stu-id="6ff41-141">NOTES</span></span>

## <span data-ttu-id="6ff41-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ff41-142">RELATED LINKS</span></span>
