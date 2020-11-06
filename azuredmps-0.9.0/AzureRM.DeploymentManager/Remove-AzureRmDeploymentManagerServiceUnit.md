---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: 993b250b0c49efc448c0198c4e9a3aea29f77714
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491622"
---
# <span data-ttu-id="4e5e9-101">Remove-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="4e5e9-101">Remove-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="4e5e9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4e5e9-102">SYNOPSIS</span></span>
<span data-ttu-id="4e5e9-103">Elimina l'unità di servizio di un servizio in una topologia di servizio.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-103">Deletes the service unit of a service in a service topology.</span></span>

## <span data-ttu-id="4e5e9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e5e9-104">SYNTAX</span></span>

### <span data-ttu-id="4e5e9-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4e5e9-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e5e9-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="4e5e9-106">ByTopologyObjectAndServiceName</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e5e9-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="4e5e9-107">ByTopologyResourceAndServiceName</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e5e9-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="4e5e9-108">ByServiceObject</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-Name] <String> [-Service] <PSServiceResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e5e9-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="4e5e9-109">ByServiceResourceId</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-Name] <String> [-ServiceResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e5e9-110">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e5e9-110">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e5e9-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="4e5e9-111">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ServiceUnit] <PSServiceUnitResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e5e9-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e5e9-112">DESCRIPTION</span></span>
<span data-ttu-id="4e5e9-113">Il cmdlet **Remove-AzureRmDeploymentManagerServiceUnit** Elimina un'unità di servizio in un servizio.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-113">The **Remove-AzureRmDeploymentManagerServiceUnit** cmdlet deletes a service unit in a service.</span></span>

<span data-ttu-id="4e5e9-114">Specificare l'unità di servizio per nome, il servizio in cui è stato definito, il nome della topologia del servizio e il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="4e5e9-115">In alternativa, puoi specificare l'oggetto ServiceUnit o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

## <span data-ttu-id="4e5e9-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e5e9-116">EXAMPLES</span></span>

### <span data-ttu-id="4e5e9-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4e5e9-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="4e5e9-118">Questo comando Elimina un'unità di servizio denominata ContosoService1Storage in un servizio ContosoService1 in una topologia di servizio denominata ContosoServiceTopology in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-118">This command deletes a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="4e5e9-119">Esempio 2: eliminare un'unità di servizio usando l'identificatore delle risorse.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-119">Example 2: Delete a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="4e5e9-120">Questo comando consente di ottenere un'unità di servizio denominata ContosoService1Storage in un servizio ContosoService1 in una topologia di servizio denominata ContosoServiceTopology in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-120">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="4e5e9-121">Esempio 3: eliminare un'unità di servizio usando l'oggetto unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-121">Example 3: Delete a service unit using the service unit object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceUnit -ServiceUnit $serviceUnitObject
```

<span data-ttu-id="4e5e9-122">Questo comando Elimina un'unità di servizio il cui nome, nome servizio, nome della topologia del servizio e ResourceGroup corrispondono rispettivamente alle proprietà Name, ServiceName, ServiceTopologyName e ResourceGroupName della $serviceUnitObject.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-122">This command deletes a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="4e5e9-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4e5e9-123">PARAMETERS</span></span>

### <span data-ttu-id="4e5e9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e5e9-124">-DefaultProfile</span></span>
<span data-ttu-id="4e5e9-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e5e9-126">-Force</span><span class="sxs-lookup"><span data-stu-id="4e5e9-126">-Force</span></span>
<span data-ttu-id="4e5e9-127">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4e5e9-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="4e5e9-128">-Name</span></span>
<span data-ttu-id="4e5e9-129">Nome dell'unità di servizio da eliminare.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-129">The name of the service unit to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName, ByServiceObject, ByServiceResourceId
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e5e9-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e5e9-130">-PassThru</span></span>
<span data-ttu-id="4e5e9-131">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="4e5e9-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="4e5e9-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e5e9-132">-ResourceGroupName</span></span>
<span data-ttu-id="4e5e9-133">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-133">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e5e9-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e5e9-134">-ResourceId</span></span>
<span data-ttu-id="4e5e9-135">Identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-135">The resource identifier.</span></span>

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

### <span data-ttu-id="4e5e9-136">-Servizio</span><span class="sxs-lookup"><span data-stu-id="4e5e9-136">-Service</span></span>
<span data-ttu-id="4e5e9-137">Oggetto Service in cui deve essere creata l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-137">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="4e5e9-138">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4e5e9-138">-ServiceName</span></span>
<span data-ttu-id="4e5e9-139">Nome del servizio a cui appartiene l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-139">The name of the service the service unit belongs to.</span></span>

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

### <span data-ttu-id="4e5e9-140">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="4e5e9-140">-ServiceResourceId</span></span>
<span data-ttu-id="4e5e9-141">Identificatore della risorsa del servizio in cui deve essere creata l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-141">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="4e5e9-142">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="4e5e9-142">-ServiceTopology</span></span>
<span data-ttu-id="4e5e9-143">Oggetto topologia del servizio in cui deve essere creata l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-143">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="4e5e9-144">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="4e5e9-144">-ServiceTopologyName</span></span>
<span data-ttu-id="4e5e9-145">Nome della topologia del servizio a cui appartiene l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-145">The name of the service topology the service unit belongs to.</span></span>

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

### <span data-ttu-id="4e5e9-146">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="4e5e9-146">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="4e5e9-147">Identificatore della risorsa della topologia del servizio in cui deve essere creata l'unità di servizio.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-147">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="4e5e9-148">-ServiceUnit</span><span class="sxs-lookup"><span data-stu-id="4e5e9-148">-ServiceUnit</span></span>
<span data-ttu-id="4e5e9-149">La risorsa da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-149">The resource to be removed.</span></span>

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

### <span data-ttu-id="4e5e9-150">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4e5e9-150">-Confirm</span></span>
<span data-ttu-id="4e5e9-151">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e5e9-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e5e9-152">-WhatIf</span></span>
<span data-ttu-id="4e5e9-153">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e5e9-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e5e9-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e5e9-155">CommonParameters</span></span>
<span data-ttu-id="4e5e9-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e5e9-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e5e9-157">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e5e9-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e5e9-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4e5e9-158">INPUTS</span></span>

### <span data-ttu-id="4e5e9-159">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="4e5e9-159">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="4e5e9-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e5e9-160">OUTPUTS</span></span>

### <span data-ttu-id="4e5e9-161">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4e5e9-161">System.Boolean</span></span>

## <span data-ttu-id="4e5e9-162">Note</span><span class="sxs-lookup"><span data-stu-id="4e5e9-162">NOTES</span></span>

## <span data-ttu-id="4e5e9-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e5e9-163">RELATED LINKS</span></span>

[<span data-ttu-id="4e5e9-164">New-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="4e5e9-164">New-AzureRmDeploymentManagerServiceUnit</span></span>](./New-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="4e5e9-165">Get-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="4e5e9-165">Get-AzureRmDeploymentManagerServiceUnit</span></span>](./Get-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="4e5e9-166">Set-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="4e5e9-166">Set-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)