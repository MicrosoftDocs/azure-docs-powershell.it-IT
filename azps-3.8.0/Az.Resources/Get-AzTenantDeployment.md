---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
ms.openlocfilehash: c3218141e495bb92216e254830ddaa7dd7a0a0c9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021736"
---
# <span data-ttu-id="ba22b-101">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="ba22b-101">Get-AzTenantDeployment</span></span>

## <span data-ttu-id="ba22b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ba22b-102">SYNOPSIS</span></span>
<span data-ttu-id="ba22b-103">Ottenere la distribuzione in ambito tenant</span><span class="sxs-lookup"><span data-stu-id="ba22b-103">Get deployment at tenant scope</span></span>

## <span data-ttu-id="ba22b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba22b-104">SYNTAX</span></span>

### <span data-ttu-id="ba22b-105">GetByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ba22b-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba22b-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="ba22b-106">GetByDeploymentId</span></span>
```
Get-AzTenantDeployment -Id <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba22b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba22b-107">DESCRIPTION</span></span>
<span data-ttu-id="ba22b-108">Il cmdlet **Get-AzTenantDeployment** ottiene le distribuzioni nell'ambito del tenant.</span><span class="sxs-lookup"><span data-stu-id="ba22b-108">The **Get-AzTenantDeployment** cmdlet gets the deployments at the tenant scope.</span></span>
<span data-ttu-id="ba22b-109">Specificare il *nome* o il parametro *ID* per filtrare i risultati.</span><span class="sxs-lookup"><span data-stu-id="ba22b-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="ba22b-110">Per impostazione predefinita, **Get-AzTenantDeployment** ottiene tutte le distribuzioni nell'ambito del tenant.</span><span class="sxs-lookup"><span data-stu-id="ba22b-110">By default, **Get-AzTenantDeployment** gets all deployments at the tenant scope.</span></span>

## <span data-ttu-id="ba22b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba22b-111">EXAMPLES</span></span>

### <span data-ttu-id="ba22b-112">Esempio 1: ottenere tutte le distribuzioni nell'ambito del tenant</span><span class="sxs-lookup"><span data-stu-id="ba22b-112">Example 1: Get all deployments at the tenant scope</span></span>
```
PS C:\>Get-AzTenantDeployment
```

<span data-ttu-id="ba22b-113">Questo comando consente di ottenere tutte le distribuzioni nell'ambito del tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="ba22b-113">This command gets all deployments at the current tenant scope.</span></span>

### <span data-ttu-id="ba22b-114">Esempio 2: ottenere una distribuzione per nome</span><span class="sxs-lookup"><span data-stu-id="ba22b-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "Deploy01"
```

<span data-ttu-id="ba22b-115">Questo comando ottiene la distribuzione "Deploy01" nell'ambito del tenant corrente.</span><span class="sxs-lookup"><span data-stu-id="ba22b-115">This command gets the "Deploy01" deployment at the current tenant scope.</span></span>
<span data-ttu-id="ba22b-116">È possibile assegnare un nome a una distribuzione quando la si crea usando i cmdlet **New-AzTenantDeployment** .</span><span class="sxs-lookup"><span data-stu-id="ba22b-116">You can assign a name to a deployment when you create it by using the **New-AzTenantDeployment** cmdlets.</span></span>
<span data-ttu-id="ba22b-117">Se non si assegna un nome, i cmdlet prevedono un nome predefinito basato sul modello usato per creare la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="ba22b-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="ba22b-118">Esempio 3: ottenere una distribuzione in base all'ID</span><span class="sxs-lookup"><span data-stu-id="ba22b-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="ba22b-119">Questo comando ottiene la distribuzione "Deploy01" nell'ambito del tenant.</span><span class="sxs-lookup"><span data-stu-id="ba22b-119">This command gets the "Deploy01" deployment at the tenant scope.</span></span>

## <span data-ttu-id="ba22b-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ba22b-120">PARAMETERS</span></span>

### <span data-ttu-id="ba22b-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ba22b-121">-ApiVersion</span></span>
<span data-ttu-id="ba22b-122">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="ba22b-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="ba22b-123">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="ba22b-123">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="ba22b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba22b-124">-DefaultProfile</span></span>
<span data-ttu-id="ba22b-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ba22b-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba22b-126">-ID</span><span class="sxs-lookup"><span data-stu-id="ba22b-126">-Id</span></span>
<span data-ttu-id="ba22b-127">ID risorsa completo della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="ba22b-127">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="ba22b-128">esempio:/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="ba22b-128">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="ba22b-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="ba22b-129">-Name</span></span>
<span data-ttu-id="ba22b-130">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="ba22b-130">The name of deployment.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba22b-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="ba22b-131">-Pre</span></span>
<span data-ttu-id="ba22b-132">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="ba22b-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ba22b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba22b-133">CommonParameters</span></span>
<span data-ttu-id="ba22b-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba22b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba22b-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba22b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba22b-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ba22b-136">INPUTS</span></span>

### <span data-ttu-id="ba22b-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ba22b-137">None</span></span>

## <span data-ttu-id="ba22b-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba22b-138">OUTPUTS</span></span>

### <span data-ttu-id="ba22b-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEPLOYMENT</span><span class="sxs-lookup"><span data-stu-id="ba22b-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="ba22b-140">Note</span><span class="sxs-lookup"><span data-stu-id="ba22b-140">NOTES</span></span>

## <span data-ttu-id="ba22b-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba22b-141">RELATED LINKS</span></span>
