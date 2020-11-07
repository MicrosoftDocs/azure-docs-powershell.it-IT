---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: 3853cc1785ca0e9f087b1e30870d17d304666df4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675598"
---
# <span data-ttu-id="5149f-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="5149f-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="5149f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5149f-102">SYNOPSIS</span></span>
<span data-ttu-id="5149f-103">Importare un file Blueprint in formato JSON in un oggetto Blueprint e salvarlo nell'ambito dell'abbonamento o del gruppo di gestione specificato.</span><span class="sxs-lookup"><span data-stu-id="5149f-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="5149f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5149f-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5149f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5149f-105">DESCRIPTION</span></span>
<span data-ttu-id="5149f-106">Importare una definizione Blueprint con i relativi elementi.</span><span class="sxs-lookup"><span data-stu-id="5149f-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="5149f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5149f-107">EXAMPLES</span></span>

### <span data-ttu-id="5149f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5149f-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="5149f-109">Importare una definizione Blueprint con i relativi elementi e salvarli all'interno di un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="5149f-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="5149f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5149f-110">PARAMETERS</span></span>

### <span data-ttu-id="5149f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5149f-111">-DefaultProfile</span></span>
<span data-ttu-id="5149f-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5149f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5149f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="5149f-113">-Force</span></span>
<span data-ttu-id="5149f-114">Quando è impostato su true, l'esecuzione non richiederà una conferma.</span><span class="sxs-lookup"><span data-stu-id="5149f-114">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="5149f-115">-InputPath</span><span class="sxs-lookup"><span data-stu-id="5149f-115">-InputPath</span></span>
<span data-ttu-id="5149f-116">Percorso di un file JSON Blueprint su disco.</span><span class="sxs-lookup"><span data-stu-id="5149f-116">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="5149f-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="5149f-117">-ManagementGroupId</span></span>
<span data-ttu-id="5149f-118">ID gruppo di gestione in cui è o verrà salvata la definizione della cianografia.</span><span class="sxs-lookup"><span data-stu-id="5149f-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="5149f-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="5149f-119">-Name</span></span>
<span data-ttu-id="5149f-120">Nome definizione modello.</span><span class="sxs-lookup"><span data-stu-id="5149f-120">Blueprint definition name.</span></span>

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

### <span data-ttu-id="5149f-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5149f-121">-SubscriptionId</span></span>
<span data-ttu-id="5149f-122">ID sottoscrizione in cui la definizione del progetto è o verrà salvata.</span><span class="sxs-lookup"><span data-stu-id="5149f-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="5149f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5149f-123">CommonParameters</span></span>
<span data-ttu-id="5149f-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5149f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5149f-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5149f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5149f-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5149f-126">INPUTS</span></span>

### <span data-ttu-id="5149f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="5149f-127">System.String</span></span>

## <span data-ttu-id="5149f-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5149f-128">OUTPUTS</span></span>

### <span data-ttu-id="5149f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5149f-129">System.String</span></span>

## <span data-ttu-id="5149f-130">Note</span><span class="sxs-lookup"><span data-stu-id="5149f-130">NOTES</span></span>

## <span data-ttu-id="5149f-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5149f-131">RELATED LINKS</span></span>
