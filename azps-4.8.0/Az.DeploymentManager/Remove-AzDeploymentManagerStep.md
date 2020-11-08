---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerStep.md
ms.openlocfilehash: 5e4af2ef006e51cee135dd642bcae7282940e8be
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031255"
---
# <span data-ttu-id="a8883-101">Remove-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="a8883-101">Remove-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="a8883-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a8883-102">SYNOPSIS</span></span>
<span data-ttu-id="a8883-103">Elimina il passaggio.</span><span class="sxs-lookup"><span data-stu-id="a8883-103">Deletes the step.</span></span>

## <span data-ttu-id="a8883-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8883-104">SYNTAX</span></span>

### <span data-ttu-id="a8883-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a8883-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8883-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8883-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerStep [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8883-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="a8883-107">InputObject</span></span>
```
Remove-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8883-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8883-108">DESCRIPTION</span></span>
<span data-ttu-id="a8883-109">Il cmdlet **Remove-AzDeploymentManagerStep** Elimina un passaggio.</span><span class="sxs-lookup"><span data-stu-id="a8883-109">The **Remove-AzDeploymentManagerStep** cmdlet deletes a step.</span></span>
<span data-ttu-id="a8883-110">Specificare il passaggio in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a8883-110">Specify the step by its name and the resource group name.</span></span> <span data-ttu-id="a8883-111">In alternativa, puoi specificare l'oggetto step o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="a8883-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

## <span data-ttu-id="a8883-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8883-112">EXAMPLES</span></span>

### <span data-ttu-id="a8883-113">Esempio 1: rimuovere un passaggio</span><span class="sxs-lookup"><span data-stu-id="a8883-113">Example 1: Remove a step</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="a8883-114">Questo comando Elimina un passaggio denominato ContosoService1WaitStep in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a8883-114">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="a8883-115">Esempio 2: rimuovere un passaggio usando l'identificatore delle risorse</span><span class="sxs-lookup"><span data-stu-id="a8883-115">Example 2: Remove a step using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="a8883-116">Questo comando Elimina un passaggio denominato ContosoService1WaitStep in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a8883-116">This command deletes a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="a8883-117">Esempio 3: rimuovere un passaggio usando un oggetto restituito da New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="a8883-117">Example 3: Remove a step using an object returned by New-AzDeploymentManagerStep</span></span>
### <span data-ttu-id="a8883-118">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a8883-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="a8883-119">Questo comando Elimina un passaggio il cui nome e ResourceGroup corrispondono rispettivamente alle proprietà Name e ResourceGroupName della $stepObject.</span><span class="sxs-lookup"><span data-stu-id="a8883-119">This command deletes a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="a8883-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a8883-120">PARAMETERS</span></span>

### <span data-ttu-id="a8883-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8883-121">-DefaultProfile</span></span>
<span data-ttu-id="a8883-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a8883-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8883-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8883-123">-InputObject</span></span>
<span data-ttu-id="a8883-124">Passaggio da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="a8883-124">The step to be removed.</span></span>

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

### <span data-ttu-id="a8883-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="a8883-125">-Name</span></span>
<span data-ttu-id="a8883-126">Nome del passaggio.</span><span class="sxs-lookup"><span data-stu-id="a8883-126">The name of the step.</span></span>

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

### <span data-ttu-id="a8883-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8883-127">-PassThru</span></span>
<span data-ttu-id="a8883-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a8883-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a8883-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8883-129">-ResourceGroupName</span></span>
<span data-ttu-id="a8883-130">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="a8883-130">The resource group.</span></span>

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

### <span data-ttu-id="a8883-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8883-131">-ResourceId</span></span>
<span data-ttu-id="a8883-132">Identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a8883-132">The resource identifier.</span></span>

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

### <span data-ttu-id="a8883-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a8883-133">-Confirm</span></span>
<span data-ttu-id="a8883-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8883-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8883-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8883-135">-WhatIf</span></span>
<span data-ttu-id="a8883-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8883-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8883-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8883-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8883-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8883-138">CommonParameters</span></span>
<span data-ttu-id="a8883-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8883-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8883-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8883-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8883-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a8883-141">INPUTS</span></span>

### <span data-ttu-id="a8883-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a8883-142">System.String</span></span>

### <span data-ttu-id="a8883-143">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="a8883-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="a8883-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8883-144">OUTPUTS</span></span>

### <span data-ttu-id="a8883-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a8883-145">System.Boolean</span></span>

## <span data-ttu-id="a8883-146">Note</span><span class="sxs-lookup"><span data-stu-id="a8883-146">NOTES</span></span>

## <span data-ttu-id="a8883-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8883-147">RELATED LINKS</span></span>
