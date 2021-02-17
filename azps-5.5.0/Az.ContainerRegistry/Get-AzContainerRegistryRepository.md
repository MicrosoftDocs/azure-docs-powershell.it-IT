---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryRepository.md
ms.openlocfilehash: 7da65515138ff6afa97e6c05f9baa764d6ab920c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196911"
---
# <span data-ttu-id="8cd9c-101">Get-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="8cd9c-101">Get-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="8cd9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cd9c-102">SYNOPSIS</span></span>
<span data-ttu-id="8cd9c-103">Ottenere o elencare archivi ACR.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-103">Get or list ACR repositories.</span></span>

## <span data-ttu-id="8cd9c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8cd9c-104">SYNTAX</span></span>

### <span data-ttu-id="8cd9c-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8cd9c-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryRepository [-First <Int32>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cd9c-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="8cd9c-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryRepository -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cd9c-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8cd9c-107">DESCRIPTION</span></span>
<span data-ttu-id="8cd9c-108">Ottenere o elencare archivi ACR.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-108">Get or list ACR repositories.</span></span>
<span data-ttu-id="8cd9c-109">List restituisce solo i nomi dei repository.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-109">List returns repository names only.</span></span>

## <span data-ttu-id="8cd9c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8cd9c-110">EXAMPLES</span></span>

### <span data-ttu-id="8cd9c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8cd9c-111">Example 1</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry
alpine
test/busybox0
test/busybox1
test/busybox10
```

<span data-ttu-id="8cd9c-112">Elencare tutti i repository nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-112">List all repositories in registry.</span></span>

### <span data-ttu-id="8cd9c-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8cd9c-113">Example 2</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry -First 3
alpine
test/busybox0
test/busybox1
```

<span data-ttu-id="8cd9c-114">Elencare i primi tre archivi nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-114">List first 3 repositories in registry.</span></span>

### <span data-ttu-id="8cd9c-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="8cd9c-115">Example 3</span></span>
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

<span data-ttu-id="8cd9c-116">Ottenere il repository alpine nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-116">Get repository alpine under registry.</span></span>

## <span data-ttu-id="8cd9c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8cd9c-117">PARAMETERS</span></span>

### <span data-ttu-id="8cd9c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cd9c-118">-DefaultProfile</span></span>
<span data-ttu-id="8cd9c-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cd9c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8cd9c-120">-Name</span></span>
<span data-ttu-id="8cd9c-121">Nome archivio.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-121">Repository Name.</span></span>

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

### <span data-ttu-id="8cd9c-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="8cd9c-122">-RegistryName</span></span>
<span data-ttu-id="8cd9c-123">Nome del Registro di sistema del contenitore di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-123">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="8cd9c-124">-First</span><span class="sxs-lookup"><span data-stu-id="8cd9c-124">-First</span></span>
<span data-ttu-id="8cd9c-125">Primi n risultati.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-125">First n results.</span></span>

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

### <span data-ttu-id="8cd9c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cd9c-126">CommonParameters</span></span>
<span data-ttu-id="8cd9c-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cd9c-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8cd9c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cd9c-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="8cd9c-129">INPUTS</span></span>

### <span data-ttu-id="8cd9c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8cd9c-130">System.String</span></span>

## <span data-ttu-id="8cd9c-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8cd9c-131">OUTPUTS</span></span>

### <span data-ttu-id="8cd9c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="8cd9c-132">System.String</span></span>

### <span data-ttu-id="8cd9c-133">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span><span class="sxs-lookup"><span data-stu-id="8cd9c-133">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span></span>

## <span data-ttu-id="8cd9c-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="8cd9c-134">NOTES</span></span>

## <span data-ttu-id="8cd9c-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8cd9c-135">RELATED LINKS</span></span>
