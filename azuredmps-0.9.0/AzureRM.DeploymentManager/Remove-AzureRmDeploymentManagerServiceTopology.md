---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: be95f5fffe4483c74d8b1438819cf084eaa0693b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490929"
---
# <span data-ttu-id="8b122-101">Remove-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="8b122-101">Remove-AzureRmDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="8b122-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8b122-102">SYNOPSIS</span></span>
<span data-ttu-id="8b122-103">Elimina una topologia di servizio e tutte le relative risorse.</span><span class="sxs-lookup"><span data-stu-id="8b122-103">Deletes a service topology and all its resources.</span></span>

## <span data-ttu-id="8b122-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8b122-104">SYNTAX</span></span>

### <span data-ttu-id="8b122-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8b122-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b122-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b122-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerServiceTopology [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b122-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="8b122-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerServiceTopology [-ServiceTopology] <PSServiceTopologyResource> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b122-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b122-108">DESCRIPTION</span></span>
<span data-ttu-id="8b122-109">Il cmdlet **Remove-AzureRmDeploymentManagerServiceTopology** Elimina una topologia di servizio.</span><span class="sxs-lookup"><span data-stu-id="8b122-109">The **Remove-AzureRmDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="8b122-110">Specificare la topologia del servizio in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8b122-110">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="8b122-111">In alternativa, puoi specificare l'oggetto ServiceTopology o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="8b122-111">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="8b122-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8b122-112">EXAMPLES</span></span>

### <span data-ttu-id="8b122-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8b122-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="8b122-114">Questo comando Elimina una topologia di servizio denominata ContosoServiceTopology in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8b122-114">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="8b122-115">Esempio 2: eliminare una topologia di servizio usando l'identificatore delle risorse.</span><span class="sxs-lookup"><span data-stu-id="8b122-115">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="8b122-116">Questo comando Elimina una topologia di servizio denominata ContosoServiceTopology in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8b122-116">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="8b122-117">Esempio 3: eliminare una topologia di servizio usando l'oggetto topologia del servizio.</span><span class="sxs-lookup"><span data-stu-id="8b122-117">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -ServiceTopology $serviceTopologyObject
```

<span data-ttu-id="8b122-118">Questo comando Elimina una topologia di servizio il cui nome e ResourceGroup corrispondono rispettivamente alle proprietà Name e ResourceGroupName della $serviceTopologyObject.</span><span class="sxs-lookup"><span data-stu-id="8b122-118">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="8b122-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8b122-119">PARAMETERS</span></span>

### <span data-ttu-id="8b122-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b122-120">-DefaultProfile</span></span>
<span data-ttu-id="8b122-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8b122-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b122-122">-Force</span><span class="sxs-lookup"><span data-stu-id="8b122-122">-Force</span></span>
<span data-ttu-id="8b122-123">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="8b122-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8b122-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="8b122-124">-Name</span></span>
<span data-ttu-id="8b122-125">Nome della topologia del servizio.</span><span class="sxs-lookup"><span data-stu-id="8b122-125">The name of the service topology.</span></span>

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

### <span data-ttu-id="8b122-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b122-126">-PassThru</span></span>
<span data-ttu-id="8b122-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="8b122-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="8b122-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b122-128">-ResourceGroupName</span></span>
<span data-ttu-id="8b122-129">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="8b122-129">The resource group.</span></span>

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

### <span data-ttu-id="8b122-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b122-130">-ResourceId</span></span>
<span data-ttu-id="8b122-131">Identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="8b122-131">The resource identifier.</span></span>

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

### <span data-ttu-id="8b122-132">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="8b122-132">-ServiceTopology</span></span>
<span data-ttu-id="8b122-133">La risorsa da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="8b122-133">The resource to be removed.</span></span>

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

### <span data-ttu-id="8b122-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8b122-134">-Confirm</span></span>
<span data-ttu-id="8b122-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b122-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b122-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b122-136">-WhatIf</span></span>
<span data-ttu-id="8b122-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8b122-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b122-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8b122-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b122-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b122-139">CommonParameters</span></span>
<span data-ttu-id="8b122-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b122-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b122-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b122-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b122-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8b122-142">INPUTS</span></span>

### <span data-ttu-id="8b122-143">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="8b122-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="8b122-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8b122-144">OUTPUTS</span></span>

### <span data-ttu-id="8b122-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8b122-145">System.Boolean</span></span>

## <span data-ttu-id="8b122-146">Note</span><span class="sxs-lookup"><span data-stu-id="8b122-146">NOTES</span></span>

## <span data-ttu-id="8b122-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8b122-147">RELATED LINKS</span></span>

[<span data-ttu-id="8b122-148">New-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="8b122-148">New-AzureRmDeploymentManagerServiceTopology</span></span>](./New-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="8b122-149">Get-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="8b122-149">Get-AzureRmDeploymentManagerServiceTopology</span></span>](./Get-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="8b122-150">Set-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="8b122-150">Set-AzureRmDeploymentManagerServiceTopology</span></span>](./Set-AzureRmDeploymentManagerServiceTopology.md)