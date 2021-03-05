---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
ms.openlocfilehash: 92a0aac5043be520f6a7ed7afc2066e0532b79ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960125"
---
# <span data-ttu-id="a3698-101">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="a3698-101">Get-AzDeployment</span></span>

## <span data-ttu-id="a3698-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3698-102">SYNOPSIS</span></span>
<span data-ttu-id="a3698-103">Ottenere la distribuzione</span><span class="sxs-lookup"><span data-stu-id="a3698-103">Get deployment</span></span>

## <span data-ttu-id="a3698-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a3698-104">SYNTAX</span></span>

### <span data-ttu-id="a3698-105">GetByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a3698-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a3698-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="a3698-106">GetByDeploymentId</span></span>
```
Get-AzDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3698-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a3698-107">DESCRIPTION</span></span>
<span data-ttu-id="a3698-108">Il cmdlet **Get-AzDeployment** ottiene le distribuzioni nell'ambito di sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="a3698-108">The **Get-AzDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="a3698-109">Specificare il *parametro Name* o *Id* per filtrare i risultati.</span><span class="sxs-lookup"><span data-stu-id="a3698-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="a3698-110">Per impostazione predefinita, **Get-AzDeployment** ottiene tutte le distribuzioni nell'ambito di sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="a3698-110">By default, **Get-AzDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="a3698-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a3698-111">EXAMPLES</span></span>

### <span data-ttu-id="a3698-112">Esempio 1: Ottenere tutte le distribuzioni nell'ambito di sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="a3698-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzDeployment
```

<span data-ttu-id="a3698-113">Questo comando recupera tutte le distribuzioni con l'ambito di sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="a3698-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="a3698-114">Esempio 2: Ottenere una distribuzione in base al nome</span><span class="sxs-lookup"><span data-stu-id="a3698-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "DeployRoles01"
```

<span data-ttu-id="a3698-115">Questo comando ottiene la distribuzione DeployRoles01 nell'ambito della sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="a3698-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="a3698-116">È possibile assegnare un nome a una distribuzione quando viene creata usando i cmdlet **New-AzDeployment.**</span><span class="sxs-lookup"><span data-stu-id="a3698-116">You can assign a name to a deployment when you create it by using the **New-AzDeployment** cmdlets.</span></span>
<span data-ttu-id="a3698-117">Se non si assegna un nome, i cmdlet forniscono un nome predefinito basato sul modello usato per creare la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="a3698-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="a3698-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3698-118">PARAMETERS</span></span>

### <span data-ttu-id="a3698-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3698-119">-DefaultProfile</span></span>
<span data-ttu-id="a3698-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a3698-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3698-121">-Id</span><span class="sxs-lookup"><span data-stu-id="a3698-121">-Id</span></span>
<span data-ttu-id="a3698-122">ID di risorsa completo della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="a3698-122">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="a3698-123">Esempio: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="a3698-123">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="a3698-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a3698-124">-Name</span></span>
<span data-ttu-id="a3698-125">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="a3698-125">The name of deployment.</span></span>

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

### <span data-ttu-id="a3698-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="a3698-126">-Pre</span></span>
<span data-ttu-id="a3698-127">Se impostato, indica che il cmdlet deve usare versioni delle API non definitiva per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="a3698-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a3698-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3698-128">CommonParameters</span></span>
<span data-ttu-id="a3698-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3698-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3698-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a3698-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3698-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="a3698-131">INPUTS</span></span>

### <span data-ttu-id="a3698-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a3698-132">None</span></span>

## <span data-ttu-id="a3698-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a3698-133">OUTPUTS</span></span>

### <span data-ttu-id="a3698-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="a3698-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="a3698-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="a3698-135">NOTES</span></span>

## <span data-ttu-id="a3698-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a3698-136">RELATED LINKS</span></span>
