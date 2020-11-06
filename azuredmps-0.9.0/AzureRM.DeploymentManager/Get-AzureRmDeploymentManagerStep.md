---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: bd17ee5dd653ee66daf014c57661b3787c04b06f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490950"
---
# <span data-ttu-id="5b998-101">Get-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="5b998-101">Get-AzureRmDeploymentManagerStep</span></span>

## <span data-ttu-id="5b998-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5b998-102">SYNOPSIS</span></span>
<span data-ttu-id="5b998-103">Ottiene il passaggio di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="5b998-103">Gets the deployment step.</span></span>

## <span data-ttu-id="5b998-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5b998-104">SYNTAX</span></span>

### <span data-ttu-id="5b998-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5b998-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerStep [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b998-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b998-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b998-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="5b998-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerStep [-Step] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b998-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b998-108">DESCRIPTION</span></span>
<span data-ttu-id="5b998-109">Il cmdlet **Get-AzureRmDeploymentManagerStep** ottiene un passaggio e restituisce un oggetto che rappresenta questo passaggio.</span><span class="sxs-lookup"><span data-stu-id="5b998-109">The **Get-AzureRmDeploymentManagerStep** cmdlet gets a step, and returns an object that represents that step.</span></span>
<span data-ttu-id="5b998-110">Specificare il passaggio in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5b998-110">Specify the step by its name and resource group name.</span></span> <span data-ttu-id="5b998-111">In alternativa, puoi specificare l'oggetto step o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="5b998-111">Alternately, you can provide the Step object or the ResourceId.</span></span>

<span data-ttu-id="5b998-112">Puoi modificare l'oggetto localmente e quindi applicare le modifiche apportate all'origine dell'elemento usando il cmdlet Set-AzureRmDeploymentManagerStep.</span><span class="sxs-lookup"><span data-stu-id="5b998-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzureRmDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="5b998-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5b998-113">EXAMPLES</span></span>

### <span data-ttu-id="5b998-114">Esempio 1: ottenere un passaggio</span><span class="sxs-lookup"><span data-stu-id="5b998-114">Example 1: Get a step</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep
```

<span data-ttu-id="5b998-115">Questo comando ottiene un passaggio denominato ContosoService1WaitStep in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5b998-115">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="5b998-116">Esempio 2: ottenere un passaggio usando l'identificatore delle risorse</span><span class="sxs-lookup"><span data-stu-id="5b998-116">Example 2: Get a step using the resource identifier</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerStep -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/steps/ContosoService1WaitStep"
```

<span data-ttu-id="5b998-117">Questo comando ottiene un passaggio denominato ContosoService1WaitStep in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5b998-117">This command gets a step named ContosoService1WaitStep in ContosoResourceGroup.</span></span>

### <span data-ttu-id="5b998-118">Esempio 3: ottenere un passaggio usando un oggetto restituito da New-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="5b998-118">Example 3: Get a step using an object returned by New-AzureRmDeploymentManagerStep</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerStep -Step $stepObject
```

 <span data-ttu-id="5b998-119">Questo comando ottiene un passaggio il cui nome e ResourceGroup corrispondono rispettivamente alle proprietà Name e ResourceGroupName della $stepObject.</span><span class="sxs-lookup"><span data-stu-id="5b998-119">This command gets a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>


## <span data-ttu-id="5b998-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5b998-120">PARAMETERS</span></span>

### <span data-ttu-id="5b998-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b998-121">-DefaultProfile</span></span>
<span data-ttu-id="5b998-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5b998-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b998-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="5b998-123">-Name</span></span>
<span data-ttu-id="5b998-124">Nome del passaggio.</span><span class="sxs-lookup"><span data-stu-id="5b998-124">The name of the step.</span></span>

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

### <span data-ttu-id="5b998-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b998-125">-ResourceGroupName</span></span>
<span data-ttu-id="5b998-126">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="5b998-126">The resource group.</span></span>

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

### <span data-ttu-id="5b998-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b998-127">-ResourceId</span></span>
<span data-ttu-id="5b998-128">Identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="5b998-128">The resource identifier.</span></span>

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

### <span data-ttu-id="5b998-129">-Step</span><span class="sxs-lookup"><span data-stu-id="5b998-129">-Step</span></span>
<span data-ttu-id="5b998-130">Oggetto risorsa passaggio.</span><span class="sxs-lookup"><span data-stu-id="5b998-130">The step resource object.</span></span>

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

### <span data-ttu-id="5b998-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b998-131">CommonParameters</span></span>
<span data-ttu-id="5b998-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b998-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5b998-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b998-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b998-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5b998-134">INPUTS</span></span>

### <span data-ttu-id="5b998-135">System. String</span><span class="sxs-lookup"><span data-stu-id="5b998-135">System.String</span></span>

### <span data-ttu-id="5b998-136">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="5b998-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="5b998-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5b998-137">OUTPUTS</span></span>

### <span data-ttu-id="5b998-138">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="5b998-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="5b998-139">Note</span><span class="sxs-lookup"><span data-stu-id="5b998-139">NOTES</span></span>

## <span data-ttu-id="5b998-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5b998-140">RELATED LINKS</span></span>
