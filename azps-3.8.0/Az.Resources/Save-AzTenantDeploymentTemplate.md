---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-aztenantdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzTenantDeploymentTemplate.md
ms.openlocfilehash: 79a60294126a990d191e4838a91c0f6554bea43b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019698"
---
# <span data-ttu-id="4abfd-101">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="4abfd-101">Save-AzTenantDeploymentTemplate</span></span>

## <span data-ttu-id="4abfd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4abfd-102">SYNOPSIS</span></span>
<span data-ttu-id="4abfd-103">Salva un modello di distribuzione in un file.</span><span class="sxs-lookup"><span data-stu-id="4abfd-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="4abfd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4abfd-104">SYNTAX</span></span>

### <span data-ttu-id="4abfd-105">SaveByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4abfd-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4abfd-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="4abfd-106">SaveByDeploymentObject</span></span>
```
Save-AzTenantDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4abfd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4abfd-107">DESCRIPTION</span></span>
<span data-ttu-id="4abfd-108">Il cmdlet **Save-AzTenantDeploymentTemplate**  salva un modello di distribuzione in un file JSON per una distribuzione in ambito tenant.</span><span class="sxs-lookup"><span data-stu-id="4abfd-108">The **Save-AzTenantDeploymentTemplate**  cmdlet saves a deployment template to a JSON file for a deployment at tenant scope.</span></span>

## <span data-ttu-id="4abfd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4abfd-109">EXAMPLES</span></span>

### <span data-ttu-id="4abfd-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4abfd-110">Example 1</span></span>
```powershell
PS C:\> Save-AzTenantDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="4abfd-111">Questo comando consente di ottenere il modello di distribuzione da TestDeployment e di salvarlo come file JSON nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="4abfd-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="4abfd-112">Esempio 2: ottenere una distribuzione e salvare il modello</span><span class="sxs-lookup"><span data-stu-id="4abfd-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzTenantDeploymentTemplate -Name "RolesDeployment" | Save-AzTenantDeploymentTemplate
```

<span data-ttu-id="4abfd-113">Questo comando consente di ottenere la distribuzione "RolesDeployment" nell'ambito del tenant corrente e di salvarne il modello.</span><span class="sxs-lookup"><span data-stu-id="4abfd-113">This command gets the deployment "RolesDeployment" at the current tenant scope and saves its template.</span></span>

## <span data-ttu-id="4abfd-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4abfd-114">PARAMETERS</span></span>

### <span data-ttu-id="4abfd-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4abfd-115">-ApiVersion</span></span>
<span data-ttu-id="4abfd-116">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="4abfd-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="4abfd-117">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="4abfd-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="4abfd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4abfd-118">-DefaultProfile</span></span>
<span data-ttu-id="4abfd-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4abfd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4abfd-120">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="4abfd-120">-DeploymentName</span></span>
<span data-ttu-id="4abfd-121">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="4abfd-121">The deployment name.</span></span>

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

### <span data-ttu-id="4abfd-122">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="4abfd-122">-DeploymentObject</span></span>
<span data-ttu-id="4abfd-123">Oggetto Deployment.</span><span class="sxs-lookup"><span data-stu-id="4abfd-123">The deployment object.</span></span>

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

### <span data-ttu-id="4abfd-124">-Force</span><span class="sxs-lookup"><span data-stu-id="4abfd-124">-Force</span></span>
<span data-ttu-id="4abfd-125">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="4abfd-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4abfd-126">-Path</span><span class="sxs-lookup"><span data-stu-id="4abfd-126">-Path</span></span>
<span data-ttu-id="4abfd-127">Percorso di output del file di modello.</span><span class="sxs-lookup"><span data-stu-id="4abfd-127">The output path of the template file.</span></span>

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

### <span data-ttu-id="4abfd-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="4abfd-128">-Pre</span></span>
<span data-ttu-id="4abfd-129">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="4abfd-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4abfd-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4abfd-130">-Confirm</span></span>
<span data-ttu-id="4abfd-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4abfd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4abfd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4abfd-132">-WhatIf</span></span>
<span data-ttu-id="4abfd-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4abfd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4abfd-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4abfd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4abfd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4abfd-135">CommonParameters</span></span>
<span data-ttu-id="4abfd-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4abfd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4abfd-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4abfd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4abfd-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4abfd-138">INPUTS</span></span>

### <span data-ttu-id="4abfd-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEPLOYMENT</span><span class="sxs-lookup"><span data-stu-id="4abfd-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="4abfd-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4abfd-140">OUTPUTS</span></span>

### <span data-ttu-id="4abfd-141">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSTemplatePath</span><span class="sxs-lookup"><span data-stu-id="4abfd-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplatePath</span></span>

## <span data-ttu-id="4abfd-142">Note</span><span class="sxs-lookup"><span data-stu-id="4abfd-142">NOTES</span></span>

## <span data-ttu-id="4abfd-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4abfd-143">RELATED LINKS</span></span>
