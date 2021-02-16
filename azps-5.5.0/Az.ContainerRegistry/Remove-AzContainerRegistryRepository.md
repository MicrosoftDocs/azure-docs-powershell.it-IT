---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryRepository.md
ms.openlocfilehash: a99d020bbdef81868fb0e4338c7bc6c722723254
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199110"
---
# <span data-ttu-id="0f5cd-101">Remove-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="0f5cd-101">Remove-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="0f5cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f5cd-102">SYNOPSIS</span></span>
<span data-ttu-id="0f5cd-103">Eliminare un repository da ACR.</span><span class="sxs-lookup"><span data-stu-id="0f5cd-103">Delete repository from ACR.</span></span>

## <span data-ttu-id="0f5cd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f5cd-104">SYNTAX</span></span>

```
Remove-AzContainerRegistryRepository -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f5cd-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0f5cd-105">DESCRIPTION</span></span>
<span data-ttu-id="0f5cd-106">Eliminare un repository da ACR.</span><span class="sxs-lookup"><span data-stu-id="0f5cd-106">Delete repository from ACR.</span></span>

## <span data-ttu-id="0f5cd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f5cd-107">EXAMPLES</span></span>

### <span data-ttu-id="0f5cd-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0f5cd-108">Example 1</span></span>
```powershell
Remove-AzContainerRegistryRepository -RegistryName registry -Name test/busybox15

ManifestsDeleted                                                          TagsDeleted
----------------                                                          -----------
{sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab} {latest}
```

<span data-ttu-id="0f5cd-109">Eliminare il test del repository/busybox15 nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="0f5cd-109">Delete repository test/busybox15 under registry.</span></span>

## <span data-ttu-id="0f5cd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f5cd-110">PARAMETERS</span></span>

### <span data-ttu-id="0f5cd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f5cd-111">-DefaultProfile</span></span>
<span data-ttu-id="0f5cd-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0f5cd-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f5cd-113">-Name</span><span class="sxs-lookup"><span data-stu-id="0f5cd-113">-Name</span></span>
<span data-ttu-id="0f5cd-114">Nome archivio.</span><span class="sxs-lookup"><span data-stu-id="0f5cd-114">Repository Name.</span></span>

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

### <span data-ttu-id="0f5cd-115">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="0f5cd-115">-RegistryName</span></span>
<span data-ttu-id="0f5cd-116">Nome del Registro di sistema del contenitore di Azure.</span><span class="sxs-lookup"><span data-stu-id="0f5cd-116">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="0f5cd-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f5cd-117">-Confirm</span></span>
<span data-ttu-id="0f5cd-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f5cd-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f5cd-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f5cd-119">-WhatIf</span></span>
<span data-ttu-id="0f5cd-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f5cd-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f5cd-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f5cd-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f5cd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f5cd-122">CommonParameters</span></span>
<span data-ttu-id="0f5cd-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f5cd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f5cd-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0f5cd-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f5cd-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="0f5cd-125">INPUTS</span></span>

### <span data-ttu-id="0f5cd-126">System.String</span><span class="sxs-lookup"><span data-stu-id="0f5cd-126">System.String</span></span>

## <span data-ttu-id="0f5cd-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f5cd-127">OUTPUTS</span></span>

### <span data-ttu-id="0f5cd-128">Microsoft.Azure.Commands.ContainerRegistry.Models.PSDeletedRepository</span><span class="sxs-lookup"><span data-stu-id="0f5cd-128">Microsoft.Azure.Commands.ContainerRegistry.Models.PSDeletedRepository</span></span>

## <span data-ttu-id="0f5cd-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="0f5cd-129">NOTES</span></span>

## <span data-ttu-id="0f5cd-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f5cd-130">RELATED LINKS</span></span>
