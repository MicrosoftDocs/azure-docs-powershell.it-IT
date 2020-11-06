---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: 21d0b4f7feec5b32ff732f880924becddd84db73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490697"
---
# <span data-ttu-id="85f23-101">Get-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="85f23-101">Get-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="85f23-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="85f23-102">SYNOPSIS</span></span>
<span data-ttu-id="85f23-103">Ottiene un implementazione.</span><span class="sxs-lookup"><span data-stu-id="85f23-103">Gets a rollout.</span></span>

## <span data-ttu-id="85f23-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85f23-104">SYNTAX</span></span>

### <span data-ttu-id="85f23-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="85f23-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [[-RetryAttempt] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85f23-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="85f23-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="85f23-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="85f23-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="85f23-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85f23-108">DESCRIPTION</span></span>
<span data-ttu-id="85f23-109">Il cmdlet **Get-AzureRmDeploymentManagerRollout** ottiene un'implementazione e restituisce un oggetto che rappresenta l'implementazione con tutte le informazioni dettagliate sullo stato di avanzamento dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="85f23-109">The **Get-AzureRmDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="85f23-110">Specificare l'implementazione per nome e nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="85f23-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="85f23-111">In alternativa, puoi specificare l'oggetto di implementazione o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="85f23-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="85f23-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85f23-112">EXAMPLES</span></span>

### <span data-ttu-id="85f23-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="85f23-113">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="85f23-114">Questo comando ottiene un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="85f23-114">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="85f23-115">Esempio 2: ottenere un'implementazione usando l'identificatore delle risorse</span><span class="sxs-lookup"><span data-stu-id="85f23-115">Example 2: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="85f23-116">Questo comando ottiene un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="85f23-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="85f23-117">Esempio 3: ottenere un'implementazione usando l'oggetto implementazione.</span><span class="sxs-lookup"><span data-stu-id="85f23-117">Example 3: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="85f23-118">Questo comando ottiene un implementazione il cui nome e ResourceGroup corrispondono rispettivamente alle proprietà Name e ResourceGroupName della $rolloutObject.</span><span class="sxs-lookup"><span data-stu-id="85f23-118">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="85f23-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="85f23-119">PARAMETERS</span></span>

### <span data-ttu-id="85f23-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85f23-120">-DefaultProfile</span></span>
<span data-ttu-id="85f23-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="85f23-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85f23-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="85f23-122">-Name</span></span>
<span data-ttu-id="85f23-123">Nome dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="85f23-123">The name of the rollout.</span></span>

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

### <span data-ttu-id="85f23-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85f23-124">-ResourceGroupName</span></span>
<span data-ttu-id="85f23-125">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="85f23-125">The resource group.</span></span>

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

### <span data-ttu-id="85f23-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85f23-126">-ResourceId</span></span>
<span data-ttu-id="85f23-127">Identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="85f23-127">The resource identifier.</span></span>

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

### <span data-ttu-id="85f23-128">-RetryAttempt</span><span class="sxs-lookup"><span data-stu-id="85f23-128">-RetryAttempt</span></span>
<span data-ttu-id="85f23-129">Tentativo di riprova dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="85f23-129">The retry attempt of the rollout.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Interactive
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85f23-130">-Implementazione</span><span class="sxs-lookup"><span data-stu-id="85f23-130">-Rollout</span></span>
<span data-ttu-id="85f23-131">Oggetto implementazione.</span><span class="sxs-lookup"><span data-stu-id="85f23-131">Rollout object.</span></span>

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

### <span data-ttu-id="85f23-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85f23-132">CommonParameters</span></span>
<span data-ttu-id="85f23-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85f23-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85f23-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85f23-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85f23-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="85f23-135">INPUTS</span></span>

### <span data-ttu-id="85f23-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="85f23-136">None</span></span>

## <span data-ttu-id="85f23-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85f23-137">OUTPUTS</span></span>

### <span data-ttu-id="85f23-138">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="85f23-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="85f23-139">Note</span><span class="sxs-lookup"><span data-stu-id="85f23-139">NOTES</span></span>

## <span data-ttu-id="85f23-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85f23-140">RELATED LINKS</span></span>

[<span data-ttu-id="85f23-141">Stop-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="85f23-141">Stop-AzureRmDeploymentManagerRollout</span></span>](./Stop-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="85f23-142">Riavviare-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="85f23-142">Restart-AzureRmDeploymentManagerRollout</span></span>](./Restart-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="85f23-143">Remove-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="85f23-143">Remove-AzureRmDeploymentManagerRollout</span></span>](./Remove-AzureRmDeploymentManagerRollout.md)