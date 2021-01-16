---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azmanagementgroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
ms.openlocfilehash: f45602ad2515a90e39e45edb80ca1cb0bf051f00
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382549"
---
# <span data-ttu-id="a9661-101">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="a9661-101">Save-AzManagementGroupDeploymentTemplate</span></span>

## <span data-ttu-id="a9661-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a9661-102">SYNOPSIS</span></span>
<span data-ttu-id="a9661-103">Salva un modello di distribuzione in un file.</span><span class="sxs-lookup"><span data-stu-id="a9661-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="a9661-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a9661-104">SYNTAX</span></span>

### <span data-ttu-id="a9661-105">SaveByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a9661-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzManagementGroupDeploymentTemplate -ManagementGroupId <String> -DeploymentName <String> [-Path <String>]
 [-Force] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9661-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="a9661-106">SaveByDeploymentObject</span></span>
```
Save-AzManagementGroupDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9661-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9661-107">DESCRIPTION</span></span>
<span data-ttu-id="a9661-108">Il cmdlet **Save-AzManagementGroupDeploymentTemplate**  salva un modello di distribuzione in un file JSON per una distribuzione in un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="a9661-108">The **Save-AzManagementGroupDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at a management group.</span></span>

## <span data-ttu-id="a9661-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a9661-109">EXAMPLES</span></span>

### <span data-ttu-id="a9661-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a9661-110">Example 1</span></span>
```powershell
PS C:\> Save-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -DeploymentName "TestDeployment"
```

<span data-ttu-id="a9661-111">Questo comando consente di ottenere il modello di distribuzione da TestDeployment e di salvarlo come file JSON nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="a9661-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="a9661-112">Esempio 2: ottenere una distribuzione e salvare il modello</span><span class="sxs-lookup"><span data-stu-id="a9661-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -Name "RolesDeployment" | Save-AzManagementGroupDeploymentTemplate
```

<span data-ttu-id="a9661-113">Questo comando ottiene la distribuzione "RolesDeployment" nel gruppo di gestione "myMG" e salva il modello.</span><span class="sxs-lookup"><span data-stu-id="a9661-113">This command gets the deployment "RolesDeployment" at the management group "myMG" and saves its template.</span></span>

## <span data-ttu-id="a9661-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a9661-114">PARAMETERS</span></span>

### <span data-ttu-id="a9661-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9661-115">-DefaultProfile</span></span>
<span data-ttu-id="a9661-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a9661-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9661-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="a9661-117">-DeploymentName</span></span>
<span data-ttu-id="a9661-118">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="a9661-118">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveByDeploymentName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9661-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="a9661-119">-DeploymentObject</span></span>
<span data-ttu-id="a9661-120">Oggetto Deployment.</span><span class="sxs-lookup"><span data-stu-id="a9661-120">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: SaveByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9661-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a9661-121">-Force</span></span>
<span data-ttu-id="a9661-122">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="a9661-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a9661-123">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="a9661-123">-ManagementGroupId</span></span>
<span data-ttu-id="a9661-124">ID gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="a9661-124">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9661-125">-Path</span><span class="sxs-lookup"><span data-stu-id="a9661-125">-Path</span></span>
<span data-ttu-id="a9661-126">Percorso di output del file di modello.</span><span class="sxs-lookup"><span data-stu-id="a9661-126">The output path of the template file.</span></span>

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

### <span data-ttu-id="a9661-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="a9661-127">-Pre</span></span>
<span data-ttu-id="a9661-128">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="a9661-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a9661-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a9661-129">-Confirm</span></span>
<span data-ttu-id="a9661-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9661-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9661-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9661-131">-WhatIf</span></span>
<span data-ttu-id="a9661-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a9661-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9661-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a9661-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9661-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9661-134">CommonParameters</span></span>
<span data-ttu-id="a9661-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9661-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9661-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9661-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9661-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a9661-137">INPUTS</span></span>

### <span data-ttu-id="a9661-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEPLOYMENT</span><span class="sxs-lookup"><span data-stu-id="a9661-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="a9661-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a9661-139">OUTPUTS</span></span>

### <span data-ttu-id="a9661-140">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="a9661-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="a9661-141">Note</span><span class="sxs-lookup"><span data-stu-id="a9661-141">NOTES</span></span>

## <span data-ttu-id="a9661-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a9661-142">RELATED LINKS</span></span>
