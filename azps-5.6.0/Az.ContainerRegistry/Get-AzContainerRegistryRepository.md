---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryRepository.md
ms.openlocfilehash: efcd7fb518f66c99fab8b4cd456e8f8cea424ad7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990399"
---
# <span data-ttu-id="13719-101">Get-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="13719-101">Get-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="13719-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13719-102">SYNOPSIS</span></span>
<span data-ttu-id="13719-103">Ottenere o elencare archivi ACR.</span><span class="sxs-lookup"><span data-stu-id="13719-103">Get or list ACR repositories.</span></span>

## <span data-ttu-id="13719-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="13719-104">SYNTAX</span></span>

### <span data-ttu-id="13719-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="13719-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryRepository [-First <Int32>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13719-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="13719-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryRepository -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13719-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="13719-107">DESCRIPTION</span></span>
<span data-ttu-id="13719-108">Ottenere o elencare archivi ACR.</span><span class="sxs-lookup"><span data-stu-id="13719-108">Get or list ACR repositories.</span></span>
<span data-ttu-id="13719-109">List restituisce solo i nomi dei repository.</span><span class="sxs-lookup"><span data-stu-id="13719-109">List returns repository names only.</span></span>

## <span data-ttu-id="13719-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="13719-110">EXAMPLES</span></span>

### <span data-ttu-id="13719-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="13719-111">Example 1</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry
alpine
test/busybox0
test/busybox1
test/busybox10
```

<span data-ttu-id="13719-112">Elencare tutti gli archivi nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="13719-112">List all repositories in registry.</span></span>

### <span data-ttu-id="13719-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="13719-113">Example 2</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry -First 3
alpine
test/busybox0
test/busybox1
```

<span data-ttu-id="13719-114">Elencare i primi tre archivi nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="13719-114">List first 3 repositories in registry.</span></span>

### <span data-ttu-id="13719-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="13719-115">Example 3</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry -Name alpine

Registry             : registry.azurecr.io
ImageName            : alpine
CreatedTime          : 2020-10-13T05:45:25.5896115Z
LastUpdateTime       : 2021-01-04T08:31:46.2406505Z
ManifestCount        : 7
TagCount             : 1
ChangeableAttributes : Microsoft.Azure.Commands.ContainerRegistry.Models.PSChangeableAttribute
```

<span data-ttu-id="13719-116">Ottenere il repository alpine nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="13719-116">Get repository alpine under registry.</span></span>

## <span data-ttu-id="13719-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13719-117">PARAMETERS</span></span>

### <span data-ttu-id="13719-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13719-118">-DefaultProfile</span></span>
<span data-ttu-id="13719-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="13719-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13719-120">-Name</span><span class="sxs-lookup"><span data-stu-id="13719-120">-Name</span></span>
<span data-ttu-id="13719-121">Nome archivio.</span><span class="sxs-lookup"><span data-stu-id="13719-121">Repository Name.</span></span>

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

### <span data-ttu-id="13719-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="13719-122">-RegistryName</span></span>
<span data-ttu-id="13719-123">Nome del Registro di sistema del contenitore di Azure.</span><span class="sxs-lookup"><span data-stu-id="13719-123">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="13719-124">-First</span><span class="sxs-lookup"><span data-stu-id="13719-124">-First</span></span>
<span data-ttu-id="13719-125">Primi n risultati.</span><span class="sxs-lookup"><span data-stu-id="13719-125">First n results.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13719-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13719-126">CommonParameters</span></span>
<span data-ttu-id="13719-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13719-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13719-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="13719-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13719-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="13719-129">INPUTS</span></span>

### <span data-ttu-id="13719-130">System.String</span><span class="sxs-lookup"><span data-stu-id="13719-130">System.String</span></span>

## <span data-ttu-id="13719-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="13719-131">OUTPUTS</span></span>

### <span data-ttu-id="13719-132">System.String</span><span class="sxs-lookup"><span data-stu-id="13719-132">System.String</span></span>

### <span data-ttu-id="13719-133">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span><span class="sxs-lookup"><span data-stu-id="13719-133">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span></span>

## <span data-ttu-id="13719-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="13719-134">NOTES</span></span>

## <span data-ttu-id="13719-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="13719-135">RELATED LINKS</span></span>
