---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 4a91c2f8fdda1d2cda7c75f0cf7cfab165701f3d
ms.sourcegitcommit: e57be0da5162efeb0a01f396e2343dd137920063
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "99572106"
---
# <span data-ttu-id="7d743-101">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="7d743-101">Get-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="7d743-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d743-102">SYNOPSIS</span></span>
<span data-ttu-id="7d743-103">Ottiene un servizio in una topologia di servizio.</span><span class="sxs-lookup"><span data-stu-id="7d743-103">Gets a service in a service topology.</span></span>

## <span data-ttu-id="7d743-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d743-104">SYNTAX</span></span>

### <span data-ttu-id="7d743-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7d743-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d743-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="7d743-106">ByServiceTopologyObject</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d743-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="7d743-107">ByServiceTopologyResourceId</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d743-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d743-108">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d743-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="7d743-109">InputObject</span></span>
```
Get-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d743-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7d743-110">DESCRIPTION</span></span>
<span data-ttu-id="7d743-111">Il cmdlet **Get-AzureRmDeploymentManagerService** ottiene un servizio in una topologia di servizio e restituisce un oggetto che rappresenta tale servizio.</span><span class="sxs-lookup"><span data-stu-id="7d743-111">The **Get-AzureRmDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="7d743-112">Specificare il servizio in base al nome, alla topologia di servizio in cui si trova e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7d743-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="7d743-113">In alternativa, è possibile specificare l'oggetto Servizio o l'ID Risorsa.</span><span class="sxs-lookup"><span data-stu-id="7d743-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="7d743-114">È possibile modificare l'oggetto in locale e quindi applicarvi le modifiche usando il cmdlet Set-AzureRmDeploymentManagerService servizio.</span><span class="sxs-lookup"><span data-stu-id="7d743-114">You can modify this object locally, and then apply changes to the service by using the Set-AzureRmDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="7d743-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d743-115">EXAMPLES</span></span>

### <span data-ttu-id="7d743-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7d743-116">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="7d743-117">Questo comando ottiene un servizio denominato ContosoService1 in una topologia di servizio denominata ContosoServiceTopology in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7d743-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="7d743-118">Esempio 2: Ottenere un servizio con l'identificatore di risorsa.</span><span class="sxs-lookup"><span data-stu-id="7d743-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="7d743-119">Questo comando ottiene un servizio denominato ContosoService1 in una topologia di servizio denominata ContosoServiceTopology in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7d743-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="7d743-120">Esempio 3: Ottenere un servizio con l'oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="7d743-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="7d743-121">Questo comando ottiene un servizio il cui nome, il cui nome della topologia di servizio e ResourceGroup corrispondono rispettivamente alle proprietà Name, ServiceTopologyName e ResourceGroupName del $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="7d743-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="7d743-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d743-122">PARAMETERS</span></span>

### <span data-ttu-id="7d743-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d743-123">-DefaultProfile</span></span>
<span data-ttu-id="7d743-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7d743-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d743-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7d743-125">-Name</span></span>
<span data-ttu-id="7d743-126">Nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="7d743-126">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d743-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d743-127">-ResourceGroupName</span></span>
<span data-ttu-id="7d743-128">Gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7d743-128">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d743-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d743-129">-ResourceId</span></span>
<span data-ttu-id="7d743-130">L'identificatore di risorsa.</span><span class="sxs-lookup"><span data-stu-id="7d743-130">The resource identifier.</span></span>

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

### <span data-ttu-id="7d743-131">-Service</span><span class="sxs-lookup"><span data-stu-id="7d743-131">-Service</span></span>
<span data-ttu-id="7d743-132">Oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="7d743-132">Service object.</span></span>

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

### <span data-ttu-id="7d743-133">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="7d743-133">-ServiceTopology</span></span>
<span data-ttu-id="7d743-134">Oggetto topologia di servizio in cui deve essere creato il servizio.</span><span class="sxs-lookup"><span data-stu-id="7d743-134">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="7d743-135">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="7d743-135">-ServiceTopologyName</span></span>
<span data-ttu-id="7d743-136">Nome della topologia di servizio.</span><span class="sxs-lookup"><span data-stu-id="7d743-136">The name of the service topology.</span></span>

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

### <span data-ttu-id="7d743-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="7d743-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="7d743-138">Identificatore di risorsa della topologia del servizio in cui deve essere creato il servizio.</span><span class="sxs-lookup"><span data-stu-id="7d743-138">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="7d743-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d743-139">CommonParameters</span></span>
<span data-ttu-id="7d743-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d743-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d743-141">Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d743-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d743-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="7d743-142">INPUTS</span></span>

### <span data-ttu-id="7d743-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7d743-143">None</span></span>

## <span data-ttu-id="7d743-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d743-144">OUTPUTS</span></span>

### <span data-ttu-id="7d743-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="7d743-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="7d743-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="7d743-146">NOTES</span></span>

## <span data-ttu-id="7d743-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d743-147">RELATED LINKS</span></span>

[<span data-ttu-id="7d743-148">New-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="7d743-148">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="7d743-149">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="7d743-149">Remove-AzureRmDeploymentManagerService</span></span>](./Remove-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="7d743-150">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="7d743-150">Set-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)
