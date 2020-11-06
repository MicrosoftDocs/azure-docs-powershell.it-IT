---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
ms.openlocfilehash: de2640d8a2044a8124fb87bed53b9ee433977716
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516979"
---
# <span data-ttu-id="2fc98-101">Get-AzureRmCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="2fc98-101">Get-AzureRmCognitiveServicesAccountSkus</span></span>

## <span data-ttu-id="2fc98-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2fc98-102">SYNOPSIS</span></span>
<span data-ttu-id="2fc98-103">Ottiene le SKU disponibili per un account.</span><span class="sxs-lookup"><span data-stu-id="2fc98-103">Gets the available SKUs for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fc98-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2fc98-104">SYNTAX</span></span>

```
Get-AzureRmCognitiveServicesAccountSkus [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fc98-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2fc98-105">DESCRIPTION</span></span>
<span data-ttu-id="2fc98-106">Il cmdlet **Get-AzureRmCognitiveServicesAccountSkus** ottiene gli SKU disponibili per un account di servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="2fc98-106">The **Get-AzureRmCognitiveServicesAccountSkus** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>

<span data-ttu-id="2fc98-107">L'USK è il piano di livello per un account.</span><span class="sxs-lookup"><span data-stu-id="2fc98-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="2fc98-108">Definisce il prezzo, il limite di chiamata e il tasso per l'account.</span><span class="sxs-lookup"><span data-stu-id="2fc98-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="2fc98-109">La SKU F0 è un livello gratuito.</span><span class="sxs-lookup"><span data-stu-id="2fc98-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="2fc98-110">I livelli a pagamento includono S0, S1, S2 e così via.</span><span class="sxs-lookup"><span data-stu-id="2fc98-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="2fc98-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2fc98-111">EXAMPLES</span></span>

## <span data-ttu-id="2fc98-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2fc98-112">PARAMETERS</span></span>

### <span data-ttu-id="2fc98-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="2fc98-113">-Name</span></span>
<span data-ttu-id="2fc98-114">Specifica il nome dell'account.</span><span class="sxs-lookup"><span data-stu-id="2fc98-114">Specifies the name of the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fc98-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fc98-115">-ResourceGroupName</span></span>
<span data-ttu-id="2fc98-116">Specifica il nome del gruppo di risorse a cui è assegnato l'account.</span><span class="sxs-lookup"><span data-stu-id="2fc98-116">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fc98-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fc98-117">-DefaultProfile</span></span>
<span data-ttu-id="2fc98-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2fc98-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fc98-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fc98-119">CommonParameters</span></span>
<span data-ttu-id="2fc98-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fc98-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fc98-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fc98-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fc98-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2fc98-122">INPUTS</span></span>

## <span data-ttu-id="2fc98-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2fc98-123">OUTPUTS</span></span>

### <span data-ttu-id="2fc98-124">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesSkus</span><span class="sxs-lookup"><span data-stu-id="2fc98-124">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesSkus</span></span>

## <span data-ttu-id="2fc98-125">Note</span><span class="sxs-lookup"><span data-stu-id="2fc98-125">NOTES</span></span>

## <span data-ttu-id="2fc98-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2fc98-126">RELATED LINKS</span></span>

