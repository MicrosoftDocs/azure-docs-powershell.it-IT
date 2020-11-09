---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
ms.openlocfilehash: 4828471d684e82d67a10bed7340cc560e843210a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297180"
---
# <span data-ttu-id="c25fc-101">Remove-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="c25fc-101">Remove-AzDeploymentManagerService</span></span>

## <span data-ttu-id="c25fc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c25fc-102">SYNOPSIS</span></span>
<span data-ttu-id="c25fc-103">Elimina il servizio..</span><span class="sxs-lookup"><span data-stu-id="c25fc-103">Deletes the service..</span></span> <span data-ttu-id="c25fc-104">Tutte le unità di servizio create in un servizio devono essere eliminate prima di eliminare il servizio.</span><span class="sxs-lookup"><span data-stu-id="c25fc-104">All service units created under a service need to be deleted before deleting the service.</span></span>

## <span data-ttu-id="c25fc-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c25fc-105">SYNTAX</span></span>

### <span data-ttu-id="c25fc-106">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c25fc-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c25fc-107">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="c25fc-107">ByServiceTopologyObject</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c25fc-108">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="c25fc-108">ByServiceTopologyResourceId</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c25fc-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c25fc-109">ResourceId</span></span>
```
Remove-AzDeploymentManagerService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c25fc-110">InputObject</span><span class="sxs-lookup"><span data-stu-id="c25fc-110">InputObject</span></span>
```
Remove-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c25fc-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c25fc-111">DESCRIPTION</span></span>
<span data-ttu-id="c25fc-112">Il cmdlet **Remove-AzDeploymentManagerService** Elimina un servizio in una topologia di servizio.</span><span class="sxs-lookup"><span data-stu-id="c25fc-112">The **Remove-AzDeploymentManagerService** cmdlet deletes a service under a service topology.</span></span>
<span data-ttu-id="c25fc-113">Specificare il servizio in base al nome, alla topologia del servizio e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c25fc-113">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="c25fc-114">In alternativa, puoi specificare l'oggetto servizio o il ResourceId.</span><span class="sxs-lookup"><span data-stu-id="c25fc-114">Alternately, you can provide the Service object or the ResourceId.</span></span>

## <span data-ttu-id="c25fc-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c25fc-115">EXAMPLES</span></span>

### <span data-ttu-id="c25fc-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c25fc-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="c25fc-117">Questo comando Elimina un servizio denominato ContosoService1 in una topologia di servizio denominata ContosoServiceTopology nel ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c25fc-117">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="c25fc-118">Esempio 2: eliminare un servizio usando l'identificatore delle risorse.</span><span class="sxs-lookup"><span data-stu-id="c25fc-118">Example 2: Delete a service using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="c25fc-119">Questo comando Elimina un servizio denominato ContosoService1 in una topologia di servizio denominata ContosoServiceTopology nel ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c25fc-119">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="c25fc-120">Esempio 3: eliminare un servizio usando l'oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="c25fc-120">Example 3: Delete a service using the service object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="c25fc-121">Questo comando Elimina un servizio il cui nome, il nome della topologia del servizio e ResourceGroup corrispondono rispettivamente alle proprietà Name, ServiceTopologyName e ResourceGroupName della $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="c25fc-121">This command deletes a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="c25fc-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c25fc-122">PARAMETERS</span></span>

### <span data-ttu-id="c25fc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c25fc-123">-DefaultProfile</span></span>
<span data-ttu-id="c25fc-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c25fc-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c25fc-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c25fc-125">-InputObject</span></span>
<span data-ttu-id="c25fc-126">Oggetto servizio.</span><span class="sxs-lookup"><span data-stu-id="c25fc-126">Service object.</span></span>

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

### <span data-ttu-id="c25fc-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="c25fc-127">-Name</span></span>
<span data-ttu-id="c25fc-128">Nome del servizio.</span><span class="sxs-lookup"><span data-stu-id="c25fc-128">The name of the service.</span></span>

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

### <span data-ttu-id="c25fc-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c25fc-129">-PassThru</span></span>
<span data-ttu-id="c25fc-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c25fc-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c25fc-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c25fc-131">-ResourceGroupName</span></span>
<span data-ttu-id="c25fc-132">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="c25fc-132">The resource group.</span></span>

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

### <span data-ttu-id="c25fc-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c25fc-133">-ResourceId</span></span>
<span data-ttu-id="c25fc-134">Identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c25fc-134">The resource identifier.</span></span>

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

### <span data-ttu-id="c25fc-135">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="c25fc-135">-ServiceTopologyName</span></span>
<span data-ttu-id="c25fc-136">Nome della topologia del servizio.</span><span class="sxs-lookup"><span data-stu-id="c25fc-136">The name of the service topology.</span></span>

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

### <span data-ttu-id="c25fc-137">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="c25fc-137">-ServiceTopologyObject</span></span>
<span data-ttu-id="c25fc-138">Oggetto topologia del servizio in cui deve essere creato il servizio.</span><span class="sxs-lookup"><span data-stu-id="c25fc-138">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="c25fc-139">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="c25fc-139">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="c25fc-140">Identificatore della risorsa della topologia del servizio in cui deve essere creato il servizio.</span><span class="sxs-lookup"><span data-stu-id="c25fc-140">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="c25fc-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c25fc-141">-Confirm</span></span>
<span data-ttu-id="c25fc-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c25fc-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c25fc-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c25fc-143">-WhatIf</span></span>
<span data-ttu-id="c25fc-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c25fc-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c25fc-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c25fc-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c25fc-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c25fc-146">CommonParameters</span></span>
<span data-ttu-id="c25fc-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c25fc-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c25fc-148">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c25fc-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c25fc-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c25fc-149">INPUTS</span></span>

### <span data-ttu-id="c25fc-150">System. String</span><span class="sxs-lookup"><span data-stu-id="c25fc-150">System.String</span></span>

### <span data-ttu-id="c25fc-151">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="c25fc-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="c25fc-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c25fc-152">OUTPUTS</span></span>

### <span data-ttu-id="c25fc-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c25fc-153">System.Boolean</span></span>

## <span data-ttu-id="c25fc-154">Note</span><span class="sxs-lookup"><span data-stu-id="c25fc-154">NOTES</span></span>

## <span data-ttu-id="c25fc-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c25fc-155">RELATED LINKS</span></span>
