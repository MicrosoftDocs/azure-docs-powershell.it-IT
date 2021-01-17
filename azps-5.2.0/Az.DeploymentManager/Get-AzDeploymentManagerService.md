---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
ms.openlocfilehash: da59c17b7aef90cd3f5c5b374d663292153be140
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324251"
---
# <span data-ttu-id="9d0ef-101">Get-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="9d0ef-101">Get-AzDeploymentManagerService</span></span>

## <span data-ttu-id="9d0ef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9d0ef-102">SYNOPSIS</span></span>
<span data-ttu-id="9d0ef-103">Ottiene il servizio.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-103">Gets the service.</span></span>

## <span data-ttu-id="9d0ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d0ef-104">SYNTAX</span></span>

### <span data-ttu-id="9d0ef-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9d0ef-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d0ef-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="9d0ef-106">ByServiceTopologyObject</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9d0ef-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="9d0ef-107">ByServiceTopologyResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d0ef-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d0ef-108">ResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9d0ef-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="9d0ef-109">InputObject</span></span>
```
Get-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9d0ef-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d0ef-110">DESCRIPTION</span></span>
<span data-ttu-id="9d0ef-111">Il cmdlet **Get-AzDeploymentManagerService** ottiene un servizio in una topologia di servizio e restituisce un oggetto che rappresenta tale servizio.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-111">The **Get-AzDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="9d0ef-112">Specificare il servizio in base al nome, alla topologia del servizio e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="9d0ef-113">In alternativa, puoi specificare l'oggetto servizio o il ResourceId.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="9d0ef-114">Puoi modificare l'oggetto localmente e quindi applicare le modifiche al servizio usando il cmdlet Set-AzDeploymentManagerService.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="9d0ef-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d0ef-115">EXAMPLES</span></span>

### <span data-ttu-id="9d0ef-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9d0ef-116">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="9d0ef-117">Questo comando ottiene un servizio denominato ContosoService1 in una topologia di servizio denominata ContosoServiceTopology nel ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="9d0ef-118">Esempio 2: ottenere un servizio usando l'identificatore delle risorse.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="9d0ef-119">Questo comando ottiene un servizio denominato ContosoService1 in una topologia di servizio denominata ContosoServiceTopology nel ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="9d0ef-120">Esempio 3: ottenere un servizio usando l'oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="9d0ef-121">Questo comando ottiene un servizio il cui nome, nome della topologia del servizio e ResourceGroup corrispondono rispettivamente alle proprietà Name, ServiceTopologyName e ResourceGroupName della $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
 

## <span data-ttu-id="9d0ef-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9d0ef-122">PARAMETERS</span></span>

### <span data-ttu-id="9d0ef-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d0ef-123">-DefaultProfile</span></span>
<span data-ttu-id="9d0ef-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d0ef-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d0ef-125">-InputObject</span></span>
<span data-ttu-id="9d0ef-126">Oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-126">Service object.</span></span>

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

### <span data-ttu-id="9d0ef-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="9d0ef-127">-Name</span></span>
<span data-ttu-id="9d0ef-128">Nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-128">The name of the service.</span></span>

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

### <span data-ttu-id="9d0ef-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d0ef-129">-ResourceGroupName</span></span>
<span data-ttu-id="9d0ef-130">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-130">The resource group.</span></span>

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

### <span data-ttu-id="9d0ef-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d0ef-131">-ResourceId</span></span>
<span data-ttu-id="9d0ef-132">Identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-132">The resource identifier.</span></span>

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

### <span data-ttu-id="9d0ef-133">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="9d0ef-133">-ServiceTopologyName</span></span>
<span data-ttu-id="9d0ef-134">Nome della topologia del servizio.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-134">The name of the service topology.</span></span>

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

### <span data-ttu-id="9d0ef-135">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="9d0ef-135">-ServiceTopologyObject</span></span>
<span data-ttu-id="9d0ef-136">Oggetto topologia del servizio in cui deve essere creato il servizio.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-136">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="9d0ef-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="9d0ef-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="9d0ef-138">Identificatore della risorsa della topologia del servizio in cui deve essere creato il servizio.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-138">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="9d0ef-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d0ef-139">CommonParameters</span></span>
<span data-ttu-id="9d0ef-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d0ef-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d0ef-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d0ef-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d0ef-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9d0ef-142">INPUTS</span></span>

### <span data-ttu-id="9d0ef-143">System. String</span><span class="sxs-lookup"><span data-stu-id="9d0ef-143">System.String</span></span>

### <span data-ttu-id="9d0ef-144">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="9d0ef-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="9d0ef-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d0ef-145">OUTPUTS</span></span>

### <span data-ttu-id="9d0ef-146">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="9d0ef-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="9d0ef-147">Note</span><span class="sxs-lookup"><span data-stu-id="9d0ef-147">NOTES</span></span>

## <span data-ttu-id="9d0ef-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d0ef-148">RELATED LINKS</span></span>
