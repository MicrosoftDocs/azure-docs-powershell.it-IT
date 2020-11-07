---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 54a48a025dff2bba2c1ad620237d0a84aacf7d7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684467"
---
# <span data-ttu-id="46347-101">Get-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="46347-101">Get-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="46347-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="46347-102">SYNOPSIS</span></span>
<span data-ttu-id="46347-103">Ottiene la topologia del servizio.</span><span class="sxs-lookup"><span data-stu-id="46347-103">Gets the service topology.</span></span>

## <span data-ttu-id="46347-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="46347-104">SYNTAX</span></span>

### <span data-ttu-id="46347-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="46347-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46347-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="46347-106">ResourceId</span></span>
```
Get-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="46347-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="46347-107">InputObject</span></span>
```
Get-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46347-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46347-108">DESCRIPTION</span></span>
<span data-ttu-id="46347-109">Il cmdlet **Get-AzDeploymentManagerServiceTopology** ottiene una topologia di servizio.</span><span class="sxs-lookup"><span data-stu-id="46347-109">The **Get-AzDeploymentManagerServiceTopology** cmdlet gets a service topology.</span></span>

<span data-ttu-id="46347-110">Puoi modificare l'oggetto localmente e quindi applicare le modifiche alla topologia usando il cmdlet Set-AzDeploymentManagerServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="46347-110">You can modify this object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="46347-111">Specificare la topologia del servizio in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="46347-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="46347-112">In alternativa, puoi specificare l'oggetto ServiceTopology o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="46347-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="46347-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="46347-113">EXAMPLES</span></span>

### <span data-ttu-id="46347-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="46347-114">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="46347-115">Questo comando ottiene una topologia di servizio denominata ContosoServiceTopology in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="46347-115">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="46347-116">Esempio 2: ottenere una topologia di servizio usando l'identificatore delle risorse.</span><span class="sxs-lookup"><span data-stu-id="46347-116">Example 2: Get a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="46347-117">Questo comando ottiene una topologia di servizio denominata ContosoServiceTopology in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="46347-117">This command gets a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="46347-118">Esempio 3: ottenere una topologia di servizio usando l'oggetto topologia del servizio.</span><span class="sxs-lookup"><span data-stu-id="46347-118">Example 3: Get a service topology using the service topology object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="46347-119">Questo comando ottiene una topologia di servizio il cui nome e ResourceGroup corrispondono rispettivamente alle proprietà Name e ResourceGroupName della $serviceTopologyObject.</span><span class="sxs-lookup"><span data-stu-id="46347-119">This command gets a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="46347-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="46347-120">PARAMETERS</span></span>

### <span data-ttu-id="46347-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46347-121">-DefaultProfile</span></span>
<span data-ttu-id="46347-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="46347-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46347-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46347-123">-InputObject</span></span>
<span data-ttu-id="46347-124">Oggetto Resource della topologia del servizio.</span><span class="sxs-lookup"><span data-stu-id="46347-124">Service topology resource object.</span></span>

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

### <span data-ttu-id="46347-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="46347-125">-Name</span></span>
<span data-ttu-id="46347-126">Nome della topologia del servizio.</span><span class="sxs-lookup"><span data-stu-id="46347-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="46347-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46347-127">-ResourceGroupName</span></span>
<span data-ttu-id="46347-128">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="46347-128">The resource group.</span></span>

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

### <span data-ttu-id="46347-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46347-129">-ResourceId</span></span>
<span data-ttu-id="46347-130">Identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="46347-130">The resource identifier.</span></span>

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

### <span data-ttu-id="46347-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46347-131">CommonParameters</span></span>
<span data-ttu-id="46347-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46347-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46347-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46347-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46347-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="46347-134">INPUTS</span></span>

### <span data-ttu-id="46347-135">System. String</span><span class="sxs-lookup"><span data-stu-id="46347-135">System.String</span></span>

### <span data-ttu-id="46347-136">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="46347-136">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="46347-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="46347-137">OUTPUTS</span></span>

### <span data-ttu-id="46347-138">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="46347-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="46347-139">Note</span><span class="sxs-lookup"><span data-stu-id="46347-139">NOTES</span></span>

## <span data-ttu-id="46347-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="46347-140">RELATED LINKS</span></span>
