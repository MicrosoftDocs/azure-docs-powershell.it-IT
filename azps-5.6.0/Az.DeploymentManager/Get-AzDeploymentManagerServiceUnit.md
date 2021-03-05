---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/get-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 2910afe209a83e07e65cc04b9ffa371fe4ed72d5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966350"
---
# <span data-ttu-id="27e86-101">Get-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="27e86-101">Get-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="27e86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27e86-102">SYNOPSIS</span></span>
<span data-ttu-id="27e86-103">Ottiene l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="27e86-103">Gets the service unit.</span></span>

## <span data-ttu-id="27e86-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27e86-104">SYNTAX</span></span>

### <span data-ttu-id="27e86-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="27e86-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27e86-106">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="27e86-106">ByServiceObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27e86-107">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="27e86-107">ByServiceResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [[-Name] <String>]
 [-ServiceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27e86-108">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="27e86-108">ByTopologyObjectAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="27e86-109">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="27e86-109">ByTopologyResourceAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27e86-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="27e86-110">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="27e86-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="27e86-111">InputObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27e86-112">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="27e86-112">DESCRIPTION</span></span>
<span data-ttu-id="27e86-113">Il **cmdlet Get-AzDeploymentManagerServiceUnit** ottiene un'unità di servizio in un servizio.</span><span class="sxs-lookup"><span data-stu-id="27e86-113">The **Get-AzDeploymentManagerServiceUnit** cmdlet gets a service unit in a service.</span></span>

<span data-ttu-id="27e86-114">Specificare l'unità di servizio in base al nome, al servizio in cui è stata definita, al nome della topologia di servizio e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="27e86-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="27e86-115">In alternativa, è possibile fornire l'oggetto ServiceUnit o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="27e86-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

<span data-ttu-id="27e86-116">È possibile modificare l'oggetto in locale e quindi applicare modifiche all'unità di servizio usando il cmdlet Set-AzDeploymentManagerServiceUnit servizio.</span><span class="sxs-lookup"><span data-stu-id="27e86-116">You can modify this object locally, and then apply changes to the service unit by using the Set-AzDeploymentManagerServiceUnit cmdlet.</span></span>

## <span data-ttu-id="27e86-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27e86-117">EXAMPLES</span></span>

### <span data-ttu-id="27e86-118">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="27e86-118">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="27e86-119">Questo comando ottiene un'unità di servizio denominata ContosoService1Storage in un servizio ContosoService1 in una topologia di servizio denominata ContosoServiceTopology in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="27e86-119">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="27e86-120">Esempio 2: ottenere un'unità di servizio usando l'identificatore di risorsa.</span><span class="sxs-lookup"><span data-stu-id="27e86-120">Example 2: Get a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="27e86-121">Questo comando ottiene un'unità di servizio denominata ContosoService1Storage in un servizio ContosoService1 in una topologia di servizio denominata ContosoServiceTopology in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="27e86-121">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="27e86-122">Esempio 3: Ottenere un'unità di servizio usando l'oggetto unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="27e86-122">Example 3: Get a service unit using the service unit object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="27e86-123">Questo comando ottiene un'unità di servizio il cui nome, nome del servizio, nome della topologia di servizio e Gruppo Di risorse corrispondono rispettivamente alle proprietà Name, ServiceName, ServiceTopologyName e ResourceGroupName del $serviceUnitObject.</span><span class="sxs-lookup"><span data-stu-id="27e86-123">This command gets a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="27e86-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27e86-124">PARAMETERS</span></span>

### <span data-ttu-id="27e86-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27e86-125">-DefaultProfile</span></span>
<span data-ttu-id="27e86-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="27e86-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27e86-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27e86-127">-InputObject</span></span>
<span data-ttu-id="27e86-128">Oggetto risorsa unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="27e86-128">Service unit resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27e86-129">-Name</span><span class="sxs-lookup"><span data-stu-id="27e86-129">-Name</span></span>
<span data-ttu-id="27e86-130">Nome dell'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="27e86-130">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27e86-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27e86-131">-ResourceGroupName</span></span>
<span data-ttu-id="27e86-132">Gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="27e86-132">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27e86-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27e86-133">-ResourceId</span></span>
<span data-ttu-id="27e86-134">L'identificatore di risorsa.</span><span class="sxs-lookup"><span data-stu-id="27e86-134">The resource identifier.</span></span>

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

### <span data-ttu-id="27e86-135">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="27e86-135">-ServiceName</span></span>
<span data-ttu-id="27e86-136">Il nome del servizio di cui fa parte l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="27e86-136">The name of the service the service unit is part of.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27e86-137">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="27e86-137">-ServiceObject</span></span>
<span data-ttu-id="27e86-138">Oggetto servizio in cui deve essere creata l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="27e86-138">The service object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: ByServiceObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27e86-139">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="27e86-139">-ServiceResourceId</span></span>
<span data-ttu-id="27e86-140">Identificatore della risorsa servizio in cui deve essere creata l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="27e86-140">The service resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27e86-141">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="27e86-141">-ServiceTopologyName</span></span>
<span data-ttu-id="27e86-142">Il nome della topologia di servizio di cui fa parte l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="27e86-142">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="27e86-143">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="27e86-143">-ServiceTopologyObject</span></span>
<span data-ttu-id="27e86-144">Oggetto topologia di servizio in cui deve essere creata l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="27e86-144">The service topology object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByTopologyObjectAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27e86-145">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="27e86-145">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="27e86-146">Identificatore di risorsa della topologia del servizio in cui deve essere creata l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="27e86-146">The service topology resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27e86-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27e86-147">CommonParameters</span></span>
<span data-ttu-id="27e86-148">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27e86-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27e86-149">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="27e86-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27e86-150">INPUT</span><span class="sxs-lookup"><span data-stu-id="27e86-150">INPUTS</span></span>

### <span data-ttu-id="27e86-151">System.String</span><span class="sxs-lookup"><span data-stu-id="27e86-151">System.String</span></span>

### <span data-ttu-id="27e86-152">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="27e86-152">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="27e86-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27e86-153">OUTPUTS</span></span>

### <span data-ttu-id="27e86-154">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="27e86-154">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="27e86-155">NOTE</span><span class="sxs-lookup"><span data-stu-id="27e86-155">NOTES</span></span>

## <span data-ttu-id="27e86-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27e86-156">RELATED LINKS</span></span>
