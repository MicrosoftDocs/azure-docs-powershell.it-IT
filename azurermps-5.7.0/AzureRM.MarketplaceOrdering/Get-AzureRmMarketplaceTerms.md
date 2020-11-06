---
external help file: Microsoft.Azure.Commands.MarketplaceOrdering.dll-Help.xml
Module Name: AzureRM.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.marketplaceordering/get-azurermmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Get-AzureRmMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Get-AzureRmMarketplaceTerms.md
ms.openlocfilehash: b6f5b0ddecea600b0d3a7b23ad526b78417ae993
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509844"
---
# <span data-ttu-id="a94e4-101">Get-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="a94e4-101">Get-AzureRmMarketplaceTerms</span></span>

## <span data-ttu-id="a94e4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a94e4-102">SYNOPSIS</span></span>
<span data-ttu-id="a94e4-103">Ottenere le condizioni di contratto per un ID editore (Publisher), un ID offerta (prodotto) e un ID piano (nome).</span><span class="sxs-lookup"><span data-stu-id="a94e4-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="a94e4-104">L'oggetto termini restituito da questo comando deve essere passato a Set-AzureRmMarketplaceTerms per accettare le condizioni legali.</span><span class="sxs-lookup"><span data-stu-id="a94e4-104">The terms object which is returned by this command should be passed to Set-AzureRmMarketplaceTerms to accept the legal terms.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a94e4-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a94e4-105">SYNTAX</span></span>

```
Get-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a94e4-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a94e4-106">DESCRIPTION</span></span>
<span data-ttu-id="a94e4-107">Il cmdlet **Get-AzureRmMarketplaceTerms** restituisce i termini per l'ID editore (Publisher), l'ID offerta (Product) e la tupla ID piano (nome).</span><span class="sxs-lookup"><span data-stu-id="a94e4-107">The **Get-AzureRmMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="a94e4-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a94e4-108">EXAMPLES</span></span>

### <span data-ttu-id="a94e4-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a94e4-109">Example 1</span></span>
```
PS C:\> Get-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016"
Publisher         : microsoft-ads
Product           : windows-data-science-vm
Plan              : windows2016
LicenseTextLink   : <LicenseTextLink>
PrivacyPolicyLink : <PrivacyPolicyLink>
Signature         : <Signature>
Accepted          : True
RetrieveDatetime  : <RetrieveDatetime>
```

## <span data-ttu-id="a94e4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a94e4-110">PARAMETERS</span></span>

### <span data-ttu-id="a94e4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a94e4-111">-DefaultProfile</span></span>
<span data-ttu-id="a94e4-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a94e4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a94e4-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="a94e4-113">-Name</span></span>
<span data-ttu-id="a94e4-114">Stringa identificatore piano dell'immagine da distribuire.</span><span class="sxs-lookup"><span data-stu-id="a94e4-114">Plan identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a94e4-115">-Prodotto</span><span class="sxs-lookup"><span data-stu-id="a94e4-115">-Product</span></span>
<span data-ttu-id="a94e4-116">Offerta identificatore stringa di immagine da distribuire.</span><span class="sxs-lookup"><span data-stu-id="a94e4-116">Offer identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a94e4-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="a94e4-117">-Publisher</span></span>
<span data-ttu-id="a94e4-118">Stringa dell'identificatore dell'editore dell'immagine da distribuire.</span><span class="sxs-lookup"><span data-stu-id="a94e4-118">Publisher identifier string of image being deployed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a94e4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a94e4-119">CommonParameters</span></span>
<span data-ttu-id="a94e4-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a94e4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a94e4-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a94e4-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a94e4-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a94e4-122">INPUTS</span></span>

### <span data-ttu-id="a94e4-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a94e4-123">None</span></span>

## <span data-ttu-id="a94e4-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a94e4-124">OUTPUTS</span></span>

### <span data-ttu-id="a94e4-125">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="a94e4-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="a94e4-126">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="a94e4-126">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="a94e4-127">Note</span><span class="sxs-lookup"><span data-stu-id="a94e4-127">NOTES</span></span>

## <span data-ttu-id="a94e4-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a94e4-128">RELATED LINKS</span></span>

