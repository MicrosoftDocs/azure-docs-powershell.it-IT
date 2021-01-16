---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: c01c41ff476ee4e6b8a6291f5ebcfbf4c176b775
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387488"
---
# <span data-ttu-id="373a8-101">Get-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="373a8-101">Get-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="373a8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="373a8-102">SYNOPSIS</span></span>
<span data-ttu-id="373a8-103">Ottiene l'implementazione.</span><span class="sxs-lookup"><span data-stu-id="373a8-103">Gets the rollout.</span></span>

## <span data-ttu-id="373a8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="373a8-104">SYNTAX</span></span>

### <span data-ttu-id="373a8-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="373a8-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceGroupName] <String> [[-Name] <String>] [-RetryAttempt <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="373a8-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="373a8-106">ResourceId</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="373a8-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="373a8-107">InputObject</span></span>
```
Get-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="373a8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="373a8-108">DESCRIPTION</span></span>
<span data-ttu-id="373a8-109">Il cmdlet **Get-AzDeploymentManagerRollout** ottiene un'implementazione e restituisce un oggetto che rappresenta l'implementazione con tutte le informazioni dettagliate sullo stato di avanzamento dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="373a8-109">The **Get-AzDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="373a8-110">Specificare l'implementazione per nome e nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="373a8-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="373a8-111">In alternativa, puoi specificare l'oggetto di implementazione o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="373a8-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="373a8-112">L'oggetto di implementazione restituito contiene i servizi, le unità di servizio e i passaggi distribuiti e quelli in corso.</span><span class="sxs-lookup"><span data-stu-id="373a8-112">The returned rollout object contains the services, service units and steps that have been deployed and the ones in progress.</span></span> <span data-ttu-id="373a8-113">Gli utenti che devono ancora essere distribuiti non sono presenti nella risposta.</span><span class="sxs-lookup"><span data-stu-id="373a8-113">Those that are yet to be deployed are not in the response.</span></span>

## <span data-ttu-id="373a8-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="373a8-114">EXAMPLES</span></span>

### <span data-ttu-id="373a8-115">Esempio 1 ottenere l'implementazione</span><span class="sxs-lookup"><span data-stu-id="373a8-115">Example 1 Get the rollout</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="373a8-116">Questo comando ottiene un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="373a8-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="373a8-117">Esempio 2 ottenere e visualizzare i dettagli di implementazione</span><span class="sxs-lookup"><span data-stu-id="373a8-117">Example 2 Get and display the rollout details</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

<span data-ttu-id="373a8-118">Questo comando ottiene un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="373a8-118">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="373a8-119">L'opzione-verbose Visualizza tutti i dettagli di implementazione gerarchici; Visualizzazione dei servizi, ServiceUnits e dei passaggi in ogni ServiceUnit e informazioni contestuali per ogni passaggio per una visualizzazione olistica dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="373a8-119">The -Verbose switch displays all the rollout details hierarchically; showing the Services, the ServiceUnits and the steps under each ServiceUnit and contextual information for each step for a holistic view of the rollout.</span></span>

### <span data-ttu-id="373a8-120">Esempio 3: ottenere un'implementazione usando l'identificatore delle risorse</span><span class="sxs-lookup"><span data-stu-id="373a8-120">Example 3: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="373a8-121">Questo comando ottiene un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="373a8-121">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="373a8-122">Esempio 4: ottenere un'implementazione usando l'oggetto implementazione.</span><span class="sxs-lookup"><span data-stu-id="373a8-122">Example 4: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="373a8-123">Questo comando ottiene un implementazione il cui nome e ResourceGroup corrispondono rispettivamente alle proprietà Name e ResourceGroupName della $rolloutObject.</span><span class="sxs-lookup"><span data-stu-id="373a8-123">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="373a8-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="373a8-124">PARAMETERS</span></span>

### <span data-ttu-id="373a8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="373a8-125">-DefaultProfile</span></span>
<span data-ttu-id="373a8-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="373a8-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="373a8-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="373a8-127">-InputObject</span></span>
<span data-ttu-id="373a8-128">Oggetto implementazione.</span><span class="sxs-lookup"><span data-stu-id="373a8-128">Rollout object.</span></span>

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

### <span data-ttu-id="373a8-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="373a8-129">-Name</span></span>
<span data-ttu-id="373a8-130">Nome dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="373a8-130">The name of the rollout.</span></span>

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

### <span data-ttu-id="373a8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="373a8-131">-ResourceGroupName</span></span>
<span data-ttu-id="373a8-132">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="373a8-132">The resource group.</span></span>

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

### <span data-ttu-id="373a8-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="373a8-133">-ResourceId</span></span>
<span data-ttu-id="373a8-134">Identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="373a8-134">The resource identifier.</span></span>

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

### <span data-ttu-id="373a8-135">-RetryAttempt</span><span class="sxs-lookup"><span data-stu-id="373a8-135">-RetryAttempt</span></span>
<span data-ttu-id="373a8-136">Tentativo di riprova dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="373a8-136">The retry attempt of the rollout.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Interactive
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="373a8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="373a8-137">CommonParameters</span></span>
<span data-ttu-id="373a8-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="373a8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="373a8-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="373a8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="373a8-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="373a8-140">INPUTS</span></span>

### <span data-ttu-id="373a8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="373a8-141">System.String</span></span>

### <span data-ttu-id="373a8-142">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="373a8-142">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="373a8-143">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="373a8-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="373a8-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="373a8-144">OUTPUTS</span></span>

### <span data-ttu-id="373a8-145">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="373a8-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="373a8-146">Note</span><span class="sxs-lookup"><span data-stu-id="373a8-146">NOTES</span></span>

## <span data-ttu-id="373a8-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="373a8-147">RELATED LINKS</span></span>
