---
Module Name: AzureRM.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: ''
Help Version: 0.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/AzureRM.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/AzureRM.MarketplaceOrdering.md
ms.openlocfilehash: bbbdd28f0ea3916581c20cf8f078eca1cb2ddca6
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/23/2019
ms.locfileid: "93490282"
---
# <span data-ttu-id="ccb1d-101">Modulo AzureRM. MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ccb1d-101">AzureRM.MarketplaceOrdering Module</span></span>
## <span data-ttu-id="ccb1d-102">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ccb1d-102">Description</span></span>
<span data-ttu-id="ccb1d-103">Gli argomenti di questa sezione documentano i cmdlet di PowerShell di Azure per Azure MarketplaceOrdering in Azure Resource Manager (ARM) Framework.</span><span class="sxs-lookup"><span data-stu-id="ccb1d-103">The topics in this section document the Azure PowerShell cmdlets for Azure MarketplaceOrdering in the Azure Resource Manager (ARM) framework.</span></span> <span data-ttu-id="ccb1d-104">I cmdlet sono presenti nello spazio dei nomi Microsoft. Azure. Commands. MarketplaceOrdering.</span><span class="sxs-lookup"><span data-stu-id="ccb1d-104">The cmdlets exist in the Microsoft.Azure.Commands.MarketplaceOrdering namespace.</span></span> <span data-ttu-id="ccb1d-105">Questi cmdlet consentono agli utenti di Azure di accettare le condizioni legali per un Marketplace che offre ulteriori possibilità di distribuzione a livello di programmazione per queste soluzioni.</span><span class="sxs-lookup"><span data-stu-id="ccb1d-105">These cmdlets allow azure users to accept the legal terms for a marketplace offering further allowing programmatic deployment for these solutions.</span></span> <span data-ttu-id="ccb1d-106">Gli utenti possono anche rifiutare set di termini legali già accettati.</span><span class="sxs-lookup"><span data-stu-id="ccb1d-106">Users may also reject set of legal terms already accepted.</span></span>

## <span data-ttu-id="ccb1d-107">Cmdlet AzureRM. MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="ccb1d-107">AzureRM.MarketplaceOrdering Cmdlets</span></span>
### [<span data-ttu-id="ccb1d-108">Get-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="ccb1d-108">Get-AzureRmMarketplaceTerms</span></span>](Get-AzureRmMarketplaceTerms.md)
<span data-ttu-id="ccb1d-109">Ottenere le condizioni di contratto per un ID editore (Publisher), un ID offerta (prodotto) e un ID piano (nome).</span><span class="sxs-lookup"><span data-stu-id="ccb1d-109">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="ccb1d-110">L'oggetto termini restituito da questo comando deve essere passato a Set-AzureRmMarketplaceTerms per accettare le condizioni legali.</span><span class="sxs-lookup"><span data-stu-id="ccb1d-110">The terms object which is returned by this command should be passed to Set-AzureRmMarketplaceTerms to accept the legal terms.</span></span>

### [<span data-ttu-id="ccb1d-111">Set-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="ccb1d-111">Set-AzureRmMarketplaceTerms</span></span>](Set-AzureRmMarketplaceTerms.md)
<span data-ttu-id="ccb1d-112">Accettare o rifiutare termini per un ID editore (Publisher), un ID offerta (prodotto) e un ID piano (nome).</span><span class="sxs-lookup"><span data-stu-id="ccb1d-112">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="ccb1d-113">Usare Get-AzureRmMarketplaceTerms per ottenere le condizioni per il contratto.</span><span class="sxs-lookup"><span data-stu-id="ccb1d-113">Please use Get-AzureRmMarketplaceTerms to get the agreement terms.</span></span>

