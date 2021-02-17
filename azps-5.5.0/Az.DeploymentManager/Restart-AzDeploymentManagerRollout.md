---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/restart-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
ms.openlocfilehash: ba7b62d42764f5098868e6a15eb073cb6b898e82
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194527"
---
# <span data-ttu-id="8bc98-101">Restart-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="8bc98-101">Restart-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="8bc98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bc98-102">SYNOPSIS</span></span>
<span data-ttu-id="8bc98-103">Riavvia un'implementazione non riuscita.</span><span class="sxs-lookup"><span data-stu-id="8bc98-103">Restarts a failed rollout.</span></span>

## <span data-ttu-id="8bc98-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8bc98-104">SYNTAX</span></span>

### <span data-ttu-id="8bc98-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8bc98-105">Interactive (Default)</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bc98-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8bc98-106">ResourceId</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceId] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8bc98-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="8bc98-107">InputObject</span></span>
```
Restart-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8bc98-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8bc98-108">DESCRIPTION</span></span>
<span data-ttu-id="8bc98-109">Il cmdlet **Restart-AzDeploymentManagerRollout** riavvia un'implementazione non riuscita e restituisce un oggetto che rappresenta l'implementazione con tutte le informazioni dettagliate sullo stato dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="8bc98-109">The **Restart-AzDeploymentManagerRollout** cmdlet restarts a failed rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="8bc98-110">Specificare l'implementazione in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8bc98-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="8bc98-111">In alternativa, è possibile specificare l'oggetto Rollout o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="8bc98-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>
<span data-ttu-id="8bc98-112">Il parametro facoltativo SkipSucceeded consente di ignorare tutti i passaggi successivi dell'esecuzione precedente dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="8bc98-112">Optional parameter SkipSucceeded allows you to skip all the succeeded steps in the previous run of the rollout.</span></span>

## <span data-ttu-id="8bc98-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8bc98-113">EXAMPLES</span></span>

### <span data-ttu-id="8bc98-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8bc98-114">Example 1</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="8bc98-115">Questo comando riavvia un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8bc98-115">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="8bc98-116">Il flag SkipSucceeded indica che tutti i passaggi già eseguono correttamente devono essere ignorati e l'implementazione dovrebbe continuare dall'ultima esecuzione non riuscita.</span><span class="sxs-lookup"><span data-stu-id="8bc98-116">The SkipSucceeded flag indicates that all the steps that already ran successfully should be skipped and the rollout should continue execution from where it last failed.</span></span>

### <span data-ttu-id="8bc98-117">Esempio 2: Riavviare un'implementazione con l'identificatore di risorsa</span><span class="sxs-lookup"><span data-stu-id="8bc98-117">Example 2: Restart a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="8bc98-118">Questo comando riavvia un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8bc98-118">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="8bc98-119">Esempio 3: Riavviare un'implementazione con l'oggetto di implementazione.</span><span class="sxs-lookup"><span data-stu-id="8bc98-119">Example 3: Restart a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="8bc98-120">Questo comando riavvia un'implementazione il cui nome e GruppoSocietà Risorse corrispondono rispettivamente alle proprietà Name e ResourceGroupName dell'$rolloutObject.</span><span class="sxs-lookup"><span data-stu-id="8bc98-120">This command restarts a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="8bc98-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8bc98-121">PARAMETERS</span></span>

### <span data-ttu-id="8bc98-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bc98-122">-DefaultProfile</span></span>
<span data-ttu-id="8bc98-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8bc98-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bc98-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8bc98-124">-InputObject</span></span>
<span data-ttu-id="8bc98-125">La risorsa da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="8bc98-125">The resource to be removed.</span></span>

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

### <span data-ttu-id="8bc98-126">-Name</span><span class="sxs-lookup"><span data-stu-id="8bc98-126">-Name</span></span>
<span data-ttu-id="8bc98-127">Nome dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="8bc98-127">The name of the rollout.</span></span>

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

### <span data-ttu-id="8bc98-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bc98-128">-ResourceGroupName</span></span>
<span data-ttu-id="8bc98-129">Gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8bc98-129">The resource group.</span></span>

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

### <span data-ttu-id="8bc98-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8bc98-130">-ResourceId</span></span>
<span data-ttu-id="8bc98-131">L'identificatore di risorsa.</span><span class="sxs-lookup"><span data-stu-id="8bc98-131">The resource identifier.</span></span>

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

### <span data-ttu-id="8bc98-132">-SkipSucceeded</span><span class="sxs-lookup"><span data-stu-id="8bc98-132">-SkipSucceeded</span></span>
<span data-ttu-id="8bc98-133">Ignorare i passaggi riusciti nell'esecuzione precedente dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="8bc98-133">Skip steps that succeeded in the previous run of the rollout.</span></span>

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

### <span data-ttu-id="8bc98-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8bc98-134">-Confirm</span></span>
<span data-ttu-id="8bc98-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8bc98-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8bc98-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8bc98-136">-WhatIf</span></span>
<span data-ttu-id="8bc98-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8bc98-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8bc98-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8bc98-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8bc98-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bc98-139">CommonParameters</span></span>
<span data-ttu-id="8bc98-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bc98-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bc98-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8bc98-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bc98-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="8bc98-142">INPUTS</span></span>

### <span data-ttu-id="8bc98-143">System.String</span><span class="sxs-lookup"><span data-stu-id="8bc98-143">System.String</span></span>

### <span data-ttu-id="8bc98-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="8bc98-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="8bc98-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8bc98-145">OUTPUTS</span></span>

### <span data-ttu-id="8bc98-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="8bc98-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="8bc98-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="8bc98-147">NOTES</span></span>

## <span data-ttu-id="8bc98-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8bc98-148">RELATED LINKS</span></span>
