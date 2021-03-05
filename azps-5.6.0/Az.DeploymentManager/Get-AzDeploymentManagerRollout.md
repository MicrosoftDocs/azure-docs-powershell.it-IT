---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: 53458d53dd6d8b3f698dc51fc6b1463c9a9134e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966365"
---
# <span data-ttu-id="b5ed7-101">Get-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="b5ed7-101">Get-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="b5ed7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5ed7-102">SYNOPSIS</span></span>
<span data-ttu-id="b5ed7-103">Recupera l'implementazione.</span><span class="sxs-lookup"><span data-stu-id="b5ed7-103">Gets the rollout.</span></span>

## <span data-ttu-id="b5ed7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5ed7-104">SYNTAX</span></span>

### <span data-ttu-id="b5ed7-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b5ed7-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceGroupName] <String> [[-Name] <String>] [-RetryAttempt <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b5ed7-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5ed7-106">ResourceId</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5ed7-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b5ed7-107">InputObject</span></span>
```
Get-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5ed7-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b5ed7-108">DESCRIPTION</span></span>
<span data-ttu-id="b5ed7-109">Il cmdlet **Get-AzDeploymentManagerRollout** ottiene un'implementazione e restituisce un oggetto che rappresenta l'implementazione con tutte le informazioni dettagliate sullo stato dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="b5ed7-109">The **Get-AzDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="b5ed7-110">Specificare l'implementazione in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b5ed7-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="b5ed7-111">In alternativa, è possibile specificare l'oggetto Rollout o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="b5ed7-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="b5ed7-112">L'oggetto implementazione restituito contiene i servizi, le unità di servizio e i passaggi distribuiti e quelli in corso.</span><span class="sxs-lookup"><span data-stu-id="b5ed7-112">The returned rollout object contains the services, service units and steps that have been deployed and the ones in progress.</span></span> <span data-ttu-id="b5ed7-113">Quelle ancora da distribuire non sono in risposta.</span><span class="sxs-lookup"><span data-stu-id="b5ed7-113">Those that are yet to be deployed are not in the response.</span></span>

## <span data-ttu-id="b5ed7-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5ed7-114">EXAMPLES</span></span>

### <span data-ttu-id="b5ed7-115">Esempio 1: Eseguire l'implementazione</span><span class="sxs-lookup"><span data-stu-id="b5ed7-115">Example 1 Get the rollout</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="b5ed7-116">Questo comando ottiene un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b5ed7-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="b5ed7-117">Esempio 2: Ottenere e visualizzare i dettagli dell'implementazione</span><span class="sxs-lookup"><span data-stu-id="b5ed7-117">Example 2 Get and display the rollout details</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

<span data-ttu-id="b5ed7-118">Questo comando ottiene un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b5ed7-118">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="b5ed7-119">L'opzione -Verbose visualizza tutti i dettagli dell'implementazione in modo gerarchico; Visualizzazione di Services, ServiceUnits e i passaggi descritti in ogni ServiceUnit e informazioni contestuali per ogni passaggio per una visualizzazione olistica dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="b5ed7-119">The -Verbose switch displays all the rollout details hierarchically; showing the Services, the ServiceUnits and the steps under each ServiceUnit and contextual information for each step for a holistic view of the rollout.</span></span>

### <span data-ttu-id="b5ed7-120">Esempio 3: Ottenere un'implementazione con l'identificatore di risorsa</span><span class="sxs-lookup"><span data-stu-id="b5ed7-120">Example 3: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="b5ed7-121">Questo comando ottiene un'implementazione denominata ContosoRollout in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b5ed7-121">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="b5ed7-122">Esempio 4: Ottenere un'implementazione con l'oggetto di implementazione.</span><span class="sxs-lookup"><span data-stu-id="b5ed7-122">Example 4: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="b5ed7-123">Questo comando ottiene un'implementazione il cui nome e GruppoSocietà Risorse corrispondono rispettivamente alle proprietà Name e ResourceGroupName dell'$rolloutObject.</span><span class="sxs-lookup"><span data-stu-id="b5ed7-123">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="b5ed7-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5ed7-124">PARAMETERS</span></span>

### <span data-ttu-id="b5ed7-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5ed7-125">-DefaultProfile</span></span>
<span data-ttu-id="b5ed7-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b5ed7-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5ed7-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5ed7-127">-InputObject</span></span>
<span data-ttu-id="b5ed7-128">Oggetto di implementazione.</span><span class="sxs-lookup"><span data-stu-id="b5ed7-128">Rollout object.</span></span>

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

### <span data-ttu-id="b5ed7-129">-Name</span><span class="sxs-lookup"><span data-stu-id="b5ed7-129">-Name</span></span>
<span data-ttu-id="b5ed7-130">Nome dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="b5ed7-130">The name of the rollout.</span></span>

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

### <span data-ttu-id="b5ed7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5ed7-131">-ResourceGroupName</span></span>
<span data-ttu-id="b5ed7-132">Gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b5ed7-132">The resource group.</span></span>

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

### <span data-ttu-id="b5ed7-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5ed7-133">-ResourceId</span></span>
<span data-ttu-id="b5ed7-134">L'identificatore di risorsa.</span><span class="sxs-lookup"><span data-stu-id="b5ed7-134">The resource identifier.</span></span>

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

### <span data-ttu-id="b5ed7-135">-RetryAttempt</span><span class="sxs-lookup"><span data-stu-id="b5ed7-135">-RetryAttempt</span></span>
<span data-ttu-id="b5ed7-136">Riprovare a eseguire l'implementazione.</span><span class="sxs-lookup"><span data-stu-id="b5ed7-136">The retry attempt of the rollout.</span></span>

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

### <span data-ttu-id="b5ed7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5ed7-137">CommonParameters</span></span>
<span data-ttu-id="b5ed7-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5ed7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5ed7-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b5ed7-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5ed7-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="b5ed7-140">INPUTS</span></span>

### <span data-ttu-id="b5ed7-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b5ed7-141">System.String</span></span>

### <span data-ttu-id="b5ed7-142">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b5ed7-142">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="b5ed7-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="b5ed7-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="b5ed7-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5ed7-144">OUTPUTS</span></span>

### <span data-ttu-id="b5ed7-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="b5ed7-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="b5ed7-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="b5ed7-146">NOTES</span></span>

## <span data-ttu-id="b5ed7-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5ed7-147">RELATED LINKS</span></span>
