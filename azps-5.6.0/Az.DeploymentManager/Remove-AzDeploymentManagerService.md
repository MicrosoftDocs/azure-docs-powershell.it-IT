---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
ms.openlocfilehash: 284e568e1748c8bf6da3c5d43c27acb046be6172
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980686"
---
# <span data-ttu-id="5de43-101">Remove-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="5de43-101">Remove-AzDeploymentManagerService</span></span>

## <span data-ttu-id="5de43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5de43-102">SYNOPSIS</span></span>
<span data-ttu-id="5de43-103">Elimina il servizio.</span><span class="sxs-lookup"><span data-stu-id="5de43-103">Deletes the service..</span></span> <span data-ttu-id="5de43-104">Tutte le unità di servizio create in un servizio devono essere eliminate prima di eliminare il servizio.</span><span class="sxs-lookup"><span data-stu-id="5de43-104">All service units created under a service need to be deleted before deleting the service.</span></span>

## <span data-ttu-id="5de43-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5de43-105">SYNTAX</span></span>

### <span data-ttu-id="5de43-106">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5de43-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5de43-107">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="5de43-107">ByServiceTopologyObject</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5de43-108">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="5de43-108">ByServiceTopologyResourceId</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5de43-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5de43-109">ResourceId</span></span>
```
Remove-AzDeploymentManagerService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5de43-110">InputObject</span><span class="sxs-lookup"><span data-stu-id="5de43-110">InputObject</span></span>
```
Remove-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5de43-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5de43-111">DESCRIPTION</span></span>
<span data-ttu-id="5de43-112">Il cmdlet **Remove-AzDeploymentManagerService** elimina un servizio in una topologia del servizio.</span><span class="sxs-lookup"><span data-stu-id="5de43-112">The **Remove-AzDeploymentManagerService** cmdlet deletes a service under a service topology.</span></span>
<span data-ttu-id="5de43-113">Specificare il servizio in base al nome, alla topologia di servizio in cui si trova e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5de43-113">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="5de43-114">In alternativa, è possibile specificare l'oggetto Servizio o l'ID Risorsa.</span><span class="sxs-lookup"><span data-stu-id="5de43-114">Alternately, you can provide the Service object or the ResourceId.</span></span>

## <span data-ttu-id="5de43-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5de43-115">EXAMPLES</span></span>

### <span data-ttu-id="5de43-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5de43-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="5de43-117">Questo comando elimina un servizio denominato ContosoService1 in una topologia di servizio denominata ContosoServiceTopology in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5de43-117">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="5de43-118">Esempio 2: Eliminare un servizio usando l'identificatore di risorsa.</span><span class="sxs-lookup"><span data-stu-id="5de43-118">Example 2: Delete a service using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="5de43-119">Questo comando elimina un servizio denominato ContosoService1 in una topologia di servizio denominata ContosoServiceTopology in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5de43-119">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="5de43-120">Esempio 3: Eliminare un servizio usando l'oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="5de43-120">Example 3: Delete a service using the service object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="5de43-121">Questo comando elimina un servizio il cui nome, il cui nome della topologia di servizio e ResourceGroup corrispondono rispettivamente alle proprietà Name, ServiceTopologyName e ResourceGroupName del $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="5de43-121">This command deletes a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="5de43-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5de43-122">PARAMETERS</span></span>

### <span data-ttu-id="5de43-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5de43-123">-DefaultProfile</span></span>
<span data-ttu-id="5de43-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5de43-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5de43-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5de43-125">-InputObject</span></span>
<span data-ttu-id="5de43-126">Oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="5de43-126">Service object.</span></span>

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

### <span data-ttu-id="5de43-127">-Name</span><span class="sxs-lookup"><span data-stu-id="5de43-127">-Name</span></span>
<span data-ttu-id="5de43-128">Nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="5de43-128">The name of the service.</span></span>

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

### <span data-ttu-id="5de43-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5de43-129">-PassThru</span></span>
<span data-ttu-id="5de43-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="5de43-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5de43-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5de43-131">-ResourceGroupName</span></span>
<span data-ttu-id="5de43-132">Gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5de43-132">The resource group.</span></span>

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

### <span data-ttu-id="5de43-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5de43-133">-ResourceId</span></span>
<span data-ttu-id="5de43-134">L'identificatore di risorsa.</span><span class="sxs-lookup"><span data-stu-id="5de43-134">The resource identifier.</span></span>

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

### <span data-ttu-id="5de43-135">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="5de43-135">-ServiceTopologyName</span></span>
<span data-ttu-id="5de43-136">Nome della topologia di servizio.</span><span class="sxs-lookup"><span data-stu-id="5de43-136">The name of the service topology.</span></span>

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

### <span data-ttu-id="5de43-137">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="5de43-137">-ServiceTopologyObject</span></span>
<span data-ttu-id="5de43-138">Oggetto topologia di servizio in cui deve essere creato il servizio.</span><span class="sxs-lookup"><span data-stu-id="5de43-138">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="5de43-139">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="5de43-139">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="5de43-140">Identificatore di risorsa della topologia del servizio in cui deve essere creato il servizio.</span><span class="sxs-lookup"><span data-stu-id="5de43-140">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="5de43-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5de43-141">-Confirm</span></span>
<span data-ttu-id="5de43-142">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5de43-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5de43-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5de43-143">-WhatIf</span></span>
<span data-ttu-id="5de43-144">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5de43-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5de43-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5de43-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5de43-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5de43-146">CommonParameters</span></span>
<span data-ttu-id="5de43-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5de43-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5de43-148">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5de43-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5de43-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="5de43-149">INPUTS</span></span>

### <span data-ttu-id="5de43-150">System.String</span><span class="sxs-lookup"><span data-stu-id="5de43-150">System.String</span></span>

### <span data-ttu-id="5de43-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="5de43-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="5de43-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5de43-152">OUTPUTS</span></span>

### <span data-ttu-id="5de43-153">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5de43-153">System.Boolean</span></span>

## <span data-ttu-id="5de43-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="5de43-154">NOTES</span></span>

## <span data-ttu-id="5de43-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5de43-155">RELATED LINKS</span></span>
