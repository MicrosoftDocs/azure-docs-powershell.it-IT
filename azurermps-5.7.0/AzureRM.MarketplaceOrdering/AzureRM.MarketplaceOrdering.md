---
Module Name: AzureRM.MarketplaceOrdering
Module Guid: 6e0e216b-1dff-4992-b943-b3a4f14679ab
Download Help Link: ''
Help Version: 0.1.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/AzureRM.MarketplaceOrdering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/AzureRM.MarketplaceOrdering.md
ms.openlocfilehash: 198de5436453caf633288e23f804085319a30f73
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/23/2019
ms.locfileid: "93490637"
---
# Modulo AzureRM. MarketplaceOrdering
## Descrizione
Gli argomenti di questa sezione documentano i cmdlet di PowerShell di Azure per Azure MarketplaceOrdering in Azure Resource Manager (ARM) Framework. I cmdlet sono presenti nello spazio dei nomi Microsoft. Azure. Commands. MarketplaceOrdering. Questi cmdlet consentono agli utenti di Azure di accettare le condizioni legali per un Marketplace che offre ulteriori possibilità di distribuzione a livello di programmazione per queste soluzioni. Gli utenti possono anche rifiutare set di termini legali già accettati.

## Cmdlet AzureRM. MarketplaceOrdering
### [Get-AzureRmMarketplaceTerms](Get-AzureRmMarketplaceTerms.md)
Ottenere le condizioni di contratto per un ID editore (Publisher), un ID offerta (prodotto) e un ID piano (nome). L'oggetto termini restituito da questo comando deve essere passato a Set-AzureRmMarketplaceTerms per accettare le condizioni legali.

### [Set-AzureRmMarketplaceTerms](Set-AzureRmMarketplaceTerms.md)
Accettare o rifiutare termini per un ID editore (Publisher), un ID offerta (prodotto) e un ID piano (nome). Usare Get-AzureRmMarketplaceTerms per ottenere le condizioni per il contratto.

