---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryManifest.md
ms.openlocfilehash: a37073de6a7960ae1ab90746372179db8e9d9386
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199118"
---
# <span data-ttu-id="496b3-101">Remove-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="496b3-101">Remove-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="496b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="496b3-102">SYNOPSIS</span></span>
<span data-ttu-id="496b3-103">Eliminare il manifesto ACR.</span><span class="sxs-lookup"><span data-stu-id="496b3-103">Delete ACR manifest.</span></span> 

## <span data-ttu-id="496b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="496b3-104">SYNTAX</span></span>

### <span data-ttu-id="496b3-105">ByManifestParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="496b3-105">ByManifestParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryManifest -RepositoryName <String> -Manifest <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="496b3-106">ByTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="496b3-106">ByTagParameterSet</span></span>
```
Remove-AzContainerRegistryManifest -RepositoryName <String> -Tag <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="496b3-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="496b3-107">DESCRIPTION</span></span>
<span data-ttu-id="496b3-108">Eliminare il manifesto ACR.</span><span class="sxs-lookup"><span data-stu-id="496b3-108">Delete ACR manifest.</span></span>
<span data-ttu-id="496b3-109">Per usare questo cmdlet, esegui `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="496b3-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span></span>
<span data-ttu-id="496b3-110">per prima cosa.</span><span class="sxs-lookup"><span data-stu-id="496b3-110">first.</span></span>

## <span data-ttu-id="496b3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="496b3-111">EXAMPLES</span></span>

### <span data-ttu-id="496b3-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="496b3-112">Example 1</span></span>
```powershell
Remove-AzContainerRegistryManifest -RegistryName registry -RepositoryName test/busybox27 -Manifest sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab
True
```

<span data-ttu-id="496b3-113">Eliminare il manifesto sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab per l'archivio test/busybox27 nel Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="496b3-113">Delete manifest sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab for repository test/busybox27 under registry</span></span>

### <span data-ttu-id="496b3-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="496b3-114">Example 2</span></span>
```powershell
Remove-AzContainerRegistryManifest -RegistryName registry -RepositoryName test/busybox27 -Tag latest
True
```

<span data-ttu-id="496b3-115">Elimina manifesto con il tag più recente per il repository test/busybox27 nel Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="496b3-115">Delete manifest with tag latest for repository test/busybox27 under registry</span></span>

## <span data-ttu-id="496b3-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="496b3-116">PARAMETERS</span></span>

### <span data-ttu-id="496b3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="496b3-117">-DefaultProfile</span></span>
<span data-ttu-id="496b3-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="496b3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="496b3-119">-Manifesto</span><span class="sxs-lookup"><span data-stu-id="496b3-119">-Manifest</span></span>
<span data-ttu-id="496b3-120">Riferimento manifesto.</span><span class="sxs-lookup"><span data-stu-id="496b3-120">Manifest reference.</span></span>

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

### <span data-ttu-id="496b3-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="496b3-121">-RegistryName</span></span>
<span data-ttu-id="496b3-122">Nome del Registro di sistema del contenitore di Azure.</span><span class="sxs-lookup"><span data-stu-id="496b3-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="496b3-123">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="496b3-123">-RepositoryName</span></span>
<span data-ttu-id="496b3-124">Nome archivio.</span><span class="sxs-lookup"><span data-stu-id="496b3-124">Repository Name.</span></span>

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

### <span data-ttu-id="496b3-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="496b3-125">-Tag</span></span>
<span data-ttu-id="496b3-126">Contrassegno.</span><span class="sxs-lookup"><span data-stu-id="496b3-126">Tag.</span></span>

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

### <span data-ttu-id="496b3-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="496b3-127">-Confirm</span></span>
<span data-ttu-id="496b3-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="496b3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="496b3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="496b3-129">-WhatIf</span></span>
<span data-ttu-id="496b3-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="496b3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="496b3-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="496b3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="496b3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="496b3-132">CommonParameters</span></span>
<span data-ttu-id="496b3-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="496b3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="496b3-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="496b3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="496b3-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="496b3-135">INPUTS</span></span>

### <span data-ttu-id="496b3-136">System.String</span><span class="sxs-lookup"><span data-stu-id="496b3-136">System.String</span></span>

## <span data-ttu-id="496b3-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="496b3-137">OUTPUTS</span></span>

### <span data-ttu-id="496b3-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="496b3-138">System.Boolean</span></span>

## <span data-ttu-id="496b3-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="496b3-139">NOTES</span></span>

## <span data-ttu-id="496b3-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="496b3-140">RELATED LINKS</span></span>
