---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: c02a88cdb550e1ec9cb343b286d3211045873820
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980733"
---
# <span data-ttu-id="bef91-101">Get-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="bef91-101">Get-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="bef91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bef91-102">SYNOPSIS</span></span>
<span data-ttu-id="bef91-103">Recupera la topologia del servizio.</span><span class="sxs-lookup"><span data-stu-id="bef91-103">Gets the service topology.</span></span>

## <span data-ttu-id="bef91-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bef91-104">SYNTAX</span></span>

### <span data-ttu-id="bef91-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bef91-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bef91-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="bef91-106">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bef91-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="bef91-107">InputObject</span></span>
```
Get-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bef91-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bef91-108">DESCRIPTION</span></span>
<span data-ttu-id="bef91-109">Il cmdlet **Get-AzDeploymentManagerServiceTopology** ottiene una topologia di servizio.</span><span class="sxs-lookup"><span data-stu-id="bef91-109">The **Get-AzDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="bef91-110">È possibile modificare l'oggetto in locale e quindi applicare modifiche alla topologia usando il cmdlet Set-AzDeploymentManagerServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="bef91-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="bef91-111">Specificare la topologia del servizio in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bef91-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="bef91-112">In alternativa, è possibile fornire l'oggetto ServiceTopology o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="bef91-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="bef91-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bef91-113">EXAMPLES</span></span>

### <span data-ttu-id="bef91-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bef91-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="bef91-115">Questo comando ottiene una topologia di servizio denominata ContosoServiceTopology in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="bef91-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="bef91-116">Esempio 2: Ottenere la topologia di un servizio usando l'identificatore di risorsa.</span><span class="sxs-lookup"><span data-stu-id="bef91-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="bef91-117">Questo comando ottiene una topologia di servizio denominata ContosoServiceTopology in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="bef91-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="bef91-118">Esempio 3: Ottenere una topologia del servizio usando l'oggetto topologia di servizio.</span><span class="sxs-lookup"><span data-stu-id="bef91-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="bef91-119">Questo comando ottiene una topologia di servizio il cui nome e GruppoSocietà Risorse corrispondono rispettivamente alle proprietà Name e ResourceGroupName del $serviceTopologyObject.</span><span class="sxs-lookup"><span data-stu-id="bef91-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="bef91-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bef91-120">PARAMETERS</span></span>

### <span data-ttu-id="bef91-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bef91-121">-DefaultProfile</span></span>
<span data-ttu-id="bef91-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bef91-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bef91-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bef91-123">-InputObject</span></span>
<span data-ttu-id="bef91-124">Oggetto risorsa topologia di servizio.</span><span class="sxs-lookup"><span data-stu-id="bef91-124">Service topology resource object.</span></span>

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

### <span data-ttu-id="bef91-125">-Name</span><span class="sxs-lookup"><span data-stu-id="bef91-125">-Name</span></span>
<span data-ttu-id="bef91-126">Nome della topologia di servizio.</span><span class="sxs-lookup"><span data-stu-id="bef91-126">The name of the service topology.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bef91-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bef91-127">-ResourceGroupName</span></span>
<span data-ttu-id="bef91-128">Gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bef91-128">The resource group.</span></span>

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

### <span data-ttu-id="bef91-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bef91-129">-ResourceId</span></span>
<span data-ttu-id="bef91-130">L'identificatore di risorsa.</span><span class="sxs-lookup"><span data-stu-id="bef91-130">The resource identifier.</span></span>

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

### <span data-ttu-id="bef91-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bef91-131">CommonParameters</span></span>
<span data-ttu-id="bef91-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bef91-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bef91-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bef91-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bef91-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="bef91-134">INPUTS</span></span>

### <span data-ttu-id="bef91-135">System.String</span><span class="sxs-lookup"><span data-stu-id="bef91-135">System.String</span></span>

### <span data-ttu-id="bef91-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="bef91-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="bef91-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bef91-137">OUTPUTS</span></span>

### <span data-ttu-id="bef91-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="bef91-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="bef91-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="bef91-139">NOTES</span></span>

## <span data-ttu-id="bef91-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bef91-140">RELATED LINKS</span></span>
