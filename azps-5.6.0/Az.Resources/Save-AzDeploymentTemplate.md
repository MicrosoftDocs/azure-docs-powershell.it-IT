---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/save-azdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
ms.openlocfilehash: 64ed7e109877912d7a74937e6bdf6707519aa1e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967662"
---
# <span data-ttu-id="144c0-101">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="144c0-101">Save-AzDeploymentTemplate</span></span>

## <span data-ttu-id="144c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="144c0-102">SYNOPSIS</span></span>
<span data-ttu-id="144c0-103">Salva un modello di distribuzione in un file.</span><span class="sxs-lookup"><span data-stu-id="144c0-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="144c0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="144c0-104">SYNTAX</span></span>

### <span data-ttu-id="144c0-105">SaveByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="144c0-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="144c0-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="144c0-106">SaveByDeploymentObject</span></span>
```
Save-AzDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="144c0-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="144c0-107">DESCRIPTION</span></span>
<span data-ttu-id="144c0-108">Il cmdlet **Save-AzDeploymentTemplate**  salva un modello di distribuzione in un file JSON.</span><span class="sxs-lookup"><span data-stu-id="144c0-108">The **Save-AzDeploymentTemplate**  cmdlet saves a deployment template to a JSON file.</span></span>

## <span data-ttu-id="144c0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="144c0-109">EXAMPLES</span></span>

### <span data-ttu-id="144c0-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="144c0-110">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="144c0-111">Questo comando recupera il modello di distribuzione da TestDeployment e lo salva come file JSON nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="144c0-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="144c0-112">Esempio 2: Ottenere una distribuzione e salvare il modello</span><span class="sxs-lookup"><span data-stu-id="144c0-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Save-AzDeploymentTemplate
```

<span data-ttu-id="144c0-113">Questo comando recupera la distribuzione "RolesDeployment" nell'ambito di sottoscrizione corrente e salva il modello.</span><span class="sxs-lookup"><span data-stu-id="144c0-113">This command gets the deployment "RolesDeployment" at the current subscription scope and saves its template.</span></span>

## <span data-ttu-id="144c0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="144c0-114">PARAMETERS</span></span>

### <span data-ttu-id="144c0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="144c0-115">-DefaultProfile</span></span>
<span data-ttu-id="144c0-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="144c0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="144c0-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="144c0-117">-DeploymentName</span></span>
<span data-ttu-id="144c0-118">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="144c0-118">The deployment name.</span></span>

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

### <span data-ttu-id="144c0-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="144c0-119">-DeploymentObject</span></span>
<span data-ttu-id="144c0-120">Oggetto di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="144c0-120">The deployment object.</span></span>

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

### <span data-ttu-id="144c0-121">-Force</span><span class="sxs-lookup"><span data-stu-id="144c0-121">-Force</span></span>
<span data-ttu-id="144c0-122">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="144c0-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="144c0-123">-Path</span><span class="sxs-lookup"><span data-stu-id="144c0-123">-Path</span></span>
<span data-ttu-id="144c0-124">Percorso di output del file modello.</span><span class="sxs-lookup"><span data-stu-id="144c0-124">The output path of the template file.</span></span>

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

### <span data-ttu-id="144c0-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="144c0-125">-Pre</span></span>
<span data-ttu-id="144c0-126">Se impostato, indica che il cmdlet deve usare versioni delle API non beta per determinare automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="144c0-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="144c0-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="144c0-127">-Confirm</span></span>
<span data-ttu-id="144c0-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="144c0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="144c0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="144c0-129">-WhatIf</span></span>
<span data-ttu-id="144c0-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="144c0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="144c0-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="144c0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="144c0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="144c0-132">CommonParameters</span></span>
<span data-ttu-id="144c0-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="144c0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="144c0-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="144c0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="144c0-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="144c0-135">INPUTS</span></span>

### <span data-ttu-id="144c0-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="144c0-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="144c0-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="144c0-137">OUTPUTS</span></span>

### <span data-ttu-id="144c0-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="144c0-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="144c0-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="144c0-139">NOTES</span></span>

## <span data-ttu-id="144c0-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="144c0-140">RELATED LINKS</span></span>
