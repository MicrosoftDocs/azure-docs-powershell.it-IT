---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/powershell/module/az.marketplaceordering/get-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
ms.openlocfilehash: 9878bdaa508d2cc229f494dcd53467f9c7d62ed1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965757"
---
# <span data-ttu-id="8d51f-101">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="8d51f-101">Get-AzMarketplaceTerms</span></span>

## <span data-ttu-id="8d51f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d51f-102">SYNOPSIS</span></span>
<span data-ttu-id="8d51f-103">Ottenere le condizioni del contratto per un determinato ID editore (Publisher), ID offerta(Prodotto) e ID piano(Nome).</span><span class="sxs-lookup"><span data-stu-id="8d51f-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="8d51f-104">L'oggetto termini restituito da questo comando deve essere passato Set-AzMarketplaceTerms accettare le condizioni legali.</span><span class="sxs-lookup"><span data-stu-id="8d51f-104">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

## <span data-ttu-id="8d51f-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8d51f-105">SYNTAX</span></span>

```
Get-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d51f-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8d51f-106">DESCRIPTION</span></span>
<span data-ttu-id="8d51f-107">Il cmdlet **Get-AzMarketplaceTerms** restituisce i termini per la tupla ID autore (Publisher), ID offerta(Prodotto) e ID piano(Nome).</span><span class="sxs-lookup"><span data-stu-id="8d51f-107">The **Get-AzMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="8d51f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8d51f-108">EXAMPLES</span></span>

### <span data-ttu-id="8d51f-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8d51f-109">Example 1</span></span>
```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016"
Publisher         : microsoft-ads
Product           : windows-data-science-vm
Plan              : windows2016
LicenseTextLink   : <LicenseTextLink>
PrivacyPolicyLink : <PrivacyPolicyLink>
Signature         : <Signature>
Accepted          : True
RetrieveDatetime  : <RetrieveDatetime>
```

## <span data-ttu-id="8d51f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d51f-110">PARAMETERS</span></span>

### <span data-ttu-id="8d51f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d51f-111">-DefaultProfile</span></span>
<span data-ttu-id="8d51f-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8d51f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d51f-113">-Name</span><span class="sxs-lookup"><span data-stu-id="8d51f-113">-Name</span></span>
<span data-ttu-id="8d51f-114">Plan identifier string of image being deployed.</span><span class="sxs-lookup"><span data-stu-id="8d51f-114">Plan identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d51f-115">-Prodotto</span><span class="sxs-lookup"><span data-stu-id="8d51f-115">-Product</span></span>
<span data-ttu-id="8d51f-116">Stringa identificatore dell'offerta dell'immagine da distribuire.</span><span class="sxs-lookup"><span data-stu-id="8d51f-116">Offer identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d51f-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="8d51f-117">-Publisher</span></span>
<span data-ttu-id="8d51f-118">Stringa dell'identificatore dell'editore dell'immagine da distribuire.</span><span class="sxs-lookup"><span data-stu-id="8d51f-118">Publisher identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d51f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d51f-119">CommonParameters</span></span>
<span data-ttu-id="8d51f-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d51f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d51f-121">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d51f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d51f-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="8d51f-122">INPUTS</span></span>

### <span data-ttu-id="8d51f-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8d51f-123">None</span></span>

## <span data-ttu-id="8d51f-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8d51f-124">OUTPUTS</span></span>

### <span data-ttu-id="8d51f-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="8d51f-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="8d51f-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="8d51f-126">NOTES</span></span>

## <span data-ttu-id="8d51f-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8d51f-127">RELATED LINKS</span></span>
