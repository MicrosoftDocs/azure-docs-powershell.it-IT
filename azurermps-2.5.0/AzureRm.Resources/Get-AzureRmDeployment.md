---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermdeployment
schema: 2.0.0
ms.openlocfilehash: 1a86eb136fe976ba5e229ff36bd5d0e2a2cad340
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866011"
---
# <span data-ttu-id="76d8c-101">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="76d8c-101">Get-AzureRmDeployment</span></span>

## <span data-ttu-id="76d8c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="76d8c-102">SYNOPSIS</span></span>
<span data-ttu-id="76d8c-103">Ottenere la distribuzione</span><span class="sxs-lookup"><span data-stu-id="76d8c-103">Get deployment</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76d8c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="76d8c-104">SYNTAX</span></span>

### <span data-ttu-id="76d8c-105">GetByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="76d8c-105">GetByDeploymentName (Default)</span></span>
```
Get-AzureRmDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76d8c-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="76d8c-106">GetByDeploymentId</span></span>
```
Get-AzureRmDeployment [-Id <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="76d8c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76d8c-107">DESCRIPTION</span></span>
<span data-ttu-id="76d8c-108">Il cmdlet **Get-AzureRmDeployment** ottiene le distribuzioni in corrispondenza dell'ambito corrente della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="76d8c-108">The **Get-AzureRmDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="76d8c-109">Specificare il *nome* o il parametro *ID* per filtrare i risultati.</span><span class="sxs-lookup"><span data-stu-id="76d8c-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="76d8c-110">Per impostazione predefinita, **Get-AzureRmDeployment** ottiene tutte le distribuzioni nell'ambito corrente della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="76d8c-110">By default, **Get-AzureRmDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="76d8c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="76d8c-111">EXAMPLES</span></span>

### <span data-ttu-id="76d8c-112">Esempio 1: ottenere tutte le distribuzioni all'ambito dell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="76d8c-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzureRmDeployment
```

<span data-ttu-id="76d8c-113">Questo comando consente di ottenere tutte le distribuzioni nell'ambito corrente della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="76d8c-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="76d8c-114">Esempio 2: ottenere una distribuzione per nome</span><span class="sxs-lookup"><span data-stu-id="76d8c-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "DeployRoles01"
```

<span data-ttu-id="76d8c-115">Questo comando consente di ottenere la distribuzione di DeployRoles01 nell'ambito corrente della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="76d8c-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="76d8c-116">È possibile assegnare un nome a una distribuzione quando la si crea usando i cmdlet **New-AzureRmDeployment** .</span><span class="sxs-lookup"><span data-stu-id="76d8c-116">You can assign a name to a deployment when you create it by using the **New-AzureRmDeployment** cmdlets.</span></span>
<span data-ttu-id="76d8c-117">Se non si assegna un nome, i cmdlet prevedono un nome predefinito basato sul modello usato per creare la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="76d8c-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="76d8c-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="76d8c-118">PARAMETERS</span></span>

### <span data-ttu-id="76d8c-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="76d8c-119">-ApiVersion</span></span>
<span data-ttu-id="76d8c-120">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="76d8c-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="76d8c-121">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="76d8c-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="76d8c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76d8c-122">-DefaultProfile</span></span>
<span data-ttu-id="76d8c-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="76d8c-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76d8c-124">-ID</span><span class="sxs-lookup"><span data-stu-id="76d8c-124">-Id</span></span>
<span data-ttu-id="76d8c-125">ID risorsa completo della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="76d8c-125">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="76d8c-126">esempio:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="76d8c-126">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76d8c-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="76d8c-127">-Name</span></span>
<span data-ttu-id="76d8c-128">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="76d8c-128">The name of deployment.</span></span>

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

### <span data-ttu-id="76d8c-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="76d8c-129">-Pre</span></span>
<span data-ttu-id="76d8c-130">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="76d8c-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="76d8c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76d8c-131">CommonParameters</span></span>
<span data-ttu-id="76d8c-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76d8c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76d8c-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76d8c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76d8c-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="76d8c-134">INPUTS</span></span>

### <span data-ttu-id="76d8c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="76d8c-135">System.String</span></span>

## <span data-ttu-id="76d8c-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="76d8c-136">OUTPUTS</span></span>

### <span data-ttu-id="76d8c-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEPLOYMENT</span><span class="sxs-lookup"><span data-stu-id="76d8c-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="76d8c-138">Note</span><span class="sxs-lookup"><span data-stu-id="76d8c-138">NOTES</span></span>

## <span data-ttu-id="76d8c-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="76d8c-139">RELATED LINKS</span></span>
