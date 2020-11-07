---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
ms.openlocfilehash: 6a18c886ddddc30c82746ebe76d83d9477399755
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865076"
---
# <span data-ttu-id="b7868-101">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="b7868-101">Get-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="b7868-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b7868-102">SYNOPSIS</span></span>
<span data-ttu-id="b7868-103">Ottenere la distribuzione in un gruppo di gestione del</span><span class="sxs-lookup"><span data-stu-id="b7868-103">Get deployment at a mangement group</span></span>

## <span data-ttu-id="b7868-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7868-104">SYNTAX</span></span>

### <span data-ttu-id="b7868-105">GetByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b7868-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeployment [-ManagementGroupId] <String> [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7868-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="b7868-106">GetByDeploymentId</span></span>
```
Get-AzManagementGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7868-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7868-107">DESCRIPTION</span></span>
<span data-ttu-id="b7868-108">Il cmdlet **Get-AzManagementGroupDeployment** ottiene le distribuzioni in un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="b7868-108">The **Get-AzManagementGroupDeployment** cmdlet gets the deployments at the a management group.</span></span>
<span data-ttu-id="b7868-109">Specificare il *nome* o il parametro *ID* per filtrare i risultati.</span><span class="sxs-lookup"><span data-stu-id="b7868-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="b7868-110">Per impostazione predefinita, **Get-AzManagementGroupDeployment** ottiene tutte le distribuzioni nel gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="b7868-110">By default, **Get-AzManagementGroupDeployment** gets all deployments at the management group.</span></span>

## <span data-ttu-id="b7868-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7868-111">EXAMPLES</span></span>

### <span data-ttu-id="b7868-112">Esempio 1: ottenere tutte le distribuzioni in un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="b7868-112">Example 1: Get all deployments at a management group</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG"
```

<span data-ttu-id="b7868-113">Questo comando consente di ottenere tutte le distribuzioni nel gruppo di gestione "myMG".</span><span class="sxs-lookup"><span data-stu-id="b7868-113">This command gets all deployments at the management group "myMG".</span></span>

### <span data-ttu-id="b7868-114">Esempio 2: ottenere una distribuzione per nome</span><span class="sxs-lookup"><span data-stu-id="b7868-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -ManagementGroupId "myMG" -Name "Deploy01"
```

<span data-ttu-id="b7868-115">Questo comando ottiene la distribuzione "Deploy01" nel gruppo di gestione "myMG".</span><span class="sxs-lookup"><span data-stu-id="b7868-115">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>
<span data-ttu-id="b7868-116">È possibile assegnare un nome a una distribuzione quando la si crea usando i cmdlet **New-AzManagementGroupDeployment** .</span><span class="sxs-lookup"><span data-stu-id="b7868-116">You can assign a name to a deployment when you create it by using the **New-AzManagementGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="b7868-117">Se non si assegna un nome, i cmdlet prevedono un nome predefinito basato sul modello usato per creare la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="b7868-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="b7868-118">Esempio 3: ottenere una distribuzione in base all'ID</span><span class="sxs-lookup"><span data-stu-id="b7868-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Management/managementGroups/myMG/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="b7868-119">Questo comando ottiene la distribuzione "Deploy01" nel gruppo di gestione "myMG".</span><span class="sxs-lookup"><span data-stu-id="b7868-119">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>

## <span data-ttu-id="b7868-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b7868-120">PARAMETERS</span></span>

### <span data-ttu-id="b7868-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b7868-121">-ApiVersion</span></span>
<span data-ttu-id="b7868-122">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="b7868-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="b7868-123">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="b7868-123">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7868-124">-DefaultProfile</span></span>
<span data-ttu-id="b7868-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b7868-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-126">-ID</span><span class="sxs-lookup"><span data-stu-id="b7868-126">-Id</span></span>
<span data-ttu-id="b7868-127">ID risorsa completo della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="b7868-127">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="b7868-128">esempio:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="b7868-128">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-129">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="b7868-129">-ManagementGroupId</span></span>
<span data-ttu-id="b7868-130">ID gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="b7868-130">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="b7868-131">-Name</span></span>
<span data-ttu-id="b7868-132">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="b7868-132">The name of deployment.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="b7868-133">-Pre</span></span>
<span data-ttu-id="b7868-134">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="b7868-134">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7868-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7868-135">CommonParameters</span></span>
<span data-ttu-id="b7868-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7868-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7868-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7868-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7868-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b7868-138">INPUTS</span></span>

### <span data-ttu-id="b7868-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b7868-139">None</span></span>

## <span data-ttu-id="b7868-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7868-140">OUTPUTS</span></span>

### <span data-ttu-id="b7868-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEPLOYMENT</span><span class="sxs-lookup"><span data-stu-id="b7868-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="b7868-142">Note</span><span class="sxs-lookup"><span data-stu-id="b7868-142">NOTES</span></span>

## <span data-ttu-id="b7868-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7868-143">RELATED LINKS</span></span>
