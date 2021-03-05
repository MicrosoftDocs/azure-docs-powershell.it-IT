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
# Modulo Az.MarketplaceOrdering
## Descrizione
Gli argomenti di questa sezione documentano i cmdlet di Azure PowerShell per Azure MarketplaceOrdering nel framework di Gestione risorse di Azure (ARM). I cmdlet sono presenti nello spazio dei nomi Microsoft.Azure.Commands.MarketplaceOrdering. Questi cmdlet consentono agli utenti di Azure di accettare le condizioni legali per un marketplace offrendo ulteriormente la distribuzione programmatica per queste soluzioni. Gli utenti possono anche rifiutare una serie di condizioni legali già accettate.

## Cmdlet Az.MarketplaceOrdering
### [Get-AzMarketplaceTerms](Get-AzMarketplaceTerms.md)
Ottenere le condizioni del contratto per un determinato ID editore (Publisher), ID offerta(Prodotto) e ID piano(Nome). L'oggetto termini restituito da questo comando deve essere passato Set-AzMarketplaceTerms accettare le condizioni legali.

### [Set-AzMarketplaceTerms](Set-AzMarketplaceTerms.md)
Accettare o rifiutare le condizioni per un determinato ID editore (Editore), id offerta(Prodotto) e ID piano(Nome). Usare le Get-AzMarketplaceTerms per ottenere le condizioni del contratto.

