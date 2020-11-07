---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: fbcb93ec75dc0e136c1c18743a8686f7642ef02f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684470"
---
# <span data-ttu-id="7dbdb-101">Get-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="7dbdb-101">Get-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="7dbdb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7dbdb-102">SYNOPSIS</span></span>
<span data-ttu-id="7dbdb-103">Ottiene l'implementazione.</span><span class="sxs-lookup"><span data-stu-id="7dbdb-103">Gets the rollout.</span></span>

## <span data-ttu-id="7dbdb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7dbdb-104">SYNTAX</span></span>

### <span data-ttu-id="7dbdb-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7dbdb-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-RetryAttempt <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7dbdb-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7dbdb-106">ResourceId</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7dbdb-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="7dbdb-107">InputObject</span></span>
```
Get-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7dbdb-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7dbdb-108">DESCRIPTION</span></span>
<span data-ttu-id="7dbdb-109">Il cmdlet **Get-AzDeploymentManagerRollout** ottiene un'implementazione e restituisce un oggetto che rappresenta l'implementazione con tutte le informazioni dettagliate sullo stato di avanzamento dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="7dbdb-109">The **Get-AzDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="7dbdb-110">Specificare l'implementazione per nome e nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7dbdb-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="7dbdb-111">In alternativa, puoi specificare l'oggetto di implementazione o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="7dbdb-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="7dbdb-112">L'oggetto di implementazione restituito contiene i servizi, le unità di servizio e i passaggi distribuiti e quelli in corso.</span><span class="sxs-lookup"><span data-stu-id="7dbdb-112">The returned rollout object contains the services, service units and steps that have been deployed and the ones in progress.</span></span> <span data-ttu-id="7dbdb-113">Gli utenti che devono ancora essere distribuiti non sono presenti nella risposta.</span><span class="sxs-lookup"><span data-stu-id="7dbdb-113">Those that are yet to be deployed are not in the response.</span></span>

## <span data-ttu-id="7dbdb-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7dbdb-114">EXAMPLES</span></span>

### <span data-ttu-id="7dbdb-115">Esempio 1 ottenere l'implementazione</span><span class="sxs-lookup"><span data-stu-id="7dbdb-115">Example 1 Get the rollout</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="7dbdb-116">Questo comando ottiene un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7dbdb-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="7dbdb-117">Esempio 2 ottenere e visualizzare i dettagli di implementazione</span><span class="sxs-lookup"><span data-stu-id="7dbdb-117">Example 2 Get and display the rollout details</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

<span data-ttu-id="7dbdb-118">Questo comando ottiene un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7dbdb-118">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="7dbdb-119">L'opzione-verbose Visualizza tutti i dettagli di implementazione gerarchici; Visualizzazione dei servizi, ServiceUnits e dei passaggi in ogni ServiceUnit e informazioni contestuali per ogni passaggio per una visualizzazione olistica dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="7dbdb-119">The -Verbose switch displays all the rollout details hierarchically; showing the Services, the ServiceUnits and the steps under each ServiceUnit and contextual information for each step for a holistic view of the rollout.</span></span>

### <span data-ttu-id="7dbdb-120">Esempio 3: ottenere un'implementazione usando l'identificatore delle risorse</span><span class="sxs-lookup"><span data-stu-id="7dbdb-120">Example 3: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="7dbdb-121">Questo comando ottiene un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7dbdb-121">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="7dbdb-122">Esempio 4: ottenere un'implementazione usando l'oggetto implementazione.</span><span class="sxs-lookup"><span data-stu-id="7dbdb-122">Example 4: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="7dbdb-123">Questo comando ottiene un implementazione il cui nome e ResourceGroup corrispondono rispettivamente alle proprietà Name e ResourceGroupName della $rolloutObject.</span><span class="sxs-lookup"><span data-stu-id="7dbdb-123">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="7dbdb-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7dbdb-124">PARAMETERS</span></span>

### <span data-ttu-id="7dbdb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dbdb-125">-DefaultProfile</span></span>
<span data-ttu-id="7dbdb-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7dbdb-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7dbdb-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7dbdb-127">-InputObject</span></span>
<span data-ttu-id="7dbdb-128">Oggetto implementazione.</span><span class="sxs-lookup"><span data-stu-id="7dbdb-128">Rollout object.</span></span>

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

### <span data-ttu-id="7dbdb-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="7dbdb-129">-Name</span></span>
<span data-ttu-id="7dbdb-130">Nome dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="7dbdb-130">The name of the rollout.</span></span>

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

### <span data-ttu-id="7dbdb-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7dbdb-131">-ResourceGroupName</span></span>
<span data-ttu-id="7dbdb-132">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="7dbdb-132">The resource group.</span></span>

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

### <span data-ttu-id="7dbdb-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7dbdb-133">-ResourceId</span></span>
<span data-ttu-id="7dbdb-134">Identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="7dbdb-134">The resource identifier.</span></span>

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

### <span data-ttu-id="7dbdb-135">-RetryAttempt</span><span class="sxs-lookup"><span data-stu-id="7dbdb-135">-RetryAttempt</span></span>
<span data-ttu-id="7dbdb-136">Tentativo di riprova dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="7dbdb-136">The retry attempt of the rollout.</span></span>

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

### <span data-ttu-id="7dbdb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dbdb-137">CommonParameters</span></span>
<span data-ttu-id="7dbdb-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dbdb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dbdb-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dbdb-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dbdb-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7dbdb-140">INPUTS</span></span>

### <span data-ttu-id="7dbdb-141">System. String</span><span class="sxs-lookup"><span data-stu-id="7dbdb-141">System.String</span></span>

### <span data-ttu-id="7dbdb-142">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7dbdb-142">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="7dbdb-143">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="7dbdb-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="7dbdb-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7dbdb-144">OUTPUTS</span></span>

### <span data-ttu-id="7dbdb-145">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="7dbdb-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="7dbdb-146">Note</span><span class="sxs-lookup"><span data-stu-id="7dbdb-146">NOTES</span></span>

## <span data-ttu-id="7dbdb-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7dbdb-147">RELATED LINKS</span></span>
