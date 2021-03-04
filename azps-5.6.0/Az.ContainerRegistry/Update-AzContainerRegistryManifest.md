---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/update-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryManifest.md
ms.openlocfilehash: 030f0b00ba77bc967a53ce43c4f08d66c214f67e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956286"
---
# <span data-ttu-id="8717c-101">Update-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="8717c-101">Update-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="8717c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8717c-102">SYNOPSIS</span></span>
<span data-ttu-id="8717c-103">Aggiornare il manifesto ACR.</span><span class="sxs-lookup"><span data-stu-id="8717c-103">Update ACR manifest.</span></span> 

## <span data-ttu-id="8717c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8717c-104">SYNTAX</span></span>

### <span data-ttu-id="8717c-105">ByManifestParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="8717c-105">ByManifestParameterSet (Default)</span></span>
```
Update-AzContainerRegistryManifest -RepositoryName <String> -Manifest <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8717c-106">ByTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="8717c-106">ByTagParameterSet</span></span>
```
Update-AzContainerRegistryManifest -RepositoryName <String> -Tag <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8717c-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8717c-107">DESCRIPTION</span></span>
<span data-ttu-id="8717c-108">Aggiornare il manifesto ACR.</span><span class="sxs-lookup"><span data-stu-id="8717c-108">Update ACR manifest.</span></span>
<span data-ttu-id="8717c-109">Per usare questo cmdlet, esegui `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="8717c-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span></span>
<span data-ttu-id="8717c-110">per prima cosa.</span><span class="sxs-lookup"><span data-stu-id="8717c-110">first.</span></span>

## <span data-ttu-id="8717c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8717c-111">EXAMPLES</span></span>

### <span data-ttu-id="8717c-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8717c-112">Example 1</span></span>
```powershell
Update-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Manifest sha256:185518070891758909c9f839cf4ca393ee977ac378609f700f60a771a2dfe321 -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

<span data-ttu-id="8717c-113">Aggiornare gli attributi per il manifesto sha256:185518070891758909c9f839cf4ca393ee977ac378609f700f60a771a2dfe321 nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="8717c-113">Update attributes for manifest sha256:185518070891758909c9f839cf4ca393ee977ac378609f700f60a771a2dfe321 under registry.</span></span>

### <span data-ttu-id="8717c-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8717c-114">Example 2</span></span>
```powershell
Update-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Tag latest -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

<span data-ttu-id="8717c-115">Aggiornare gli attributi per il manifesto con il tag più recente nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="8717c-115">Update attributes for manifest with tag latest under registry.</span></span>

## <span data-ttu-id="8717c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8717c-116">PARAMETERS</span></span>

### <span data-ttu-id="8717c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8717c-117">-DefaultProfile</span></span>
<span data-ttu-id="8717c-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8717c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8717c-119">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="8717c-119">-DeleteEnabled</span></span>
<span data-ttu-id="8717c-120">Elimina abilita.</span><span class="sxs-lookup"><span data-stu-id="8717c-120">Delete enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8717c-121">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="8717c-121">-ListEnabled</span></span>
<span data-ttu-id="8717c-122">Abilitazione dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="8717c-122">List enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8717c-123">-Manifesto</span><span class="sxs-lookup"><span data-stu-id="8717c-123">-Manifest</span></span>
<span data-ttu-id="8717c-124">Riferimento manifesto.</span><span class="sxs-lookup"><span data-stu-id="8717c-124">Manifest reference.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManifestParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8717c-125">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="8717c-125">-ReadEnabled</span></span>
<span data-ttu-id="8717c-126">Abilitare la lettura.</span><span class="sxs-lookup"><span data-stu-id="8717c-126">Read enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8717c-127">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="8717c-127">-RegistryName</span></span>
<span data-ttu-id="8717c-128">Nome del Registro di sistema del contenitore di Azure.</span><span class="sxs-lookup"><span data-stu-id="8717c-128">Azure Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8717c-129">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="8717c-129">-RepositoryName</span></span>
<span data-ttu-id="8717c-130">Nome archivio.</span><span class="sxs-lookup"><span data-stu-id="8717c-130">Repository Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8717c-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="8717c-131">-Tag</span></span>
<span data-ttu-id="8717c-132">Tag.</span><span class="sxs-lookup"><span data-stu-id="8717c-132">Tag.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8717c-133">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="8717c-133">-WriteEnabled</span></span>
<span data-ttu-id="8717c-134">Abilitare la scrittura.</span><span class="sxs-lookup"><span data-stu-id="8717c-134">Write enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8717c-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8717c-135">-Confirm</span></span>
<span data-ttu-id="8717c-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8717c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8717c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8717c-137">-WhatIf</span></span>
<span data-ttu-id="8717c-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8717c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8717c-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8717c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8717c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8717c-140">CommonParameters</span></span>
<span data-ttu-id="8717c-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8717c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8717c-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8717c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8717c-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="8717c-143">INPUTS</span></span>

### <span data-ttu-id="8717c-144">System.String</span><span class="sxs-lookup"><span data-stu-id="8717c-144">System.String</span></span>

## <span data-ttu-id="8717c-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8717c-145">OUTPUTS</span></span>

### <span data-ttu-id="8717c-146">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span><span class="sxs-lookup"><span data-stu-id="8717c-146">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span></span>

## <span data-ttu-id="8717c-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="8717c-147">NOTES</span></span>

## <span data-ttu-id="8717c-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8717c-148">RELATED LINKS</span></span>
