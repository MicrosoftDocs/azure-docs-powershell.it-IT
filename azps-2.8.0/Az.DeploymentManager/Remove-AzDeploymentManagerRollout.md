---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
ms.openlocfilehash: 066026331fa43af06fc2e3314ccb97d06a0f9b50
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674607"
---
# <span data-ttu-id="ecf35-101">Remove-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="ecf35-101">Remove-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="ecf35-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ecf35-102">SYNOPSIS</span></span>
<span data-ttu-id="ecf35-103">Elimina l'implementazione.</span><span class="sxs-lookup"><span data-stu-id="ecf35-103">Deletes the rollout.</span></span>

## <span data-ttu-id="ecf35-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ecf35-104">SYNTAX</span></span>

### <span data-ttu-id="ecf35-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ecf35-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecf35-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecf35-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecf35-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="ecf35-107">InputObject</span></span>
```
Remove-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecf35-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ecf35-108">DESCRIPTION</span></span>
<span data-ttu-id="ecf35-109">Il cmdlet **Remove-AzDeploymentManagerRollout** Elimina un implementazione in uno stato terminale.</span><span class="sxs-lookup"><span data-stu-id="ecf35-109">The **Remove-AzDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="ecf35-110">Specificare l'implementazione per nome e nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ecf35-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="ecf35-111">In alternativa, puoi specificare l'oggetto di implementazione o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="ecf35-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="ecf35-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ecf35-112">EXAMPLES</span></span>

### <span data-ttu-id="ecf35-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ecf35-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="ecf35-114">Questo comando Elimina un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ecf35-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="ecf35-115">Esempio 2: eliminare un'implementazione usando l'identificatore delle risorse</span><span class="sxs-lookup"><span data-stu-id="ecf35-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="ecf35-116">Questo comando Elimina un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ecf35-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="ecf35-117">Esempio 3: eliminare un'implementazione usando l'oggetto implementazione.</span><span class="sxs-lookup"><span data-stu-id="ecf35-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="ecf35-118">Questo comando Elimina un implementazione il cui nome e ResourceGroup corrispondono rispettivamente alle proprietà Name e ResourceGroupName della $rolloutObject.</span><span class="sxs-lookup"><span data-stu-id="ecf35-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="ecf35-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ecf35-119">PARAMETERS</span></span>

### <span data-ttu-id="ecf35-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecf35-120">-DefaultProfile</span></span>
<span data-ttu-id="ecf35-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ecf35-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecf35-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ecf35-122">-InputObject</span></span>
<span data-ttu-id="ecf35-123">La risorsa da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ecf35-123">The resource to be removed.</span></span>

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

### <span data-ttu-id="ecf35-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="ecf35-124">-Name</span></span>
<span data-ttu-id="ecf35-125">Nome dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="ecf35-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="ecf35-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ecf35-126">-PassThru</span></span>
<span data-ttu-id="ecf35-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ecf35-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ecf35-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecf35-128">-ResourceGroupName</span></span>
<span data-ttu-id="ecf35-129">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="ecf35-129">The resource group.</span></span>

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

### <span data-ttu-id="ecf35-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecf35-130">-ResourceId</span></span>
<span data-ttu-id="ecf35-131">Identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ecf35-131">The resource identifier.</span></span>

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

### <span data-ttu-id="ecf35-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ecf35-132">-Confirm</span></span>
<span data-ttu-id="ecf35-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecf35-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecf35-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecf35-134">-WhatIf</span></span>
<span data-ttu-id="ecf35-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ecf35-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecf35-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ecf35-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecf35-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecf35-137">CommonParameters</span></span>
<span data-ttu-id="ecf35-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecf35-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecf35-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecf35-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecf35-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ecf35-140">INPUTS</span></span>

### <span data-ttu-id="ecf35-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ecf35-141">System.String</span></span>

### <span data-ttu-id="ecf35-142">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="ecf35-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="ecf35-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ecf35-143">OUTPUTS</span></span>

### <span data-ttu-id="ecf35-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ecf35-144">System.Boolean</span></span>

## <span data-ttu-id="ecf35-145">Note</span><span class="sxs-lookup"><span data-stu-id="ecf35-145">NOTES</span></span>

## <span data-ttu-id="ecf35-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ecf35-146">RELATED LINKS</span></span>
