---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azmanagementgroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
ms.openlocfilehash: f45602ad2515a90e39e45edb80ca1cb0bf051f00
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201822"
---
# <span data-ttu-id="1c123-101">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="1c123-101">Save-AzManagementGroupDeploymentTemplate</span></span>

## <span data-ttu-id="1c123-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c123-102">SYNOPSIS</span></span>
<span data-ttu-id="1c123-103">Salva un modello di distribuzione in un file.</span><span class="sxs-lookup"><span data-stu-id="1c123-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="1c123-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c123-104">SYNTAX</span></span>

### <span data-ttu-id="1c123-105">SaveByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1c123-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzManagementGroupDeploymentTemplate -ManagementGroupId <String> -DeploymentName <String> [-Path <String>]
 [-Force] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c123-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="1c123-106">SaveByDeploymentObject</span></span>
```
Save-AzManagementGroupDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c123-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1c123-107">DESCRIPTION</span></span>
<span data-ttu-id="1c123-108">Il cmdlet **Save-AzManagementGroupDeploymentTemplate**  salva un modello di distribuzione in un file JSON per una distribuzione in un gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="1c123-108">The **Save-AzManagementGroupDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at a management group.</span></span>

## <span data-ttu-id="1c123-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c123-109">EXAMPLES</span></span>

### <span data-ttu-id="1c123-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1c123-110">Example 1</span></span>
```powershell
PS C:\> Save-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -DeploymentName "TestDeployment"
```

<span data-ttu-id="1c123-111">Questo comando recupera il modello di distribuzione da TestDeployment e lo salva come file JSON nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="1c123-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="1c123-112">Esempio 2: Ottenere una distribuzione e salvare il modello</span><span class="sxs-lookup"><span data-stu-id="1c123-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -Name "RolesDeployment" | Save-AzManagementGroupDeploymentTemplate
```

<span data-ttu-id="1c123-113">Questo comando recupera la distribuzione "RolesDeployment" nel gruppo di gestione "myMG" e salva il modello.</span><span class="sxs-lookup"><span data-stu-id="1c123-113">This command gets the deployment "RolesDeployment" at the management group "myMG" and saves its template.</span></span>

## <span data-ttu-id="1c123-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c123-114">PARAMETERS</span></span>

### <span data-ttu-id="1c123-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c123-115">-DefaultProfile</span></span>
<span data-ttu-id="1c123-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1c123-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c123-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="1c123-117">-DeploymentName</span></span>
<span data-ttu-id="1c123-118">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="1c123-118">The deployment name.</span></span>

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

### <span data-ttu-id="1c123-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="1c123-119">-DeploymentObject</span></span>
<span data-ttu-id="1c123-120">Oggetto di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="1c123-120">The deployment object.</span></span>

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

### <span data-ttu-id="1c123-121">-Force</span><span class="sxs-lookup"><span data-stu-id="1c123-121">-Force</span></span>
<span data-ttu-id="1c123-122">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="1c123-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1c123-123">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="1c123-123">-ManagementGroupId</span></span>
<span data-ttu-id="1c123-124">ID del gruppo di gestione.</span><span class="sxs-lookup"><span data-stu-id="1c123-124">The management group id.</span></span>

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

### <span data-ttu-id="1c123-125">-Path</span><span class="sxs-lookup"><span data-stu-id="1c123-125">-Path</span></span>
<span data-ttu-id="1c123-126">Percorso di output del file modello.</span><span class="sxs-lookup"><span data-stu-id="1c123-126">The output path of the template file.</span></span>

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

### <span data-ttu-id="1c123-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="1c123-127">-Pre</span></span>
<span data-ttu-id="1c123-128">Se impostato, indica che il cmdlet deve usare versioni delle API non beta per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="1c123-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1c123-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c123-129">-Confirm</span></span>
<span data-ttu-id="1c123-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c123-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c123-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c123-131">-WhatIf</span></span>
<span data-ttu-id="1c123-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c123-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c123-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c123-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c123-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c123-134">CommonParameters</span></span>
<span data-ttu-id="1c123-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c123-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c123-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1c123-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c123-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="1c123-137">INPUTS</span></span>

### <span data-ttu-id="1c123-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="1c123-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="1c123-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c123-139">OUTPUTS</span></span>

### <span data-ttu-id="1c123-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="1c123-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="1c123-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="1c123-141">NOTES</span></span>

## <span data-ttu-id="1c123-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c123-142">RELATED LINKS</span></span>
