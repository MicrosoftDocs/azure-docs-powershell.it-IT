---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
ms.openlocfilehash: 3c632e6ffbf26e3aaacb725e9b663ffafbc49ec2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181767"
---
# <span data-ttu-id="0ee9b-101">Get-AzCognitiveServicesAccountSku</span><span class="sxs-lookup"><span data-stu-id="0ee9b-101">Get-AzCognitiveServicesAccountSku</span></span>

## <span data-ttu-id="0ee9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ee9b-102">SYNOPSIS</span></span>
<span data-ttu-id="0ee9b-103">Ottiene gli SKU disponibili per un account.</span><span class="sxs-lookup"><span data-stu-id="0ee9b-103">Gets the available SKUs for an account.</span></span>

## <span data-ttu-id="0ee9b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ee9b-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountSku [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ee9b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0ee9b-105">DESCRIPTION</span></span>
<span data-ttu-id="0ee9b-106">Il cmdlet **Get-AzCognitiveServicesAccountSku** ottiene gli SKU disponibili per un account di Servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="0ee9b-106">The **Get-AzCognitiveServicesAccountSku** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="0ee9b-107">Lo SKU è il piano di livello per un account.</span><span class="sxs-lookup"><span data-stu-id="0ee9b-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="0ee9b-108">Definisce il prezzo, il limite di chiamata e la tariffa per l'account.</span><span class="sxs-lookup"><span data-stu-id="0ee9b-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="0ee9b-109">Lo SKU F0 è un livello gratuito.</span><span class="sxs-lookup"><span data-stu-id="0ee9b-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="0ee9b-110">I livelli a pagamento includono S0, S1, S2 e così via.</span><span class="sxs-lookup"><span data-stu-id="0ee9b-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="0ee9b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ee9b-111">EXAMPLES</span></span>

### <span data-ttu-id="0ee9b-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0ee9b-112">Example 1</span></span>
```powershell
PS C:\> (Get-AzCognitiveServicesAccountSku -Type 'TextAnalytics' -Location "westus").Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="0ee9b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ee9b-113">PARAMETERS</span></span>

### <span data-ttu-id="0ee9b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ee9b-114">-DefaultProfile</span></span>
<span data-ttu-id="0ee9b-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="0ee9b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ee9b-116">-Location</span><span class="sxs-lookup"><span data-stu-id="0ee9b-116">-Location</span></span>
<span data-ttu-id="0ee9b-117">Posizione account di Servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="0ee9b-117">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="0ee9b-118">-Type</span><span class="sxs-lookup"><span data-stu-id="0ee9b-118">-Type</span></span>
<span data-ttu-id="0ee9b-119">Tipo di account di Servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="0ee9b-119">Cognitive Services Account Type.</span></span>

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

### <span data-ttu-id="0ee9b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ee9b-120">CommonParameters</span></span>
<span data-ttu-id="0ee9b-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ee9b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ee9b-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0ee9b-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ee9b-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="0ee9b-123">INPUTS</span></span>

### <span data-ttu-id="0ee9b-124">System.String</span><span class="sxs-lookup"><span data-stu-id="0ee9b-124">System.String</span></span>

## <span data-ttu-id="0ee9b-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ee9b-125">OUTPUTS</span></span>

### <span data-ttu-id="0ee9b-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span><span class="sxs-lookup"><span data-stu-id="0ee9b-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span></span>

## <span data-ttu-id="0ee9b-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="0ee9b-127">NOTES</span></span>

## <span data-ttu-id="0ee9b-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ee9b-128">RELATED LINKS</span></span>
