---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/publish-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
ms.openlocfilehash: 5286b8953a9f28c5e63fe176f19d9d885e9c1d06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675592"
---
# <span data-ttu-id="a4a46-101">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="a4a46-101">Publish-AzBlueprint</span></span>

## <span data-ttu-id="a4a46-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a4a46-102">SYNOPSIS</span></span>
<span data-ttu-id="a4a46-103">Pubblicare una nuova versione di un modello.</span><span class="sxs-lookup"><span data-stu-id="a4a46-103">Publish a new version of a blueprint.</span></span>

## <span data-ttu-id="a4a46-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4a46-104">SYNTAX</span></span>

```
Publish-AzBlueprint -Version <String> -ChangeNote <String> -Blueprint <PSBlueprint> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4a46-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4a46-105">DESCRIPTION</span></span>
<span data-ttu-id="a4a46-106">Pubblicare una nuova versione di una definizione Blueprint.</span><span class="sxs-lookup"><span data-stu-id="a4a46-106">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="a4a46-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4a46-107">EXAMPLES</span></span>

### <span data-ttu-id="a4a46-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a4a46-108">Example 1</span></span>
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
<span data-ttu-id="a4a46-109">Pubblicare una nuova versione di una definizione Blueprint.</span><span class="sxs-lookup"><span data-stu-id="a4a46-109">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="a4a46-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a4a46-110">PARAMETERS</span></span>

### <span data-ttu-id="a4a46-111">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="a4a46-111">-Blueprint</span></span>
<span data-ttu-id="a4a46-112">Oggetto Blueprint.</span><span class="sxs-lookup"><span data-stu-id="a4a46-112">Blueprint object.</span></span>

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

### <span data-ttu-id="a4a46-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4a46-113">-DefaultProfile</span></span>
<span data-ttu-id="a4a46-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a4a46-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4a46-115">-Versione</span><span class="sxs-lookup"><span data-stu-id="a4a46-115">-Version</span></span>
<span data-ttu-id="a4a46-116">Versione per la definizione del modello.</span><span class="sxs-lookup"><span data-stu-id="a4a46-116">Version for the blueprint definition.</span></span>

### <span data-ttu-id="a4a46-117">-ChangeNote</span><span class="sxs-lookup"><span data-stu-id="a4a46-117">-ChangeNote</span></span>
<span data-ttu-id="a4a46-118">Note per descrivere il contenuto di questa versione Blueprint.</span><span class="sxs-lookup"><span data-stu-id="a4a46-118">Notes to describe the contents of this blueprint version.</span></span>

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

### <span data-ttu-id="a4a46-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4a46-119">CommonParameters</span></span>
<span data-ttu-id="a4a46-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4a46-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a4a46-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4a46-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4a46-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a4a46-122">INPUTS</span></span>

### <span data-ttu-id="a4a46-123">System. String</span><span class="sxs-lookup"><span data-stu-id="a4a46-123">System.String</span></span>

### <span data-ttu-id="a4a46-124">Microsoft. Azure. Commands. Blueprint. Models. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="a4a46-124">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="a4a46-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4a46-125">OUTPUTS</span></span>

### <span data-ttu-id="a4a46-126">Microsoft. Azure. Commands. Blueprint. Models. PSPublishedBlueprint</span><span class="sxs-lookup"><span data-stu-id="a4a46-126">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span></span>

## <span data-ttu-id="a4a46-127">Note</span><span class="sxs-lookup"><span data-stu-id="a4a46-127">NOTES</span></span>

## <span data-ttu-id="a4a46-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4a46-128">RELATED LINKS</span></span>
