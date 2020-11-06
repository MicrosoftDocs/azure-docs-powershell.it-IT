---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: f329468dce9c520eb647bb0d927ba91de64a5c33
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490846"
---
# <span data-ttu-id="876a5-101">Remove-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="876a5-101">Remove-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="876a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="876a5-102">SYNOPSIS</span></span>
<span data-ttu-id="876a5-103">Elimina un'implementazione.</span><span class="sxs-lookup"><span data-stu-id="876a5-103">Deletes a rollout.</span></span>

## <span data-ttu-id="876a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="876a5-104">SYNTAX</span></span>

### <span data-ttu-id="876a5-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="876a5-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="876a5-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="876a5-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="876a5-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="876a5-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="876a5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="876a5-108">DESCRIPTION</span></span>
<span data-ttu-id="876a5-109">Il cmdlet **Remove-AzureRmDeploymentManagerRollout** Elimina un implementazione in uno stato terminale.</span><span class="sxs-lookup"><span data-stu-id="876a5-109">The **Remove-AzureRmDeploymentManagerRollout** cmdlet deletes a rollout in a terminal state.</span></span>
<span data-ttu-id="876a5-110">Specificare l'implementazione per nome e nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="876a5-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="876a5-111">In alternativa, puoi specificare l'oggetto di implementazione o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="876a5-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="876a5-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="876a5-112">EXAMPLES</span></span>

### <span data-ttu-id="876a5-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="876a5-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="876a5-114">Questo comando Elimina un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="876a5-114">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="876a5-115">Esempio 2: eliminare un'implementazione usando l'identificatore delle risorse</span><span class="sxs-lookup"><span data-stu-id="876a5-115">Example 2: Delete a rollout using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="876a5-116">Questo comando Elimina un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="876a5-116">This command deletes a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="876a5-117">Esempio 3: eliminare un'implementazione usando l'oggetto implementazione.</span><span class="sxs-lookup"><span data-stu-id="876a5-117">Example 3: Delete a rollout using the rollout object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="876a5-118">Questo comando Elimina un implementazione il cui nome e ResourceGroup corrispondono rispettivamente alle proprietà Name e ResourceGroupName della $rolloutObject.</span><span class="sxs-lookup"><span data-stu-id="876a5-118">This command deletes a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="876a5-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="876a5-119">PARAMETERS</span></span>

### <span data-ttu-id="876a5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="876a5-120">-DefaultProfile</span></span>
<span data-ttu-id="876a5-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="876a5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="876a5-122">-Force</span><span class="sxs-lookup"><span data-stu-id="876a5-122">-Force</span></span>
<span data-ttu-id="876a5-123">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="876a5-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="876a5-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="876a5-124">-Name</span></span>
<span data-ttu-id="876a5-125">Nome dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="876a5-125">The name of the rollout.</span></span>

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

### <span data-ttu-id="876a5-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="876a5-126">-PassThru</span></span>
<span data-ttu-id="876a5-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="876a5-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="876a5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="876a5-128">-ResourceGroupName</span></span>
<span data-ttu-id="876a5-129">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="876a5-129">The resource group.</span></span>

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

### <span data-ttu-id="876a5-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="876a5-130">-ResourceId</span></span>
<span data-ttu-id="876a5-131">Identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="876a5-131">The resource identifier.</span></span>

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

### <span data-ttu-id="876a5-132">-Implementazione</span><span class="sxs-lookup"><span data-stu-id="876a5-132">-Rollout</span></span>
<span data-ttu-id="876a5-133">La risorsa da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="876a5-133">The resource to be removed.</span></span>

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

### <span data-ttu-id="876a5-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="876a5-134">-Confirm</span></span>
<span data-ttu-id="876a5-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="876a5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="876a5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="876a5-136">-WhatIf</span></span>
<span data-ttu-id="876a5-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="876a5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="876a5-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="876a5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="876a5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="876a5-139">CommonParameters</span></span>
<span data-ttu-id="876a5-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="876a5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="876a5-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="876a5-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="876a5-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="876a5-142">INPUTS</span></span>

### <span data-ttu-id="876a5-143">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="876a5-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="876a5-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="876a5-144">OUTPUTS</span></span>

### <span data-ttu-id="876a5-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="876a5-145">System.Boolean</span></span>

## <span data-ttu-id="876a5-146">Note</span><span class="sxs-lookup"><span data-stu-id="876a5-146">NOTES</span></span>

## <span data-ttu-id="876a5-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="876a5-147">RELATED LINKS</span></span>

[<span data-ttu-id="876a5-148">Get-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="876a5-148">Get-AzureRmDeploymentManagerRollout</span></span>](./Get-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="876a5-149">Stop-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="876a5-149">Stop-AzureRmDeploymentManagerRollout</span></span>](./Stop-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="876a5-150">Riavviare-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="876a5-150">Restart-AzureRmDeploymentManagerRollout</span></span>](./Restart-AzureRmDeploymentManagerRollout.md)