---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerService.md
ms.openlocfilehash: 3dda11ec4fddde67a3ae4300f884290831ac28ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684469"
---
# <span data-ttu-id="d707f-101">Get-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="d707f-101">Get-AzDeploymentManagerService</span></span>

## <span data-ttu-id="d707f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d707f-102">SYNOPSIS</span></span>
<span data-ttu-id="d707f-103">Ottiene il servizio.</span><span class="sxs-lookup"><span data-stu-id="d707f-103">Gets the service.</span></span>

## <span data-ttu-id="d707f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d707f-104">SYNTAX</span></span>

### <span data-ttu-id="d707f-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d707f-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d707f-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="d707f-106">ByServiceTopologyObject</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d707f-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="d707f-107">ByServiceTopologyResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d707f-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d707f-108">ResourceId</span></span>
```
Get-AzDeploymentManagerService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d707f-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="d707f-109">InputObject</span></span>
```
Get-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d707f-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d707f-110">DESCRIPTION</span></span>
<span data-ttu-id="d707f-111">Il cmdlet **Get-AzDeploymentManagerService** ottiene un servizio in una topologia di servizio e restituisce un oggetto che rappresenta tale servizio.</span><span class="sxs-lookup"><span data-stu-id="d707f-111">The **Get-AzDeploymentManagerService** cmdlet gets a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="d707f-112">Specificare il servizio in base al nome, alla topologia del servizio e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d707f-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="d707f-113">In alternativa, puoi specificare l'oggetto servizio o il ResourceId.</span><span class="sxs-lookup"><span data-stu-id="d707f-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

<span data-ttu-id="d707f-114">Puoi modificare l'oggetto localmente e quindi applicare le modifiche al servizio usando il cmdlet Set-AzDeploymentManagerService.</span><span class="sxs-lookup"><span data-stu-id="d707f-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="d707f-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d707f-115">EXAMPLES</span></span>

### <span data-ttu-id="d707f-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d707f-116">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="d707f-117">Questo comando ottiene un servizio denominato ContosoService1 in una topologia di servizio denominata ContosoServiceTopology nel ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d707f-117">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="d707f-118">Esempio 2: ottenere un servizio usando l'identificatore delle risorse.</span><span class="sxs-lookup"><span data-stu-id="d707f-118">Example 2: Get a service using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="d707f-119">Questo comando ottiene un servizio denominato ContosoService1 in una topologia di servizio denominata ContosoServiceTopology nel ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d707f-119">This command gets a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="d707f-120">Esempio 3: ottenere un servizio usando l'oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="d707f-120">Example 3: Get a service using the service object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="d707f-121">Questo comando ottiene un servizio il cui nome, nome della topologia del servizio e ResourceGroup corrispondono rispettivamente alle proprietà Name, ServiceTopologyName e ResourceGroupName della $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="d707f-121">This command gets a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
 

## <span data-ttu-id="d707f-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d707f-122">PARAMETERS</span></span>

### <span data-ttu-id="d707f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d707f-123">-DefaultProfile</span></span>
<span data-ttu-id="d707f-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d707f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d707f-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d707f-125">-InputObject</span></span>
<span data-ttu-id="d707f-126">Oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="d707f-126">Service object.</span></span>

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

### <span data-ttu-id="d707f-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="d707f-127">-Name</span></span>
<span data-ttu-id="d707f-128">Nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="d707f-128">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d707f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d707f-129">-ResourceGroupName</span></span>
<span data-ttu-id="d707f-130">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="d707f-130">The resource group.</span></span>

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

### <span data-ttu-id="d707f-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d707f-131">-ResourceId</span></span>
<span data-ttu-id="d707f-132">Identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d707f-132">The resource identifier.</span></span>

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

### <span data-ttu-id="d707f-133">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="d707f-133">-ServiceTopologyName</span></span>
<span data-ttu-id="d707f-134">Nome della topologia del servizio.</span><span class="sxs-lookup"><span data-stu-id="d707f-134">The name of the service topology.</span></span>

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

### <span data-ttu-id="d707f-135">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="d707f-135">-ServiceTopologyObject</span></span>
<span data-ttu-id="d707f-136">Oggetto topologia del servizio in cui deve essere creato il servizio.</span><span class="sxs-lookup"><span data-stu-id="d707f-136">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="d707f-137">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="d707f-137">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="d707f-138">Identificatore della risorsa della topologia del servizio in cui deve essere creato il servizio.</span><span class="sxs-lookup"><span data-stu-id="d707f-138">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="d707f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d707f-139">CommonParameters</span></span>
<span data-ttu-id="d707f-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d707f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d707f-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d707f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d707f-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d707f-142">INPUTS</span></span>

### <span data-ttu-id="d707f-143">System. String</span><span class="sxs-lookup"><span data-stu-id="d707f-143">System.String</span></span>

### <span data-ttu-id="d707f-144">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="d707f-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="d707f-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d707f-145">OUTPUTS</span></span>

### <span data-ttu-id="d707f-146">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="d707f-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="d707f-147">Note</span><span class="sxs-lookup"><span data-stu-id="d707f-147">NOTES</span></span>

## <span data-ttu-id="d707f-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d707f-148">RELATED LINKS</span></span>
