---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
ms.openlocfilehash: 813291fd0014665958dbee85be36060801b3e569
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976462"
---
# <span data-ttu-id="32ba4-101">Remove-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="32ba4-101">Remove-AzDeploymentScript</span></span>

## <span data-ttu-id="32ba4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32ba4-102">SYNOPSIS</span></span>
<span data-ttu-id="32ba4-103">Rimuove uno script di distribuzione e le risorse associate.</span><span class="sxs-lookup"><span data-stu-id="32ba4-103">Removes a deployment script and its associated resources.</span></span>


## <span data-ttu-id="32ba4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32ba4-104">SYNTAX</span></span>

### <span data-ttu-id="32ba4-105">RemoveDeploymentScriptLogByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="32ba4-105">RemoveDeploymentScriptLogByName (Default)</span></span>
```
Remove-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32ba4-106">RemoveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="32ba4-106">RemoveDeploymentScriptLogByResourceId</span></span>
```
Remove-AzDeploymentScript [-Id] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32ba4-107">RemoveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="32ba4-107">RemoveDeploymentScriptLogByInputObject</span></span>
```
Remove-AzDeploymentScript [-InputObject] <PsDeploymentScript> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32ba4-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="32ba4-108">DESCRIPTION</span></span>
<span data-ttu-id="32ba4-109">Il cmdlet **Remove-AzDeploymentScript** rimuove uno script di distribuzione e le risorse associate.</span><span class="sxs-lookup"><span data-stu-id="32ba4-109">The **Remove-AzDeploymentScript** cmdlet removes a deployment script and its associated resources.</span></span>

## <span data-ttu-id="32ba4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32ba4-110">EXAMPLES</span></span>

### <span data-ttu-id="32ba4-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="32ba4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="32ba4-112">Elimina uno script di distribuzione con il nome MyDeploymentScript nel gruppo di risorse DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="32ba4-112">Deletes a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

## <span data-ttu-id="32ba4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32ba4-113">PARAMETERS</span></span>

### <span data-ttu-id="32ba4-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32ba4-114">-Confirm</span></span>
<span data-ttu-id="32ba4-115">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32ba4-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32ba4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32ba4-116">-DefaultProfile</span></span>
<span data-ttu-id="32ba4-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="32ba4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32ba4-118">-Id</span><span class="sxs-lookup"><span data-stu-id="32ba4-118">-Id</span></span>
<span data-ttu-id="32ba4-119">ID di risorsa completo dello script di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="32ba4-119">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="32ba4-120">Esempio: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="32ba4-120">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByResourceId
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32ba4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32ba4-121">-InputObject</span></span>
<span data-ttu-id="32ba4-122">Oggetto PowerShell dello script di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="32ba4-122">The deployment script PowerShell object.</span></span>

```yaml
Type: PsDeploymentScript
Parameter Sets: RemoveDeploymentScriptLogByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32ba4-123">-Name</span><span class="sxs-lookup"><span data-stu-id="32ba4-123">-Name</span></span>
<span data-ttu-id="32ba4-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="32ba4-124">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32ba4-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32ba4-125">-PassThru</span></span>
<span data-ttu-id="32ba4-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="32ba4-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="32ba4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32ba4-127">-ResourceGroupName</span></span>
<span data-ttu-id="32ba4-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="32ba4-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32ba4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32ba4-129">-WhatIf</span></span>
<span data-ttu-id="32ba4-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32ba4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32ba4-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32ba4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32ba4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32ba4-132">CommonParameters</span></span>
<span data-ttu-id="32ba4-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32ba4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="32ba4-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32ba4-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32ba4-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="32ba4-135">INPUTS</span></span>

### <span data-ttu-id="32ba4-136">System.String</span><span class="sxs-lookup"><span data-stu-id="32ba4-136">System.String</span></span>

### <span data-ttu-id="32ba4-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="32ba4-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="32ba4-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32ba4-138">OUTPUTS</span></span>

### <span data-ttu-id="32ba4-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="32ba4-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="32ba4-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="32ba4-140">NOTES</span></span>

## <span data-ttu-id="32ba4-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32ba4-141">RELATED LINKS</span></span>