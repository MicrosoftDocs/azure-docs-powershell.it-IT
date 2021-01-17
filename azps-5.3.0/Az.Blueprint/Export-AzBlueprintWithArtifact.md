---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 647d626a0b4d59f219020d66c3c1ec8a5218355b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488732"
---
# <span data-ttu-id="b7ea0-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="b7ea0-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="b7ea0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b7ea0-102">SYNOPSIS</span></span>
<span data-ttu-id="b7ea0-103">Esportare la definizione del modello specificata nel percorso di output specificato come file JSON.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="b7ea0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7ea0-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7ea0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7ea0-105">DESCRIPTION</span></span>
<span data-ttu-id="b7ea0-106">Esportare una definizione Blueprint con i relativi elementi e Salva su disco.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="b7ea0-107">Questo cmdlet Esporta la versione più recente (bozza o pubblicata) della cianografia.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="b7ea0-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7ea0-108">EXAMPLES</span></span>

### <span data-ttu-id="b7ea0-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b7ea0-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="b7ea0-110">Esportare una definizione Blueprint con i relativi elementi e Salva su disco.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="b7ea0-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b7ea0-111">PARAMETERS</span></span>

### <span data-ttu-id="b7ea0-112">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="b7ea0-112">-Blueprint</span></span>
<span data-ttu-id="b7ea0-113">Oggetto definizione Blueprint da esportare.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-113">The blueprint definition object to export.</span></span>

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

### <span data-ttu-id="b7ea0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7ea0-114">-DefaultProfile</span></span>
<span data-ttu-id="b7ea0-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7ea0-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b7ea0-116">-Force</span></span>
<span data-ttu-id="b7ea0-117">Quando è impostato su true, l'esecuzione non richiederà una conferma.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-117">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="b7ea0-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="b7ea0-118">-OutputPath</span></span>
<span data-ttu-id="b7ea0-119">Percorso di un file su disco in cui esportare la definizione Blueprint in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

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

### <span data-ttu-id="b7ea0-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7ea0-120">-PassThru</span></span>
<span data-ttu-id="b7ea0-121">Quando viene impostato, il cmdlet restituirà un oggetto che rappresenta la definizione del modello esportato.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-121">When set, the cmdlet will return an object representing the exported blueprint definition.</span></span> <span data-ttu-id="b7ea0-122">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b7ea0-123">-Versione</span><span class="sxs-lookup"><span data-stu-id="b7ea0-123">-Version</span></span>
<span data-ttu-id="b7ea0-124">Versione di definizione del modello pubblicata.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-124">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="b7ea0-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b7ea0-125">-Confirm</span></span>
<span data-ttu-id="b7ea0-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7ea0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7ea0-127">-WhatIf</span></span>
<span data-ttu-id="b7ea0-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b7ea0-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7ea0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7ea0-130">CommonParameters</span></span>
<span data-ttu-id="b7ea0-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7ea0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7ea0-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7ea0-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7ea0-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b7ea0-133">INPUTS</span></span>

### <span data-ttu-id="b7ea0-134">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="b7ea0-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="b7ea0-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b7ea0-135">System.String</span></span>

## <span data-ttu-id="b7ea0-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7ea0-136">OUTPUTS</span></span>

### <span data-ttu-id="b7ea0-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b7ea0-137">System.String</span></span>

## <span data-ttu-id="b7ea0-138">Note</span><span class="sxs-lookup"><span data-stu-id="b7ea0-138">NOTES</span></span>

## <span data-ttu-id="b7ea0-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7ea0-139">RELATED LINKS</span></span>
