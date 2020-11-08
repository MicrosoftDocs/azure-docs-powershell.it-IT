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
# Modulo AZ. MarketplaceOrdering
## Descrizione
Gli argomenti di questa sezione documentano i cmdlet di PowerShell di Azure per Azure MarketplaceOrdering in Azure Resource Manager (ARM) Framework. I cmdlet sono presenti nello spazio dei nomi Microsoft. Azure. Commands. MarketplaceOrdering. Questi cmdlet consentono agli utenti di Azure di accettare le condizioni legali per un Marketplace che offre ulteriori possibilità di distribuzione a livello di programmazione per queste soluzioni. Gli utenti possono anche rifiutare set di termini legali già accettati.

## Cmdlet AZ. MarketplaceOrdering
### [Get-AzMarketplaceTerms](Get-AzMarketplaceTerms.md)
Ottenere le condizioni di contratto per un ID editore (Publisher), un ID offerta (prodotto) e un ID piano (nome). L'oggetto termini restituito da questo comando deve essere passato a Set-AzMarketplaceTerms per accettare le condizioni legali.

### [Set-AzMarketplaceTerms](Set-AzMarketplaceTerms.md)
Accettare o rifiutare termini per un ID editore (Publisher), un ID offerta (prodotto) e un ID piano (nome). Usare Get-AzMarketplaceTerms per ottenere le condizioni per il contratto.

