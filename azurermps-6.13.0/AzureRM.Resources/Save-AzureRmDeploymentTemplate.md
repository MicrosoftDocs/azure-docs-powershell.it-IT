---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/save-azurermdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmDeploymentTemplate.md
ms.openlocfilehash: ed9309599b83079858d02fddeffe7dad4b3bb2dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520865"
---
# <span data-ttu-id="d229a-101">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="d229a-101">Save-AzureRmDeploymentTemplate</span></span>

## <span data-ttu-id="d229a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d229a-102">SYNOPSIS</span></span>
<span data-ttu-id="d229a-103">Salva un modello di distribuzione in un file.</span><span class="sxs-lookup"><span data-stu-id="d229a-103">Saves a deployment template to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d229a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d229a-104">SYNTAX</span></span>

### <span data-ttu-id="d229a-105">SaveByDeploymentName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d229a-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzureRmDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d229a-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="d229a-106">SaveByDeploymentObject</span></span>
```
Save-AzureRmDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d229a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d229a-107">DESCRIPTION</span></span>
<span data-ttu-id="d229a-108">Il cmdlet **Save-AzureRmDeploymentTemplate**  salva un modello di distribuzione in un file JSON.</span><span class="sxs-lookup"><span data-stu-id="d229a-108">The **Save-AzureRmDeploymentTemplate**  cmdlet saves a deployment template to a JSON file.</span></span>

## <span data-ttu-id="d229a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d229a-109">EXAMPLES</span></span>

### <span data-ttu-id="d229a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d229a-110">Example 1</span></span>
```powershell
PS C:\> Save-AzureRmDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="d229a-111">Questo comando consente di ottenere il modello di distribuzione da TestDeployment e di salvarlo come file JSON nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="d229a-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="d229a-112">Esempio 2: ottenere una distribuzione e salvare il modello</span><span class="sxs-lookup"><span data-stu-id="d229a-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "RolesDeployment" | Save-AzureRmDeploymentTemplate
```

<span data-ttu-id="d229a-113">Questo comando ottiene la distribuzione "RolesDeployment" nell'ambito corrente della sottoscrizione e salva il modello.</span><span class="sxs-lookup"><span data-stu-id="d229a-113">This command gets the deployment "RolesDeployment" at the current subscription scope and saves its template.</span></span>

## <span data-ttu-id="d229a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d229a-114">PARAMETERS</span></span>

### <span data-ttu-id="d229a-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d229a-115">-ApiVersion</span></span>
<span data-ttu-id="d229a-116">Quando è impostato, indica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="d229a-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="d229a-117">Se non viene specificato, la versione dell'API viene determinata automaticamente come l'ultima disponibile.</span><span class="sxs-lookup"><span data-stu-id="d229a-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="d229a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d229a-118">-DefaultProfile</span></span>
<span data-ttu-id="d229a-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d229a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d229a-120">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="d229a-120">-DeploymentName</span></span>
<span data-ttu-id="d229a-121">Nome della distribuzione.</span><span class="sxs-lookup"><span data-stu-id="d229a-121">The deployment name.</span></span>

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

### <span data-ttu-id="d229a-122">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="d229a-122">-DeploymentObject</span></span>
<span data-ttu-id="d229a-123">Oggetto Deployment.</span><span class="sxs-lookup"><span data-stu-id="d229a-123">The deployment object.</span></span>

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

### <span data-ttu-id="d229a-124">-Force</span><span class="sxs-lookup"><span data-stu-id="d229a-124">-Force</span></span>
<span data-ttu-id="d229a-125">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="d229a-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d229a-126">-Path</span><span class="sxs-lookup"><span data-stu-id="d229a-126">-Path</span></span>
<span data-ttu-id="d229a-127">Percorso di output del file di modello.</span><span class="sxs-lookup"><span data-stu-id="d229a-127">The output path of the template file.</span></span>

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

### <span data-ttu-id="d229a-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="d229a-128">-Pre</span></span>
<span data-ttu-id="d229a-129">Quando è impostato, indica che il cmdlet deve usare le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="d229a-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d229a-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d229a-130">-Confirm</span></span>
<span data-ttu-id="d229a-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d229a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d229a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d229a-132">-WhatIf</span></span>
<span data-ttu-id="d229a-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d229a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d229a-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d229a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d229a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d229a-135">CommonParameters</span></span>
<span data-ttu-id="d229a-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d229a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d229a-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d229a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d229a-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d229a-138">INPUTS</span></span>

### <span data-ttu-id="d229a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d229a-139">System.String</span></span>

## <span data-ttu-id="d229a-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d229a-140">OUTPUTS</span></span>

### <span data-ttu-id="d229a-141">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels</span><span class="sxs-lookup"><span data-stu-id="d229a-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels</span></span>

## <span data-ttu-id="d229a-142">Note</span><span class="sxs-lookup"><span data-stu-id="d229a-142">NOTES</span></span>

## <span data-ttu-id="d229a-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d229a-143">RELATED LINKS</span></span>
