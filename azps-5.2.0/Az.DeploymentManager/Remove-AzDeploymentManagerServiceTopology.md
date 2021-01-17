---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 7323883028d062cf11f4e1befe1ea42cb1f8bcb2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340048"
---
# <span data-ttu-id="a1e8a-101">Remove-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="a1e8a-101">Remove-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="a1e8a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a1e8a-102">SYNOPSIS</span></span>
<span data-ttu-id="a1e8a-103">Elimina la topologia del servizio.</span><span class="sxs-lookup"><span data-stu-id="a1e8a-103">Deletes the service topology.</span></span> <span data-ttu-id="a1e8a-104">Tutti i servizi creati in una topologia di servizio devono essere eliminati prima di eliminare la topologia del servizio.</span><span class="sxs-lookup"><span data-stu-id="a1e8a-104">All services created under a service topology need to be deleted before deleting the service topology.</span></span>

## <span data-ttu-id="a1e8a-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1e8a-105">SYNTAX</span></span>

### <span data-ttu-id="a1e8a-106">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a1e8a-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1e8a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1e8a-107">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1e8a-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="a1e8a-108">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1e8a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1e8a-109">DESCRIPTION</span></span>
<span data-ttu-id="a1e8a-110">Il cmdlet **Remove-AzDeploymentManagerServiceTopology** Elimina una topologia di servizio.</span><span class="sxs-lookup"><span data-stu-id="a1e8a-110">The **Remove-AzDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="a1e8a-111">Specificare la topologia del servizio in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a1e8a-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="a1e8a-112">In alternativa, puoi specificare l'oggetto ServiceTopology o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="a1e8a-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="a1e8a-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1e8a-113">EXAMPLES</span></span>

### <span data-ttu-id="a1e8a-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a1e8a-114">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="a1e8a-115">Questo comando Elimina una topologia di servizio denominata ContosoServiceTopology in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a1e8a-115">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="a1e8a-116">Esempio 2: eliminare una topologia di servizio usando l'identificatore delle risorse.</span><span class="sxs-lookup"><span data-stu-id="a1e8a-116">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="a1e8a-117">Questo comando Elimina una topologia di servizio denominata ContosoServiceTopology in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a1e8a-117">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="a1e8a-118">Esempio 3: eliminare una topologia di servizio usando l'oggetto topologia del servizio.</span><span class="sxs-lookup"><span data-stu-id="a1e8a-118">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="a1e8a-119">Questo comando Elimina una topologia di servizio il cui nome e ResourceGroup corrispondono rispettivamente alle proprietà Name e ResourceGroupName della $serviceTopologyObject.</span><span class="sxs-lookup"><span data-stu-id="a1e8a-119">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="a1e8a-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a1e8a-120">PARAMETERS</span></span>

### <span data-ttu-id="a1e8a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1e8a-121">-DefaultProfile</span></span>
<span data-ttu-id="a1e8a-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a1e8a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1e8a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1e8a-123">-InputObject</span></span>
<span data-ttu-id="a1e8a-124">La risorsa da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="a1e8a-124">The resource to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1e8a-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1e8a-125">-Name</span></span>
<span data-ttu-id="a1e8a-126">Nome della topologia del servizio.</span><span class="sxs-lookup"><span data-stu-id="a1e8a-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="a1e8a-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1e8a-127">-PassThru</span></span>
<span data-ttu-id="a1e8a-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a1e8a-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a1e8a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1e8a-129">-ResourceGroupName</span></span>
<span data-ttu-id="a1e8a-130">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="a1e8a-130">The resource group.</span></span>

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

### <span data-ttu-id="a1e8a-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1e8a-131">-ResourceId</span></span>
<span data-ttu-id="a1e8a-132">Identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a1e8a-132">The resource identifier.</span></span>

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

### <span data-ttu-id="a1e8a-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a1e8a-133">-Confirm</span></span>
<span data-ttu-id="a1e8a-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1e8a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1e8a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1e8a-135">-WhatIf</span></span>
<span data-ttu-id="a1e8a-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1e8a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1e8a-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1e8a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1e8a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1e8a-138">CommonParameters</span></span>
<span data-ttu-id="a1e8a-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1e8a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1e8a-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1e8a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1e8a-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a1e8a-141">INPUTS</span></span>

### <span data-ttu-id="a1e8a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a1e8a-142">System.String</span></span>

### <span data-ttu-id="a1e8a-143">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="a1e8a-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="a1e8a-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1e8a-144">OUTPUTS</span></span>

### <span data-ttu-id="a1e8a-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a1e8a-145">System.Boolean</span></span>

## <span data-ttu-id="a1e8a-146">Note</span><span class="sxs-lookup"><span data-stu-id="a1e8a-146">NOTES</span></span>

## <span data-ttu-id="a1e8a-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1e8a-147">RELATED LINKS</span></span>
