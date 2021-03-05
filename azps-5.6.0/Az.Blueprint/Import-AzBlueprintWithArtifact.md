---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: eb0fddc34a83d5a23aeb990c920f36d7a3e03ff2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978877"
---
# <span data-ttu-id="b97cc-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="b97cc-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="b97cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b97cc-102">SYNOPSIS</span></span>
<span data-ttu-id="b97cc-103">Importare un file di progetto in formato JSON in un oggetto progetto e salvarlo all'interno della sottoscrizione o del gruppo di gestione specificato.</span><span class="sxs-lookup"><span data-stu-id="b97cc-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="b97cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b97cc-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-IncludeSubFolders] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b97cc-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b97cc-105">DESCRIPTION</span></span>
<span data-ttu-id="b97cc-106">Importare una definizione di progetto con i relativi elementi.</span><span class="sxs-lookup"><span data-stu-id="b97cc-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="b97cc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b97cc-107">EXAMPLES</span></span>

### <span data-ttu-id="b97cc-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b97cc-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="b97cc-109">Importare una definizione di progetto con i relativi elementi e salvarla all'interno di una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="b97cc-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="b97cc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b97cc-110">PARAMETERS</span></span>

### <span data-ttu-id="b97cc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b97cc-111">-DefaultProfile</span></span>
<span data-ttu-id="b97cc-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b97cc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b97cc-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b97cc-113">-Force</span></span>
<span data-ttu-id="b97cc-114">Se impostato su true, l'esecuzione non richiede una conferma.</span><span class="sxs-lookup"><span data-stu-id="b97cc-114">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="b97cc-115">-IncludeSubFolders</span><span class="sxs-lookup"><span data-stu-id="b97cc-115">-IncludeSubFolders</span></span>
<span data-ttu-id="b97cc-116">Se impostato su true, verrà incluso l'elemento nelle sottocartelle.</span><span class="sxs-lookup"><span data-stu-id="b97cc-116">When set to true, artifact in the subfolders will be included.</span></span>

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

### <span data-ttu-id="b97cc-117">-InputPath</span><span class="sxs-lookup"><span data-stu-id="b97cc-117">-InputPath</span></span>
<span data-ttu-id="b97cc-118">Percorso di un file JSON del progetto sul disco.</span><span class="sxs-lookup"><span data-stu-id="b97cc-118">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="b97cc-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="b97cc-119">-ManagementGroupId</span></span>
<span data-ttu-id="b97cc-120">ID gruppo di gestione in cui la definizione del progetto è o verrà salvata.</span><span class="sxs-lookup"><span data-stu-id="b97cc-120">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="b97cc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b97cc-121">-Name</span></span>
<span data-ttu-id="b97cc-122">Nome della definizione del progetto.</span><span class="sxs-lookup"><span data-stu-id="b97cc-122">Blueprint definition name.</span></span>

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

### <span data-ttu-id="b97cc-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b97cc-123">-PassThru</span></span>
<span data-ttu-id="b97cc-124">Quando è impostato, il cmdlet restituisce un oggetto che rappresenta la definizione del progetto importata.</span><span class="sxs-lookup"><span data-stu-id="b97cc-124">When set, the cmdlet will return an object representing the imported blueprint definition.</span></span> <span data-ttu-id="b97cc-125">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="b97cc-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b97cc-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b97cc-126">-SubscriptionId</span></span>
<span data-ttu-id="b97cc-127">ID abbonamento in cui verrà o sarà salvata la definizione del progetto.</span><span class="sxs-lookup"><span data-stu-id="b97cc-127">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="b97cc-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b97cc-128">-Confirm</span></span>
<span data-ttu-id="b97cc-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b97cc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b97cc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b97cc-130">-WhatIf</span></span>
<span data-ttu-id="b97cc-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b97cc-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b97cc-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b97cc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b97cc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b97cc-133">CommonParameters</span></span>
<span data-ttu-id="b97cc-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b97cc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b97cc-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b97cc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b97cc-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="b97cc-136">INPUTS</span></span>

### <span data-ttu-id="b97cc-137">System.String</span><span class="sxs-lookup"><span data-stu-id="b97cc-137">System.String</span></span>

## <span data-ttu-id="b97cc-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b97cc-138">OUTPUTS</span></span>

### <span data-ttu-id="b97cc-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b97cc-139">System.String</span></span>

## <span data-ttu-id="b97cc-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="b97cc-140">NOTES</span></span>

## <span data-ttu-id="b97cc-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b97cc-141">RELATED LINKS</span></span>
