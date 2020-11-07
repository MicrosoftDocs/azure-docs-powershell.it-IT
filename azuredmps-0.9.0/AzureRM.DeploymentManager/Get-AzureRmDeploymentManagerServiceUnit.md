---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: e83f619bd14a2e0ba2012a206d0c3dffd5204863
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685167"
---
# <span data-ttu-id="33641-101">Get-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="33641-101">Get-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="33641-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="33641-102">SYNOPSIS</span></span>
<span data-ttu-id="33641-103">Ottiene un'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="33641-103">Gets a service unit.</span></span>

## <span data-ttu-id="33641-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="33641-104">SYNTAX</span></span>

### <span data-ttu-id="33641-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="33641-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33641-106">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="33641-106">ByServiceObject</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String>
 [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33641-107">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="33641-107">ByServiceResourceId</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33641-108">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="33641-108">ByTopologyObjectAndServiceName</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33641-109">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="33641-109">ByTopologyResourceAndServiceName</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33641-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="33641-110">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="33641-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="33641-111">InputObject</span></span>
```
Get-AzureRmDeploymentManagerServiceUnit [-ServiceUnit] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33641-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33641-112">DESCRIPTION</span></span>
<span data-ttu-id="33641-113">Il cmdlet **Get-AzureRmDeploymentManagerServiceUnit** ottiene un'unità di servizio in un servizio.</span><span class="sxs-lookup"><span data-stu-id="33641-113">The **Get-AzureRmDeploymentManagerServiceUnit** cmdlet gets a service unit in a service.</span></span>

<span data-ttu-id="33641-114">Specificare l'unità di servizio per nome, il servizio in cui è stato definito, il nome della topologia del servizio e il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="33641-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="33641-115">In alternativa, puoi specificare l'oggetto ServiceUnit o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="33641-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

<span data-ttu-id="33641-116">Puoi modificare l'oggetto localmente e quindi applicare le modifiche all'unità di servizio usando il cmdlet Set-AzureRmDeploymentManagerServiceUnit.</span><span class="sxs-lookup"><span data-stu-id="33641-116">You can modify this object locally, and then apply changes to the service unit by using the Set-AzureRmDeploymentManagerServiceUnit cmdlet.</span></span>

## <span data-ttu-id="33641-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="33641-117">EXAMPLES</span></span>

### <span data-ttu-id="33641-118">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="33641-118">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="33641-119">Questo comando consente di ottenere un'unità di servizio denominata ContosoService1Storage in un servizio ContosoService1 in una topologia di servizio denominata ContosoServiceTopology in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="33641-119">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="33641-120">Esempio 2: ottenere un'unità di servizio usando l'identificatore delle risorse.</span><span class="sxs-lookup"><span data-stu-id="33641-120">Example 2: Get a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="33641-121">Questo comando consente di ottenere un'unità di servizio denominata ContosoService1Storage in un servizio ContosoService1 in una topologia di servizio denominata ContosoServiceTopology in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="33641-121">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="33641-122">Esempio 3: ottenere un'unità di servizio usando l'oggetto unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="33641-122">Example 3: Get a service unit using the service unit object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceUnit -ServiceUnit $serviceUnitObject
```

<span data-ttu-id="33641-123">Questo comando consente di ottenere un'unità di servizio il cui nome, nome servizio, nome della topologia del servizio e ResourceGroup corrispondono rispettivamente alle proprietà Name, ServiceName, ServiceTopologyName e ResourceGroupName della $serviceUnitObject.</span><span class="sxs-lookup"><span data-stu-id="33641-123">This command gets a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="33641-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="33641-124">PARAMETERS</span></span>

### <span data-ttu-id="33641-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33641-125">-DefaultProfile</span></span>
<span data-ttu-id="33641-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="33641-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33641-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="33641-127">-Name</span></span>
<span data-ttu-id="33641-128">Nome dell'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="33641-128">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33641-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33641-129">-ResourceGroupName</span></span>
<span data-ttu-id="33641-130">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="33641-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33641-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33641-131">-ResourceId</span></span>
<span data-ttu-id="33641-132">Identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="33641-132">The resource identifier.</span></span>

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

### <span data-ttu-id="33641-133">-Servizio</span><span class="sxs-lookup"><span data-stu-id="33641-133">-Service</span></span>
<span data-ttu-id="33641-134">Oggetto Service in cui deve essere creata l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="33641-134">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="33641-135">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="33641-135">-ServiceName</span></span>
<span data-ttu-id="33641-136">Nome del servizio a cui fa parte l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="33641-136">The name of the service the service unit is part of.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33641-137">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="33641-137">-ServiceResourceId</span></span>
<span data-ttu-id="33641-138">Identificatore della risorsa del servizio in cui deve essere creata l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="33641-138">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="33641-139">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="33641-139">-ServiceTopology</span></span>
<span data-ttu-id="33641-140">Oggetto topologia del servizio in cui deve essere creata l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="33641-140">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="33641-141">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="33641-141">-ServiceTopologyName</span></span>
<span data-ttu-id="33641-142">Nome della topologia del servizio di cui fa parte l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="33641-142">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="33641-143">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="33641-143">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="33641-144">Identificatore della risorsa della topologia del servizio in cui deve essere creata l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="33641-144">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="33641-145">-ServiceUnit</span><span class="sxs-lookup"><span data-stu-id="33641-145">-ServiceUnit</span></span>
<span data-ttu-id="33641-146">Oggetto risorsa unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="33641-146">Service unit resource object.</span></span>

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

### <span data-ttu-id="33641-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33641-147">CommonParameters</span></span>
<span data-ttu-id="33641-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33641-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33641-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33641-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33641-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="33641-150">INPUTS</span></span>

### <span data-ttu-id="33641-151">Nessuno</span><span class="sxs-lookup"><span data-stu-id="33641-151">None</span></span>

## <span data-ttu-id="33641-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="33641-152">OUTPUTS</span></span>

### <span data-ttu-id="33641-153">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="33641-153">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="33641-154">Note</span><span class="sxs-lookup"><span data-stu-id="33641-154">NOTES</span></span>

## <span data-ttu-id="33641-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="33641-155">RELATED LINKS</span></span>

[<span data-ttu-id="33641-156">New-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="33641-156">New-AzureRmDeploymentManagerServiceUnit</span></span>](./New-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="33641-157">Remove-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="33641-157">Remove-AzureRmDeploymentManagerServiceUnit</span></span>](./Remove-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="33641-158">Set-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="33641-158">Set-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)