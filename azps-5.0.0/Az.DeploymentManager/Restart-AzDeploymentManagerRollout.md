---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/restart-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
ms.openlocfilehash: ba7b62d42764f5098868e6a15eb073cb6b898e82
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297162"
---
# <span data-ttu-id="2b9b5-101">Restart-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="2b9b5-101">Restart-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="2b9b5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2b9b5-102">SYNOPSIS</span></span>
<span data-ttu-id="2b9b5-103">Riavvia un implementazione non riuscita.</span><span class="sxs-lookup"><span data-stu-id="2b9b5-103">Restarts a failed rollout.</span></span>

## <span data-ttu-id="2b9b5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b9b5-104">SYNTAX</span></span>

### <span data-ttu-id="2b9b5-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2b9b5-105">Interactive (Default)</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b9b5-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b9b5-106">ResourceId</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceId] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b9b5-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="2b9b5-107">InputObject</span></span>
```
Restart-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b9b5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b9b5-108">DESCRIPTION</span></span>
<span data-ttu-id="2b9b5-109">Il cmdlet **Restart-AzDeploymentManagerRollout riavvia** un'implementazione non riuscita e restituisce un oggetto che rappresenta l'implementazione con tutte le informazioni dettagliate sullo stato di avanzamento dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="2b9b5-109">The **Restart-AzDeploymentManagerRollout** cmdlet restarts a failed rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="2b9b5-110">Specificare l'implementazione per nome e nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2b9b5-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="2b9b5-111">In alternativa, puoi specificare l'oggetto di implementazione o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="2b9b5-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>
<span data-ttu-id="2b9b5-112">Il parametro facoltativo SkipSucceeded consente di ignorare tutti i passaggi riusciti nella precedente esecuzione dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="2b9b5-112">Optional parameter SkipSucceeded allows you to skip all the succeeded steps in the previous run of the rollout.</span></span>

## <span data-ttu-id="2b9b5-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b9b5-113">EXAMPLES</span></span>

### <span data-ttu-id="2b9b5-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2b9b5-114">Example 1</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="2b9b5-115">Questo comando riavvia un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2b9b5-115">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="2b9b5-116">Il flag SkipSucceeded indica che tutti i passaggi già eseguiti correttamente devono essere ignorati e che l'implementazione deve continuare l'esecuzione da dove l'ultima operazione non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="2b9b5-116">The SkipSucceeded flag indicates that all the steps that already ran successfully should be skipped and the rollout should continue execution from where it last failed.</span></span>

### <span data-ttu-id="2b9b5-117">Esempio 2: riavviare un implementazione con l'identificatore delle risorse</span><span class="sxs-lookup"><span data-stu-id="2b9b5-117">Example 2: Restart a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="2b9b5-118">Questo comando riavvia un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2b9b5-118">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="2b9b5-119">Esempio 3: riavviare un implementazione usando l'oggetto di implementazione.</span><span class="sxs-lookup"><span data-stu-id="2b9b5-119">Example 3: Restart a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="2b9b5-120">Questo comando Riavvia un implementazione il cui nome e ResourceGroup corrispondono rispettivamente alle proprietà Name e ResourceGroupName della $rolloutObject.</span><span class="sxs-lookup"><span data-stu-id="2b9b5-120">This command restarts a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="2b9b5-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2b9b5-121">PARAMETERS</span></span>

### <span data-ttu-id="2b9b5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b9b5-122">-DefaultProfile</span></span>
<span data-ttu-id="2b9b5-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2b9b5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b9b5-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b9b5-124">-InputObject</span></span>
<span data-ttu-id="2b9b5-125">La risorsa da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="2b9b5-125">The resource to be removed.</span></span>

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

### <span data-ttu-id="2b9b5-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="2b9b5-126">-Name</span></span>
<span data-ttu-id="2b9b5-127">Nome dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="2b9b5-127">The name of the rollout.</span></span>

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

### <span data-ttu-id="2b9b5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b9b5-128">-ResourceGroupName</span></span>
<span data-ttu-id="2b9b5-129">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="2b9b5-129">The resource group.</span></span>

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

### <span data-ttu-id="2b9b5-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b9b5-130">-ResourceId</span></span>
<span data-ttu-id="2b9b5-131">Identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="2b9b5-131">The resource identifier.</span></span>

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

### <span data-ttu-id="2b9b5-132">-SkipSucceeded</span><span class="sxs-lookup"><span data-stu-id="2b9b5-132">-SkipSucceeded</span></span>
<span data-ttu-id="2b9b5-133">Ignorare i passaggi che sono riusciti a eseguire nell'esecuzione precedente dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="2b9b5-133">Skip steps that succeeded in the previous run of the rollout.</span></span>

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

### <span data-ttu-id="2b9b5-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2b9b5-134">-Confirm</span></span>
<span data-ttu-id="2b9b5-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b9b5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b9b5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b9b5-136">-WhatIf</span></span>
<span data-ttu-id="2b9b5-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b9b5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b9b5-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b9b5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b9b5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b9b5-139">CommonParameters</span></span>
<span data-ttu-id="2b9b5-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b9b5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b9b5-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b9b5-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b9b5-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2b9b5-142">INPUTS</span></span>

### <span data-ttu-id="2b9b5-143">System. String</span><span class="sxs-lookup"><span data-stu-id="2b9b5-143">System.String</span></span>

### <span data-ttu-id="2b9b5-144">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="2b9b5-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="2b9b5-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b9b5-145">OUTPUTS</span></span>

### <span data-ttu-id="2b9b5-146">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="2b9b5-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="2b9b5-147">Note</span><span class="sxs-lookup"><span data-stu-id="2b9b5-147">NOTES</span></span>

## <span data-ttu-id="2b9b5-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b9b5-148">RELATED LINKS</span></span>
