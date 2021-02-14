---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: 43877ecb7fe7e90f0619a26a54eea534ac1390b3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181951"
---
# <span data-ttu-id="500fe-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="500fe-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="500fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="500fe-102">SYNOPSIS</span></span>
<span data-ttu-id="500fe-103">Importare un file di progetto in formato JSON in un oggetto progetto e salvarlo all'interno della sottoscrizione o del gruppo di gestione specificato.</span><span class="sxs-lookup"><span data-stu-id="500fe-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="500fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="500fe-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-IncludeSubFolders] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="500fe-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="500fe-105">DESCRIPTION</span></span>
<span data-ttu-id="500fe-106">Importare una definizione di progetto con i relativi elementi.</span><span class="sxs-lookup"><span data-stu-id="500fe-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="500fe-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="500fe-107">EXAMPLES</span></span>

### <span data-ttu-id="500fe-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="500fe-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="500fe-109">Importare una definizione di progetto con i relativi elementi e salvarla all'interno di una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="500fe-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="500fe-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="500fe-110">PARAMETERS</span></span>

### <span data-ttu-id="500fe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="500fe-111">-DefaultProfile</span></span>
<span data-ttu-id="500fe-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="500fe-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="500fe-113">-Force</span><span class="sxs-lookup"><span data-stu-id="500fe-113">-Force</span></span>
<span data-ttu-id="500fe-114">Se impostato su true, l'esecuzione non richiede una conferma.</span><span class="sxs-lookup"><span data-stu-id="500fe-114">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="500fe-115">-IncludeSubFolders</span><span class="sxs-lookup"><span data-stu-id="500fe-115">-IncludeSubFolders</span></span>
<span data-ttu-id="500fe-116">Se impostato su true, verrà incluso l'elemento nelle sottocartelle.</span><span class="sxs-lookup"><span data-stu-id="500fe-116">When set to true, artifact in the subfolders will be included.</span></span>

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

### <span data-ttu-id="500fe-117">-InputPath</span><span class="sxs-lookup"><span data-stu-id="500fe-117">-InputPath</span></span>
<span data-ttu-id="500fe-118">Percorso di un file JSON del progetto sul disco.</span><span class="sxs-lookup"><span data-stu-id="500fe-118">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="500fe-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="500fe-119">-ManagementGroupId</span></span>
<span data-ttu-id="500fe-120">ID gruppo di gestione in cui la definizione del progetto è o verrà salvata.</span><span class="sxs-lookup"><span data-stu-id="500fe-120">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="500fe-121">-Name</span><span class="sxs-lookup"><span data-stu-id="500fe-121">-Name</span></span>
<span data-ttu-id="500fe-122">Nome della definizione del progetto.</span><span class="sxs-lookup"><span data-stu-id="500fe-122">Blueprint definition name.</span></span>

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

### <span data-ttu-id="500fe-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="500fe-123">-PassThru</span></span>
<span data-ttu-id="500fe-124">Quando è impostato, il cmdlet restituisce un oggetto che rappresenta la definizione del progetto importata.</span><span class="sxs-lookup"><span data-stu-id="500fe-124">When set, the cmdlet will return an object representing the imported blueprint definition.</span></span> <span data-ttu-id="500fe-125">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="500fe-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="500fe-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="500fe-126">-SubscriptionId</span></span>
<span data-ttu-id="500fe-127">ID abbonamento in cui verrà o sarà salvata la definizione del progetto.</span><span class="sxs-lookup"><span data-stu-id="500fe-127">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="500fe-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="500fe-128">-Confirm</span></span>
<span data-ttu-id="500fe-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="500fe-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="500fe-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="500fe-130">-WhatIf</span></span>
<span data-ttu-id="500fe-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="500fe-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="500fe-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="500fe-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="500fe-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="500fe-133">CommonParameters</span></span>
<span data-ttu-id="500fe-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="500fe-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="500fe-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="500fe-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="500fe-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="500fe-136">INPUTS</span></span>

### <span data-ttu-id="500fe-137">System.String</span><span class="sxs-lookup"><span data-stu-id="500fe-137">System.String</span></span>

## <span data-ttu-id="500fe-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="500fe-138">OUTPUTS</span></span>

### <span data-ttu-id="500fe-139">System.String</span><span class="sxs-lookup"><span data-stu-id="500fe-139">System.String</span></span>

## <span data-ttu-id="500fe-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="500fe-140">NOTES</span></span>

## <span data-ttu-id="500fe-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="500fe-141">RELATED LINKS</span></span>
