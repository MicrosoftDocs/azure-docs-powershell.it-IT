---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azmanagementgroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
ms.openlocfilehash: 536d8f0d7f92e4ca880998293d74d0fc2f1617f1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188886"
---
# <span data-ttu-id="be654-101">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="be654-101">Save-AzManagementGroupDeploymentTemplate</span></span>

## <span data-ttu-id="be654-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="be654-102">SYNOPSIS</span></span>
<span data-ttu-id="be654-103">Salva un modello di distribuzione in un file.</span><span class="sxs-lookup"><span data-stu-id="be654-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="be654-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="be654-104">SYNTAX</span></span>

### <span data-ttu-id="be654-105">SaveByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="be654-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzManagementGroupDeploymentTemplate -ManagementGroupId <String> -DeploymentName <String> [-Path <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be654-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="be654-106">SaveByDeploymentObject</span></span>
```
Save-AzManagementGroupDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="be654-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be654-107">DESCRIPTION</span></span>
<span data-ttu-id="be654-108">Il cmdlet **Save-AzManagementGroupDeploymentTemplate**  salva un modello di distribuzione in un file JSON per una distribuzione in un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="be654-108">The **Save-AzManagementGroupDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at a management group.</span></span>

## <span data-ttu-id="be654-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="be654-109">EXAMPLES</span></span>

### <span data-ttu-id="be654-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="be654-110">Example 1</span></span>
```powershell
PS C:\> Save-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -DeploymentName "TestDeployment"
```

<span data-ttu-id="be654-111">Questo comando consente di ottenere il modello di distribuzione da TestDeployment e di salvarlo come file JSON nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="be654-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="be654-112">Esempio 2: ottenere una distribuzione e salvare il modello</span><span class="sxs-lookup"><span data-stu-id="be654-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -Name "RolesDeployment" | Save-AzManagementGroupDeploymentTemplate
```

<span data-ttu-id="be654-113">Questo comando ottiene la distribuzione "RolesDeployment" nel gruppo di gestione "myMG" e salva il modello.</span><span class="sxs-lookup"><span data-stu-id="be654-113">This command gets the deployment "RolesDeployment" at the management group "myMG" and saves its template.</span></span>

## <span data-ttu-id="be654-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="be654-114">PARAMETERS</span></span>

### <span data-ttu-id="be654-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="be654-115">-ApiVersion</span></span>
<span data-ttu-id="be654-116">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="be654-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="be654-117">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="be654-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="be654-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be654-118">-DefaultProfile</span></span>
<span data-ttu-id="be654-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="be654-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be654-120">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="be654-120">-DeploymentName</span></span>
<span data-ttu-id="be654-121">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="be654-121">The deployment name.</span></span>

```yaml
Type: String
Parameter Sets: SaveByDeploymentName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be654-122">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="be654-122">-DeploymentObject</span></span>
<span data-ttu-id="be654-123">Oggetto Deployment.</span><span class="sxs-lookup"><span data-stu-id="be654-123">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: SaveByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be654-124">-Force</span><span class="sxs-lookup"><span data-stu-id="be654-124">-Force</span></span>
<span data-ttu-id="be654-125">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="be654-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="be654-126">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="be654-126">-ManagementGroupId</span></span>
<span data-ttu-id="be654-127">ID gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="be654-127">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: SaveByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be654-128">-Path</span><span class="sxs-lookup"><span data-stu-id="be654-128">-Path</span></span>
<span data-ttu-id="be654-129">Percorso di output del file di modello.</span><span class="sxs-lookup"><span data-stu-id="be654-129">The output path of the template file.</span></span>

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

### <span data-ttu-id="be654-130">-Pre</span><span class="sxs-lookup"><span data-stu-id="be654-130">-Pre</span></span>
<span data-ttu-id="be654-131">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="be654-131">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="be654-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="be654-132">-Confirm</span></span>
<span data-ttu-id="be654-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be654-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be654-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be654-134">-WhatIf</span></span>
<span data-ttu-id="be654-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be654-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be654-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be654-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be654-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be654-137">CommonParameters</span></span>
<span data-ttu-id="be654-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be654-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be654-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be654-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be654-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="be654-140">INPUTS</span></span>

### <span data-ttu-id="be654-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEPLOYMENT</span><span class="sxs-lookup"><span data-stu-id="be654-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="be654-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="be654-142">OUTPUTS</span></span>

### <span data-ttu-id="be654-143">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="be654-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="be654-144">Note</span><span class="sxs-lookup"><span data-stu-id="be654-144">NOTES</span></span>

## <span data-ttu-id="be654-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="be654-145">RELATED LINKS</span></span>
