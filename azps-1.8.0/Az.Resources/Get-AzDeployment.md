---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
ms.openlocfilehash: cde9c4f8827840047e7fa4a1c597ed6338ed8e54
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677405"
---
# <span data-ttu-id="8c3ef-101">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="8c3ef-101">Get-AzDeployment</span></span>

## <span data-ttu-id="8c3ef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8c3ef-102">SYNOPSIS</span></span>
<span data-ttu-id="8c3ef-103">Ottenere la distribuzione</span><span class="sxs-lookup"><span data-stu-id="8c3ef-103">Get deployment</span></span>

## <span data-ttu-id="8c3ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8c3ef-104">SYNTAX</span></span>

### <span data-ttu-id="8c3ef-105">GetByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8c3ef-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8c3ef-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="8c3ef-106">GetByDeploymentId</span></span>
```
Get-AzDeployment [-Id <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8c3ef-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8c3ef-107">DESCRIPTION</span></span>
<span data-ttu-id="8c3ef-108">Il cmdlet **Get-AzDeployment** ottiene le distribuzioni in corrispondenza dell'ambito corrente della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="8c3ef-108">The **Get-AzDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="8c3ef-109">Specificare il *nome* o il parametro *ID* per filtrare i risultati.</span><span class="sxs-lookup"><span data-stu-id="8c3ef-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="8c3ef-110">Per impostazione predefinita, **Get-AzDeployment** ottiene tutte le distribuzioni nell'ambito corrente della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="8c3ef-110">By default, **Get-AzDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="8c3ef-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8c3ef-111">EXAMPLES</span></span>

### <span data-ttu-id="8c3ef-112">Esempio 1: ottenere tutte le distribuzioni all'ambito dell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="8c3ef-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzDeployment
```

<span data-ttu-id="8c3ef-113">Questo comando consente di ottenere tutte le distribuzioni nell'ambito corrente della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="8c3ef-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="8c3ef-114">Esempio 2: ottenere una distribuzione per nome</span><span class="sxs-lookup"><span data-stu-id="8c3ef-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "DeployRoles01"
```

<span data-ttu-id="8c3ef-115">Questo comando consente di ottenere la distribuzione di DeployRoles01 nell'ambito corrente della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="8c3ef-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="8c3ef-116">È possibile assegnare un nome a una distribuzione quando la si crea usando i cmdlet **New-AzDeployment** .</span><span class="sxs-lookup"><span data-stu-id="8c3ef-116">You can assign a name to a deployment when you create it by using the **New-AzDeployment** cmdlets.</span></span>
<span data-ttu-id="8c3ef-117">Se non si assegna un nome, i cmdlet prevedono un nome predefinito basato sul modello usato per creare la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="8c3ef-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="8c3ef-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8c3ef-118">PARAMETERS</span></span>

### <span data-ttu-id="8c3ef-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8c3ef-119">-ApiVersion</span></span>
<span data-ttu-id="8c3ef-120">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="8c3ef-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="8c3ef-121">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="8c3ef-121">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c3ef-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c3ef-122">-DefaultProfile</span></span>
<span data-ttu-id="8c3ef-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8c3ef-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c3ef-124">-ID</span><span class="sxs-lookup"><span data-stu-id="8c3ef-124">-Id</span></span>
<span data-ttu-id="8c3ef-125">ID risorsa completo della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="8c3ef-125">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="8c3ef-126">esempio:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="8c3ef-126">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c3ef-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="8c3ef-127">-Name</span></span>
<span data-ttu-id="8c3ef-128">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="8c3ef-128">The name of deployment.</span></span>

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

### <span data-ttu-id="8c3ef-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="8c3ef-129">-Pre</span></span>
<span data-ttu-id="8c3ef-130">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="8c3ef-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="8c3ef-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c3ef-131">CommonParameters</span></span>
<span data-ttu-id="8c3ef-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c3ef-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c3ef-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c3ef-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c3ef-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8c3ef-134">INPUTS</span></span>

### <span data-ttu-id="8c3ef-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8c3ef-135">None</span></span>

## <span data-ttu-id="8c3ef-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8c3ef-136">OUTPUTS</span></span>

### <span data-ttu-id="8c3ef-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEPLOYMENT</span><span class="sxs-lookup"><span data-stu-id="8c3ef-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="8c3ef-138">Note</span><span class="sxs-lookup"><span data-stu-id="8c3ef-138">NOTES</span></span>

## <span data-ttu-id="8c3ef-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8c3ef-139">RELATED LINKS</span></span>