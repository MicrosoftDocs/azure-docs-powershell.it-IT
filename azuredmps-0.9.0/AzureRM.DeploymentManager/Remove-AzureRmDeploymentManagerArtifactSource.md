---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: 7473f125511995efb1f6273d3b8adb675a58d06d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490849"
---
# <span data-ttu-id="a396b-101">Remove-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="a396b-101">Remove-AzureRmDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="a396b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a396b-102">SYNOPSIS</span></span>
<span data-ttu-id="a396b-103">Elimina un'origine di elementi.</span><span class="sxs-lookup"><span data-stu-id="a396b-103">Deletes an artifact source.</span></span>

## <span data-ttu-id="a396b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a396b-104">SYNTAX</span></span>

### <span data-ttu-id="a396b-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a396b-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a396b-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="a396b-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerArtifactSource [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a396b-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="a396b-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerArtifactSource [-ArtifactSource] <PSArtifactSource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a396b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a396b-108">DESCRIPTION</span></span>
<span data-ttu-id="a396b-109">Il cmdlet **Remove-AzureRmDeploymentManagerArtifactSource** Elimina un'origine dell'elemento specificando l'origine dell'elemento in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a396b-109">The **Remove-AzureRmDeploymentManagerArtifactSource** cmdlet deletes an artifact source Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="a396b-110">In alternativa, puoi specificare l'oggetto ArtifactSource o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="a396b-110">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="a396b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a396b-111">EXAMPLES</span></span>

### <span data-ttu-id="a396b-112">Esempio 1: eliminare un'origine di un elemento</span><span class="sxs-lookup"><span data-stu-id="a396b-112">Example 1: Delete an artifact source</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="a396b-113">Questo comando Elimina un'origine di elementi denominata ContosoArtifactSource in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a396b-113">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="a396b-114">Esempio 2: eliminare un'origine di un elemento usando l'identificatore delle risorse</span><span class="sxs-lookup"><span data-stu-id="a396b-114">Example 2: Delete an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="a396b-115">Questo comando Elimina un'origine di elementi denominata ContosoArtifactSource in ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a396b-115">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="a396b-116">Esempio 3: eliminare un'origine di un elemento usando un oggetto</span><span class="sxs-lookup"><span data-stu-id="a396b-116">Example 3: Delete an artifact source using an object</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerArtifactSource -ArtifactSource $artifactSourceObject
```

<span data-ttu-id="a396b-117">Questo comando Elimina un'origine di elementi il cui nome e ResourceGroup corrispondono rispettivamente alle proprietà Name e ResourceGroupName della $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="a396b-117">This command deletes an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="a396b-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a396b-118">PARAMETERS</span></span>

### <span data-ttu-id="a396b-119">-ArtifactSource</span><span class="sxs-lookup"><span data-stu-id="a396b-119">-ArtifactSource</span></span>
<span data-ttu-id="a396b-120">Archivio elementi da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="a396b-120">The artifact store to be removed.</span></span>

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

### <span data-ttu-id="a396b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a396b-121">-DefaultProfile</span></span>
<span data-ttu-id="a396b-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a396b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a396b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="a396b-123">-Force</span></span>
<span data-ttu-id="a396b-124">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="a396b-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a396b-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="a396b-125">-Name</span></span>
<span data-ttu-id="a396b-126">Nome dell'origine dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="a396b-126">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a396b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a396b-127">-PassThru</span></span>
<span data-ttu-id="a396b-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="a396b-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a396b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a396b-129">-ResourceGroupName</span></span>
<span data-ttu-id="a396b-130">Gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="a396b-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a396b-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a396b-131">-ResourceId</span></span>
<span data-ttu-id="a396b-132">Identificatore della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a396b-132">The resource identifier.</span></span>

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

### <span data-ttu-id="a396b-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a396b-133">-Confirm</span></span>
<span data-ttu-id="a396b-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a396b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a396b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a396b-135">-WhatIf</span></span>
<span data-ttu-id="a396b-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a396b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a396b-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a396b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a396b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a396b-138">CommonParameters</span></span>
<span data-ttu-id="a396b-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a396b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a396b-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a396b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a396b-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a396b-141">INPUTS</span></span>

### <span data-ttu-id="a396b-142">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="a396b-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="a396b-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a396b-143">OUTPUTS</span></span>

### <span data-ttu-id="a396b-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a396b-144">System.Boolean</span></span>

## <span data-ttu-id="a396b-145">Note</span><span class="sxs-lookup"><span data-stu-id="a396b-145">NOTES</span></span>

## <span data-ttu-id="a396b-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a396b-146">RELATED LINKS</span></span>

[<span data-ttu-id="a396b-147">New-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="a396b-147">New-AzureRmDeploymentManagerArtifactSource</span></span>](./New-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="a396b-148">Get-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="a396b-148">Get-AzureRmDeploymentManagerArtifactSource</span></span>](./Get-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="a396b-149">Set-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="a396b-149">Set-AzureRmDeploymentManagerArtifactSource</span></span>](./Set-AzureRmDeploymentManagerArtifactSource.md)