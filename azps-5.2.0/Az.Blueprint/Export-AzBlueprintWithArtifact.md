---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 647d626a0b4d59f219020d66c3c1ec8a5218355b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363859"
---
# <span data-ttu-id="6c9c5-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="6c9c5-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="6c9c5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6c9c5-102">SYNOPSIS</span></span>
<span data-ttu-id="6c9c5-103">Esportare la definizione del modello specificata nel percorso di output specificato come file JSON.</span><span class="sxs-lookup"><span data-stu-id="6c9c5-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="6c9c5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c9c5-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c9c5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c9c5-105">DESCRIPTION</span></span>
<span data-ttu-id="6c9c5-106">Esportare una definizione Blueprint con i relativi elementi e Salva su disco.</span><span class="sxs-lookup"><span data-stu-id="6c9c5-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="6c9c5-107">Questo cmdlet Esporta la versione più recente (bozza o pubblicata) della cianografia.</span><span class="sxs-lookup"><span data-stu-id="6c9c5-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="6c9c5-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c9c5-108">EXAMPLES</span></span>

### <span data-ttu-id="6c9c5-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6c9c5-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="6c9c5-110">Esportare una definizione Blueprint con i relativi elementi e Salva su disco.</span><span class="sxs-lookup"><span data-stu-id="6c9c5-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="6c9c5-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6c9c5-111">PARAMETERS</span></span>

### <span data-ttu-id="6c9c5-112">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="6c9c5-112">-Blueprint</span></span>
<span data-ttu-id="6c9c5-113">Oggetto definizione Blueprint da esportare.</span><span class="sxs-lookup"><span data-stu-id="6c9c5-113">The blueprint definition object to export.</span></span>

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

### <span data-ttu-id="6c9c5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c9c5-114">-DefaultProfile</span></span>
<span data-ttu-id="6c9c5-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6c9c5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c9c5-116">-Force</span><span class="sxs-lookup"><span data-stu-id="6c9c5-116">-Force</span></span>
<span data-ttu-id="6c9c5-117">Quando è impostato su true, l'esecuzione non richiederà una conferma.</span><span class="sxs-lookup"><span data-stu-id="6c9c5-117">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="6c9c5-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="6c9c5-118">-OutputPath</span></span>
<span data-ttu-id="6c9c5-119">Percorso di un file su disco in cui esportare la definizione Blueprint in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="6c9c5-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

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

### <span data-ttu-id="6c9c5-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c9c5-120">-PassThru</span></span>
<span data-ttu-id="6c9c5-121">Quando viene impostato, il cmdlet restituirà un oggetto che rappresenta la definizione del modello esportato.</span><span class="sxs-lookup"><span data-stu-id="6c9c5-121">When set, the cmdlet will return an object representing the exported blueprint definition.</span></span> <span data-ttu-id="6c9c5-122">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="6c9c5-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6c9c5-123">-Versione</span><span class="sxs-lookup"><span data-stu-id="6c9c5-123">-Version</span></span>
<span data-ttu-id="6c9c5-124">Versione di definizione del modello pubblicata.</span><span class="sxs-lookup"><span data-stu-id="6c9c5-124">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="6c9c5-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6c9c5-125">-Confirm</span></span>
<span data-ttu-id="6c9c5-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c9c5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c9c5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c9c5-127">-WhatIf</span></span>
<span data-ttu-id="6c9c5-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c9c5-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6c9c5-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c9c5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c9c5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c9c5-130">CommonParameters</span></span>
<span data-ttu-id="6c9c5-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c9c5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c9c5-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c9c5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c9c5-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6c9c5-133">INPUTS</span></span>

### <span data-ttu-id="6c9c5-134">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="6c9c5-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="6c9c5-135">System. String</span><span class="sxs-lookup"><span data-stu-id="6c9c5-135">System.String</span></span>

## <span data-ttu-id="6c9c5-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c9c5-136">OUTPUTS</span></span>

### <span data-ttu-id="6c9c5-137">System. String</span><span class="sxs-lookup"><span data-stu-id="6c9c5-137">System.String</span></span>

## <span data-ttu-id="6c9c5-138">Note</span><span class="sxs-lookup"><span data-stu-id="6c9c5-138">NOTES</span></span>

## <span data-ttu-id="6c9c5-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c9c5-139">RELATED LINKS</span></span>
