---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
ms.openlocfilehash: 1755438dfc5bdb9b4eedf46ec364e851a2bca154
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997218"
---
# <span data-ttu-id="dfa85-101">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="dfa85-101">Get-AzTenantDeployment</span></span>

## <span data-ttu-id="dfa85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfa85-102">SYNOPSIS</span></span>
<span data-ttu-id="dfa85-103">Ottenere la distribuzione nell'ambito tenant</span><span class="sxs-lookup"><span data-stu-id="dfa85-103">Get deployment at tenant scope</span></span>

## <span data-ttu-id="dfa85-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dfa85-104">SYNTAX</span></span>

### <span data-ttu-id="dfa85-105">GetByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dfa85-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dfa85-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="dfa85-106">GetByDeploymentId</span></span>
```
Get-AzTenantDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dfa85-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dfa85-107">DESCRIPTION</span></span>
<span data-ttu-id="dfa85-108">Il cmdlet **Get-AzTenantDeployment** ottiene le distribuzioni nell'ambito tenant.</span><span class="sxs-lookup"><span data-stu-id="dfa85-108">The **Get-AzTenantDeployment** cmdlet gets the deployments at the tenant scope.</span></span>
<span data-ttu-id="dfa85-109">Specificare il *parametro Name* o *Id* per filtrare i risultati.</span><span class="sxs-lookup"><span data-stu-id="dfa85-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="dfa85-110">Per impostazione **predefinita, Get-AzTenantDeployment** ottiene tutte le distribuzioni nell'ambito tenant.</span><span class="sxs-lookup"><span data-stu-id="dfa85-110">By default, **Get-AzTenantDeployment** gets all deployments at the tenant scope.</span></span>

## <span data-ttu-id="dfa85-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dfa85-111">EXAMPLES</span></span>

### <span data-ttu-id="dfa85-112">Esempio 1: Ottenere tutte le distribuzioni nell'ambito tenant</span><span class="sxs-lookup"><span data-stu-id="dfa85-112">Example 1: Get all deployments at the tenant scope</span></span>
```
PS C:\>Get-AzTenantDeployment
```

<span data-ttu-id="dfa85-113">Questo comando recupera tutte le distribuzioni nell'ambito tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="dfa85-113">This command gets all deployments at the current tenant scope.</span></span>

### <span data-ttu-id="dfa85-114">Esempio 2: Ottenere una distribuzione in base al nome</span><span class="sxs-lookup"><span data-stu-id="dfa85-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "Deploy01"
```

<span data-ttu-id="dfa85-115">Questo comando ottiene la distribuzione "Deploy01" nell'ambito tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="dfa85-115">This command gets the "Deploy01" deployment at the current tenant scope.</span></span>
<span data-ttu-id="dfa85-116">È possibile assegnare un nome a una distribuzione quando viene creata usando i cmdlet **New-AzTenantDeployment.**</span><span class="sxs-lookup"><span data-stu-id="dfa85-116">You can assign a name to a deployment when you create it by using the **New-AzTenantDeployment** cmdlets.</span></span>
<span data-ttu-id="dfa85-117">Se non si assegna un nome, i cmdlet forniscono un nome predefinito basato sul modello usato per creare la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="dfa85-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="dfa85-118">Esempio 3: Ottenere una distribuzione in base all'ID</span><span class="sxs-lookup"><span data-stu-id="dfa85-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="dfa85-119">Questo comando ottiene la distribuzione "Deploy01" nell'ambito tenant.</span><span class="sxs-lookup"><span data-stu-id="dfa85-119">This command gets the "Deploy01" deployment at the tenant scope.</span></span>

## <span data-ttu-id="dfa85-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dfa85-120">PARAMETERS</span></span>

### <span data-ttu-id="dfa85-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfa85-121">-DefaultProfile</span></span>
<span data-ttu-id="dfa85-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dfa85-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfa85-123">-Id</span><span class="sxs-lookup"><span data-stu-id="dfa85-123">-Id</span></span>
<span data-ttu-id="dfa85-124">ID di risorsa completo della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="dfa85-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="dfa85-125">Esempio: /providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="dfa85-125">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="dfa85-126">-Name</span><span class="sxs-lookup"><span data-stu-id="dfa85-126">-Name</span></span>
<span data-ttu-id="dfa85-127">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="dfa85-127">The name of deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfa85-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="dfa85-128">-Pre</span></span>
<span data-ttu-id="dfa85-129">Se impostato, indica che il cmdlet deve usare versioni delle API non beta per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="dfa85-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="dfa85-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfa85-130">CommonParameters</span></span>
<span data-ttu-id="dfa85-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfa85-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfa85-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dfa85-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfa85-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="dfa85-133">INPUTS</span></span>

### <span data-ttu-id="dfa85-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="dfa85-134">None</span></span>

## <span data-ttu-id="dfa85-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dfa85-135">OUTPUTS</span></span>

### <span data-ttu-id="dfa85-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="dfa85-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="dfa85-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="dfa85-137">NOTES</span></span>

## <span data-ttu-id="dfa85-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dfa85-138">RELATED LINKS</span></span>
