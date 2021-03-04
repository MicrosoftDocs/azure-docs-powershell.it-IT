---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
ms.openlocfilehash: 96f5f9e3dd0390d714b0ee7a74b3f585b46dcc1b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966302"
---
# <span data-ttu-id="6dda6-101">Remove-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="6dda6-101">Remove-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="6dda6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6dda6-102">SYNOPSIS</span></span>
<span data-ttu-id="6dda6-103">Elimina il passaggio.</span><span class="sxs-lookup"><span data-stu-id="6dda6-103">Deletes the step.</span></span>

## <span data-ttu-id="6dda6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6dda6-104">SYNTAX</span></span>

### <span data-ttu-id="6dda6-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6dda6-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6dda6-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6dda6-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6dda6-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="6dda6-107">InputObject</span></span>
```
Remove-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6dda6-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6dda6-108">DESCRIPTION</span></span>
<span data-ttu-id="6dda6-109">Il cmdlet **Remove-AzDeploymentManagerStep** elimina un passaggio.</span><span class="sxs-lookup"><span data-stu-id="6dda6-109">The **Remove-AzDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="6dda6-110">Specificare il passaggio in base al nome e al gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6dda6-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="6dda6-111">In alternativa, è possibile specificare l'oggetto Step o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="6dda6-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="6dda6-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6dda6-112">EXAMPLES</span></span>

### <span data-ttu-id="6dda6-113">Esempio 1: Rimuovere un passaggio</span><span class="sxs-lookup"><span data-stu-id="6dda6-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="6dda6-114">Questo comando elimina un passaggio denominato ContosoService1WaitStep in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6dda6-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="6dda6-115">Esempio 2: Rimuovere un passaggio con l'identificatore di risorsa</span><span class="sxs-lookup"><span data-stu-id="6dda6-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="6dda6-116">Questo comando elimina un passaggio denominato ContosoService1WaitStep in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6dda6-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="6dda6-117">Esempio 3: Rimuovere un passaggio usando un oggetto restituito da New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="6dda6-117">Example 3: Remove a step using an object returned by New-AzDeploymentManagerStep</span></span>
### <span data-ttu-id="6dda6-118">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6dda6-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="6dda6-119">Questo comando elimina un passaggio il cui nome e GruppoSocietà Risorse corrispondono rispettivamente alle proprietà Name e ResourceGroupName dell'$stepObject.</span><span class="sxs-lookup"><span data-stu-id="6dda6-119">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="6dda6-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6dda6-120">PARAMETERS</span></span>

### <span data-ttu-id="6dda6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dda6-121">-DefaultProfile</span></span>
<span data-ttu-id="6dda6-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6dda6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dda6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6dda6-123">-InputObject</span></span>
<span data-ttu-id="6dda6-124">Il passaggio da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6dda6-124">The step to be removed.</span></span>

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

### <span data-ttu-id="6dda6-125">-Name</span><span class="sxs-lookup"><span data-stu-id="6dda6-125">-Name</span></span>
<span data-ttu-id="6dda6-126">Nome del passaggio.</span><span class="sxs-lookup"><span data-stu-id="6dda6-126">The name of the step.</span></span>

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

### <span data-ttu-id="6dda6-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6dda6-127">-PassThru</span></span>
<span data-ttu-id="6dda6-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6dda6-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="6dda6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dda6-129">-ResourceGroupName</span></span>
<span data-ttu-id="6dda6-130">Gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6dda6-130">The resource group.</span></span>

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

### <span data-ttu-id="6dda6-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6dda6-131">-ResourceId</span></span>
<span data-ttu-id="6dda6-132">L'identificatore di risorsa.</span><span class="sxs-lookup"><span data-stu-id="6dda6-132">The resource identifier.</span></span>

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

### <span data-ttu-id="6dda6-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6dda6-133">-Confirm</span></span>
<span data-ttu-id="6dda6-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dda6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dda6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dda6-135">-WhatIf</span></span>
<span data-ttu-id="6dda6-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6dda6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6dda6-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6dda6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dda6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dda6-138">CommonParameters</span></span>
<span data-ttu-id="6dda6-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dda6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dda6-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6dda6-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dda6-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="6dda6-141">INPUTS</span></span>

### <span data-ttu-id="6dda6-142">System.String</span><span class="sxs-lookup"><span data-stu-id="6dda6-142">System.String</span></span>

### <span data-ttu-id="6dda6-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="6dda6-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="6dda6-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6dda6-144">OUTPUTS</span></span>

### <span data-ttu-id="6dda6-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6dda6-145">System.Boolean</span></span>

## <span data-ttu-id="6dda6-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="6dda6-146">NOTES</span></span>

## <span data-ttu-id="6dda6-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6dda6-147">RELATED LINKS</span></span>
