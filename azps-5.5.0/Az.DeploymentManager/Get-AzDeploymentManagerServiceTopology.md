---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: f3d85ef89bbc6d427801120f5c7a3a37a8fc855a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177006"
---
# <span data-ttu-id="254bd-101">Get-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="254bd-101">Get-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="254bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="254bd-102">SYNOPSIS</span></span>
<span data-ttu-id="254bd-103">Recupera la topologia del servizio.</span><span class="sxs-lookup"><span data-stu-id="254bd-103">Gets the service topology.</span></span>

## <span data-ttu-id="254bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="254bd-104">SYNTAX</span></span>

### <span data-ttu-id="254bd-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="254bd-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="254bd-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="254bd-106">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="254bd-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="254bd-107">InputObject</span></span>
```
Get-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="254bd-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="254bd-108">DESCRIPTION</span></span>
<span data-ttu-id="254bd-109">Il cmdlet **Get-AzDeploymentManagerServiceTopology** ottiene una topologia di servizio.</span><span class="sxs-lookup"><span data-stu-id="254bd-109">The **Get-AzDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="254bd-110">È possibile modificare l'oggetto in locale e quindi applicare modifiche alla topologia usando il cmdlet Set-AzDeploymentManagerServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="254bd-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="254bd-111">Specificare la topologia del servizio in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="254bd-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="254bd-112">In alternativa, è possibile fornire l'oggetto ServiceTopology o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="254bd-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="254bd-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="254bd-113">EXAMPLES</span></span>

### <span data-ttu-id="254bd-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="254bd-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="254bd-115">Questo comando ottiene una topologia di servizio denominata ContosoServiceTopology in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="254bd-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="254bd-116">Esempio 2: Ottenere la topologia di un servizio usando l'identificatore di risorsa.</span><span class="sxs-lookup"><span data-stu-id="254bd-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="254bd-117">Questo comando ottiene una topologia di servizio denominata ContosoServiceTopology in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="254bd-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="254bd-118">Esempio 3: Ottenere una topologia del servizio usando l'oggetto topologia di servizio.</span><span class="sxs-lookup"><span data-stu-id="254bd-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="254bd-119">Questo comando ottiene una topologia di servizio il cui nome e GruppoSocietà Risorse corrispondono rispettivamente alle proprietà Name e ResourceGroupName del $serviceTopologyObject.</span><span class="sxs-lookup"><span data-stu-id="254bd-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="254bd-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="254bd-120">PARAMETERS</span></span>

### <span data-ttu-id="254bd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="254bd-121">-DefaultProfile</span></span>
<span data-ttu-id="254bd-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="254bd-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="254bd-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="254bd-123">-InputObject</span></span>
<span data-ttu-id="254bd-124">Oggetto risorsa topologia di servizio.</span><span class="sxs-lookup"><span data-stu-id="254bd-124">Service topology resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="254bd-125">-Name</span><span class="sxs-lookup"><span data-stu-id="254bd-125">-Name</span></span>
<span data-ttu-id="254bd-126">Nome della topologia di servizio.</span><span class="sxs-lookup"><span data-stu-id="254bd-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="254bd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="254bd-127">-ResourceGroupName</span></span>
<span data-ttu-id="254bd-128">Gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="254bd-128">The resource group.</span></span>

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

### <span data-ttu-id="254bd-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="254bd-129">-ResourceId</span></span>
<span data-ttu-id="254bd-130">L'identificatore di risorsa.</span><span class="sxs-lookup"><span data-stu-id="254bd-130">The resource identifier.</span></span>

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

### <span data-ttu-id="254bd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="254bd-131">CommonParameters</span></span>
<span data-ttu-id="254bd-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="254bd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="254bd-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="254bd-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="254bd-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="254bd-134">INPUTS</span></span>

### <span data-ttu-id="254bd-135">System.String</span><span class="sxs-lookup"><span data-stu-id="254bd-135">System.String</span></span>

### <span data-ttu-id="254bd-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="254bd-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="254bd-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="254bd-137">OUTPUTS</span></span>

### <span data-ttu-id="254bd-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="254bd-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="254bd-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="254bd-139">NOTES</span></span>

## <span data-ttu-id="254bd-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="254bd-140">RELATED LINKS</span></span>
