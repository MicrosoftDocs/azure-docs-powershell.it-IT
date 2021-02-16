---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 647d626a0b4d59f219020d66c3c1ec8a5218355b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177887"
---
# <span data-ttu-id="c247c-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="c247c-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="c247c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c247c-102">SYNOPSIS</span></span>
<span data-ttu-id="c247c-103">Esportare la definizione del progetto specificata nella posizione di output specificata come file JSON.</span><span class="sxs-lookup"><span data-stu-id="c247c-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="c247c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c247c-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c247c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c247c-105">DESCRIPTION</span></span>
<span data-ttu-id="c247c-106">Esportare una definizione di progetto con i relativi elementi e salvarla su disco.</span><span class="sxs-lookup"><span data-stu-id="c247c-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="c247c-107">Questo cmdlet esporta la versione più recente (bozza o pubblicata) della progetto.</span><span class="sxs-lookup"><span data-stu-id="c247c-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="c247c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c247c-108">EXAMPLES</span></span>

### <span data-ttu-id="c247c-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c247c-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="c247c-110">Esportare una definizione di progetto con i relativi elementi e salvarla su disco.</span><span class="sxs-lookup"><span data-stu-id="c247c-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="c247c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c247c-111">PARAMETERS</span></span>

### <span data-ttu-id="c247c-112">-Progetto</span><span class="sxs-lookup"><span data-stu-id="c247c-112">-Blueprint</span></span>
<span data-ttu-id="c247c-113">Oggetto di definizione della progetto da esportare.</span><span class="sxs-lookup"><span data-stu-id="c247c-113">The blueprint definition object to export.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c247c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c247c-114">-DefaultProfile</span></span>
<span data-ttu-id="c247c-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c247c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c247c-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c247c-116">-Force</span></span>
<span data-ttu-id="c247c-117">Se impostato su true, l'esecuzione non richiede una conferma.</span><span class="sxs-lookup"><span data-stu-id="c247c-117">When set to true, execution will not ask for a confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c247c-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="c247c-118">-OutputPath</span></span>
<span data-ttu-id="c247c-119">Percorso di un file sul disco in cui esportare la definizione del progetto in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="c247c-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

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

### <span data-ttu-id="c247c-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c247c-120">-PassThru</span></span>
<span data-ttu-id="c247c-121">Quando è impostato, il cmdlet restituisce un oggetto che rappresenta la definizione del progetto esportata.</span><span class="sxs-lookup"><span data-stu-id="c247c-121">When set, the cmdlet will return an object representing the exported blueprint definition.</span></span> <span data-ttu-id="c247c-122">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="c247c-122">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c247c-123">-Version</span><span class="sxs-lookup"><span data-stu-id="c247c-123">-Version</span></span>
<span data-ttu-id="c247c-124">Versione della definizione del progetto pubblicata.</span><span class="sxs-lookup"><span data-stu-id="c247c-124">Published blueprint definition version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c247c-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c247c-125">-Confirm</span></span>
<span data-ttu-id="c247c-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c247c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c247c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c247c-127">-WhatIf</span></span>
<span data-ttu-id="c247c-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c247c-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c247c-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c247c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c247c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c247c-130">CommonParameters</span></span>
<span data-ttu-id="c247c-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c247c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c247c-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c247c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c247c-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="c247c-133">INPUTS</span></span>

### <span data-ttu-id="c247c-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="c247c-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="c247c-135">System.String</span><span class="sxs-lookup"><span data-stu-id="c247c-135">System.String</span></span>

## <span data-ttu-id="c247c-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c247c-136">OUTPUTS</span></span>

### <span data-ttu-id="c247c-137">System.String</span><span class="sxs-lookup"><span data-stu-id="c247c-137">System.String</span></span>

## <span data-ttu-id="c247c-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="c247c-138">NOTES</span></span>

## <span data-ttu-id="c247c-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c247c-139">RELATED LINKS</span></span>
