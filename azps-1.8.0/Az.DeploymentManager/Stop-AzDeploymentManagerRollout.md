---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/stop-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Stop-AzDeploymentManagerRollout.md
ms.openlocfilehash: d68ca0e13c279e58715b57ae73a2c8e2f4f30d8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684428"
---
# <span data-ttu-id="ee551-101">Stop-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="ee551-101">Stop-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="ee551-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ee551-102">SYNOPSIS</span></span>
<span data-ttu-id="ee551-103">Interrompe l'implementazione.</span><span class="sxs-lookup"><span data-stu-id="ee551-103">Stops the rollout.</span></span>

## <span data-ttu-id="ee551-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee551-104">SYNTAX</span></span>

### <span data-ttu-id="ee551-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ee551-105">Interactive (Default)</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee551-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee551-106">ResourceId</span></span>
```
Stop-AzDeploymentManagerRollout [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee551-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="ee551-107">InputObject</span></span>
```
Stop-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee551-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee551-108">DESCRIPTION</span></span>
<span data-ttu-id="ee551-109">Il cmdlet **Stop-AzDeploymentManagerRollout** interrompe l'implementazione in corso e restituisce un oggetto che rappresenta lo stato corrente dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="ee551-109">The **Stop-AzDeploymentManagerRollout** cmdlet stops a rollout in progress and returns an object that represents the current state of the rollout.</span></span>
<span data-ttu-id="ee551-110">Specificare l'implementazione per nome e nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ee551-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="ee551-111">In alternativa, puoi specificare l'oggetto di implementazione o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="ee551-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="ee551-112">Tieni presente che una volta arrestata l'implementazione, non può essere ripresa o riavviata.</span><span class="sxs-lookup"><span data-stu-id="ee551-112">Note that once a rollout is stopped, it cannot be resumed or restarted.</span></span> <span data-ttu-id="ee551-113">È possibile creare una nuova implementazione solo.</span><span class="sxs-lookup"><span data-stu-id="ee551-113">You can only create a new rollout.</span></span>

## <span data-ttu-id="ee551-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee551-114">EXAMPLES</span></span>

### <span data-ttu-id="ee551-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ee551-115">Example 1</span></span>
```powershell
PS C:\> Stop-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="ee551-116">Questo comando interrompe un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ee551-116">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="ee551-117">Esempio 2: interrompere l'implementazione usando l'identificatore delle risorse</span><span class="sxs-lookup"><span data-stu-id="ee551-117">Example 2: Stop a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="ee551-118">Questo comando interrompe un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ee551-118">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="ee551-119">Esempio 3: interrompere l'implementazione usando l'oggetto di implementazione.</span><span class="sxs-lookup"><span data-stu-id="ee551-119">Example 3: Stop a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="ee551-120">Questo comando interrompe un implementazione il cui nome e ResourceGroup corrispondono rispettivamente alle proprietà Name e ResourceGroupName della $rolloutObject.</span><span class="sxs-lookup"><span data-stu-id="ee551-120">This command stops a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="ee551-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ee551-121">PARAMETERS</span></span>

### <span data-ttu-id="ee551-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee551-122">-DefaultProfile</span></span>
<span data-ttu-id="ee551-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ee551-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee551-124">-Force</span><span class="sxs-lookup"><span data-stu-id="ee551-124">-Force</span></span>
<span data-ttu-id="ee551-125">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="ee551-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ee551-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee551-126">-InputObject</span></span>
<span data-ttu-id="ee551-127">L'implementazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ee551-127">The rollout to be removed.</span></span>

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

### <span data-ttu-id="ee551-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="ee551-128">-Name</span></span>
<span data-ttu-id="ee551-129">Nome dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="ee551-129">The name of the rollout.</span></span>

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

### <span data-ttu-id="ee551-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee551-130">-ResourceGroupName</span></span>
<span data-ttu-id="ee551-131">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="ee551-131">The resource group.</span></span>

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

### <span data-ttu-id="ee551-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee551-132">-ResourceId</span></span>
<span data-ttu-id="ee551-133">Identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ee551-133">The resource identifier.</span></span>

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

### <span data-ttu-id="ee551-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ee551-134">-Confirm</span></span>
<span data-ttu-id="ee551-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee551-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee551-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee551-136">-WhatIf</span></span>
<span data-ttu-id="ee551-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee551-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee551-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee551-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee551-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee551-139">CommonParameters</span></span>
<span data-ttu-id="ee551-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee551-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee551-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee551-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee551-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ee551-142">INPUTS</span></span>

### <span data-ttu-id="ee551-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ee551-143">System.String</span></span>

### <span data-ttu-id="ee551-144">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="ee551-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="ee551-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee551-145">OUTPUTS</span></span>

### <span data-ttu-id="ee551-146">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="ee551-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="ee551-147">Note</span><span class="sxs-lookup"><span data-stu-id="ee551-147">NOTES</span></span>

## <span data-ttu-id="ee551-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee551-148">RELATED LINKS</span></span>