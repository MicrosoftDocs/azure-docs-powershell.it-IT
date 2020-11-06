---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/restart-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: ee1ef6e5b8bcee4af1d3aef67767269042c552df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491621"
---
# <span data-ttu-id="6e700-101">Restart-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="6e700-101">Restart-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="6e700-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6e700-102">SYNOPSIS</span></span>
<span data-ttu-id="6e700-103">Riavviare un implementazione non riuscita.</span><span class="sxs-lookup"><span data-stu-id="6e700-103">Restart a failed rollout.</span></span>

## <span data-ttu-id="6e700-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6e700-104">SYNTAX</span></span>

### <span data-ttu-id="6e700-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6e700-105">Interactive (Default)</span></span>
```
Restart-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e700-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e700-106">ResourceId</span></span>
```
Restart-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e700-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="6e700-107">InputObject</span></span>
```
Restart-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e700-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e700-108">DESCRIPTION</span></span>
<span data-ttu-id="6e700-109">Il cmdlet **Restart-AzureRmDeploymentManagerRollout riavvia** un'implementazione non riuscita e restituisce un oggetto che rappresenta l'implementazione con tutte le informazioni dettagliate sullo stato di avanzamento dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="6e700-109">The **Restart-AzureRmDeploymentManagerRollout** cmdlet restarts a failed rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="6e700-110">Specificare l'implementazione per nome e nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6e700-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="6e700-111">In alternativa, puoi specificare l'oggetto di implementazione o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="6e700-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>
<span data-ttu-id="6e700-112">Il parametro facoltativo SkipSucceeded consente di ignorare tutti i passaggi riusciti nella precedente esecuzione dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="6e700-112">Optional parameter SkipSucceeded allows you to skip all the succeeded steps in the previous run of the rollout.</span></span>

## <span data-ttu-id="6e700-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6e700-113">EXAMPLES</span></span>

### <span data-ttu-id="6e700-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6e700-114">Example 1</span></span>
```powershell
PS C:\> Restart-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="6e700-115">Questo comando riavvia un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6e700-115">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="6e700-116">Il flag SkipSucceeded indica che tutti i passaggi già eseguiti correttamente devono essere ignorati e che l'implementazione deve continuare l'esecuzione da dove l'ultima operazione non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="6e700-116">The SkipSucceeded flag indicates that all the steps that already ran successfully should be skipped and the rollout should continue execution from where it last failed.</span></span>

### <span data-ttu-id="6e700-117">Esempio 2: riavviare un implementazione con l'identificatore delle risorse</span><span class="sxs-lookup"><span data-stu-id="6e700-117">Example 2: Restart a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="6e700-118">Questo comando riavvia un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6e700-118">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="6e700-119">Esempio 3: riavviare un implementazione usando l'oggetto di implementazione.</span><span class="sxs-lookup"><span data-stu-id="6e700-119">Example 3: Restart a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="6e700-120">Questo comando Riavvia un implementazione il cui nome e ResourceGroup corrispondono rispettivamente alle proprietà Name e ResourceGroupName della $rolloutObject.</span><span class="sxs-lookup"><span data-stu-id="6e700-120">This command restarts a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="6e700-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6e700-121">PARAMETERS</span></span>

### <span data-ttu-id="6e700-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e700-122">-DefaultProfile</span></span>
<span data-ttu-id="6e700-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6e700-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e700-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="6e700-124">-Name</span></span>
<span data-ttu-id="6e700-125">Nome dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="6e700-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="6e700-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e700-126">-ResourceGroupName</span></span>
<span data-ttu-id="6e700-127">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="6e700-127">The resource group.</span></span>

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

### <span data-ttu-id="6e700-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e700-128">-ResourceId</span></span>
<span data-ttu-id="6e700-129">Identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6e700-129">The resource identifier.</span></span>

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

### <span data-ttu-id="6e700-130">-Implementazione</span><span class="sxs-lookup"><span data-stu-id="6e700-130">-Rollout</span></span>
<span data-ttu-id="6e700-131">La risorsa da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6e700-131">The resource to be removed.</span></span>

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

### <span data-ttu-id="6e700-132">-SkipSucceeded</span><span class="sxs-lookup"><span data-stu-id="6e700-132">-SkipSucceeded</span></span>
<span data-ttu-id="6e700-133">Ignorare i passaggi che sono riusciti a eseguire nell'esecuzione precedente dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="6e700-133">Skip steps that succeeded in the previous run of the rollout.</span></span>

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

### <span data-ttu-id="6e700-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6e700-134">-Confirm</span></span>
<span data-ttu-id="6e700-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e700-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e700-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e700-136">-WhatIf</span></span>
<span data-ttu-id="6e700-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6e700-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e700-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6e700-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e700-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e700-139">CommonParameters</span></span>
<span data-ttu-id="6e700-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e700-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e700-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e700-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e700-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6e700-142">INPUTS</span></span>

### <span data-ttu-id="6e700-143">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="6e700-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="6e700-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6e700-144">OUTPUTS</span></span>

### <span data-ttu-id="6e700-145">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="6e700-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="6e700-146">Note</span><span class="sxs-lookup"><span data-stu-id="6e700-146">NOTES</span></span>

## <span data-ttu-id="6e700-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6e700-147">RELATED LINKS</span></span>

[<span data-ttu-id="6e700-148">Get-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="6e700-148">Get-AzureRmDeploymentManagerRollout</span></span>](./Get-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="6e700-149">Stop-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="6e700-149">Stop-AzureRmDeploymentManagerRollout</span></span>](./Stop-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="6e700-150">Remove-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="6e700-150">Remove-AzureRmDeploymentManagerRollout</span></span>](./Remove-AzureRmDeploymentManagerRollout.md)