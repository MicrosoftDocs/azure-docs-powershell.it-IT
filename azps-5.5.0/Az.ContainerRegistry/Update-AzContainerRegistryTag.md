---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryTag.md
ms.openlocfilehash: 48fb77eb9c718a09a7e13e6d6ab5af5bfc60c912
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204666"
---
# <span data-ttu-id="d011a-101">Update-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="d011a-101">Update-AzContainerRegistryTag</span></span>

## <span data-ttu-id="d011a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d011a-102">SYNOPSIS</span></span>
<span data-ttu-id="d011a-103">Aggiornare il tag ACR.</span><span class="sxs-lookup"><span data-stu-id="d011a-103">Update ACR tag.</span></span>

## <span data-ttu-id="d011a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d011a-104">SYNTAX</span></span>

```
Update-AzContainerRegistryTag -RepositoryName <String> -Name <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d011a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d011a-105">DESCRIPTION</span></span>
<span data-ttu-id="d011a-106">Aggiornare il tag ACR.</span><span class="sxs-lookup"><span data-stu-id="d011a-106">Update ACR tag.</span></span>
<span data-ttu-id="d011a-107">Per usare questo cmdlet, esegui `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="d011a-107">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span></span>
<span data-ttu-id="d011a-108">per prima cosa.</span><span class="sxs-lookup"><span data-stu-id="d011a-108">first.</span></span>

## <span data-ttu-id="d011a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d011a-109">EXAMPLES</span></span>

### <span data-ttu-id="d011a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d011a-110">Example 1</span></span>
```powershell
Update-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -Name latest -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute
```

<span data-ttu-id="d011a-111">Aggiornare gli attributi per il tag più recente nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="d011a-111">Update attributes for tag latest under registry.</span></span>

## <span data-ttu-id="d011a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d011a-112">PARAMETERS</span></span>

### <span data-ttu-id="d011a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d011a-113">-DefaultProfile</span></span>
<span data-ttu-id="d011a-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d011a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d011a-115">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="d011a-115">-DeleteEnabled</span></span>
<span data-ttu-id="d011a-116">Elimina abilita.</span><span class="sxs-lookup"><span data-stu-id="d011a-116">Delete enable.</span></span>

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

### <span data-ttu-id="d011a-117">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="d011a-117">-ListEnabled</span></span>
<span data-ttu-id="d011a-118">Abilitazione dell'elenco.</span><span class="sxs-lookup"><span data-stu-id="d011a-118">List enable.</span></span>

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

### <span data-ttu-id="d011a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d011a-119">-Name</span></span>
<span data-ttu-id="d011a-120">Contrassegno.</span><span class="sxs-lookup"><span data-stu-id="d011a-120">Tag.</span></span>

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

### <span data-ttu-id="d011a-121">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="d011a-121">-ReadEnabled</span></span>
<span data-ttu-id="d011a-122">Abilitare la lettura.</span><span class="sxs-lookup"><span data-stu-id="d011a-122">Read enable.</span></span>

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

### <span data-ttu-id="d011a-123">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="d011a-123">-RegistryName</span></span>
<span data-ttu-id="d011a-124">Nome del Registro di sistema del contenitore di Azure.</span><span class="sxs-lookup"><span data-stu-id="d011a-124">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="d011a-125">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="d011a-125">-RepositoryName</span></span>
<span data-ttu-id="d011a-126">Nome archivio.</span><span class="sxs-lookup"><span data-stu-id="d011a-126">Repository Name.</span></span>

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

### <span data-ttu-id="d011a-127">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="d011a-127">-WriteEnabled</span></span>
<span data-ttu-id="d011a-128">Abilitare la scrittura.</span><span class="sxs-lookup"><span data-stu-id="d011a-128">Write enable.</span></span>

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

### <span data-ttu-id="d011a-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d011a-129">-Confirm</span></span>
<span data-ttu-id="d011a-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d011a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d011a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d011a-131">-WhatIf</span></span>
<span data-ttu-id="d011a-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d011a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d011a-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d011a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d011a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d011a-134">CommonParameters</span></span>
<span data-ttu-id="d011a-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d011a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d011a-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d011a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d011a-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="d011a-137">INPUTS</span></span>

### <span data-ttu-id="d011a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d011a-138">System.String</span></span>

## <span data-ttu-id="d011a-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d011a-139">OUTPUTS</span></span>

### <span data-ttu-id="d011a-140">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span><span class="sxs-lookup"><span data-stu-id="d011a-140">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span></span>

## <span data-ttu-id="d011a-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="d011a-141">NOTES</span></span>

## <span data-ttu-id="d011a-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d011a-142">RELATED LINKS</span></span>
