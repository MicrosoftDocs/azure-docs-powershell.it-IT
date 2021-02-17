---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
ms.openlocfilehash: 68bc2af69c3450f0c52c5613057ba4b2db211ee8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196518"
---
# <span data-ttu-id="85546-101">Get-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="85546-101">Get-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="85546-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85546-102">SYNOPSIS</span></span>
<span data-ttu-id="85546-103">Ottiene il passaggio.</span><span class="sxs-lookup"><span data-stu-id="85546-103">Gets the step.</span></span>

## <span data-ttu-id="85546-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85546-104">SYNTAX</span></span>

### <span data-ttu-id="85546-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="85546-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerStep [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85546-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="85546-106">ResourceId</span></span>
```
Get-AzDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="85546-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="85546-107">InputObject</span></span>
```
Get-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="85546-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="85546-108">DESCRIPTION</span></span>
<span data-ttu-id="85546-109">Il cmdlet **Get-AzDeploymentManagerStep** ottiene un passaggio e restituisce un oggetto che rappresenta tale passaggio.</span><span class="sxs-lookup"><span data-stu-id="85546-109">The **Get-AzDeploymentManagerStep** cmdlet gets a step, and returns an object that represents that step.</span></span>
<span data-ttu-id="85546-110">Specificare il passaggio in base al nome e al gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="85546-110">Specify the step by its name and resource group name.</span></span> <span data-ttu-id="85546-111">In alternativa, è possibile specificare l'oggetto Step o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="85546-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

<span data-ttu-id="85546-112">È possibile modificare l'oggetto in locale e quindi applicare le modifiche all'origine dell'elemento usando il cmdlet Set-AzDeploymentManagerStep.</span><span class="sxs-lookup"><span data-stu-id="85546-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="85546-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85546-113">EXAMPLES</span></span>

### <span data-ttu-id="85546-114">Esempio 1: Eseguire un passaggio</span><span class="sxs-lookup"><span data-stu-id="85546-114">Example 1: Get a step</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="85546-115">Questo comando ottiene un passaggio denominato ContosoService1WaitStep in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="85546-115">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="85546-116">Esempio 2: Ottenere un passaggio usando l'identificatore di risorsa</span><span class="sxs-lookup"><span data-stu-id="85546-116">Example 2: Get a step using the resource identifier</span></span>
### <span data-ttu-id="85546-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="85546-117">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="85546-118">Questo comando ottiene un passaggio denominato ContosoService1WaitStep in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="85546-118">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="85546-119">Esempio 3: Eseguire un passaggio usando un oggetto restituito da New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="85546-119">Example 3: Get a step using an object returned by New-AzDeploymentManagerStep</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="85546-120">Questo comando ottiene un passaggio il cui nome e Gruppo Risorse corrispondono rispettivamente alle proprietà Name e ResourceGroupName dell'$stepObject.</span><span class="sxs-lookup"><span data-stu-id="85546-120">This command gets a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="85546-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85546-121">PARAMETERS</span></span>

### <span data-ttu-id="85546-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85546-122">-DefaultProfile</span></span>
<span data-ttu-id="85546-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="85546-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85546-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85546-124">-InputObject</span></span>
<span data-ttu-id="85546-125">Oggetto risorsa passaggio.</span><span class="sxs-lookup"><span data-stu-id="85546-125">The step resource object.</span></span>

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

### <span data-ttu-id="85546-126">-Name</span><span class="sxs-lookup"><span data-stu-id="85546-126">-Name</span></span>
<span data-ttu-id="85546-127">Nome del passaggio.</span><span class="sxs-lookup"><span data-stu-id="85546-127">The name of the step.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85546-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85546-128">-ResourceGroupName</span></span>
<span data-ttu-id="85546-129">Gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="85546-129">The resource group.</span></span>

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

### <span data-ttu-id="85546-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85546-130">-ResourceId</span></span>
<span data-ttu-id="85546-131">L'identificatore di risorsa.</span><span class="sxs-lookup"><span data-stu-id="85546-131">The resource identifier.</span></span>

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

### <span data-ttu-id="85546-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85546-132">CommonParameters</span></span>
<span data-ttu-id="85546-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85546-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85546-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="85546-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85546-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="85546-135">INPUTS</span></span>

### <span data-ttu-id="85546-136">System.String</span><span class="sxs-lookup"><span data-stu-id="85546-136">System.String</span></span>

### <span data-ttu-id="85546-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="85546-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="85546-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85546-138">OUTPUTS</span></span>

### <span data-ttu-id="85546-139">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="85546-139">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="85546-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="85546-140">NOTES</span></span>

## <span data-ttu-id="85546-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85546-141">RELATED LINKS</span></span>
