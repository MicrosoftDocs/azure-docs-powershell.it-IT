---
Module Name: Az.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
ms.openlocfilehash: dfcfd580312209bfdb0c197b95c2f655b9ac0723
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191474"
---
# <span data-ttu-id="05a23-101">Modulo AZ. MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="05a23-101">Az.MarketplaceOrdering Module</span></span>
## <span data-ttu-id="05a23-102">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05a23-102">Description</span></span>
<span data-ttu-id="05a23-103">Gli argomenti di questa sezione documentano i cmdlet di PowerShell di Azure per Azure MarketplaceOrdering in Azure Resource Manager (ARM) Framework.</span><span class="sxs-lookup"><span data-stu-id="05a23-103">The topics in this section document the Azure PowerShell cmdlets for Azure MarketplaceOrdering in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="05a23-104">I cmdlet sono presenti nello spazio dei nomi Microsoft. Azure. Commands. MarketplaceOrdering.</span><span class="sxs-lookup"><span data-stu-id="05a23-104">The cmdlets exist in the Microsoft.Azure.Commands.MarketplaceOrdering namespace.</span></span> <span data-ttu-id="05a23-105">Questi cmdlet consentono agli utenti di Azure di accettare le condizioni legali per un Marketplace che offre ulteriori possibilità di distribuzione a livello di programmazione per queste soluzioni.</span><span class="sxs-lookup"><span data-stu-id="05a23-105">These cmdlets allow azure users to accept the legal terms for a marketplace offering further allowing programmatic deployment for these solutions.</span></span> <span data-ttu-id="05a23-106">Gli utenti possono anche rifiutare set di termini legali già accettati.</span><span class="sxs-lookup"><span data-stu-id="05a23-106">Users may also reject set of legal terms already accepted.</span></span>

## <span data-ttu-id="05a23-107">Cmdlet AZ. MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="05a23-107">Az.MarketplaceOrdering Cmdlets</span></span>
### [<span data-ttu-id="05a23-108">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="05a23-108">Get-AzMarketplaceTerms</span></span>](Get-AzMarketplaceTerms.md)
<span data-ttu-id="05a23-109">Ottenere le condizioni di contratto per un ID editore (Publisher), un ID offerta (prodotto) e un ID piano (nome).</span><span class="sxs-lookup"><span data-stu-id="05a23-109">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="05a23-110">L'oggetto termini restituito da questo comando deve essere passato a Set-AzMarketplaceTerms per accettare le condizioni legali.</span><span class="sxs-lookup"><span data-stu-id="05a23-110">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

### [<span data-ttu-id="05a23-111">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="05a23-111">Set-AzMarketplaceTerms</span></span>](Set-AzMarketplaceTerms.md)
<span data-ttu-id="05a23-112">Accettare o rifiutare termini per un ID editore (Publisher), un ID offerta (prodotto) e un ID piano (nome).</span><span class="sxs-lookup"><span data-stu-id="05a23-112">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="05a23-113">Usare Get-AzMarketplaceTerms per ottenere le condizioni per il contratto.</span><span class="sxs-lookup"><span data-stu-id="05a23-113">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>
