---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryTag.md
ms.openlocfilehash: 37308ab02db132e03cf4f44536bc44d0d6845a86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990358"
---
# <span data-ttu-id="1cc98-101">Get-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="1cc98-101">Get-AzContainerRegistryTag</span></span>

## <span data-ttu-id="1cc98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cc98-102">SYNOPSIS</span></span>
<span data-ttu-id="1cc98-103">Ottenere o elencare il tag ACR.</span><span class="sxs-lookup"><span data-stu-id="1cc98-103">Get or list ACR tag.</span></span> 

## <span data-ttu-id="1cc98-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1cc98-104">SYNTAX</span></span>

### <span data-ttu-id="1cc98-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1cc98-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryTag -RepositoryName <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1cc98-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cc98-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryTag -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1cc98-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1cc98-107">DESCRIPTION</span></span>
<span data-ttu-id="1cc98-108">Ottenere o elencare il tag ACR.</span><span class="sxs-lookup"><span data-stu-id="1cc98-108">Get or list ACR tag.</span></span>
<span data-ttu-id="1cc98-109">Per usare questo cmdlet, esegui `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span><span class="sxs-lookup"><span data-stu-id="1cc98-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span></span>
<span data-ttu-id="1cc98-110">per prima cosa.</span><span class="sxs-lookup"><span data-stu-id="1cc98-110">first.</span></span>

## <span data-ttu-id="1cc98-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1cc98-111">EXAMPLES</span></span>

### <span data-ttu-id="1cc98-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1cc98-112">Example 1</span></span>
```powershell
Get-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine

Registry                    ImageName Tags
--------                    --------- ----
registry.azurecr.io alpine    {latest}
```

<span data-ttu-id="1cc98-113">Tag di elenco per l'archivio alpine nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="1cc98-113">List tags for repository alpine under registry.</span></span>

### <span data-ttu-id="1cc98-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1cc98-114">Example 2</span></span>
```powershell
Get-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -name latest

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttributeBase
```

<span data-ttu-id="1cc98-115">Ottenere il tag più recente per l'archivio alpine nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="1cc98-115">Get tag latest for repository alpine under registry.</span></span>

## <span data-ttu-id="1cc98-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1cc98-116">PARAMETERS</span></span>

### <span data-ttu-id="1cc98-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cc98-117">-DefaultProfile</span></span>
<span data-ttu-id="1cc98-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1cc98-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cc98-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1cc98-119">-Name</span></span>
<span data-ttu-id="1cc98-120">Tag.</span><span class="sxs-lookup"><span data-stu-id="1cc98-120">Tag.</span></span>

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

### <span data-ttu-id="1cc98-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="1cc98-121">-RegistryName</span></span>
<span data-ttu-id="1cc98-122">Nome del Registro di sistema del contenitore di Azure.</span><span class="sxs-lookup"><span data-stu-id="1cc98-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="1cc98-123">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="1cc98-123">-RepositoryName</span></span>
<span data-ttu-id="1cc98-124">Nome archivio.</span><span class="sxs-lookup"><span data-stu-id="1cc98-124">Repository Name.</span></span>

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

### <span data-ttu-id="1cc98-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cc98-125">CommonParameters</span></span>
<span data-ttu-id="1cc98-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cc98-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cc98-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1cc98-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cc98-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="1cc98-128">INPUTS</span></span>

### <span data-ttu-id="1cc98-129">System.String</span><span class="sxs-lookup"><span data-stu-id="1cc98-129">System.String</span></span>

## <span data-ttu-id="1cc98-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1cc98-130">OUTPUTS</span></span>

### <span data-ttu-id="1cc98-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span><span class="sxs-lookup"><span data-stu-id="1cc98-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span></span>

### <span data-ttu-id="1cc98-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagList</span><span class="sxs-lookup"><span data-stu-id="1cc98-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagList</span></span>

## <span data-ttu-id="1cc98-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="1cc98-133">NOTES</span></span>

## <span data-ttu-id="1cc98-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1cc98-134">RELATED LINKS</span></span>
