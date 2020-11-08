---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerRollout.md
ms.openlocfilehash: 8e5e2c25f69d6e61c21a0f616f49079710c2d5db
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022358"
---
# <span data-ttu-id="98d8d-101">Remove-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="98d8d-101">Remove-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="98d8d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="98d8d-102">SYNOPSIS</span></span>
<span data-ttu-id="98d8d-103">Elimina l'implementazione.</span><span class="sxs-lookup"><span data-stu-id="98d8d-103">Deletes the rollout.</span></span>

## <span data-ttu-id="98d8d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="98d8d-104">SYNTAX</span></span>

### <span data-ttu-id="98d8d-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="98d8d-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98d8d-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="98d8d-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerRollout [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98d8d-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="98d8d-107">InputObject</span></span>
```
Remove-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98d8d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98d8d-108">DESCRIPTION</span></span>
<span data-ttu-id="98d8d-109">Il cmdlet **Remove-AzDeploymentManagerRollout** Elimina un implementazione in uno stato terminale.</span><span class="sxs-lookup"><span data-stu-id="98d8d-109">The **Remove-AzDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="98d8d-110">Specificare l'implementazione per nome e nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="98d8d-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="98d8d-111">In alternativa, puoi specificare l'oggetto di implementazione o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="98d8d-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="98d8d-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="98d8d-112">EXAMPLES</span></span>

### <span data-ttu-id="98d8d-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="98d8d-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="98d8d-114">Questo comando Elimina un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="98d8d-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="98d8d-115">Esempio 2: eliminare un'implementazione usando l'identificatore delle risorse</span><span class="sxs-lookup"><span data-stu-id="98d8d-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="98d8d-116">Questo comando Elimina un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="98d8d-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="98d8d-117">Esempio 3: eliminare un'implementazione usando l'oggetto implementazione.</span><span class="sxs-lookup"><span data-stu-id="98d8d-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="98d8d-118">Questo comando Elimina un implementazione il cui nome e ResourceGroup corrispondono rispettivamente alle proprietà Name e ResourceGroupName della $rolloutObject.</span><span class="sxs-lookup"><span data-stu-id="98d8d-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="98d8d-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="98d8d-119">PARAMETERS</span></span>

### <span data-ttu-id="98d8d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98d8d-120">-DefaultProfile</span></span>
<span data-ttu-id="98d8d-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="98d8d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98d8d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98d8d-122">-InputObject</span></span>
<span data-ttu-id="98d8d-123">La risorsa da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="98d8d-123">The resource to be removed.</span></span>

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

### <span data-ttu-id="98d8d-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="98d8d-124">-Name</span></span>
<span data-ttu-id="98d8d-125">Nome dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="98d8d-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="98d8d-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98d8d-126">-PassThru</span></span>
<span data-ttu-id="98d8d-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="98d8d-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="98d8d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98d8d-128">-ResourceGroupName</span></span>
<span data-ttu-id="98d8d-129">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="98d8d-129">The resource group.</span></span>

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

### <span data-ttu-id="98d8d-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98d8d-130">-ResourceId</span></span>
<span data-ttu-id="98d8d-131">Identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="98d8d-131">The resource identifier.</span></span>

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

### <span data-ttu-id="98d8d-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="98d8d-132">-Confirm</span></span>
<span data-ttu-id="98d8d-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98d8d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98d8d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98d8d-134">-WhatIf</span></span>
<span data-ttu-id="98d8d-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98d8d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98d8d-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98d8d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98d8d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98d8d-137">CommonParameters</span></span>
<span data-ttu-id="98d8d-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98d8d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98d8d-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98d8d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98d8d-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="98d8d-140">INPUTS</span></span>

### <span data-ttu-id="98d8d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="98d8d-141">System.String</span></span>

### <span data-ttu-id="98d8d-142">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="98d8d-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="98d8d-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="98d8d-143">OUTPUTS</span></span>

### <span data-ttu-id="98d8d-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="98d8d-144">System.Boolean</span></span>

## <span data-ttu-id="98d8d-145">Note</span><span class="sxs-lookup"><span data-stu-id="98d8d-145">NOTES</span></span>

## <span data-ttu-id="98d8d-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="98d8d-146">RELATED LINKS</span></span>
