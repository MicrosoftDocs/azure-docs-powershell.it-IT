---
Module Name: Az.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: https://docs.microsoft.com/powershell/module/az.marketplaceordering
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Az.MarketplaceOrdering.md
ms.openlocfilehash: 2720635840051dd85eb613fabb1ac32ba32c6f60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991058"
---
# <span data-ttu-id="d534f-101">Modulo Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="d534f-101">Az.MarketplaceOrdering Module</span></span>
## <span data-ttu-id="d534f-102">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d534f-102">Description</span></span>
<span data-ttu-id="d534f-103">Gli argomenti di questa sezione documentano i cmdlet di Azure PowerShell per Azure MarketplaceOrdering nel framework di Gestione risorse di Azure (ARM).</span><span class="sxs-lookup"><span data-stu-id="d534f-103">The topics in this section document the Azure PowerShell cmdlets for Azure MarketplaceOrdering in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="d534f-104">I cmdlet sono presenti nello spazio dei nomi Microsoft.Azure.Commands.MarketplaceOrdering.</span><span class="sxs-lookup"><span data-stu-id="d534f-104">The cmdlets exist in the Microsoft.Azure.Commands.MarketplaceOrdering namespace.</span></span> <span data-ttu-id="d534f-105">Questi cmdlet consentono agli utenti di Azure di accettare le condizioni legali per un marketplace offrendo ulteriormente la distribuzione programmatica per queste soluzioni.</span><span class="sxs-lookup"><span data-stu-id="d534f-105">These cmdlets allow azure users to accept the legal terms for a marketplace offering further allowing programmatic deployment for these solutions.</span></span> <span data-ttu-id="d534f-106">Gli utenti possono anche rifiutare una serie di condizioni legali già accettate.</span><span class="sxs-lookup"><span data-stu-id="d534f-106">Users may also reject set of legal terms already accepted.</span></span>

## <span data-ttu-id="d534f-107">Cmdlet Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="d534f-107">Az.MarketplaceOrdering Cmdlets</span></span>
### [<span data-ttu-id="d534f-108">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="d534f-108">Get-AzMarketplaceTerms</span></span>](Get-AzMarketplaceTerms.md)
<span data-ttu-id="d534f-109">Ottenere le condizioni del contratto per un determinato ID editore (Publisher), ID offerta(Prodotto) e ID piano(Nome).</span><span class="sxs-lookup"><span data-stu-id="d534f-109">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="d534f-110">L'oggetto termini restituito da questo comando deve essere passato Set-AzMarketplaceTerms accettare le condizioni legali.</span><span class="sxs-lookup"><span data-stu-id="d534f-110">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

### [<span data-ttu-id="d534f-111">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="d534f-111">Set-AzMarketplaceTerms</span></span>](Set-AzMarketplaceTerms.md)
<span data-ttu-id="d534f-112">Accettare o rifiutare le condizioni per un determinato ID editore (Editore), id offerta(Prodotto) e ID piano(Nome).</span><span class="sxs-lookup"><span data-stu-id="d534f-112">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="d534f-113">Usare le Get-AzMarketplaceTerms per ottenere le condizioni del contratto.</span><span class="sxs-lookup"><span data-stu-id="d534f-113">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

