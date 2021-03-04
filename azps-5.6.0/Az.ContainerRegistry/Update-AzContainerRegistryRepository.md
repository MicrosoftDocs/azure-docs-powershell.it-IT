---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/update-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryRepository.md
ms.openlocfilehash: 45572cbd2255a604e492c7740d1749a0ad968845
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956285"
---
# <span data-ttu-id="eb938-101">Update-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="eb938-101">Update-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="eb938-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb938-102">SYNOPSIS</span></span>
<span data-ttu-id="eb938-103">Aggiornare l'archivio ACR.</span><span class="sxs-lookup"><span data-stu-id="eb938-103">Update ACR repository.</span></span>

## <span data-ttu-id="eb938-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eb938-104">SYNTAX</span></span>

```
Update-AzContainerRegistryRepository -Name <String> [-DeleteEnabled <Boolean>] [-WriteEnabled <Boolean>]
 [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb938-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="eb938-105">DESCRIPTION</span></span>
<span data-ttu-id="eb938-106">Aggiornare l'archivio ACR.</span><span class="sxs-lookup"><span data-stu-id="eb938-106">Update ACR repository.</span></span>

## <span data-ttu-id="eb938-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eb938-107">EXAMPLES</span></span>

### <span data-ttu-id="eb938-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="eb938-108">Example 1</span></span>
```powershell
Update-AzContainerRegistryRepository -RegistryName registry -Name test/busybox8 -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry             : registry.azurecr.io
ImageName            : test/busybox8
CreatedTime          : 2020-12-11T08:57:56.2070002Z
LastUpdateTime       : 2020-12-11T08:57:56.5188237Z
ManifestCount        : 1
TagCount             : 1
ChangeableAttributes : Microsoft.Azure.Commands.ContainerRegistry.Models.PSChangeableAttribute
```

<span data-ttu-id="eb938-109">Aggiornare gli attributi per l'archivio alpine nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="eb938-109">Update attributes for repository alpine under registry.</span></span>

## <span data-ttu-id="eb938-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb938-110">PARAMETERS</span></span>

### <span data-ttu-id="eb938-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb938-111">-DefaultProfile</span></span>
<span data-ttu-id="eb938-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eb938-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb938-113">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="eb938-113">-DeleteEnabled</span></span>
<span data-ttu-id="eb938-114">Elimina abilita.</span><span class="sxs-lookup"><span data-stu-id="eb938-114">Delete enable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb938-115">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="eb938-115">-ListEnabled</span></span>
<span data-ttu-id="eb938-116">Abilitazione dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="eb938-116">List enable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb938-117">-Name</span><span class="sxs-lookup"><span data-stu-id="eb938-117">-Name</span></span>
<span data-ttu-id="eb938-118">Nome archivio.</span><span class="sxs-lookup"><span data-stu-id="eb938-118">Repository Name.</span></span>

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

### <span data-ttu-id="eb938-119">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="eb938-119">-ReadEnabled</span></span>
<span data-ttu-id="eb938-120">Abilitare la lettura.</span><span class="sxs-lookup"><span data-stu-id="eb938-120">Read enable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb938-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="eb938-121">-RegistryName</span></span>
<span data-ttu-id="eb938-122">Nome del Registro di sistema del contenitore di Azure.</span><span class="sxs-lookup"><span data-stu-id="eb938-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="eb938-123">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="eb938-123">-WriteEnabled</span></span>
<span data-ttu-id="eb938-124">Abilitare la scrittura.</span><span class="sxs-lookup"><span data-stu-id="eb938-124">Write enable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb938-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb938-125">-Confirm</span></span>
<span data-ttu-id="eb938-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb938-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb938-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb938-127">-WhatIf</span></span>
<span data-ttu-id="eb938-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eb938-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb938-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eb938-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb938-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb938-130">CommonParameters</span></span>
<span data-ttu-id="eb938-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb938-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb938-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="eb938-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb938-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="eb938-133">INPUTS</span></span>

### <span data-ttu-id="eb938-134">System.String</span><span class="sxs-lookup"><span data-stu-id="eb938-134">System.String</span></span>

## <span data-ttu-id="eb938-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eb938-135">OUTPUTS</span></span>

### <span data-ttu-id="eb938-136">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span><span class="sxs-lookup"><span data-stu-id="eb938-136">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span></span>

## <span data-ttu-id="eb938-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="eb938-137">NOTES</span></span>

## <span data-ttu-id="eb938-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eb938-138">RELATED LINKS</span></span>
