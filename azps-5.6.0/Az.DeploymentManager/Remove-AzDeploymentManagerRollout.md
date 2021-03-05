---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
ms.openlocfilehash: 3ade9bfd724a84e162c0cedd937f2255ebb5b6a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980701"
---
# <span data-ttu-id="60b05-101">Remove-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="60b05-101">Remove-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="60b05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60b05-102">SYNOPSIS</span></span>
<span data-ttu-id="60b05-103">Elimina l'implementazione.</span><span class="sxs-lookup"><span data-stu-id="60b05-103">Deletes the rollout.</span></span>

## <span data-ttu-id="60b05-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60b05-104">SYNTAX</span></span>

### <span data-ttu-id="60b05-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="60b05-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60b05-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="60b05-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60b05-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="60b05-107">InputObject</span></span>
```
Remove-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60b05-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="60b05-108">DESCRIPTION</span></span>
<span data-ttu-id="60b05-109">Il cmdlet **Remove-AzDeploymentManagerRollout** elimina un'implementazione in uno stato terminale.</span><span class="sxs-lookup"><span data-stu-id="60b05-109">The **Remove-AzDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="60b05-110">Specificare l'implementazione in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="60b05-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="60b05-111">In alternativa, è possibile specificare l'oggetto Rollout o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="60b05-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="60b05-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60b05-112">EXAMPLES</span></span>

### <span data-ttu-id="60b05-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="60b05-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="60b05-114">Questo comando elimina un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="60b05-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="60b05-115">Esempio 2: Eliminare un'implementazione con l'identificatore di risorsa</span><span class="sxs-lookup"><span data-stu-id="60b05-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="60b05-116">Questo comando elimina un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="60b05-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="60b05-117">Esempio 3: Eliminare un'implementazione usando l'oggetto di implementazione.</span><span class="sxs-lookup"><span data-stu-id="60b05-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="60b05-118">Questo comando elimina un'implementazione il cui nome e Gruppo Di risorse corrispondono rispettivamente alle proprietà Name e ResourceGroupName dell'$rolloutObject.</span><span class="sxs-lookup"><span data-stu-id="60b05-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="60b05-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60b05-119">PARAMETERS</span></span>

### <span data-ttu-id="60b05-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60b05-120">-DefaultProfile</span></span>
<span data-ttu-id="60b05-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60b05-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60b05-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60b05-122">-InputObject</span></span>
<span data-ttu-id="60b05-123">La risorsa da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="60b05-123">The resource to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60b05-124">-Name</span><span class="sxs-lookup"><span data-stu-id="60b05-124">-Name</span></span>
<span data-ttu-id="60b05-125">Nome dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="60b05-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="60b05-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60b05-126">-PassThru</span></span>
<span data-ttu-id="60b05-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="60b05-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="60b05-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60b05-128">-ResourceGroupName</span></span>
<span data-ttu-id="60b05-129">Gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="60b05-129">The resource group.</span></span>

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

### <span data-ttu-id="60b05-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60b05-130">-ResourceId</span></span>
<span data-ttu-id="60b05-131">L'identificatore di risorsa.</span><span class="sxs-lookup"><span data-stu-id="60b05-131">The resource identifier.</span></span>

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

### <span data-ttu-id="60b05-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60b05-132">-Confirm</span></span>
<span data-ttu-id="60b05-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60b05-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60b05-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60b05-134">-WhatIf</span></span>
<span data-ttu-id="60b05-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60b05-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60b05-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60b05-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60b05-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60b05-137">CommonParameters</span></span>
<span data-ttu-id="60b05-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60b05-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60b05-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="60b05-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60b05-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="60b05-140">INPUTS</span></span>

### <span data-ttu-id="60b05-141">System.String</span><span class="sxs-lookup"><span data-stu-id="60b05-141">System.String</span></span>

### <span data-ttu-id="60b05-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="60b05-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="60b05-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60b05-143">OUTPUTS</span></span>

### <span data-ttu-id="60b05-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="60b05-144">System.Boolean</span></span>

## <span data-ttu-id="60b05-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="60b05-145">NOTES</span></span>

## <span data-ttu-id="60b05-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60b05-146">RELATED LINKS</span></span>
