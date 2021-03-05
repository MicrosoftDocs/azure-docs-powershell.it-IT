---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryManifest.md
ms.openlocfilehash: 5477dc0402d79228a9283f9c9e88b0fd34e425ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004414"
---
# <span data-ttu-id="41f90-101">Get-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="41f90-101">Get-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="41f90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41f90-102">SYNOPSIS</span></span>
<span data-ttu-id="41f90-103">Ottenere o elencare il manifesto ACR.</span><span class="sxs-lookup"><span data-stu-id="41f90-103">Get or list ACR manifest.</span></span> 

## <span data-ttu-id="41f90-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="41f90-104">SYNTAX</span></span>

### <span data-ttu-id="41f90-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="41f90-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryManifest -RepositoryName <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="41f90-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="41f90-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryManifest -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41f90-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="41f90-107">DESCRIPTION</span></span>
<span data-ttu-id="41f90-108">Ottenere o elencare il manifesto ACR.</span><span class="sxs-lookup"><span data-stu-id="41f90-108">Get or list ACR manifest.</span></span>
<span data-ttu-id="41f90-109">Per usare questo cmdlet, esegui `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span><span class="sxs-lookup"><span data-stu-id="41f90-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span></span>
<span data-ttu-id="41f90-110">per prima cosa.</span><span class="sxs-lookup"><span data-stu-id="41f90-110">first.</span></span>

## <span data-ttu-id="41f90-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="41f90-111">EXAMPLES</span></span>

### <span data-ttu-id="41f90-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="41f90-112">Example 1</span></span>
```powershell
Get-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine

Registry                    ImageName                   ManifestsAttributes
--------                    ---------                   -------------------
registry.azurecr.io         registry.azurecr.io         {Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase, Microsoft.Azure.Comm…}
```

<span data-ttu-id="41f90-113">Manifesti di elenco per l'archivio alpine nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="41f90-113">List manifests for repository alpine under registry.</span></span>

### <span data-ttu-id="41f90-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="41f90-114">Example 2</span></span>
```powershell
Get-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Name sha256:a5426f084c755f4d6c1d1562a2d456aa574a24a61706f6806415627360c06ac0

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

<span data-ttu-id="41f90-115">Ottenere il manifesto sha256:a5426f084c755f4d6c1d1562a2d456aa574a24a61706f6806415627360c06ac0 per il repository alpine nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="41f90-115">Get manifests sha256:a5426f084c755f4d6c1d1562a2d456aa574a24a61706f6806415627360c06ac0 for repository alpine under registry.</span></span>

## <span data-ttu-id="41f90-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41f90-116">PARAMETERS</span></span>

### <span data-ttu-id="41f90-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41f90-117">-DefaultProfile</span></span>
<span data-ttu-id="41f90-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="41f90-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41f90-119">-Name</span><span class="sxs-lookup"><span data-stu-id="41f90-119">-Name</span></span>
<span data-ttu-id="41f90-120">Riferimento manifesto.</span><span class="sxs-lookup"><span data-stu-id="41f90-120">Manifest reference.</span></span>

```yaml
Type: System.String
Parameter Sets: GetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41f90-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="41f90-121">-RegistryName</span></span>
<span data-ttu-id="41f90-122">Nome del Registro di sistema del contenitore di Azure.</span><span class="sxs-lookup"><span data-stu-id="41f90-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="41f90-123">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="41f90-123">-RepositoryName</span></span>
<span data-ttu-id="41f90-124">Nome archivio.</span><span class="sxs-lookup"><span data-stu-id="41f90-124">Repository Name.</span></span>

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

### <span data-ttu-id="41f90-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41f90-125">CommonParameters</span></span>
<span data-ttu-id="41f90-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41f90-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41f90-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="41f90-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41f90-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="41f90-128">INPUTS</span></span>

### <span data-ttu-id="41f90-129">System.String</span><span class="sxs-lookup"><span data-stu-id="41f90-129">System.String</span></span>

## <span data-ttu-id="41f90-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="41f90-130">OUTPUTS</span></span>

### <span data-ttu-id="41f90-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span><span class="sxs-lookup"><span data-stu-id="41f90-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span></span>

### <span data-ttu-id="41f90-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSAcrManifest</span><span class="sxs-lookup"><span data-stu-id="41f90-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSAcrManifest</span></span>

## <span data-ttu-id="41f90-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="41f90-133">NOTES</span></span>

## <span data-ttu-id="41f90-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="41f90-134">RELATED LINKS</span></span>
