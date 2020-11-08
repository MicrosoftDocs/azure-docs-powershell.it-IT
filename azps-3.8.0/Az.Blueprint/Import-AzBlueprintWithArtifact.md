---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: 7a1778ce107e9753f78876aff3a2dfba19e138e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021644"
---
# <span data-ttu-id="ef37f-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="ef37f-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="ef37f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ef37f-102">SYNOPSIS</span></span>
<span data-ttu-id="ef37f-103">Importare un file Blueprint in formato JSON in un oggetto Blueprint e salvarlo nell'ambito dell'abbonamento o del gruppo di gestione specificato.</span><span class="sxs-lookup"><span data-stu-id="ef37f-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="ef37f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ef37f-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef37f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef37f-105">DESCRIPTION</span></span>
<span data-ttu-id="ef37f-106">Importare una definizione Blueprint con i relativi elementi.</span><span class="sxs-lookup"><span data-stu-id="ef37f-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="ef37f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ef37f-107">EXAMPLES</span></span>

### <span data-ttu-id="ef37f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ef37f-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="ef37f-109">Importare una definizione Blueprint con i relativi elementi e salvarli all'interno di un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="ef37f-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="ef37f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ef37f-110">PARAMETERS</span></span>

### <span data-ttu-id="ef37f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef37f-111">-DefaultProfile</span></span>
<span data-ttu-id="ef37f-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ef37f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef37f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ef37f-113">-Force</span></span>
<span data-ttu-id="ef37f-114">Quando è impostato su true, l'esecuzione non richiederà una conferma.</span><span class="sxs-lookup"><span data-stu-id="ef37f-114">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="ef37f-115">-IncludeSubFolders</span><span class="sxs-lookup"><span data-stu-id="ef37f-115">-IncludeSubFolders</span></span>
<span data-ttu-id="ef37f-116">Quando è impostato su true, l'elemento nelle sottocartelle verrà incluso.</span><span class="sxs-lookup"><span data-stu-id="ef37f-116">When set to true, artifact in the subfolders will be included.</span></span>

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

### <span data-ttu-id="ef37f-117">-InputPath</span><span class="sxs-lookup"><span data-stu-id="ef37f-117">-InputPath</span></span>
<span data-ttu-id="ef37f-118">Percorso di un file JSON Blueprint su disco.</span><span class="sxs-lookup"><span data-stu-id="ef37f-118">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="ef37f-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="ef37f-119">-ManagementGroupId</span></span>
<span data-ttu-id="ef37f-120">ID gruppo di gestione in cui è o verrà salvata la definizione della cianografia.</span><span class="sxs-lookup"><span data-stu-id="ef37f-120">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="ef37f-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="ef37f-121">-Name</span></span>
<span data-ttu-id="ef37f-122">Nome definizione modello.</span><span class="sxs-lookup"><span data-stu-id="ef37f-122">Blueprint definition name.</span></span>

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

### <span data-ttu-id="ef37f-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ef37f-123">-SubscriptionId</span></span>
<span data-ttu-id="ef37f-124">ID sottoscrizione in cui la definizione del progetto è o verrà salvata.</span><span class="sxs-lookup"><span data-stu-id="ef37f-124">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="ef37f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef37f-125">CommonParameters</span></span>
<span data-ttu-id="ef37f-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef37f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ef37f-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef37f-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef37f-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ef37f-128">INPUTS</span></span>

### <span data-ttu-id="ef37f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ef37f-129">System.String</span></span>

## <span data-ttu-id="ef37f-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ef37f-130">OUTPUTS</span></span>

### <span data-ttu-id="ef37f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ef37f-131">System.String</span></span>

## <span data-ttu-id="ef37f-132">Note</span><span class="sxs-lookup"><span data-stu-id="ef37f-132">NOTES</span></span>

## <span data-ttu-id="ef37f-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ef37f-133">RELATED LINKS</span></span>
