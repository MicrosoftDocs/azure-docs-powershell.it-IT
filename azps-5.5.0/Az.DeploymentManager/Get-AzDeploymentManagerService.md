---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
ms.openlocfilehash: da59c17b7aef90cd3f5c5b374d663292153be140
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177007"
---
# <span data-ttu-id="da47e-101">Get-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="da47e-101">Get-AzDeploymentManagerService</span></span>

## <span data-ttu-id="da47e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da47e-102">SYNOPSIS</span></span>
<span data-ttu-id="da47e-103">Ottiene il servizio.</span><span class="sxs-lookup"><span data-stu-id="da47e-103">Gets the service.</span></span>

## <span data-ttu-id="da47e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da47e-104">SYNTAX</span></span>

### <span data-ttu-id="da47e-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="da47e-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da47e-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="da47e-106">ByServiceTopologyObject</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da47e-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="da47e-107">ByServiceTopologyResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da47e-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="da47e-108">ResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="da47e-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="da47e-109">InputObject</span></span>
```
Get-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="da47e-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="da47e-110">DESCRIPTION</span></span>
<span data-ttu-id="da47e-111">Il cmdlet **Get-AzDeploymentManagerService** ottiene un servizio in una topologia di servizio e restituisce un oggetto che rappresenta tale servizio.</span><span class="sxs-lookup"><span data-stu-id="da47e-111">The **Get-AzDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="da47e-112">Specificare il servizio in base al nome, alla topologia di servizio in cui si trova e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="da47e-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="da47e-113">In alternativa, è possibile fornire l'oggetto Servizio o l'ID Risorsa.</span><span class="sxs-lookup"><span data-stu-id="da47e-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="da47e-114">È possibile modificare l'oggetto in locale e quindi applicarvi le modifiche usando il cmdlet Set-AzDeploymentManagerService servizio.</span><span class="sxs-lookup"><span data-stu-id="da47e-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="da47e-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da47e-115">EXAMPLES</span></span>

### <span data-ttu-id="da47e-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="da47e-116">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="da47e-117">Questo comando ottiene un servizio denominato ContosoService1 in una topologia di servizio denominata ContosoServiceTopology in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="da47e-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="da47e-118">Esempio 2: Ottenere un servizio con l'identificatore di risorsa.</span><span class="sxs-lookup"><span data-stu-id="da47e-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="da47e-119">Questo comando ottiene un servizio denominato ContosoService1 in una topologia di servizio denominata ContosoServiceTopology in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="da47e-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="da47e-120">Esempio 3: Ottenere un servizio con l'oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="da47e-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="da47e-121">Questo comando ottiene un servizio il cui nome, il nome della topologia di servizio e il gruppo di risorse corrispondono rispettivamente alle proprietà Name, ServiceTopologyName e ResourceGroupName del $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="da47e-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
 

## <span data-ttu-id="da47e-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da47e-122">PARAMETERS</span></span>

### <span data-ttu-id="da47e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da47e-123">-DefaultProfile</span></span>
<span data-ttu-id="da47e-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="da47e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da47e-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da47e-125">-InputObject</span></span>
<span data-ttu-id="da47e-126">Oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="da47e-126">Service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da47e-127">-Name</span><span class="sxs-lookup"><span data-stu-id="da47e-127">-Name</span></span>
<span data-ttu-id="da47e-128">Nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="da47e-128">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da47e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da47e-129">-ResourceGroupName</span></span>
<span data-ttu-id="da47e-130">Gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="da47e-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da47e-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="da47e-131">-ResourceId</span></span>
<span data-ttu-id="da47e-132">L'identificatore di risorsa.</span><span class="sxs-lookup"><span data-stu-id="da47e-132">The resource identifier.</span></span>

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

### <span data-ttu-id="da47e-133">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="da47e-133">-ServiceTopologyName</span></span>
<span data-ttu-id="da47e-134">Nome della topologia di servizio.</span><span class="sxs-lookup"><span data-stu-id="da47e-134">The name of the service topology.</span></span>

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

### <span data-ttu-id="da47e-135">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="da47e-135">-ServiceTopologyObject</span></span>
<span data-ttu-id="da47e-136">Oggetto topologia di servizio in cui deve essere creato il servizio.</span><span class="sxs-lookup"><span data-stu-id="da47e-136">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da47e-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="da47e-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="da47e-138">Identificatore di risorsa della topologia del servizio in cui deve essere creato il servizio.</span><span class="sxs-lookup"><span data-stu-id="da47e-138">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da47e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da47e-139">CommonParameters</span></span>
<span data-ttu-id="da47e-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da47e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da47e-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="da47e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da47e-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="da47e-142">INPUTS</span></span>

### <span data-ttu-id="da47e-143">System.String</span><span class="sxs-lookup"><span data-stu-id="da47e-143">System.String</span></span>

### <span data-ttu-id="da47e-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="da47e-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="da47e-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da47e-145">OUTPUTS</span></span>

### <span data-ttu-id="da47e-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="da47e-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="da47e-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="da47e-147">NOTES</span></span>

## <span data-ttu-id="da47e-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da47e-148">RELATED LINKS</span></span>
