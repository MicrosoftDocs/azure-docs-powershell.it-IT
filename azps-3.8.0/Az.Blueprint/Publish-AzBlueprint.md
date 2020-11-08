---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/publish-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
ms.openlocfilehash: e61beaa43f881aa148401ef91cd4cb37c1f18d88
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018949"
---
# <span data-ttu-id="42f18-101">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="42f18-101">Publish-AzBlueprint</span></span>

## <span data-ttu-id="42f18-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="42f18-102">SYNOPSIS</span></span>
<span data-ttu-id="42f18-103">Pubblicare una nuova versione di un modello.</span><span class="sxs-lookup"><span data-stu-id="42f18-103">Publish a new version of a blueprint.</span></span>

## <span data-ttu-id="42f18-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42f18-104">SYNTAX</span></span>

```
Publish-AzBlueprint -Version <String> -ChangeNote <String> -Blueprint <PSBlueprint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="42f18-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42f18-105">DESCRIPTION</span></span>
<span data-ttu-id="42f18-106">Pubblicare una nuova versione di una definizione Blueprint.</span><span class="sxs-lookup"><span data-stu-id="42f18-106">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="42f18-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42f18-107">EXAMPLES</span></span>

### <span data-ttu-id="42f18-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="42f18-108">Example 1</span></span>
```powershell
PS C:\> Publish-AzBlueprint -Blueprint $bp -Version 1.0 

Name           : SimpleBlueprint
Id             : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/versions/1.0
SubscriptionId : 00000000-1111-0000-1111-000000000000
Version        : 1.0
Description    : My simple blueprint
TimeCreated    : 2019-05-30
TargetScope    : Subscription
Parameters     : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroups : {storageRG}
```
<span data-ttu-id="42f18-109">Pubblicare una nuova versione di una definizione Blueprint.</span><span class="sxs-lookup"><span data-stu-id="42f18-109">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="42f18-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="42f18-110">PARAMETERS</span></span>

### <span data-ttu-id="42f18-111">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="42f18-111">-Blueprint</span></span>
<span data-ttu-id="42f18-112">Oggetto Blueprint.</span><span class="sxs-lookup"><span data-stu-id="42f18-112">Blueprint object.</span></span>

```yaml
Type: PSBlueprint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42f18-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42f18-113">-DefaultProfile</span></span>
<span data-ttu-id="42f18-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="42f18-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42f18-115">-Versione</span><span class="sxs-lookup"><span data-stu-id="42f18-115">-Version</span></span>
<span data-ttu-id="42f18-116">Versione per la definizione del modello.</span><span class="sxs-lookup"><span data-stu-id="42f18-116">Version for the blueprint definition.</span></span>

### <span data-ttu-id="42f18-117">-ChangeNote</span><span class="sxs-lookup"><span data-stu-id="42f18-117">-ChangeNote</span></span>
<span data-ttu-id="42f18-118">Note per descrivere il contenuto di questa versione Blueprint.</span><span class="sxs-lookup"><span data-stu-id="42f18-118">Notes to describe the contents of this blueprint version.</span></span>

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

### <span data-ttu-id="42f18-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42f18-119">CommonParameters</span></span>
<span data-ttu-id="42f18-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42f18-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="42f18-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42f18-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42f18-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="42f18-122">INPUTS</span></span>

### <span data-ttu-id="42f18-123">System. String</span><span class="sxs-lookup"><span data-stu-id="42f18-123">System.String</span></span>

### <span data-ttu-id="42f18-124">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="42f18-124">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="42f18-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42f18-125">OUTPUTS</span></span>

### <span data-ttu-id="42f18-126">Microsoft. Azure. Commands. Blueprint. Models. PSPublishedBlueprint</span><span class="sxs-lookup"><span data-stu-id="42f18-126">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span></span>

## <span data-ttu-id="42f18-127">Note</span><span class="sxs-lookup"><span data-stu-id="42f18-127">NOTES</span></span>

## <span data-ttu-id="42f18-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42f18-128">RELATED LINKS</span></span>
