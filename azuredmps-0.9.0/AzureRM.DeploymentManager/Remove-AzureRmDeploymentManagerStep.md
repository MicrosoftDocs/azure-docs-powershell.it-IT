---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: 3abceb6c3c270378c911036967698f459cbe063a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490933"
---
# <span data-ttu-id="9cd5e-101">Remove-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="9cd5e-101">Remove-AzureRmDeploymentManagerStep</span></span>

## <span data-ttu-id="9cd5e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9cd5e-102">SYNOPSIS</span></span>
<span data-ttu-id="9cd5e-103">Elimina un passaggio.</span><span class="sxs-lookup"><span data-stu-id="9cd5e-103">Deletes a step.</span></span>

## <span data-ttu-id="9cd5e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9cd5e-104">SYNTAX</span></span>

### <span data-ttu-id="9cd5e-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9cd5e-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cd5e-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9cd5e-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerStep [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cd5e-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="9cd5e-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerStep [-Step] <PSStepResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cd5e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9cd5e-108">DESCRIPTION</span></span>
<span data-ttu-id="9cd5e-109">Il cmdlet **Remove-AzureRmDeploymentManagerStep** Elimina un passaggio.</span><span class="sxs-lookup"><span data-stu-id="9cd5e-109">The **Remove-AzureRmDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="9cd5e-110">Specificare il passaggio in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9cd5e-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="9cd5e-111">In alternativa, puoi specificare l'oggetto step o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="9cd5e-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="9cd5e-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9cd5e-112">EXAMPLES</span></span>
### <span data-ttu-id="9cd5e-113">Esempio 1: rimuovere un passaggio</span><span class="sxs-lookup"><span data-stu-id="9cd5e-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="9cd5e-114">Questo comando Elimina un passaggio denominato ContosoService1WaitStep in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9cd5e-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="9cd5e-115">Esempio 2: rimuovere un passaggio usando l'identificatore delle risorse</span><span class="sxs-lookup"><span data-stu-id="9cd5e-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="9cd5e-116">Questo comando Elimina un passaggio denominato ContosoService1WaitStep in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9cd5e-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="9cd5e-117">Esempio 3: rimuovere un passaggio usando un oggetto restituito da New-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="9cd5e-117">Example 3: Remove a step using an object returned by New-AzureRmDeploymentManagerStep</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerStep -Step $stepObject
```

 <span data-ttu-id="9cd5e-118">Questo comando Elimina un passaggio il cui nome e ResourceGroup corrispondono rispettivamente alle proprietà Name e ResourceGroupName della $stepObject.</span><span class="sxs-lookup"><span data-stu-id="9cd5e-118">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="9cd5e-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9cd5e-119">PARAMETERS</span></span>

### <span data-ttu-id="9cd5e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cd5e-120">-DefaultProfile</span></span>
<span data-ttu-id="9cd5e-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9cd5e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cd5e-122">-Force</span><span class="sxs-lookup"><span data-stu-id="9cd5e-122">-Force</span></span>
<span data-ttu-id="9cd5e-123">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="9cd5e-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9cd5e-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="9cd5e-124">-Name</span></span>
<span data-ttu-id="9cd5e-125">Nome del passaggio.</span><span class="sxs-lookup"><span data-stu-id="9cd5e-125">The name of the step.</span></span>

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

### <span data-ttu-id="9cd5e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9cd5e-126">-PassThru</span></span>
<span data-ttu-id="9cd5e-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="9cd5e-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9cd5e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cd5e-128">-ResourceGroupName</span></span>
<span data-ttu-id="9cd5e-129">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="9cd5e-129">The resource group.</span></span>

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

### <span data-ttu-id="9cd5e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9cd5e-130">-ResourceId</span></span>
<span data-ttu-id="9cd5e-131">Identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="9cd5e-131">The resource identifier.</span></span>

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

### <span data-ttu-id="9cd5e-132">-Step</span><span class="sxs-lookup"><span data-stu-id="9cd5e-132">-Step</span></span>
<span data-ttu-id="9cd5e-133">Passaggio da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="9cd5e-133">The step to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9cd5e-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9cd5e-134">-Confirm</span></span>
<span data-ttu-id="9cd5e-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9cd5e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cd5e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cd5e-136">-WhatIf</span></span>
<span data-ttu-id="9cd5e-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9cd5e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cd5e-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9cd5e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cd5e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cd5e-139">CommonParameters</span></span>
<span data-ttu-id="9cd5e-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cd5e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9cd5e-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cd5e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cd5e-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9cd5e-142">INPUTS</span></span>

### <span data-ttu-id="9cd5e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="9cd5e-143">System.String</span></span>

### <span data-ttu-id="9cd5e-144">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="9cd5e-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="9cd5e-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9cd5e-145">OUTPUTS</span></span>

### <span data-ttu-id="9cd5e-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9cd5e-146">System.Boolean</span></span>

## <span data-ttu-id="9cd5e-147">Note</span><span class="sxs-lookup"><span data-stu-id="9cd5e-147">NOTES</span></span>

## <span data-ttu-id="9cd5e-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9cd5e-148">RELATED LINKS</span></span>
