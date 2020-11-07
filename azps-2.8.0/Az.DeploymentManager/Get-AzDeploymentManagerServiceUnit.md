---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 607e094a03d43704057af80266a6f9f2b669d3b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674623"
---
# <span data-ttu-id="08bb1-101">Get-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="08bb1-101">Get-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="08bb1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="08bb1-102">SYNOPSIS</span></span>
<span data-ttu-id="08bb1-103">Ottiene l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="08bb1-103">Gets the service unit.</span></span>

## <span data-ttu-id="08bb1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="08bb1-104">SYNTAX</span></span>

### <span data-ttu-id="08bb1-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="08bb1-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08bb1-106">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="08bb1-106">ByServiceObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String>
 [-ServiceObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08bb1-107">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="08bb1-107">ByServiceResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> [-ServiceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08bb1-108">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="08bb1-108">ByTopologyObjectAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="08bb1-109">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="08bb1-109">ByTopologyResourceAndServiceName</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08bb1-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="08bb1-110">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="08bb1-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="08bb1-111">InputObject</span></span>
```
Get-AzDeploymentManagerServiceUnit [-ServiceUnitObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08bb1-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08bb1-112">DESCRIPTION</span></span>
<span data-ttu-id="08bb1-113">Il cmdlet **Get-AzDeploymentManagerServiceUnit** ottiene un'unità di servizio in un servizio.</span><span class="sxs-lookup"><span data-stu-id="08bb1-113">The **Get-AzDeploymentManagerServiceUnit** cmdlet gets a service unit in a service.</span></span>

<span data-ttu-id="08bb1-114">Specificare l'unità di servizio per nome, il servizio in cui è stato definito, il nome della topologia del servizio e il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="08bb1-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="08bb1-115">In alternativa, puoi specificare l'oggetto ServiceUnit o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="08bb1-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

<span data-ttu-id="08bb1-116">Puoi modificare l'oggetto localmente e quindi applicare le modifiche all'unità di servizio usando il cmdlet Set-AzDeploymentManagerServiceUnit.</span><span class="sxs-lookup"><span data-stu-id="08bb1-116">You can modify this object locally, and then apply changes to the service unit by using the Set-AzDeploymentManagerServiceUnit cmdlet.</span></span>

## <span data-ttu-id="08bb1-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="08bb1-117">EXAMPLES</span></span>

### <span data-ttu-id="08bb1-118">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="08bb1-118">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="08bb1-119">Questo comando consente di ottenere un'unità di servizio denominata ContosoService1Storage in un servizio ContosoService1 in una topologia di servizio denominata ContosoServiceTopology in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="08bb1-119">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="08bb1-120">Esempio 2: ottenere un'unità di servizio usando l'identificatore delle risorse.</span><span class="sxs-lookup"><span data-stu-id="08bb1-120">Example 2: Get a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="08bb1-121">Questo comando consente di ottenere un'unità di servizio denominata ContosoService1Storage in un servizio ContosoService1 in una topologia di servizio denominata ContosoServiceTopology in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="08bb1-121">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="08bb1-122">Esempio 3: ottenere un'unità di servizio usando l'oggetto unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="08bb1-122">Example 3: Get a service unit using the service unit object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="08bb1-123">Questo comando consente di ottenere un'unità di servizio il cui nome, nome servizio, nome della topologia del servizio e ResourceGroup corrispondono rispettivamente alle proprietà Name, ServiceName, ServiceTopologyName e ResourceGroupName della $serviceUnitObject.</span><span class="sxs-lookup"><span data-stu-id="08bb1-123">This command gets a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="08bb1-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="08bb1-124">PARAMETERS</span></span>

### <span data-ttu-id="08bb1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08bb1-125">-DefaultProfile</span></span>
<span data-ttu-id="08bb1-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="08bb1-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08bb1-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="08bb1-127">-Name</span></span>
<span data-ttu-id="08bb1-128">Nome dell'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="08bb1-128">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceObject, ByServiceResourceId, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08bb1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08bb1-129">-ResourceGroupName</span></span>
<span data-ttu-id="08bb1-130">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="08bb1-130">The resource group.</span></span>

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

### <span data-ttu-id="08bb1-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08bb1-131">-ResourceId</span></span>
<span data-ttu-id="08bb1-132">Identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="08bb1-132">The resource identifier.</span></span>

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

### <span data-ttu-id="08bb1-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="08bb1-133">-ServiceName</span></span>
<span data-ttu-id="08bb1-134">Nome del servizio a cui fa parte l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="08bb1-134">The name of the service the service unit is part of.</span></span>

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

### <span data-ttu-id="08bb1-135">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="08bb1-135">-ServiceObject</span></span>
<span data-ttu-id="08bb1-136">Oggetto Service in cui deve essere creata l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="08bb1-136">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="08bb1-137">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="08bb1-137">-ServiceResourceId</span></span>
<span data-ttu-id="08bb1-138">Identificatore della risorsa del servizio in cui deve essere creata l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="08bb1-138">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="08bb1-139">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="08bb1-139">-ServiceTopologyName</span></span>
<span data-ttu-id="08bb1-140">Nome della topologia del servizio di cui fa parte l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="08bb1-140">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="08bb1-141">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="08bb1-141">-ServiceTopologyObject</span></span>
<span data-ttu-id="08bb1-142">Oggetto topologia del servizio in cui deve essere creata l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="08bb1-142">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="08bb1-143">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="08bb1-143">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="08bb1-144">Identificatore della risorsa della topologia del servizio in cui deve essere creata l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="08bb1-144">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="08bb1-145">-ServiceUnitObject</span><span class="sxs-lookup"><span data-stu-id="08bb1-145">-ServiceUnitObject</span></span>
<span data-ttu-id="08bb1-146">Oggetto risorsa unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="08bb1-146">Service unit resource object.</span></span>

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

### <span data-ttu-id="08bb1-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08bb1-147">CommonParameters</span></span>
<span data-ttu-id="08bb1-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08bb1-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08bb1-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08bb1-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08bb1-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="08bb1-150">INPUTS</span></span>

### <span data-ttu-id="08bb1-151">System. String</span><span class="sxs-lookup"><span data-stu-id="08bb1-151">System.String</span></span>

### <span data-ttu-id="08bb1-152">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="08bb1-152">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="08bb1-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="08bb1-153">OUTPUTS</span></span>

### <span data-ttu-id="08bb1-154">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="08bb1-154">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="08bb1-155">Note</span><span class="sxs-lookup"><span data-stu-id="08bb1-155">NOTES</span></span>

## <span data-ttu-id="08bb1-156">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="08bb1-156">RELATED LINKS</span></span>
