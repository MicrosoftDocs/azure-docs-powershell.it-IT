---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/Remove-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryTag.md
ms.openlocfilehash: 6fbc5b33bb8e9c865b5ea869deed5044ee08198f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956414"
---
# <span data-ttu-id="c7ccc-101">Remove-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="c7ccc-101">Remove-AzContainerRegistryTag</span></span>

## <span data-ttu-id="c7ccc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7ccc-102">SYNOPSIS</span></span>
<span data-ttu-id="c7ccc-103">Rimuovere il contrassegno tag ACR.</span><span class="sxs-lookup"><span data-stu-id="c7ccc-103">Untag ACR tag.</span></span>

## <span data-ttu-id="c7ccc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7ccc-104">SYNTAX</span></span>

```
Remove-AzContainerRegistryTag -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7ccc-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c7ccc-105">DESCRIPTION</span></span>
<span data-ttu-id="c7ccc-106">Rimuovere il contrassegno tag ACR.</span><span class="sxs-lookup"><span data-stu-id="c7ccc-106">Untag ACR tag.</span></span>
<span data-ttu-id="c7ccc-107">Per usare questo cmdlet, esegui `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="c7ccc-107">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span></span>
<span data-ttu-id="c7ccc-108">per prima cosa.</span><span class="sxs-lookup"><span data-stu-id="c7ccc-108">first.</span></span>

## <span data-ttu-id="c7ccc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7ccc-109">EXAMPLES</span></span>

### <span data-ttu-id="c7ccc-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c7ccc-110">Example 1</span></span>
```powershell
Remove-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -Name latest
True
```

<span data-ttu-id="c7ccc-111">Rimuovere il contrassegno alpine:tag nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="c7ccc-111">Untag alpine:tag under registry.</span></span>

## <span data-ttu-id="c7ccc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7ccc-112">PARAMETERS</span></span>

### <span data-ttu-id="c7ccc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7ccc-113">-DefaultProfile</span></span>
<span data-ttu-id="c7ccc-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c7ccc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7ccc-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c7ccc-115">-Name</span></span>
<span data-ttu-id="c7ccc-116">Contrassegno.</span><span class="sxs-lookup"><span data-stu-id="c7ccc-116">Tag.</span></span>

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

### <span data-ttu-id="c7ccc-117">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="c7ccc-117">-RegistryName</span></span>
<span data-ttu-id="c7ccc-118">Nome del Registro di sistema del contenitore di Azure.</span><span class="sxs-lookup"><span data-stu-id="c7ccc-118">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="c7ccc-119">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="c7ccc-119">-RepositoryName</span></span>
<span data-ttu-id="c7ccc-120">Nome archivio.</span><span class="sxs-lookup"><span data-stu-id="c7ccc-120">Repository Name.</span></span>

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

### <span data-ttu-id="c7ccc-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7ccc-121">-Confirm</span></span>
<span data-ttu-id="c7ccc-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7ccc-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7ccc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7ccc-123">-WhatIf</span></span>
<span data-ttu-id="c7ccc-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c7ccc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7ccc-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c7ccc-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7ccc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7ccc-126">CommonParameters</span></span>
<span data-ttu-id="c7ccc-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7ccc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7ccc-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c7ccc-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7ccc-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="c7ccc-129">INPUTS</span></span>

### <span data-ttu-id="c7ccc-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c7ccc-130">System.String</span></span>

## <span data-ttu-id="c7ccc-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7ccc-131">OUTPUTS</span></span>

### <span data-ttu-id="c7ccc-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c7ccc-132">System.Boolean</span></span>

## <span data-ttu-id="c7ccc-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="c7ccc-133">NOTES</span></span>

## <span data-ttu-id="c7ccc-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7ccc-134">RELATED LINKS</span></span>
