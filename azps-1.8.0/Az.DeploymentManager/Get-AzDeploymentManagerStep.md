---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
ms.openlocfilehash: eb0c7db4706aacfba4010632422869f0dca54694
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684465"
---
# <span data-ttu-id="6ec73-101">Get-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="6ec73-101">Get-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="6ec73-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6ec73-102">SYNOPSIS</span></span>
<span data-ttu-id="6ec73-103">Ottiene il passaggio.</span><span class="sxs-lookup"><span data-stu-id="6ec73-103">Gets the step.</span></span>

## <span data-ttu-id="6ec73-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ec73-104">SYNTAX</span></span>

### <span data-ttu-id="6ec73-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6ec73-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ec73-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ec73-106">ResourceId</span></span>
```
Get-AzDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6ec73-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="6ec73-107">InputObject</span></span>
```
Get-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6ec73-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ec73-108">DESCRIPTION</span></span>
<span data-ttu-id="6ec73-109">Il cmdlet **Get-AzDeploymentManagerStep** ottiene un passaggio e restituisce un oggetto che rappresenta questo passaggio.</span><span class="sxs-lookup"><span data-stu-id="6ec73-109">The **Get-AzDeploymentManagerStep** cmdlet gets a step, and returns an object that represents that step.</span></span>
<span data-ttu-id="6ec73-110">Specificare il passaggio in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6ec73-110">Specify the step by its name and resource group name.</span></span> <span data-ttu-id="6ec73-111">In alternativa, puoi specificare l'oggetto step o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="6ec73-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

<span data-ttu-id="6ec73-112">Puoi modificare l'oggetto localmente e quindi applicare le modifiche apportate all'origine dell'elemento usando il cmdlet Set-AzDeploymentManagerStep.</span><span class="sxs-lookup"><span data-stu-id="6ec73-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="6ec73-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ec73-113">EXAMPLES</span></span>

### <span data-ttu-id="6ec73-114">Esempio 1: ottenere un passaggio</span><span class="sxs-lookup"><span data-stu-id="6ec73-114">Example 1: Get a step</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="6ec73-115">Questo comando ottiene un passaggio denominato ContosoService1WaitStep in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6ec73-115">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="6ec73-116">Esempio 2: ottenere un passaggio usando l'identificatore delle risorse</span><span class="sxs-lookup"><span data-stu-id="6ec73-116">Example 2: Get a step using the resource identifier</span></span>
### <span data-ttu-id="6ec73-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6ec73-117">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="6ec73-118">Questo comando ottiene un passaggio denominato ContosoService1WaitStep in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6ec73-118">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="6ec73-119">Esempio 3: ottenere un passaggio usando un oggetto restituito da New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="6ec73-119">Example 3: Get a step using an object returned by New-AzDeploymentManagerStep</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="6ec73-120">Questo comando ottiene un passaggio il cui nome e ResourceGroup corrispondono rispettivamente alle proprietà Name e ResourceGroupName della $stepObject.</span><span class="sxs-lookup"><span data-stu-id="6ec73-120">This command gets a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="6ec73-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6ec73-121">PARAMETERS</span></span>

### <span data-ttu-id="6ec73-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ec73-122">-DefaultProfile</span></span>
<span data-ttu-id="6ec73-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6ec73-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ec73-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ec73-124">-InputObject</span></span>
<span data-ttu-id="6ec73-125">Oggetto risorsa passaggio.</span><span class="sxs-lookup"><span data-stu-id="6ec73-125">The step resource object.</span></span>

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

### <span data-ttu-id="6ec73-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="6ec73-126">-Name</span></span>
<span data-ttu-id="6ec73-127">Nome del passaggio.</span><span class="sxs-lookup"><span data-stu-id="6ec73-127">The name of the step.</span></span>

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

### <span data-ttu-id="6ec73-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ec73-128">-ResourceGroupName</span></span>
<span data-ttu-id="6ec73-129">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="6ec73-129">The resource group.</span></span>

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

### <span data-ttu-id="6ec73-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ec73-130">-ResourceId</span></span>
<span data-ttu-id="6ec73-131">Identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6ec73-131">The resource identifier.</span></span>

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

### <span data-ttu-id="6ec73-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ec73-132">CommonParameters</span></span>
<span data-ttu-id="6ec73-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ec73-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ec73-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ec73-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ec73-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6ec73-135">INPUTS</span></span>

### <span data-ttu-id="6ec73-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6ec73-136">System.String</span></span>

### <span data-ttu-id="6ec73-137">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="6ec73-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="6ec73-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ec73-138">OUTPUTS</span></span>

### <span data-ttu-id="6ec73-139">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="6ec73-139">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="6ec73-140">Note</span><span class="sxs-lookup"><span data-stu-id="6ec73-140">NOTES</span></span>

## <span data-ttu-id="6ec73-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ec73-141">RELATED LINKS</span></span>
