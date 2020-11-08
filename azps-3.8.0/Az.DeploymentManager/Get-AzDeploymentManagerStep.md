---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerStep.md
ms.openlocfilehash: 68bc2af69c3450f0c52c5613057ba4b2db211ee8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022345"
---
# <span data-ttu-id="22c81-101">Get-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="22c81-101">Get-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="22c81-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="22c81-102">SYNOPSIS</span></span>
<span data-ttu-id="22c81-103">Ottiene il passaggio.</span><span class="sxs-lookup"><span data-stu-id="22c81-103">Gets the step.</span></span>

## <span data-ttu-id="22c81-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22c81-104">SYNTAX</span></span>

### <span data-ttu-id="22c81-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="22c81-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerStep [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22c81-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="22c81-106">ResourceId</span></span>
```
Get-AzDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="22c81-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="22c81-107">InputObject</span></span>
```
Get-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22c81-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22c81-108">DESCRIPTION</span></span>
<span data-ttu-id="22c81-109">Il cmdlet **Get-AzDeploymentManagerStep** ottiene un passaggio e restituisce un oggetto che rappresenta questo passaggio.</span><span class="sxs-lookup"><span data-stu-id="22c81-109">The **Get-AzDeploymentManagerStep** cmdlet gets a step, and returns an object that represents that step.</span></span>
<span data-ttu-id="22c81-110">Specificare il passaggio in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="22c81-110">Specify the step by its name and resource group name.</span></span> <span data-ttu-id="22c81-111">In alternativa, puoi specificare l'oggetto step o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="22c81-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

<span data-ttu-id="22c81-112">Puoi modificare l'oggetto localmente e quindi applicare le modifiche apportate all'origine dell'elemento usando il cmdlet Set-AzDeploymentManagerStep.</span><span class="sxs-lookup"><span data-stu-id="22c81-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="22c81-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22c81-113">EXAMPLES</span></span>

### <span data-ttu-id="22c81-114">Esempio 1: ottenere un passaggio</span><span class="sxs-lookup"><span data-stu-id="22c81-114">Example 1: Get a step</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="22c81-115">Questo comando ottiene un passaggio denominato ContosoService1WaitStep in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="22c81-115">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="22c81-116">Esempio 2: ottenere un passaggio usando l'identificatore delle risorse</span><span class="sxs-lookup"><span data-stu-id="22c81-116">Example 2: Get a step using the resource identifier</span></span>
### <span data-ttu-id="22c81-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="22c81-117">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="22c81-118">Questo comando ottiene un passaggio denominato ContosoService1WaitStep in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="22c81-118">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="22c81-119">Esempio 3: ottenere un passaggio usando un oggetto restituito da New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="22c81-119">Example 3: Get a step using an object returned by New-AzDeploymentManagerStep</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerStep -InputObject $stepObject
```

 <span data-ttu-id="22c81-120">Questo comando ottiene un passaggio il cui nome e ResourceGroup corrispondono rispettivamente alle proprietà Name e ResourceGroupName della $stepObject.</span><span class="sxs-lookup"><span data-stu-id="22c81-120">This command gets a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>

## <span data-ttu-id="22c81-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="22c81-121">PARAMETERS</span></span>

### <span data-ttu-id="22c81-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22c81-122">-DefaultProfile</span></span>
<span data-ttu-id="22c81-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="22c81-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22c81-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22c81-124">-InputObject</span></span>
<span data-ttu-id="22c81-125">Oggetto risorsa passaggio.</span><span class="sxs-lookup"><span data-stu-id="22c81-125">The step resource object.</span></span>

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

### <span data-ttu-id="22c81-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="22c81-126">-Name</span></span>
<span data-ttu-id="22c81-127">Nome del passaggio.</span><span class="sxs-lookup"><span data-stu-id="22c81-127">The name of the step.</span></span>

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

### <span data-ttu-id="22c81-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22c81-128">-ResourceGroupName</span></span>
<span data-ttu-id="22c81-129">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="22c81-129">The resource group.</span></span>

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

### <span data-ttu-id="22c81-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22c81-130">-ResourceId</span></span>
<span data-ttu-id="22c81-131">Identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="22c81-131">The resource identifier.</span></span>

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

### <span data-ttu-id="22c81-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22c81-132">CommonParameters</span></span>
<span data-ttu-id="22c81-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22c81-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22c81-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22c81-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22c81-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="22c81-135">INPUTS</span></span>

### <span data-ttu-id="22c81-136">System. String</span><span class="sxs-lookup"><span data-stu-id="22c81-136">System.String</span></span>

### <span data-ttu-id="22c81-137">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="22c81-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="22c81-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22c81-138">OUTPUTS</span></span>

### <span data-ttu-id="22c81-139">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="22c81-139">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="22c81-140">Note</span><span class="sxs-lookup"><span data-stu-id="22c81-140">NOTES</span></span>

## <span data-ttu-id="22c81-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22c81-141">RELATED LINKS</span></span>
