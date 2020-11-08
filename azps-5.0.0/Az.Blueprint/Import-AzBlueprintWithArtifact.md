---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: 43877ecb7fe7e90f0619a26a54eea534ac1390b3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199572"
---
# <span data-ttu-id="fa142-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="fa142-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="fa142-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fa142-102">SYNOPSIS</span></span>
<span data-ttu-id="fa142-103">Importare un file Blueprint in formato JSON in un oggetto Blueprint e salvarlo nell'ambito dell'abbonamento o del gruppo di gestione specificato.</span><span class="sxs-lookup"><span data-stu-id="fa142-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="fa142-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fa142-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-IncludeSubFolders] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa142-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa142-105">DESCRIPTION</span></span>
<span data-ttu-id="fa142-106">Importare una definizione Blueprint con i relativi elementi.</span><span class="sxs-lookup"><span data-stu-id="fa142-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="fa142-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fa142-107">EXAMPLES</span></span>

### <span data-ttu-id="fa142-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fa142-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="fa142-109">Importare una definizione Blueprint con i relativi elementi e salvarli all'interno di un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="fa142-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="fa142-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fa142-110">PARAMETERS</span></span>

### <span data-ttu-id="fa142-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa142-111">-DefaultProfile</span></span>
<span data-ttu-id="fa142-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fa142-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa142-113">-Force</span><span class="sxs-lookup"><span data-stu-id="fa142-113">-Force</span></span>
<span data-ttu-id="fa142-114">Quando è impostato su true, l'esecuzione non richiederà una conferma.</span><span class="sxs-lookup"><span data-stu-id="fa142-114">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="fa142-115">-IncludeSubFolders</span><span class="sxs-lookup"><span data-stu-id="fa142-115">-IncludeSubFolders</span></span>
<span data-ttu-id="fa142-116">Quando è impostato su true, l'elemento nelle sottocartelle verrà incluso.</span><span class="sxs-lookup"><span data-stu-id="fa142-116">When set to true, artifact in the subfolders will be included.</span></span>

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

### <span data-ttu-id="fa142-117">-InputPath</span><span class="sxs-lookup"><span data-stu-id="fa142-117">-InputPath</span></span>
<span data-ttu-id="fa142-118">Percorso di un file JSON Blueprint su disco.</span><span class="sxs-lookup"><span data-stu-id="fa142-118">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="fa142-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="fa142-119">-ManagementGroupId</span></span>
<span data-ttu-id="fa142-120">ID gruppo di gestione in cui è o verrà salvata la definizione della cianografia.</span><span class="sxs-lookup"><span data-stu-id="fa142-120">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="fa142-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="fa142-121">-Name</span></span>
<span data-ttu-id="fa142-122">Nome definizione modello.</span><span class="sxs-lookup"><span data-stu-id="fa142-122">Blueprint definition name.</span></span>

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

### <span data-ttu-id="fa142-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa142-123">-PassThru</span></span>
<span data-ttu-id="fa142-124">Quando viene impostato, il cmdlet restituirà un oggetto che rappresenta la definizione del modello importato.</span><span class="sxs-lookup"><span data-stu-id="fa142-124">When set, the cmdlet will return an object representing the imported blueprint definition.</span></span> <span data-ttu-id="fa142-125">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="fa142-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fa142-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fa142-126">-SubscriptionId</span></span>
<span data-ttu-id="fa142-127">ID sottoscrizione in cui la definizione del progetto è o verrà salvata.</span><span class="sxs-lookup"><span data-stu-id="fa142-127">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="fa142-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fa142-128">-Confirm</span></span>
<span data-ttu-id="fa142-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa142-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa142-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa142-130">-WhatIf</span></span>
<span data-ttu-id="fa142-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fa142-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fa142-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fa142-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa142-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa142-133">CommonParameters</span></span>
<span data-ttu-id="fa142-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa142-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa142-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa142-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa142-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fa142-136">INPUTS</span></span>

### <span data-ttu-id="fa142-137">System. String</span><span class="sxs-lookup"><span data-stu-id="fa142-137">System.String</span></span>

## <span data-ttu-id="fa142-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fa142-138">OUTPUTS</span></span>

### <span data-ttu-id="fa142-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fa142-139">System.String</span></span>

## <span data-ttu-id="fa142-140">Note</span><span class="sxs-lookup"><span data-stu-id="fa142-140">NOTES</span></span>

## <span data-ttu-id="fa142-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fa142-141">RELATED LINKS</span></span>
