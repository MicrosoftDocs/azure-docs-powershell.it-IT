---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
ms.openlocfilehash: 6c873dfda563c24104abc5e89b00569358084d96
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206019"
---
# <span data-ttu-id="962e3-101">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="962e3-101">Get-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="962e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="962e3-102">SYNOPSIS</span></span>
<span data-ttu-id="962e3-103">Ottenere la distribuzione presso un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="962e3-103">Get deployment at a management group</span></span>

## <span data-ttu-id="962e3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="962e3-104">SYNTAX</span></span>

### <span data-ttu-id="962e3-105">GetByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="962e3-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeployment [-ManagementGroupId] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="962e3-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="962e3-106">GetByDeploymentId</span></span>
```
Get-AzManagementGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="962e3-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="962e3-107">DESCRIPTION</span></span>
<span data-ttu-id="962e3-108">Il cmdlet **Get-AzManagementGroupDeployment ottiene** le distribuzioni nel gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="962e3-108">The **Get-AzManagementGroupDeployment** cmdlet gets the deployments at the a management group.</span></span>
<span data-ttu-id="962e3-109">Specificare il *parametro Name* o *Id* per filtrare i risultati.</span><span class="sxs-lookup"><span data-stu-id="962e3-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="962e3-110">Per impostazione **predefinita, Get-AzManagementGroupDeployment** ottiene tutte le distribuzioni nel gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="962e3-110">By default, **Get-AzManagementGroupDeployment** gets all deployments at the management group.</span></span>

## <span data-ttu-id="962e3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="962e3-111">EXAMPLES</span></span>

### <span data-ttu-id="962e3-112">Esempio 1: Ottenere tutte le distribuzioni in un gruppo di gestione</span><span class="sxs-lookup"><span data-stu-id="962e3-112">Example 1: Get all deployments at a management group</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG"
```

<span data-ttu-id="962e3-113">Questo comando recupera tutte le distribuzioni nel gruppo di gestione "myMG".</span><span class="sxs-lookup"><span data-stu-id="962e3-113">This command gets all deployments at the management group "myMG".</span></span>

### <span data-ttu-id="962e3-114">Esempio 2: Ottenere una distribuzione in base al nome</span><span class="sxs-lookup"><span data-stu-id="962e3-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -ManagementGroupId "myMG" -Name "Deploy01"
```

<span data-ttu-id="962e3-115">Questo comando recupera la distribuzione "Deploy01" nel gruppo di gestione "myMG".</span><span class="sxs-lookup"><span data-stu-id="962e3-115">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>
<span data-ttu-id="962e3-116">È possibile assegnare un nome a una distribuzione quando viene creata usando i cmdlet **New-AzManagementGroupDeployment.**</span><span class="sxs-lookup"><span data-stu-id="962e3-116">You can assign a name to a deployment when you create it by using the **New-AzManagementGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="962e3-117">Se non si assegna un nome, i cmdlet forniscono un nome predefinito basato sul modello usato per creare la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="962e3-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="962e3-118">Esempio 3: Ottenere una distribuzione in base all'ID</span><span class="sxs-lookup"><span data-stu-id="962e3-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Management/managementGroups/myMG/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="962e3-119">Questo comando recupera la distribuzione "Deploy01" nel gruppo di gestione "myMG".</span><span class="sxs-lookup"><span data-stu-id="962e3-119">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>

## <span data-ttu-id="962e3-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="962e3-120">PARAMETERS</span></span>

### <span data-ttu-id="962e3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="962e3-121">-DefaultProfile</span></span>
<span data-ttu-id="962e3-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="962e3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="962e3-123">-Id</span><span class="sxs-lookup"><span data-stu-id="962e3-123">-Id</span></span>
<span data-ttu-id="962e3-124">ID di risorsa completo della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="962e3-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="962e3-125">Esempio: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="962e3-125">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="962e3-126">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="962e3-126">-ManagementGroupId</span></span>
<span data-ttu-id="962e3-127">ID del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="962e3-127">The management group id.</span></span>

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

### <span data-ttu-id="962e3-128">-Name</span><span class="sxs-lookup"><span data-stu-id="962e3-128">-Name</span></span>
<span data-ttu-id="962e3-129">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="962e3-129">The name of deployment.</span></span>

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

### <span data-ttu-id="962e3-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="962e3-130">-Pre</span></span>
<span data-ttu-id="962e3-131">Se impostato, indica che il cmdlet deve usare versioni delle API non beta per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="962e3-131">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="962e3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="962e3-132">CommonParameters</span></span>
<span data-ttu-id="962e3-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="962e3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="962e3-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="962e3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="962e3-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="962e3-135">INPUTS</span></span>

### <span data-ttu-id="962e3-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="962e3-136">None</span></span>

## <span data-ttu-id="962e3-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="962e3-137">OUTPUTS</span></span>

### <span data-ttu-id="962e3-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="962e3-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="962e3-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="962e3-139">NOTES</span></span>

## <span data-ttu-id="962e3-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="962e3-140">RELATED LINKS</span></span>
