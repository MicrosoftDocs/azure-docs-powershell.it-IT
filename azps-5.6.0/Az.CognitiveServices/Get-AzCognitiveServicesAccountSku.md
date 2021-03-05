---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
ms.openlocfilehash: eb9865d69d51fffc7488379bada256a812503a24
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981229"
---
# <span data-ttu-id="3a248-101">Get-AzCognitiveServicesAccountSku</span><span class="sxs-lookup"><span data-stu-id="3a248-101">Get-AzCognitiveServicesAccountSku</span></span>

## <span data-ttu-id="3a248-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a248-102">SYNOPSIS</span></span>
<span data-ttu-id="3a248-103">Recupera gli SKU disponibili per un account.</span><span class="sxs-lookup"><span data-stu-id="3a248-103">Gets the available SKUs for an account.</span></span>

## <span data-ttu-id="3a248-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3a248-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountSku [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a248-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3a248-105">DESCRIPTION</span></span>
<span data-ttu-id="3a248-106">Il cmdlet **Get-AzCognitiveServicesAccountSku** ottiene gli SKU disponibili per un account di Servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="3a248-106">The **Get-AzCognitiveServicesAccountSku** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="3a248-107">Lo SKU è il piano di livello per un account.</span><span class="sxs-lookup"><span data-stu-id="3a248-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="3a248-108">Definisce il prezzo, il limite di chiamata e la tariffa per l'account.</span><span class="sxs-lookup"><span data-stu-id="3a248-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="3a248-109">Lo SKU F0 è un livello gratuito.</span><span class="sxs-lookup"><span data-stu-id="3a248-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="3a248-110">I livelli a pagamento includono S0, S1, S2 e così via.</span><span class="sxs-lookup"><span data-stu-id="3a248-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="3a248-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3a248-111">EXAMPLES</span></span>

### <span data-ttu-id="3a248-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3a248-112">Example 1</span></span>
```powershell
PS C:\> (Get-AzCognitiveServicesAccountSku -Type 'TextAnalytics' -Location "westus").Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="3a248-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a248-113">PARAMETERS</span></span>

### <span data-ttu-id="3a248-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a248-114">-DefaultProfile</span></span>
<span data-ttu-id="3a248-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3a248-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a248-116">-Location</span><span class="sxs-lookup"><span data-stu-id="3a248-116">-Location</span></span>
<span data-ttu-id="3a248-117">Posizione dell'account di Servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="3a248-117">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="3a248-118">-Type</span><span class="sxs-lookup"><span data-stu-id="3a248-118">-Type</span></span>
<span data-ttu-id="3a248-119">Tipo di account di Servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="3a248-119">Cognitive Services Account Type.</span></span>

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

### <span data-ttu-id="3a248-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a248-120">CommonParameters</span></span>
<span data-ttu-id="3a248-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a248-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a248-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3a248-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a248-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="3a248-123">INPUTS</span></span>

### <span data-ttu-id="3a248-124">System.String</span><span class="sxs-lookup"><span data-stu-id="3a248-124">System.String</span></span>

## <span data-ttu-id="3a248-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3a248-125">OUTPUTS</span></span>

### <span data-ttu-id="3a248-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span><span class="sxs-lookup"><span data-stu-id="3a248-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span></span>

## <span data-ttu-id="3a248-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="3a248-127">NOTES</span></span>

## <span data-ttu-id="3a248-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3a248-128">RELATED LINKS</span></span>
