---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/get-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
ms.openlocfilehash: b729eb0ca1c0cc3b051600b59f260ebfb16d6b6e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180262"
---
# <span data-ttu-id="5f407-101">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="5f407-101">Get-AzMarketplaceTerms</span></span>

## <span data-ttu-id="5f407-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f407-102">SYNOPSIS</span></span>
<span data-ttu-id="5f407-103">Ottenere le condizioni del contratto per un determinato ID editore (Publisher), ID offerta(Prodotto) e ID piano(Nome).</span><span class="sxs-lookup"><span data-stu-id="5f407-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="5f407-104">L'oggetto termini restituito da questo comando deve essere passato Set-AzMarketplaceTerms accettare le condizioni legali.</span><span class="sxs-lookup"><span data-stu-id="5f407-104">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

## <span data-ttu-id="5f407-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5f407-105">SYNTAX</span></span>

```
Get-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f407-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5f407-106">DESCRIPTION</span></span>
<span data-ttu-id="5f407-107">Il cmdlet **Get-AzMarketplaceTerms** restituisce i termini per la tupla ID autore (Publisher), ID offerta(Prodotto) e ID piano(Nome).</span><span class="sxs-lookup"><span data-stu-id="5f407-107">The **Get-AzMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="5f407-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5f407-108">EXAMPLES</span></span>

### <span data-ttu-id="5f407-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5f407-109">Example 1</span></span>
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

## <span data-ttu-id="5f407-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f407-110">PARAMETERS</span></span>

### <span data-ttu-id="5f407-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f407-111">-DefaultProfile</span></span>
<span data-ttu-id="5f407-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5f407-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f407-113">-Name</span><span class="sxs-lookup"><span data-stu-id="5f407-113">-Name</span></span>
<span data-ttu-id="5f407-114">Stringa identificatore del piano per la distribuzione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="5f407-114">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="5f407-115">-Prodotto</span><span class="sxs-lookup"><span data-stu-id="5f407-115">-Product</span></span>
<span data-ttu-id="5f407-116">Stringa identificatore dell'offerta dell'immagine da distribuire.</span><span class="sxs-lookup"><span data-stu-id="5f407-116">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="5f407-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="5f407-117">-Publisher</span></span>
<span data-ttu-id="5f407-118">Stringa dell'identificatore dell'editore dell'immagine da distribuire.</span><span class="sxs-lookup"><span data-stu-id="5f407-118">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="5f407-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f407-119">CommonParameters</span></span>
<span data-ttu-id="5f407-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f407-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f407-121">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f407-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f407-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="5f407-122">INPUTS</span></span>

### <span data-ttu-id="5f407-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5f407-123">None</span></span>

## <span data-ttu-id="5f407-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5f407-124">OUTPUTS</span></span>

### <span data-ttu-id="5f407-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="5f407-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="5f407-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="5f407-126">NOTES</span></span>

## <span data-ttu-id="5f407-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5f407-127">RELATED LINKS</span></span>
