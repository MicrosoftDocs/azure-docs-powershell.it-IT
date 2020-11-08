---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-aztenantdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
ms.openlocfilehash: dcee9317e6aad113088dc3498a337e16e61b6320
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203272"
---
# <span data-ttu-id="b65af-101">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="b65af-101">Save-AzTenantDeploymentTemplate</span></span>

## <span data-ttu-id="b65af-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b65af-102">SYNOPSIS</span></span>
<span data-ttu-id="b65af-103">Salva un modello di distribuzione in un file.</span><span class="sxs-lookup"><span data-stu-id="b65af-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="b65af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b65af-104">SYNTAX</span></span>

### <span data-ttu-id="b65af-105">SaveByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b65af-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b65af-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="b65af-106">SaveByDeploymentObject</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b65af-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b65af-107">DESCRIPTION</span></span>
<span data-ttu-id="b65af-108">Il cmdlet **Save-AzTenantDeploymentTemplate**  salva un modello di distribuzione in un file JSON per una distribuzione in ambito tenant.</span><span class="sxs-lookup"><span data-stu-id="b65af-108">The **Save-AzTenantDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at tenant scope.</span></span>

## <span data-ttu-id="b65af-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b65af-109">EXAMPLES</span></span>

### <span data-ttu-id="b65af-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b65af-110">Example 1</span></span>
```powershell
PS C:\> Save-AzTenantDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="b65af-111">Questo comando consente di ottenere il modello di distribuzione da TestDeployment e di salvarlo come file JSON nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="b65af-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="b65af-112">Esempio 2: ottenere una distribuzione e salvare il modello</span><span class="sxs-lookup"><span data-stu-id="b65af-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzTenantDeploymentTemplate -Name "RolesDeployment" | Save-AzTenantDeploymentTemplate
```

<span data-ttu-id="b65af-113">Questo comando consente di ottenere la distribuzione "RolesDeployment" nell'ambito del tenant corrente e di salvarne il modello.</span><span class="sxs-lookup"><span data-stu-id="b65af-113">This command gets the deployment "RolesDeployment" at the current tenant scope and saves its template.</span></span>

## <span data-ttu-id="b65af-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b65af-114">PARAMETERS</span></span>

### <span data-ttu-id="b65af-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b65af-115">-DefaultProfile</span></span>
<span data-ttu-id="b65af-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b65af-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b65af-117">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="b65af-117">-DeploymentName</span></span>
<span data-ttu-id="b65af-118">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="b65af-118">The deployment name.</span></span>

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

### <span data-ttu-id="b65af-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="b65af-119">-DeploymentObject</span></span>
<span data-ttu-id="b65af-120">Oggetto Deployment.</span><span class="sxs-lookup"><span data-stu-id="b65af-120">The deployment object.</span></span>

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

### <span data-ttu-id="b65af-121">-Force</span><span class="sxs-lookup"><span data-stu-id="b65af-121">-Force</span></span>
<span data-ttu-id="b65af-122">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="b65af-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b65af-123">-Path</span><span class="sxs-lookup"><span data-stu-id="b65af-123">-Path</span></span>
<span data-ttu-id="b65af-124">Percorso di output del file di modello.</span><span class="sxs-lookup"><span data-stu-id="b65af-124">The output path of the template file.</span></span>

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

### <span data-ttu-id="b65af-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="b65af-125">-Pre</span></span>
<span data-ttu-id="b65af-126">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="b65af-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="b65af-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b65af-127">-Confirm</span></span>
<span data-ttu-id="b65af-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b65af-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b65af-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b65af-129">-WhatIf</span></span>
<span data-ttu-id="b65af-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b65af-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b65af-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b65af-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b65af-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b65af-132">CommonParameters</span></span>
<span data-ttu-id="b65af-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b65af-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b65af-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b65af-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b65af-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b65af-135">INPUTS</span></span>

### <span data-ttu-id="b65af-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEPLOYMENT</span><span class="sxs-lookup"><span data-stu-id="b65af-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="b65af-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b65af-137">OUTPUTS</span></span>

### <span data-ttu-id="b65af-138">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="b65af-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="b65af-139">Note</span><span class="sxs-lookup"><span data-stu-id="b65af-139">NOTES</span></span>

## <span data-ttu-id="b65af-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b65af-140">RELATED LINKS</span></span>
