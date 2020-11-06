---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: f5e0b1e0b2e85eb3c17a53b0108e853535712db1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507135"
---
# <span data-ttu-id="e3ac0-101">Get-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="e3ac0-101">Get-AzureRmDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="e3ac0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e3ac0-102">SYNOPSIS</span></span>
<span data-ttu-id="e3ac0-103">Ottiene una topologia di servizio.</span><span class="sxs-lookup"><span data-stu-id="e3ac0-103">Gets a service topology.</span></span>

## <span data-ttu-id="e3ac0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3ac0-104">SYNTAX</span></span>

### <span data-ttu-id="e3ac0-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e3ac0-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3ac0-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3ac0-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3ac0-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="e3ac0-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerServiceTopology [-ServiceTopology] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3ac0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3ac0-108">DESCRIPTION</span></span>
<span data-ttu-id="e3ac0-109">Il cmdlet **Get-AzureRmDeploymentManagerServiceTopology** ottiene una topologia di servizio.</span><span class="sxs-lookup"><span data-stu-id="e3ac0-109">The **Get-AzureRmDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="e3ac0-110">Puoi modificare l'oggetto localmente e quindi applicare le modifiche alla topologia usando il cmdlet Set-AzureRmDeploymentManagerServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="e3ac0-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzureRmDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="e3ac0-111">Specificare la topologia del servizio in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e3ac0-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="e3ac0-112">In alternativa, puoi specificare l'oggetto ServiceTopology o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="e3ac0-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="e3ac0-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3ac0-113">EXAMPLES</span></span>

### <span data-ttu-id="e3ac0-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e3ac0-114">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="e3ac0-115">Questo comando ottiene una topologia di servizio denominata ContosoServiceTopology in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e3ac0-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="e3ac0-116">Esempio 2: ottenere una topologia di servizio usando l'identificatore delle risorse.</span><span class="sxs-lookup"><span data-stu-id="e3ac0-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="e3ac0-117">Questo comando ottiene una topologia di servizio denominata ContosoServiceTopology in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e3ac0-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="e3ac0-118">Esempio 3: ottenere una topologia di servizio usando l'oggetto topologia del servizio.</span><span class="sxs-lookup"><span data-stu-id="e3ac0-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerService -ServiceTopology $serviceTopologyObject
```

<span data-ttu-id="e3ac0-119">Questo comando ottiene una topologia di servizio il cui nome e ResourceGroup corrispondono rispettivamente alle proprietà Name e ResourceGroupName della $serviceTopologyObject.</span><span class="sxs-lookup"><span data-stu-id="e3ac0-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="e3ac0-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e3ac0-120">PARAMETERS</span></span>

### <span data-ttu-id="e3ac0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3ac0-121">-DefaultProfile</span></span>
<span data-ttu-id="e3ac0-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3ac0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3ac0-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3ac0-123">-Name</span></span>
<span data-ttu-id="e3ac0-124">Nome della topologia del servizio.</span><span class="sxs-lookup"><span data-stu-id="e3ac0-124">The name of the service topology.</span></span>

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

### <span data-ttu-id="e3ac0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3ac0-125">-ResourceGroupName</span></span>
<span data-ttu-id="e3ac0-126">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="e3ac0-126">The resource group.</span></span>

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

### <span data-ttu-id="e3ac0-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3ac0-127">-ResourceId</span></span>
<span data-ttu-id="e3ac0-128">Identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e3ac0-128">The resource identifier.</span></span>

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

### <span data-ttu-id="e3ac0-129">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="e3ac0-129">-ServiceTopology</span></span>
<span data-ttu-id="e3ac0-130">Oggetto Resource della topologia del servizio.</span><span class="sxs-lookup"><span data-stu-id="e3ac0-130">Service topology resource object.</span></span>

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

### <span data-ttu-id="e3ac0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3ac0-131">CommonParameters</span></span>
<span data-ttu-id="e3ac0-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3ac0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3ac0-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3ac0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3ac0-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e3ac0-134">INPUTS</span></span>

### <span data-ttu-id="e3ac0-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e3ac0-135">None</span></span>

## <span data-ttu-id="e3ac0-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3ac0-136">OUTPUTS</span></span>

### <span data-ttu-id="e3ac0-137">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="e3ac0-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="e3ac0-138">Note</span><span class="sxs-lookup"><span data-stu-id="e3ac0-138">NOTES</span></span>

## <span data-ttu-id="e3ac0-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3ac0-139">RELATED LINKS</span></span>

[<span data-ttu-id="e3ac0-140">New-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="e3ac0-140">New-AzureRmDeploymentManagerServiceTopology</span></span>](./New-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="e3ac0-141">Remove-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="e3ac0-141">Remove-AzureRmDeploymentManagerServiceTopology</span></span>](./Remove-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="e3ac0-142">Set-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="e3ac0-142">Set-AzureRmDeploymentManagerServiceTopology</span></span>](./Set-AzureRmDeploymentManagerServiceTopology.md)