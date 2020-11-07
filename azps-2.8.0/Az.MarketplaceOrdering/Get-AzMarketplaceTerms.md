---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/get-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
ms.openlocfilehash: 730861b055259fd0aee5490de2421abe96afc10b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673868"
---
# <span data-ttu-id="ca032-101">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="ca032-101">Get-AzMarketplaceTerms</span></span>

## <span data-ttu-id="ca032-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ca032-102">SYNOPSIS</span></span>
<span data-ttu-id="ca032-103">Ottenere le condizioni di contratto per un ID editore (Publisher), un ID offerta (prodotto) e un ID piano (nome).</span><span class="sxs-lookup"><span data-stu-id="ca032-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="ca032-104">L'oggetto termini restituito da questo comando deve essere passato a Set-AzMarketplaceTerms per accettare le condizioni legali.</span><span class="sxs-lookup"><span data-stu-id="ca032-104">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

## <span data-ttu-id="ca032-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca032-105">SYNTAX</span></span>

```
Get-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca032-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca032-106">DESCRIPTION</span></span>
<span data-ttu-id="ca032-107">Il cmdlet **Get-AzMarketplaceTerms** restituisce i termini per l'ID editore (Publisher), l'ID offerta (Product) e la tupla ID piano (nome).</span><span class="sxs-lookup"><span data-stu-id="ca032-107">The **Get-AzMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="ca032-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca032-108">EXAMPLES</span></span>

### <span data-ttu-id="ca032-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ca032-109">Example 1</span></span>
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

## <span data-ttu-id="ca032-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ca032-110">PARAMETERS</span></span>

### <span data-ttu-id="ca032-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca032-111">-DefaultProfile</span></span>
<span data-ttu-id="ca032-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ca032-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca032-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca032-113">-Name</span></span>
<span data-ttu-id="ca032-114">Stringa identificatore piano dell'immagine da distribuire.</span><span class="sxs-lookup"><span data-stu-id="ca032-114">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="ca032-115">-Prodotto</span><span class="sxs-lookup"><span data-stu-id="ca032-115">-Product</span></span>
<span data-ttu-id="ca032-116">Offerta identificatore stringa di immagine da distribuire.</span><span class="sxs-lookup"><span data-stu-id="ca032-116">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="ca032-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="ca032-117">-Publisher</span></span>
<span data-ttu-id="ca032-118">Stringa dell'identificatore dell'editore dell'immagine da distribuire.</span><span class="sxs-lookup"><span data-stu-id="ca032-118">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="ca032-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca032-119">CommonParameters</span></span>
<span data-ttu-id="ca032-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca032-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca032-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca032-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca032-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ca032-122">INPUTS</span></span>

### <span data-ttu-id="ca032-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ca032-123">None</span></span>

## <span data-ttu-id="ca032-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca032-124">OUTPUTS</span></span>

### <span data-ttu-id="ca032-125">Microsoft. Azure. Commands. MarketplaceOrdering. Models. PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="ca032-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="ca032-126">Note</span><span class="sxs-lookup"><span data-stu-id="ca032-126">NOTES</span></span>

## <span data-ttu-id="ca032-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca032-127">RELATED LINKS</span></span>