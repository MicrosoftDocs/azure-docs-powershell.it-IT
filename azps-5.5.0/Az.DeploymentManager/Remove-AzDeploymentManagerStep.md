---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
ms.openlocfilehash: 5e4af2ef006e51cee135dd642bcae7282940e8be
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198014"
---
# <span data-ttu-id="89c2b-101">Remove-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="89c2b-101">Remove-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="89c2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89c2b-102">SYNOPSIS</span></span>
<span data-ttu-id="89c2b-103">Elimina il passaggio.</span><span class="sxs-lookup"><span data-stu-id="89c2b-103">Deletes the step.</span></span>

## <span data-ttu-id="89c2b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="89c2b-104">SYNTAX</span></span>

### <span data-ttu-id="89c2b-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="89c2b-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89c2b-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="89c2b-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89c2b-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="89c2b-107">InputObject</span></span>
```
Remove-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89c2b-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="89c2b-108">DESCRIPTION</span></span>
<span data-ttu-id="89c2b-109">Il cmdlet **Remove-AzDeploymentManagerStep** elimina un passaggio.</span><span class="sxs-lookup"><span data-stu-id="89c2b-109">The **Remove-AzDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="89c2b-110">Specificare il passaggio in base al nome e al gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="89c2b-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="89c2b-111">In alternativa, è possibile specificare l'oggetto Step o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="89c2b-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="89c2b-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="89c2b-112">EXAMPLES</span></span>

### <span data-ttu-id="89c2b-113">Esempio 1: Rimuovere un passaggio</span><span class="sxs-lookup"><span data-stu-id="89c2b-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="89c2b-114">Questo comando elimina un passaggio denominato ContosoService1WaitStep in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="89c2b-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="89c2b-115">Esempio 2: Rimuovere un passaggio usando l'identificatore di risorsa</span><span class="sxs-lookup"><span data-stu-id="89c2b-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="89c2b-116">Questo comando elimina un passaggio denominato ContosoService1WaitStep in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="89c2b-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="89c2b-117">Esempio 3: Rimuovere un passaggio usando un oggetto restituito da New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="89c2b-117">Example 3: Remove a step using an object returned by New-AzDeploymentManagerStep</span></span>
### <span data-ttu-id="89c2b-118">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="89c2b-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="89c2b-119">Questo comando elimina un passaggio il cui nome e gruppo di risorse corrispondono rispettivamente alle proprietà Name e ResourceGroupName dell'$stepObject.</span><span class="sxs-lookup"><span data-stu-id="89c2b-119">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="89c2b-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89c2b-120">PARAMETERS</span></span>

### <span data-ttu-id="89c2b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89c2b-121">-DefaultProfile</span></span>
<span data-ttu-id="89c2b-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="89c2b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89c2b-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89c2b-123">-InputObject</span></span>
<span data-ttu-id="89c2b-124">Il passaggio da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="89c2b-124">The step to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89c2b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="89c2b-125">-Name</span></span>
<span data-ttu-id="89c2b-126">Nome del passaggio.</span><span class="sxs-lookup"><span data-stu-id="89c2b-126">The name of the step.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89c2b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89c2b-127">-PassThru</span></span>
<span data-ttu-id="89c2b-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="89c2b-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="89c2b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89c2b-129">-ResourceGroupName</span></span>
<span data-ttu-id="89c2b-130">Gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="89c2b-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89c2b-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89c2b-131">-ResourceId</span></span>
<span data-ttu-id="89c2b-132">L'identificatore di risorsa.</span><span class="sxs-lookup"><span data-stu-id="89c2b-132">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89c2b-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89c2b-133">-Confirm</span></span>
<span data-ttu-id="89c2b-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89c2b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89c2b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89c2b-135">-WhatIf</span></span>
<span data-ttu-id="89c2b-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="89c2b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89c2b-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="89c2b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89c2b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89c2b-138">CommonParameters</span></span>
<span data-ttu-id="89c2b-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89c2b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89c2b-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="89c2b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89c2b-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="89c2b-141">INPUTS</span></span>

### <span data-ttu-id="89c2b-142">System.String</span><span class="sxs-lookup"><span data-stu-id="89c2b-142">System.String</span></span>

### <span data-ttu-id="89c2b-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="89c2b-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="89c2b-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="89c2b-144">OUTPUTS</span></span>

### <span data-ttu-id="89c2b-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="89c2b-145">System.Boolean</span></span>

## <span data-ttu-id="89c2b-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="89c2b-146">NOTES</span></span>

## <span data-ttu-id="89c2b-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="89c2b-147">RELATED LINKS</span></span>
