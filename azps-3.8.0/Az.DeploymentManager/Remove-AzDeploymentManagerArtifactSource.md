---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: fa9dc4f8234e9c6e709d59f3945b05eeceef4316
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022362"
---
# <span data-ttu-id="fdf04-101">Remove-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="fdf04-101">Remove-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="fdf04-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fdf04-102">SYNOPSIS</span></span>
<span data-ttu-id="fdf04-103">Elimina l'origine dell'elemento specificata.</span><span class="sxs-lookup"><span data-stu-id="fdf04-103">Deletes the specified artifact source.</span></span>

## <span data-ttu-id="fdf04-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fdf04-104">SYNTAX</span></span>

### <span data-ttu-id="fdf04-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fdf04-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdf04-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="fdf04-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdf04-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="fdf04-107">InputObject</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdf04-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fdf04-108">DESCRIPTION</span></span>
<span data-ttu-id="fdf04-109">Il cmdlet **Remove-AzDeploymentManagerArtifactSource** Elimina un'origine dell'elemento specificando l'origine dell'elemento in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fdf04-109">The **Remove-AzDeploymentManagerArtifactSource** cmdlet deletes an artifact source Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="fdf04-110">In alternativa, puoi specificare l'oggetto ArtifactSource o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="fdf04-110">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="fdf04-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fdf04-111">EXAMPLES</span></span>

### <span data-ttu-id="fdf04-112">Esempio 1: eliminare un'origine di un elemento</span><span class="sxs-lookup"><span data-stu-id="fdf04-112">Example 1: Delete an artifact source</span></span>
### <span data-ttu-id="fdf04-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fdf04-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="fdf04-114">Questo comando Elimina un'origine di elementi denominata ContosoArtifactSource in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fdf04-114">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="fdf04-115">Esempio 2: eliminare un'origine di un elemento usando l'identificatore delle risorse</span><span class="sxs-lookup"><span data-stu-id="fdf04-115">Example 2: Delete an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="fdf04-116">Questo comando Elimina un'origine di elementi denominata ContosoArtifactSource in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="fdf04-116">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="fdf04-117">Esempio 3: eliminare un'origine di un elemento usando un oggetto</span><span class="sxs-lookup"><span data-stu-id="fdf04-117">Example 3: Delete an artifact source using an object</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="fdf04-118">Questo comando Elimina un'origine di elementi il cui nome e ResourceGroup corrispondono rispettivamente alle proprietà Name e ResourceGroupName della $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="fdf04-118">This command deletes an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="fdf04-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fdf04-119">PARAMETERS</span></span>

### <span data-ttu-id="fdf04-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdf04-120">-DefaultProfile</span></span>
<span data-ttu-id="fdf04-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fdf04-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdf04-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdf04-122">-InputObject</span></span>
<span data-ttu-id="fdf04-123">Origine dell'elemento da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="fdf04-123">The artifact source to be removed.</span></span>

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

### <span data-ttu-id="fdf04-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="fdf04-124">-Name</span></span>
<span data-ttu-id="fdf04-125">Nome dell'origine dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="fdf04-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="fdf04-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fdf04-126">-PassThru</span></span>
<span data-ttu-id="fdf04-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="fdf04-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="fdf04-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdf04-128">-ResourceGroupName</span></span>
<span data-ttu-id="fdf04-129">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="fdf04-129">The resource group.</span></span>

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

### <span data-ttu-id="fdf04-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fdf04-130">-ResourceId</span></span>
<span data-ttu-id="fdf04-131">Identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="fdf04-131">The resource identifier.</span></span>

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

### <span data-ttu-id="fdf04-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fdf04-132">-Confirm</span></span>
<span data-ttu-id="fdf04-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdf04-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdf04-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdf04-134">-WhatIf</span></span>
<span data-ttu-id="fdf04-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fdf04-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdf04-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fdf04-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdf04-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdf04-137">CommonParameters</span></span>
<span data-ttu-id="fdf04-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdf04-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdf04-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fdf04-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdf04-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fdf04-140">INPUTS</span></span>

### <span data-ttu-id="fdf04-141">System. String</span><span class="sxs-lookup"><span data-stu-id="fdf04-141">System.String</span></span>

### <span data-ttu-id="fdf04-142">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="fdf04-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="fdf04-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fdf04-143">OUTPUTS</span></span>

### <span data-ttu-id="fdf04-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fdf04-144">System.Boolean</span></span>

## <span data-ttu-id="fdf04-145">Note</span><span class="sxs-lookup"><span data-stu-id="fdf04-145">NOTES</span></span>

## <span data-ttu-id="fdf04-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fdf04-146">RELATED LINKS</span></span>
