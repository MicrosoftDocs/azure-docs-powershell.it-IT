---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/remove-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryRepository.md
ms.openlocfilehash: 1c0ad2ae46987a526be4e8fda110dada914bd27e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975453"
---
# <span data-ttu-id="c015e-101">Remove-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="c015e-101">Remove-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="c015e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c015e-102">SYNOPSIS</span></span>
<span data-ttu-id="c015e-103">Eliminare un repository da ACR.</span><span class="sxs-lookup"><span data-stu-id="c015e-103">Delete repository from ACR.</span></span>

## <span data-ttu-id="c015e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c015e-104">SYNTAX</span></span>

```
Remove-AzContainerRegistryRepository -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c015e-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c015e-105">DESCRIPTION</span></span>
<span data-ttu-id="c015e-106">Eliminare un repository da ACR.</span><span class="sxs-lookup"><span data-stu-id="c015e-106">Delete repository from ACR.</span></span>

## <span data-ttu-id="c015e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c015e-107">EXAMPLES</span></span>

### <span data-ttu-id="c015e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c015e-108">Example 1</span></span>
```powershell
Remove-AzContainerRegistryRepository -RegistryName registry -Name test/busybox15

ManifestsDeleted                                                          TagsDeleted
----------------                                                          -----------
{sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab} {latest}
```

<span data-ttu-id="c015e-109">Eliminare il test del repository/busybox15 nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="c015e-109">Delete repository test/busybox15 under registry.</span></span>

## <span data-ttu-id="c015e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c015e-110">PARAMETERS</span></span>

### <span data-ttu-id="c015e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c015e-111">-DefaultProfile</span></span>
<span data-ttu-id="c015e-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c015e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c015e-113">-Name</span><span class="sxs-lookup"><span data-stu-id="c015e-113">-Name</span></span>
<span data-ttu-id="c015e-114">Nome archivio.</span><span class="sxs-lookup"><span data-stu-id="c015e-114">Repository Name.</span></span>

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

### <span data-ttu-id="c015e-115">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="c015e-115">-RegistryName</span></span>
<span data-ttu-id="c015e-116">Nome del Registro di sistema del contenitore di Azure.</span><span class="sxs-lookup"><span data-stu-id="c015e-116">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="c015e-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c015e-117">-Confirm</span></span>
<span data-ttu-id="c015e-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c015e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c015e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c015e-119">-WhatIf</span></span>
<span data-ttu-id="c015e-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c015e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c015e-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c015e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c015e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c015e-122">CommonParameters</span></span>
<span data-ttu-id="c015e-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c015e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c015e-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c015e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c015e-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="c015e-125">INPUTS</span></span>

### <span data-ttu-id="c015e-126">System.String</span><span class="sxs-lookup"><span data-stu-id="c015e-126">System.String</span></span>

## <span data-ttu-id="c015e-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c015e-127">OUTPUTS</span></span>

### <span data-ttu-id="c015e-128">Microsoft.Azure.Commands.ContainerRegistry.Models.PSDeletedRepository</span><span class="sxs-lookup"><span data-stu-id="c015e-128">Microsoft.Azure.Commands.ContainerRegistry.Models.PSDeletedRepository</span></span>

## <span data-ttu-id="c015e-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="c015e-129">NOTES</span></span>

## <span data-ttu-id="c015e-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c015e-130">RELATED LINKS</span></span>
