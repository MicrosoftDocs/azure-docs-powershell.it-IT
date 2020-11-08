---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/stop-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
ms.openlocfilehash: cd59cd39fb2834bed2162a257905fea643c0a767
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190762"
---
# <span data-ttu-id="2ce80-101">Stop-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="2ce80-101">Stop-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="2ce80-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2ce80-102">SYNOPSIS</span></span>
<span data-ttu-id="2ce80-103">Interrompe l'implementazione.</span><span class="sxs-lookup"><span data-stu-id="2ce80-103">Stops the rollout.</span></span>

## <span data-ttu-id="2ce80-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ce80-104">SYNTAX</span></span>

### <span data-ttu-id="2ce80-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2ce80-105">Interactive (Default)</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ce80-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ce80-106">ResourceId</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ce80-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="2ce80-107">InputObject</span></span>
```
Stop-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ce80-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ce80-108">DESCRIPTION</span></span>
<span data-ttu-id="2ce80-109">Il cmdlet **Stop-AzDeploymentManagerRollout** interrompe l'implementazione in corso e restituisce un oggetto che rappresenta lo stato corrente dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="2ce80-109">The **Stop-AzDeploymentManagerRollout** cmdlet stops a rollout in progress and returns an object that represents the current state of the rollout.</span></span>
<span data-ttu-id="2ce80-110">Specificare l'implementazione per nome e nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2ce80-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="2ce80-111">In alternativa, puoi specificare l'oggetto di implementazione o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="2ce80-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="2ce80-112">Tieni presente che una volta arrestata l'implementazione, non può essere ripresa o riavviata.</span><span class="sxs-lookup"><span data-stu-id="2ce80-112">Note that once a rollout is stopped, it cannot be resumed or restarted.</span></span> <span data-ttu-id="2ce80-113">È possibile creare una nuova implementazione solo.</span><span class="sxs-lookup"><span data-stu-id="2ce80-113">You can only create a new rollout.</span></span>

## <span data-ttu-id="2ce80-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ce80-114">EXAMPLES</span></span>

### <span data-ttu-id="2ce80-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2ce80-115">Example 1</span></span>
```powershell
PS C:\> Stop-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="2ce80-116">Questo comando interrompe un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2ce80-116">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="2ce80-117">Esempio 2: interrompere l'implementazione usando l'identificatore delle risorse</span><span class="sxs-lookup"><span data-stu-id="2ce80-117">Example 2: Stop a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="2ce80-118">Questo comando interrompe un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2ce80-118">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="2ce80-119">Esempio 3: interrompere l'implementazione usando l'oggetto di implementazione.</span><span class="sxs-lookup"><span data-stu-id="2ce80-119">Example 3: Stop a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="2ce80-120">Questo comando interrompe un implementazione il cui nome e ResourceGroup corrispondono rispettivamente alle proprietà Name e ResourceGroupName della $rolloutObject.</span><span class="sxs-lookup"><span data-stu-id="2ce80-120">This command stops a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="2ce80-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2ce80-121">PARAMETERS</span></span>

### <span data-ttu-id="2ce80-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ce80-122">-DefaultProfile</span></span>
<span data-ttu-id="2ce80-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2ce80-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ce80-124">-Force</span><span class="sxs-lookup"><span data-stu-id="2ce80-124">-Force</span></span>
<span data-ttu-id="2ce80-125">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="2ce80-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2ce80-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ce80-126">-InputObject</span></span>
<span data-ttu-id="2ce80-127">L'implementazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="2ce80-127">The rollout to be removed.</span></span>

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

### <span data-ttu-id="2ce80-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="2ce80-128">-Name</span></span>
<span data-ttu-id="2ce80-129">Nome dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="2ce80-129">The name of the rollout.</span></span>

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

### <span data-ttu-id="2ce80-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ce80-130">-ResourceGroupName</span></span>
<span data-ttu-id="2ce80-131">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="2ce80-131">The resource group.</span></span>

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

### <span data-ttu-id="2ce80-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ce80-132">-ResourceId</span></span>
<span data-ttu-id="2ce80-133">Identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="2ce80-133">The resource identifier.</span></span>

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

### <span data-ttu-id="2ce80-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2ce80-134">-Confirm</span></span>
<span data-ttu-id="2ce80-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ce80-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ce80-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ce80-136">-WhatIf</span></span>
<span data-ttu-id="2ce80-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ce80-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ce80-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ce80-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ce80-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ce80-139">CommonParameters</span></span>
<span data-ttu-id="2ce80-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ce80-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ce80-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ce80-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ce80-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2ce80-142">INPUTS</span></span>

### <span data-ttu-id="2ce80-143">System. String</span><span class="sxs-lookup"><span data-stu-id="2ce80-143">System.String</span></span>

### <span data-ttu-id="2ce80-144">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="2ce80-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="2ce80-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ce80-145">OUTPUTS</span></span>

### <span data-ttu-id="2ce80-146">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="2ce80-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="2ce80-147">Note</span><span class="sxs-lookup"><span data-stu-id="2ce80-147">NOTES</span></span>

## <span data-ttu-id="2ce80-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ce80-148">RELATED LINKS</span></span>
