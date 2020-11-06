---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 4b2cd4ef2dde674b10d51dc378578acbd13c4a7b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490845"
---
# <span data-ttu-id="e0295-101">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="e0295-101">Remove-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="e0295-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e0295-102">SYNOPSIS</span></span>
<span data-ttu-id="e0295-103">Elimina un servizio in una topologia di servizio.</span><span class="sxs-lookup"><span data-stu-id="e0295-103">Deletes a service in a service topology.</span></span>

## <span data-ttu-id="e0295-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e0295-104">SYNTAX</span></span>

### <span data-ttu-id="e0295-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e0295-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0295-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="e0295-106">ByServiceTopologyObject</span></span>
```
Remove-AzureRmDeploymentManagerService [-Name] <String> [-ServiceTopology] <PSServiceTopologyResource> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0295-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="e0295-107">ByServiceTopologyResourceId</span></span>
```
Remove-AzureRmDeploymentManagerService [-Name] <String> [-ServiceTopologyResourceId] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0295-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0295-108">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerService [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0295-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="e0295-109">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0295-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0295-110">DESCRIPTION</span></span>
<span data-ttu-id="e0295-111">Il cmdlet **Remove-AzureRmDeploymentManagerService** Elimina un servizio in una topologia di servizio.</span><span class="sxs-lookup"><span data-stu-id="e0295-111">The **Remove-AzureRmDeploymentManagerService** cmdlet deletes a service under a service topology.</span></span>
<span data-ttu-id="e0295-112">Specificare il servizio in base al nome, alla topologia del servizio e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e0295-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="e0295-113">In alternativa, puoi specificare l'oggetto servizio o il ResourceId.</span><span class="sxs-lookup"><span data-stu-id="e0295-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

## <span data-ttu-id="e0295-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e0295-114">EXAMPLES</span></span>

### <span data-ttu-id="e0295-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e0295-115">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="e0295-116">Questo comando Elimina un servizio denominato ContosoService1 in una topologia di servizio denominata ContosoServiceTopology nel ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e0295-116">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="e0295-117">Esempio 2: eliminare un servizio usando l'identificatore delle risorse.</span><span class="sxs-lookup"><span data-stu-id="e0295-117">Example 2: Delete a service using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="e0295-118">Questo comando Elimina un servizio denominato ContosoService1 in una topologia di servizio denominata ContosoServiceTopology nel ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e0295-118">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="e0295-119">Esempio 3: eliminare un servizio usando l'oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="e0295-119">Example 3: Delete a service using the service object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="e0295-120">Questo comando Elimina un servizio il cui nome, il nome della topologia del servizio e ResourceGroup corrispondono rispettivamente alle proprietà Name, ServiceTopologyName e ResourceGroupName della $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="e0295-120">This command deletes a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="e0295-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e0295-121">PARAMETERS</span></span>

### <span data-ttu-id="e0295-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0295-122">-DefaultProfile</span></span>
<span data-ttu-id="e0295-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e0295-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0295-124">-Force</span><span class="sxs-lookup"><span data-stu-id="e0295-124">-Force</span></span>
<span data-ttu-id="e0295-125">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="e0295-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e0295-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="e0295-126">-Name</span></span>
<span data-ttu-id="e0295-127">Nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="e0295-127">The name of the service.</span></span>

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

### <span data-ttu-id="e0295-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0295-128">-PassThru</span></span>
<span data-ttu-id="e0295-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="e0295-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e0295-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0295-130">-ResourceGroupName</span></span>
<span data-ttu-id="e0295-131">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="e0295-131">The resource group.</span></span>

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

### <span data-ttu-id="e0295-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0295-132">-ResourceId</span></span>
<span data-ttu-id="e0295-133">Identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e0295-133">The resource identifier.</span></span>

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

### <span data-ttu-id="e0295-134">-Servizio</span><span class="sxs-lookup"><span data-stu-id="e0295-134">-Service</span></span>
<span data-ttu-id="e0295-135">La risorsa da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="e0295-135">The resource to be removed.</span></span>

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

### <span data-ttu-id="e0295-136">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="e0295-136">-ServiceTopology</span></span>
<span data-ttu-id="e0295-137">Oggetto topologia del servizio in cui deve essere creato il servizio.</span><span class="sxs-lookup"><span data-stu-id="e0295-137">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0295-138">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="e0295-138">-ServiceTopologyName</span></span>
<span data-ttu-id="e0295-139">Nome della topologia del servizio a cui appartiene il servizio.</span><span class="sxs-lookup"><span data-stu-id="e0295-139">The name of the service topology the service belongs to.</span></span>

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

### <span data-ttu-id="e0295-140">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="e0295-140">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="e0295-141">Identificatore della risorsa della topologia del servizio in cui deve essere creato il servizio.</span><span class="sxs-lookup"><span data-stu-id="e0295-141">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0295-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e0295-142">-Confirm</span></span>
<span data-ttu-id="e0295-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0295-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0295-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0295-144">-WhatIf</span></span>
<span data-ttu-id="e0295-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0295-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0295-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0295-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0295-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0295-147">CommonParameters</span></span>
<span data-ttu-id="e0295-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0295-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0295-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0295-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0295-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e0295-150">INPUTS</span></span>

### <span data-ttu-id="e0295-151">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="e0295-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="e0295-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e0295-152">OUTPUTS</span></span>

### <span data-ttu-id="e0295-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e0295-153">System.Boolean</span></span>

## <span data-ttu-id="e0295-154">Note</span><span class="sxs-lookup"><span data-stu-id="e0295-154">NOTES</span></span>

## <span data-ttu-id="e0295-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e0295-155">RELATED LINKS</span></span>

[<span data-ttu-id="e0295-156">New-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="e0295-156">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="e0295-157">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="e0295-157">Get-AzureRmDeploymentManagerService</span></span>](./Get-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="e0295-158">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="e0295-158">Set-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)