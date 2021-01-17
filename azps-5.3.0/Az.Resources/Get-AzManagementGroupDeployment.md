---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
ms.openlocfilehash: 6c873dfda563c24104abc5e89b00569358084d96
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474280"
---
# <span data-ttu-id="5a7fe-101">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="5a7fe-101">Get-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="5a7fe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5a7fe-102">SYNOPSIS</span></span>
<span data-ttu-id="5a7fe-103">Ottenere la distribuzione in un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="5a7fe-103">Get deployment at a management group</span></span>

## <span data-ttu-id="5a7fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5a7fe-104">SYNTAX</span></span>

### <span data-ttu-id="5a7fe-105">GetByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5a7fe-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeployment [-ManagementGroupId] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a7fe-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="5a7fe-106">GetByDeploymentId</span></span>
```
Get-AzManagementGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5a7fe-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a7fe-107">DESCRIPTION</span></span>
<span data-ttu-id="5a7fe-108">Il cmdlet **Get-AzManagementGroupDeployment** ottiene le distribuzioni in un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="5a7fe-108">The **Get-AzManagementGroupDeployment** cmdlet gets the deployments at the a management group.</span></span>
<span data-ttu-id="5a7fe-109">Specificare il *nome* o il parametro *ID* per filtrare i risultati.</span><span class="sxs-lookup"><span data-stu-id="5a7fe-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="5a7fe-110">Per impostazione predefinita, **Get-AzManagementGroupDeployment** ottiene tutte le distribuzioni nel gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="5a7fe-110">By default, **Get-AzManagementGroupDeployment** gets all deployments at the management group.</span></span>

## <span data-ttu-id="5a7fe-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5a7fe-111">EXAMPLES</span></span>

### <span data-ttu-id="5a7fe-112">Esempio 1: ottenere tutte le distribuzioni in un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="5a7fe-112">Example 1: Get all deployments at a management group</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG"
```

<span data-ttu-id="5a7fe-113">Questo comando consente di ottenere tutte le distribuzioni nel gruppo di gestione "myMG".</span><span class="sxs-lookup"><span data-stu-id="5a7fe-113">This command gets all deployments at the management group "myMG".</span></span>

### <span data-ttu-id="5a7fe-114">Esempio 2: ottenere una distribuzione per nome</span><span class="sxs-lookup"><span data-stu-id="5a7fe-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -ManagementGroupId "myMG" -Name "Deploy01"
```

<span data-ttu-id="5a7fe-115">Questo comando ottiene la distribuzione "Deploy01" nel gruppo di gestione "myMG".</span><span class="sxs-lookup"><span data-stu-id="5a7fe-115">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>
<span data-ttu-id="5a7fe-116">È possibile assegnare un nome a una distribuzione quando la si crea usando i cmdlet **New-AzManagementGroupDeployment** .</span><span class="sxs-lookup"><span data-stu-id="5a7fe-116">You can assign a name to a deployment when you create it by using the **New-AzManagementGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="5a7fe-117">Se non si assegna un nome, i cmdlet prevedono un nome predefinito basato sul modello usato per creare la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="5a7fe-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="5a7fe-118">Esempio 3: ottenere una distribuzione in base all'ID</span><span class="sxs-lookup"><span data-stu-id="5a7fe-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Management/managementGroups/myMG/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="5a7fe-119">Questo comando ottiene la distribuzione "Deploy01" nel gruppo di gestione "myMG".</span><span class="sxs-lookup"><span data-stu-id="5a7fe-119">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>

## <span data-ttu-id="5a7fe-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5a7fe-120">PARAMETERS</span></span>

### <span data-ttu-id="5a7fe-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a7fe-121">-DefaultProfile</span></span>
<span data-ttu-id="5a7fe-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5a7fe-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a7fe-123">-ID</span><span class="sxs-lookup"><span data-stu-id="5a7fe-123">-Id</span></span>
<span data-ttu-id="5a7fe-124">ID risorsa completo della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="5a7fe-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="5a7fe-125">esempio:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="5a7fe-125">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a7fe-126">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="5a7fe-126">-ManagementGroupId</span></span>
<span data-ttu-id="5a7fe-127">ID gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="5a7fe-127">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a7fe-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="5a7fe-128">-Name</span></span>
<span data-ttu-id="5a7fe-129">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="5a7fe-129">The name of deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a7fe-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="5a7fe-130">-Pre</span></span>
<span data-ttu-id="5a7fe-131">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="5a7fe-131">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="5a7fe-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a7fe-132">CommonParameters</span></span>
<span data-ttu-id="5a7fe-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a7fe-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a7fe-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a7fe-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a7fe-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5a7fe-135">INPUTS</span></span>

### <span data-ttu-id="5a7fe-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5a7fe-136">None</span></span>

## <span data-ttu-id="5a7fe-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5a7fe-137">OUTPUTS</span></span>

### <span data-ttu-id="5a7fe-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEPLOYMENT</span><span class="sxs-lookup"><span data-stu-id="5a7fe-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="5a7fe-139">Note</span><span class="sxs-lookup"><span data-stu-id="5a7fe-139">NOTES</span></span>

## <span data-ttu-id="5a7fe-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5a7fe-140">RELATED LINKS</span></span>
