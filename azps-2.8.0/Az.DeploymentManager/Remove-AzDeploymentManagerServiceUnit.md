---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 3ba27cf26ccc555ea79a2b46100bee6be7e3c7fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674601"
---
# <span data-ttu-id="50e2d-101">Remove-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="50e2d-101">Remove-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="50e2d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="50e2d-102">SYNOPSIS</span></span>
<span data-ttu-id="50e2d-103">Elimina l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="50e2d-103">Deletes the service unit.</span></span>

## <span data-ttu-id="50e2d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50e2d-104">SYNTAX</span></span>

### <span data-ttu-id="50e2d-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="50e2d-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50e2d-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="50e2d-106">ByTopologyObjectAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50e2d-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="50e2d-107">ByTopologyResourceAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50e2d-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="50e2d-108">ByServiceObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50e2d-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="50e2d-109">ByServiceResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50e2d-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="50e2d-110">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50e2d-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="50e2d-111">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50e2d-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50e2d-112">DESCRIPTION</span></span>
<span data-ttu-id="50e2d-113">Il cmdlet **Remove-AzDeploymentManagerServiceUnit** Elimina un'unità di servizio in un servizio.</span><span class="sxs-lookup"><span data-stu-id="50e2d-113">The **Remove-AzDeploymentManagerServiceUnit** cmdlet deletes a service unit in a service.</span></span>

<span data-ttu-id="50e2d-114">Specificare l'unità di servizio per nome, il servizio in cui è stato definito, il nome della topologia del servizio e il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="50e2d-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="50e2d-115">In alternativa, puoi specificare l'oggetto ServiceUnit o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="50e2d-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

## <span data-ttu-id="50e2d-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50e2d-116">EXAMPLES</span></span>

### <span data-ttu-id="50e2d-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="50e2d-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="50e2d-118">Questo comando Elimina un'unità di servizio denominata ContosoService1Storage in un servizio ContosoService1 in una topologia di servizio denominata ContosoServiceTopology in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="50e2d-118">This command deletes a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="50e2d-119">Esempio 2: eliminare un'unità di servizio usando l'identificatore delle risorse.</span><span class="sxs-lookup"><span data-stu-id="50e2d-119">Example 2: Delete a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="50e2d-120">Questo comando consente di ottenere un'unità di servizio denominata ContosoService1Storage in un servizio ContosoService1 in una topologia di servizio denominata ContosoServiceTopology in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="50e2d-120">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="50e2d-121">Esempio 3: eliminare un'unità di servizio usando l'oggetto unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="50e2d-121">Example 3: Delete a service unit using the service unit object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="50e2d-122">Questo comando Elimina un'unità di servizio il cui nome, nome servizio, nome della topologia del servizio e ResourceGroup corrispondono rispettivamente alle proprietà Name, ServiceName, ServiceTopologyName e ResourceGroupName della $serviceUnitObject.</span><span class="sxs-lookup"><span data-stu-id="50e2d-122">This command deletes a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="50e2d-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50e2d-123">PARAMETERS</span></span>

### <span data-ttu-id="50e2d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50e2d-124">-DefaultProfile</span></span>
<span data-ttu-id="50e2d-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50e2d-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50e2d-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50e2d-126">-InputObject</span></span>
<span data-ttu-id="50e2d-127">Oggetto risorsa unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="50e2d-127">Service unit resource object.</span></span>

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

### <span data-ttu-id="50e2d-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="50e2d-128">-Name</span></span>
<span data-ttu-id="50e2d-129">Nome dell'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="50e2d-129">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName, ByServiceObject, ByServiceResourceId
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50e2d-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50e2d-130">-PassThru</span></span>
<span data-ttu-id="50e2d-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="50e2d-131">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50e2d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50e2d-132">-ResourceGroupName</span></span>
<span data-ttu-id="50e2d-133">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="50e2d-133">The resource group.</span></span>

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

### <span data-ttu-id="50e2d-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50e2d-134">-ResourceId</span></span>
<span data-ttu-id="50e2d-135">Identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="50e2d-135">The resource identifier.</span></span>

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

### <span data-ttu-id="50e2d-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="50e2d-136">-ServiceName</span></span>
<span data-ttu-id="50e2d-137">Nome del servizio a cui fa parte l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="50e2d-137">The name of the service the service unit is part of.</span></span>

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

### <span data-ttu-id="50e2d-138">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="50e2d-138">-ServiceObject</span></span>
<span data-ttu-id="50e2d-139">Oggetto Service in cui deve essere creata l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="50e2d-139">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="50e2d-140">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="50e2d-140">-ServiceResourceId</span></span>
<span data-ttu-id="50e2d-141">Identificatore della risorsa del servizio in cui deve essere creata l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="50e2d-141">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="50e2d-142">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="50e2d-142">-ServiceTopologyName</span></span>
<span data-ttu-id="50e2d-143">Nome della topologia del servizio di cui fa parte l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="50e2d-143">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="50e2d-144">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="50e2d-144">-ServiceTopologyObject</span></span>
<span data-ttu-id="50e2d-145">Oggetto topologia del servizio in cui deve essere creata l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="50e2d-145">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="50e2d-146">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="50e2d-146">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="50e2d-147">Identificatore della risorsa della topologia del servizio in cui deve essere creata l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="50e2d-147">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="50e2d-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="50e2d-148">-Confirm</span></span>
<span data-ttu-id="50e2d-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50e2d-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50e2d-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50e2d-150">-WhatIf</span></span>
<span data-ttu-id="50e2d-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50e2d-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50e2d-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50e2d-152">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50e2d-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50e2d-153">CommonParameters</span></span>
<span data-ttu-id="50e2d-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50e2d-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50e2d-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50e2d-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50e2d-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="50e2d-156">INPUTS</span></span>

### <span data-ttu-id="50e2d-157">System. String</span><span class="sxs-lookup"><span data-stu-id="50e2d-157">System.String</span></span>

### <span data-ttu-id="50e2d-158">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="50e2d-158">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="50e2d-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50e2d-159">OUTPUTS</span></span>

### <span data-ttu-id="50e2d-160">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="50e2d-160">System.Boolean</span></span>

## <span data-ttu-id="50e2d-161">Note</span><span class="sxs-lookup"><span data-stu-id="50e2d-161">NOTES</span></span>

## <span data-ttu-id="50e2d-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50e2d-162">RELATED LINKS</span></span>
