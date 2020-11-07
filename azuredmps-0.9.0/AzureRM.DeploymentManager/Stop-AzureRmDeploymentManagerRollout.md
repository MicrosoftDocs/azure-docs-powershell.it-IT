---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/stop-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: 3c4f221fc00187c4faea2dbcc1a5014822c476c8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685166"
---
# <span data-ttu-id="7fcc8-101">Stop-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="7fcc8-101">Stop-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="7fcc8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7fcc8-102">SYNOPSIS</span></span>
<span data-ttu-id="7fcc8-103">Interrompe l'implementazione in corso.</span><span class="sxs-lookup"><span data-stu-id="7fcc8-103">Stops a rollout in progress.</span></span>

## <span data-ttu-id="7fcc8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7fcc8-104">SYNTAX</span></span>

### <span data-ttu-id="7fcc8-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7fcc8-105">Interactive (Default)</span></span>
```
Stop-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fcc8-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fcc8-106">ResourceId</span></span>
```
Stop-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fcc8-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="7fcc8-107">InputObject</span></span>
```
Stop-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fcc8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7fcc8-108">DESCRIPTION</span></span>
<span data-ttu-id="7fcc8-109">Il cmdlet **Stop-AzureRmDeploymentManagerRollout** interrompe l'implementazione in corso e restituisce un oggetto che rappresenta lo stato corrente dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="7fcc8-109">The **Stop-AzureRmDeploymentManagerRollout** cmdlet stops a rollout in progress and returns an object that represents the current state of the rollout.</span></span>
<span data-ttu-id="7fcc8-110">Specificare l'implementazione per nome e nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7fcc8-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="7fcc8-111">In alternativa, puoi specificare l'oggetto di implementazione o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="7fcc8-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="7fcc8-112">Tieni presente che una volta arrestata l'implementazione, non può essere ripresa o riavviata.</span><span class="sxs-lookup"><span data-stu-id="7fcc8-112">Note that once a rollout is stopped, it cannot be resumed or restarted.</span></span> <span data-ttu-id="7fcc8-113">È possibile creare una nuova implementazione solo.</span><span class="sxs-lookup"><span data-stu-id="7fcc8-113">You can only create a new rollout.</span></span>

## <span data-ttu-id="7fcc8-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7fcc8-114">EXAMPLES</span></span>

### <span data-ttu-id="7fcc8-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7fcc8-115">Example 1</span></span>
```powershell
PS C:\> Stop-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="7fcc8-116">Questo comando interrompe un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7fcc8-116">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="7fcc8-117">Esempio 2: interrompere l'implementazione usando l'identificatore delle risorse</span><span class="sxs-lookup"><span data-stu-id="7fcc8-117">Example 2: Stop a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="7fcc8-118">Questo comando interrompe un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7fcc8-118">This command stops a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="7fcc8-119">Esempio 3: interrompere l'implementazione usando l'oggetto di implementazione.</span><span class="sxs-lookup"><span data-stu-id="7fcc8-119">Example 3: Stop a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="7fcc8-120">Questo comando interrompe un implementazione il cui nome e ResourceGroup corrispondono rispettivamente alle proprietà Name e ResourceGroupName della $rolloutObject.</span><span class="sxs-lookup"><span data-stu-id="7fcc8-120">This command stops a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="7fcc8-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7fcc8-121">PARAMETERS</span></span>

### <span data-ttu-id="7fcc8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fcc8-122">-DefaultProfile</span></span>
<span data-ttu-id="7fcc8-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7fcc8-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fcc8-124">-Force</span><span class="sxs-lookup"><span data-stu-id="7fcc8-124">-Force</span></span>
<span data-ttu-id="7fcc8-125">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="7fcc8-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7fcc8-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="7fcc8-126">-Name</span></span>
<span data-ttu-id="7fcc8-127">Nome dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="7fcc8-127">The name of the rollout.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fcc8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fcc8-128">-ResourceGroupName</span></span>
<span data-ttu-id="7fcc8-129">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="7fcc8-129">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fcc8-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fcc8-130">-ResourceId</span></span>
<span data-ttu-id="7fcc8-131">Identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="7fcc8-131">The resource identifier.</span></span>

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

### <span data-ttu-id="7fcc8-132">-Implementazione</span><span class="sxs-lookup"><span data-stu-id="7fcc8-132">-Rollout</span></span>
<span data-ttu-id="7fcc8-133">La risorsa da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="7fcc8-133">The resource to be removed.</span></span>

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

### <span data-ttu-id="7fcc8-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7fcc8-134">-Confirm</span></span>
<span data-ttu-id="7fcc8-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7fcc8-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fcc8-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fcc8-136">-WhatIf</span></span>
<span data-ttu-id="7fcc8-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7fcc8-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7fcc8-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7fcc8-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fcc8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fcc8-139">CommonParameters</span></span>
<span data-ttu-id="7fcc8-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fcc8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fcc8-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fcc8-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fcc8-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7fcc8-142">INPUTS</span></span>

### <span data-ttu-id="7fcc8-143">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="7fcc8-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="7fcc8-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7fcc8-144">OUTPUTS</span></span>

### <span data-ttu-id="7fcc8-145">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="7fcc8-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="7fcc8-146">Note</span><span class="sxs-lookup"><span data-stu-id="7fcc8-146">NOTES</span></span>

## <span data-ttu-id="7fcc8-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7fcc8-147">RELATED LINKS</span></span>

[<span data-ttu-id="7fcc8-148">Get-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="7fcc8-148">Get-AzureRmDeploymentManagerRollout</span></span>](./Get-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="7fcc8-149">Riavviare-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="7fcc8-149">Restart-AzureRmDeploymentManagerRollout</span></span>](./Restart-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="7fcc8-150">Remove-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="7fcc8-150">Remove-AzureRmDeploymentManagerRollout</span></span>](./Remove-AzureRmDeploymentManagerRollout.md)