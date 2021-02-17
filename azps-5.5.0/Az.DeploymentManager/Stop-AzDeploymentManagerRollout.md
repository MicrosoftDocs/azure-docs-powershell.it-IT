---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/stop-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
ms.openlocfilehash: cd59cd39fb2834bed2162a257905fea643c0a767
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196486"
---
# <span data-ttu-id="42d54-101">Stop-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="42d54-101">Stop-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="42d54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42d54-102">SYNOPSIS</span></span>
<span data-ttu-id="42d54-103">Interrompe l'implementazione.</span><span class="sxs-lookup"><span data-stu-id="42d54-103">Stops the rollout.</span></span>

## <span data-ttu-id="42d54-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42d54-104">SYNTAX</span></span>

### <span data-ttu-id="42d54-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="42d54-105">Interactive (Default)</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42d54-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="42d54-106">ResourceId</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42d54-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="42d54-107">InputObject</span></span>
```
Stop-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42d54-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="42d54-108">DESCRIPTION</span></span>
<span data-ttu-id="42d54-109">Il cmdlet **Stop-AzDeploymentManagerRollout** interrompe un'implementazione in corso e restituisce un oggetto che rappresenta lo stato corrente dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="42d54-109">The **Stop-AzDeploymentManagerRollout** cmdlet stops a rollout in progress and returns an object that represents the current state of the rollout.</span></span>
<span data-ttu-id="42d54-110">Specificare l'implementazione in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="42d54-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="42d54-111">In alternativa, è possibile specificare l'oggetto Rollout o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="42d54-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="42d54-112">Una volta interrotta un'implementazione, non è possibile riprenderla o riavviarla.</span><span class="sxs-lookup"><span data-stu-id="42d54-112">Note that once a rollout is stopped, it cannot be resumed or restarted.</span></span> <span data-ttu-id="42d54-113">È possibile creare solo una nuova implementazione.</span><span class="sxs-lookup"><span data-stu-id="42d54-113">You can only create a new rollout.</span></span>

## <span data-ttu-id="42d54-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42d54-114">EXAMPLES</span></span>

### <span data-ttu-id="42d54-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="42d54-115">Example 1</span></span>
```powershell
PS C:\> Stop-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="42d54-116">Questo comando interrompe un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="42d54-116">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="42d54-117">Esempio 2: Interrompere un'implementazione con l'identificatore di risorsa</span><span class="sxs-lookup"><span data-stu-id="42d54-117">Example 2: Stop a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="42d54-118">Questo comando interrompe un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="42d54-118">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="42d54-119">Esempio 3: Interrompere un'implementazione usando l'oggetto di implementazione.</span><span class="sxs-lookup"><span data-stu-id="42d54-119">Example 3: Stop a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="42d54-120">Questo comando interrompe un'implementazione il cui nome e GruppoSocietà Risorse corrispondono rispettivamente alle proprietà Name e ResourceGroupName dell'$rolloutObject.</span><span class="sxs-lookup"><span data-stu-id="42d54-120">This command stops a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="42d54-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42d54-121">PARAMETERS</span></span>

### <span data-ttu-id="42d54-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42d54-122">-DefaultProfile</span></span>
<span data-ttu-id="42d54-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="42d54-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42d54-124">-Force</span><span class="sxs-lookup"><span data-stu-id="42d54-124">-Force</span></span>
<span data-ttu-id="42d54-125">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="42d54-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="42d54-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42d54-126">-InputObject</span></span>
<span data-ttu-id="42d54-127">L'implementazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="42d54-127">The rollout to be removed.</span></span>

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

### <span data-ttu-id="42d54-128">-Name</span><span class="sxs-lookup"><span data-stu-id="42d54-128">-Name</span></span>
<span data-ttu-id="42d54-129">Nome dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="42d54-129">The name of the rollout.</span></span>

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

### <span data-ttu-id="42d54-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42d54-130">-ResourceGroupName</span></span>
<span data-ttu-id="42d54-131">Gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="42d54-131">The resource group.</span></span>

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

### <span data-ttu-id="42d54-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42d54-132">-ResourceId</span></span>
<span data-ttu-id="42d54-133">L'identificatore di risorsa.</span><span class="sxs-lookup"><span data-stu-id="42d54-133">The resource identifier.</span></span>

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

### <span data-ttu-id="42d54-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42d54-134">-Confirm</span></span>
<span data-ttu-id="42d54-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42d54-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42d54-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42d54-136">-WhatIf</span></span>
<span data-ttu-id="42d54-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="42d54-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42d54-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="42d54-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42d54-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42d54-139">CommonParameters</span></span>
<span data-ttu-id="42d54-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42d54-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42d54-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="42d54-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42d54-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="42d54-142">INPUTS</span></span>

### <span data-ttu-id="42d54-143">System.String</span><span class="sxs-lookup"><span data-stu-id="42d54-143">System.String</span></span>

### <span data-ttu-id="42d54-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="42d54-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="42d54-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42d54-145">OUTPUTS</span></span>

### <span data-ttu-id="42d54-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="42d54-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="42d54-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="42d54-147">NOTES</span></span>

## <span data-ttu-id="42d54-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42d54-148">RELATED LINKS</span></span>
