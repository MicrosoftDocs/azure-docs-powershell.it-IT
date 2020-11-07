---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
ms.openlocfilehash: 7fe9a0e87d656063491d2787ad8afcdeb6fef4f2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675508"
---
# <span data-ttu-id="30eed-101">Get-AzCognitiveServicesAccountSku</span><span class="sxs-lookup"><span data-stu-id="30eed-101">Get-AzCognitiveServicesAccountSku</span></span>

## <span data-ttu-id="30eed-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="30eed-102">SYNOPSIS</span></span>
<span data-ttu-id="30eed-103">Ottiene le SKU disponibili per un account.</span><span class="sxs-lookup"><span data-stu-id="30eed-103">Gets the available SKUs for an account.</span></span>

## <span data-ttu-id="30eed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30eed-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountSku [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30eed-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30eed-105">DESCRIPTION</span></span>
<span data-ttu-id="30eed-106">Il cmdlet **Get-AzCognitiveServicesAccountSku** ottiene gli SKU disponibili per un account di servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="30eed-106">The **Get-AzCognitiveServicesAccountSku** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="30eed-107">L'USK è il piano di livello per un account.</span><span class="sxs-lookup"><span data-stu-id="30eed-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="30eed-108">Definisce il prezzo, il limite di chiamata e il tasso per l'account.</span><span class="sxs-lookup"><span data-stu-id="30eed-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="30eed-109">La SKU F0 è un livello gratuito.</span><span class="sxs-lookup"><span data-stu-id="30eed-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="30eed-110">I livelli a pagamento includono S0, S1, S2 e così via.</span><span class="sxs-lookup"><span data-stu-id="30eed-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="30eed-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30eed-111">EXAMPLES</span></span>

### <span data-ttu-id="30eed-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="30eed-112">Example 1</span></span>
```powershell
PS C:\> (Get-AzCognitiveServicesAccountSku -Type 'TextAnalytics' -Location "westus").Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="30eed-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="30eed-113">PARAMETERS</span></span>

### <span data-ttu-id="30eed-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30eed-114">-DefaultProfile</span></span>
<span data-ttu-id="30eed-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="30eed-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30eed-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="30eed-116">-Location</span></span>
<span data-ttu-id="30eed-117">Posizione dell'account dei servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="30eed-117">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="30eed-118">-Digitare</span><span class="sxs-lookup"><span data-stu-id="30eed-118">-Type</span></span>
<span data-ttu-id="30eed-119">Tipo di account servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="30eed-119">Cognitive Services Account Type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30eed-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30eed-120">CommonParameters</span></span>
<span data-ttu-id="30eed-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30eed-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30eed-122">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30eed-122">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30eed-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="30eed-123">INPUTS</span></span>

### <span data-ttu-id="30eed-124">System. String</span><span class="sxs-lookup"><span data-stu-id="30eed-124">System.String</span></span>

## <span data-ttu-id="30eed-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30eed-125">OUTPUTS</span></span>

### <span data-ttu-id="30eed-126">Microsoft. Azure. Management. CognitiveServices. Models. ResourceSku</span><span class="sxs-lookup"><span data-stu-id="30eed-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span></span>

## <span data-ttu-id="30eed-127">Note</span><span class="sxs-lookup"><span data-stu-id="30eed-127">NOTES</span></span>

## <span data-ttu-id="30eed-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30eed-128">RELATED LINKS</span></span>