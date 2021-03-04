---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/update-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryTag.md
ms.openlocfilehash: 68d4eab2088bc1091d812399aade67659d7db31b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956270"
---
# <span data-ttu-id="93d29-101">Update-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="93d29-101">Update-AzContainerRegistryTag</span></span>

## <span data-ttu-id="93d29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93d29-102">SYNOPSIS</span></span>
<span data-ttu-id="93d29-103">Aggiornare il tag ACR.</span><span class="sxs-lookup"><span data-stu-id="93d29-103">Update ACR tag.</span></span>

## <span data-ttu-id="93d29-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93d29-104">SYNTAX</span></span>

```
Update-AzContainerRegistryTag -RepositoryName <String> -Name <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93d29-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="93d29-105">DESCRIPTION</span></span>
<span data-ttu-id="93d29-106">Aggiornare il tag ACR.</span><span class="sxs-lookup"><span data-stu-id="93d29-106">Update ACR tag.</span></span>
<span data-ttu-id="93d29-107">Per usare questo cmdlet, esegui `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="93d29-107">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span></span>
<span data-ttu-id="93d29-108">per prima cosa.</span><span class="sxs-lookup"><span data-stu-id="93d29-108">first.</span></span>

## <span data-ttu-id="93d29-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93d29-109">EXAMPLES</span></span>

### <span data-ttu-id="93d29-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="93d29-110">Example 1</span></span>
```powershell
Update-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -Name latest -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute
```

<span data-ttu-id="93d29-111">Aggiornare gli attributi per il tag più recente nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="93d29-111">Update attributes for tag latest under registry.</span></span>

## <span data-ttu-id="93d29-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93d29-112">PARAMETERS</span></span>

### <span data-ttu-id="93d29-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93d29-113">-DefaultProfile</span></span>
<span data-ttu-id="93d29-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="93d29-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93d29-115">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="93d29-115">-DeleteEnabled</span></span>
<span data-ttu-id="93d29-116">Elimina abilita.</span><span class="sxs-lookup"><span data-stu-id="93d29-116">Delete enable.</span></span>

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

### <span data-ttu-id="93d29-117">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="93d29-117">-ListEnabled</span></span>
<span data-ttu-id="93d29-118">Abilitazione dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="93d29-118">List enable.</span></span>

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

### <span data-ttu-id="93d29-119">-Name</span><span class="sxs-lookup"><span data-stu-id="93d29-119">-Name</span></span>
<span data-ttu-id="93d29-120">Contrassegno.</span><span class="sxs-lookup"><span data-stu-id="93d29-120">Tag.</span></span>

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

### <span data-ttu-id="93d29-121">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="93d29-121">-ReadEnabled</span></span>
<span data-ttu-id="93d29-122">Abilitare la lettura.</span><span class="sxs-lookup"><span data-stu-id="93d29-122">Read enable.</span></span>

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

### <span data-ttu-id="93d29-123">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="93d29-123">-RegistryName</span></span>
<span data-ttu-id="93d29-124">Nome del Registro di sistema del contenitore di Azure.</span><span class="sxs-lookup"><span data-stu-id="93d29-124">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="93d29-125">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="93d29-125">-RepositoryName</span></span>
<span data-ttu-id="93d29-126">Nome archivio.</span><span class="sxs-lookup"><span data-stu-id="93d29-126">Repository Name.</span></span>

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

### <span data-ttu-id="93d29-127">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="93d29-127">-WriteEnabled</span></span>
<span data-ttu-id="93d29-128">Abilitare la scrittura.</span><span class="sxs-lookup"><span data-stu-id="93d29-128">Write enable.</span></span>

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

### <span data-ttu-id="93d29-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93d29-129">-Confirm</span></span>
<span data-ttu-id="93d29-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93d29-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93d29-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93d29-131">-WhatIf</span></span>
<span data-ttu-id="93d29-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="93d29-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93d29-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="93d29-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93d29-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93d29-134">CommonParameters</span></span>
<span data-ttu-id="93d29-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93d29-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93d29-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="93d29-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93d29-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="93d29-137">INPUTS</span></span>

### <span data-ttu-id="93d29-138">System.String</span><span class="sxs-lookup"><span data-stu-id="93d29-138">System.String</span></span>

## <span data-ttu-id="93d29-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93d29-139">OUTPUTS</span></span>

### <span data-ttu-id="93d29-140">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span><span class="sxs-lookup"><span data-stu-id="93d29-140">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span></span>

## <span data-ttu-id="93d29-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="93d29-141">NOTES</span></span>

## <span data-ttu-id="93d29-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93d29-142">RELATED LINKS</span></span>
