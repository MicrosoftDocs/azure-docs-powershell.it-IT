---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
ms.openlocfilehash: 75ebbe0eedd9aad396500701d5e94efff76069f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325399"
---
# <span data-ttu-id="4d2ed-101">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="4d2ed-101">Get-AzDeployment</span></span>

## <span data-ttu-id="4d2ed-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4d2ed-102">SYNOPSIS</span></span>
<span data-ttu-id="4d2ed-103">Ottenere la distribuzione</span><span class="sxs-lookup"><span data-stu-id="4d2ed-103">Get deployment</span></span>

## <span data-ttu-id="4d2ed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d2ed-104">SYNTAX</span></span>

### <span data-ttu-id="4d2ed-105">GetByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4d2ed-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d2ed-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="4d2ed-106">GetByDeploymentId</span></span>
```
Get-AzDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d2ed-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d2ed-107">DESCRIPTION</span></span>
<span data-ttu-id="4d2ed-108">Il cmdlet **Get-AzDeployment** ottiene le distribuzioni in corrispondenza dell'ambito corrente della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="4d2ed-108">The **Get-AzDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="4d2ed-109">Specificare il *nome* o il parametro *ID* per filtrare i risultati.</span><span class="sxs-lookup"><span data-stu-id="4d2ed-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="4d2ed-110">Per impostazione predefinita, **Get-AzDeployment** ottiene tutte le distribuzioni nell'ambito corrente della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="4d2ed-110">By default, **Get-AzDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="4d2ed-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d2ed-111">EXAMPLES</span></span>

### <span data-ttu-id="4d2ed-112">Esempio 1: ottenere tutte le distribuzioni all'ambito dell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="4d2ed-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzDeployment
```

<span data-ttu-id="4d2ed-113">Questo comando consente di ottenere tutte le distribuzioni nell'ambito corrente della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="4d2ed-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="4d2ed-114">Esempio 2: ottenere una distribuzione per nome</span><span class="sxs-lookup"><span data-stu-id="4d2ed-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "DeployRoles01"
```

<span data-ttu-id="4d2ed-115">Questo comando consente di ottenere la distribuzione di DeployRoles01 nell'ambito corrente della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="4d2ed-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="4d2ed-116">È possibile assegnare un nome a una distribuzione quando la si crea usando i cmdlet **New-AzDeployment** .</span><span class="sxs-lookup"><span data-stu-id="4d2ed-116">You can assign a name to a deployment when you create it by using the **New-AzDeployment** cmdlets.</span></span>
<span data-ttu-id="4d2ed-117">Se non si assegna un nome, i cmdlet prevedono un nome predefinito basato sul modello usato per creare la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="4d2ed-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="4d2ed-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4d2ed-118">PARAMETERS</span></span>

### <span data-ttu-id="4d2ed-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d2ed-119">-DefaultProfile</span></span>
<span data-ttu-id="4d2ed-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4d2ed-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d2ed-121">-ID</span><span class="sxs-lookup"><span data-stu-id="4d2ed-121">-Id</span></span>
<span data-ttu-id="4d2ed-122">ID risorsa completo della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="4d2ed-122">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="4d2ed-123">esempio:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="4d2ed-123">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="4d2ed-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="4d2ed-124">-Name</span></span>
<span data-ttu-id="4d2ed-125">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="4d2ed-125">The name of deployment.</span></span>

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

### <span data-ttu-id="4d2ed-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="4d2ed-126">-Pre</span></span>
<span data-ttu-id="4d2ed-127">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="4d2ed-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4d2ed-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d2ed-128">CommonParameters</span></span>
<span data-ttu-id="4d2ed-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d2ed-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d2ed-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d2ed-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d2ed-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4d2ed-131">INPUTS</span></span>

### <span data-ttu-id="4d2ed-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4d2ed-132">None</span></span>

## <span data-ttu-id="4d2ed-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d2ed-133">OUTPUTS</span></span>

### <span data-ttu-id="4d2ed-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEPLOYMENT</span><span class="sxs-lookup"><span data-stu-id="4d2ed-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="4d2ed-135">Note</span><span class="sxs-lookup"><span data-stu-id="4d2ed-135">NOTES</span></span>

## <span data-ttu-id="4d2ed-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d2ed-136">RELATED LINKS</span></span>
