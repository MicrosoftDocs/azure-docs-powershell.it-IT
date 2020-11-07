---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 2c349d99e8a3529d4f1423a43bd31ab2500664c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675610"
---
# <span data-ttu-id="38c38-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="38c38-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="38c38-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="38c38-102">SYNOPSIS</span></span>
<span data-ttu-id="38c38-103">Esportare la definizione del modello specificata nel percorso di output specificato come file JSON.</span><span class="sxs-lookup"><span data-stu-id="38c38-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="38c38-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38c38-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38c38-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38c38-105">DESCRIPTION</span></span>
<span data-ttu-id="38c38-106">Esportare una definizione Blueprint con i relativi elementi e Salva su disco.</span><span class="sxs-lookup"><span data-stu-id="38c38-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="38c38-107">Questo cmdlet Esporta la versione più recente (bozza o pubblicata) della cianografia.</span><span class="sxs-lookup"><span data-stu-id="38c38-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="38c38-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38c38-108">EXAMPLES</span></span>

### <span data-ttu-id="38c38-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="38c38-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="38c38-110">Esportare una definizione Blueprint con i relativi elementi e Salva su disco.</span><span class="sxs-lookup"><span data-stu-id="38c38-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="38c38-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38c38-111">PARAMETERS</span></span>

### <span data-ttu-id="38c38-112">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="38c38-112">-Blueprint</span></span>
<span data-ttu-id="38c38-113">Oggetto definizione Blueprint da esportare.</span><span class="sxs-lookup"><span data-stu-id="38c38-113">The blueprint definition object to export.</span></span>

```yaml
Type: PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38c38-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38c38-114">-DefaultProfile</span></span>
<span data-ttu-id="38c38-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38c38-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38c38-116">-Force</span><span class="sxs-lookup"><span data-stu-id="38c38-116">-Force</span></span>
<span data-ttu-id="38c38-117">Quando è impostato su true, l'esecuzione non richiederà una conferma.</span><span class="sxs-lookup"><span data-stu-id="38c38-117">When set to true, execution will not ask for a confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38c38-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="38c38-118">-OutputPath</span></span>
<span data-ttu-id="38c38-119">Percorso di un file su disco in cui esportare la definizione Blueprint in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="38c38-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38c38-120">-Versione</span><span class="sxs-lookup"><span data-stu-id="38c38-120">-Version</span></span>
<span data-ttu-id="38c38-121">Versione di definizione del modello pubblicata.</span><span class="sxs-lookup"><span data-stu-id="38c38-121">Published blueprint definition version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38c38-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38c38-122">CommonParameters</span></span>
<span data-ttu-id="38c38-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38c38-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="38c38-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38c38-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38c38-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="38c38-125">INPUTS</span></span>

### <span data-ttu-id="38c38-126">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="38c38-126">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="38c38-127">System. String</span><span class="sxs-lookup"><span data-stu-id="38c38-127">System.String</span></span>

## <span data-ttu-id="38c38-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38c38-128">OUTPUTS</span></span>

### <span data-ttu-id="38c38-129">System. String</span><span class="sxs-lookup"><span data-stu-id="38c38-129">System.String</span></span>

## <span data-ttu-id="38c38-130">Note</span><span class="sxs-lookup"><span data-stu-id="38c38-130">NOTES</span></span>

## <span data-ttu-id="38c38-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38c38-131">RELATED LINKS</span></span>
