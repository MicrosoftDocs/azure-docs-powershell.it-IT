---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: b10d73e118b590a06c2af5a1755a59d219f9f180
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962110"
---
# <span data-ttu-id="cb2e2-101">Remove-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="cb2e2-101">Remove-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="cb2e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb2e2-102">SYNOPSIS</span></span>
<span data-ttu-id="cb2e2-103">Elimina l'origine dell'elemento specificata.</span><span class="sxs-lookup"><span data-stu-id="cb2e2-103">Deletes the specified artifact source.</span></span>

## <span data-ttu-id="cb2e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cb2e2-104">SYNTAX</span></span>

### <span data-ttu-id="cb2e2-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cb2e2-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb2e2-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb2e2-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb2e2-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="cb2e2-107">InputObject</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb2e2-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cb2e2-108">DESCRIPTION</span></span>
<span data-ttu-id="cb2e2-109">Il cmdlet **Remove-AzDeploymentManagerArtifactSource** elimina un'origine dell'elemento Specifica l'origine dell'elemento in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cb2e2-109">The **Remove-AzDeploymentManagerArtifactSource** cmdlet deletes an artifact source Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="cb2e2-110">In alternativa, è possibile fornire l'oggetto ArtifactSource o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="cb2e2-110">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="cb2e2-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cb2e2-111">EXAMPLES</span></span>

### <span data-ttu-id="cb2e2-112">Esempio 1: Eliminare un'origine dell'elemento</span><span class="sxs-lookup"><span data-stu-id="cb2e2-112">Example 1: Delete an artifact source</span></span>
### <span data-ttu-id="cb2e2-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cb2e2-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="cb2e2-114">Questo comando elimina un'origine dell'elemento denominata ContosoArtifactSource in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="cb2e2-114">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="cb2e2-115">Esempio 2: Eliminare un'origine dell'elemento usando l'identificatore di risorsa</span><span class="sxs-lookup"><span data-stu-id="cb2e2-115">Example 2: Delete an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="cb2e2-116">Questo comando elimina un'origine dell'elemento denominata ContosoArtifactSource in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="cb2e2-116">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="cb2e2-117">Esempio 3: Eliminare un'origine dell'elemento usando un oggetto</span><span class="sxs-lookup"><span data-stu-id="cb2e2-117">Example 3: Delete an artifact source using an object</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="cb2e2-118">Questo comando elimina un'origine dell'elemento il cui nome e gruppo di risorse corrispondono, rispettivamente, alle proprietà Name e ResourceGroupName $artifactSourceObject dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="cb2e2-118">This command deletes an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="cb2e2-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb2e2-119">PARAMETERS</span></span>

### <span data-ttu-id="cb2e2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb2e2-120">-DefaultProfile</span></span>
<span data-ttu-id="cb2e2-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cb2e2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb2e2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb2e2-122">-InputObject</span></span>
<span data-ttu-id="cb2e2-123">L'origine dell'elemento da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="cb2e2-123">The artifact source to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb2e2-124">-Name</span><span class="sxs-lookup"><span data-stu-id="cb2e2-124">-Name</span></span>
<span data-ttu-id="cb2e2-125">Nome dell'origine dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="cb2e2-125">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb2e2-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb2e2-126">-PassThru</span></span>
<span data-ttu-id="cb2e2-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="cb2e2-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="cb2e2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb2e2-128">-ResourceGroupName</span></span>
<span data-ttu-id="cb2e2-129">Gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cb2e2-129">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb2e2-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb2e2-130">-ResourceId</span></span>
<span data-ttu-id="cb2e2-131">L'identificatore di risorsa.</span><span class="sxs-lookup"><span data-stu-id="cb2e2-131">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb2e2-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb2e2-132">-Confirm</span></span>
<span data-ttu-id="cb2e2-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb2e2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb2e2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb2e2-134">-WhatIf</span></span>
<span data-ttu-id="cb2e2-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cb2e2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb2e2-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cb2e2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb2e2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb2e2-137">CommonParameters</span></span>
<span data-ttu-id="cb2e2-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb2e2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb2e2-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cb2e2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb2e2-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="cb2e2-140">INPUTS</span></span>

### <span data-ttu-id="cb2e2-141">System.String</span><span class="sxs-lookup"><span data-stu-id="cb2e2-141">System.String</span></span>

### <span data-ttu-id="cb2e2-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="cb2e2-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="cb2e2-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cb2e2-143">OUTPUTS</span></span>

### <span data-ttu-id="cb2e2-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cb2e2-144">System.Boolean</span></span>

## <span data-ttu-id="cb2e2-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="cb2e2-145">NOTES</span></span>

## <span data-ttu-id="cb2e2-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cb2e2-146">RELATED LINKS</span></span>
