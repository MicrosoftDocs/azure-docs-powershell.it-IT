---
title: guida introduttiva ad Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 01/14/2019
ms.openlocfilehash: 483e74d7d047562b1c170c3767495161b9c5eb2f
ms.sourcegitcommit: c6fd0e490fa0e33b8b768b679682a47d8faae1cf
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/16/2019
ms.locfileid: "54342002"
---
# <a name="get-started-with-azure-powershell"></a>guida introduttiva ad Azure PowerShell

Azure PowerShell è progettato per la gestione e l'amministrazione delle risorse di Azure dalla riga di comando. Usare Azure PowerShell quando si vogliono creare strumenti automatizzati che usano il modello di Azure Resource Manager.
È possibile provarlo nel browser con [Azure Cloud Shell](/azure/cloud-shell/overview) oppure installarlo nel computer locale.

Questo articolo consente di iniziare a usare Azure PowerShell e ne illustra i concetti fondamentali.

## <a name="install-or-run-in-azure-cloud-shell"></a>Installazione o esecuzione in Azure Cloud Shell

Il modo più semplice per iniziare a usare Azure PowerShell è provarlo in un ambiente Azure Cloud Shell.
Per iniziare subito a usare Azure Cloud Shell, vedere [Guida introduttiva a PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).
Cloud Shell esegue PowerShell 6 in un contenitore Linux, per cui le funzionalità specifiche di Windows non sono disponibili.

Quando si è pronti per installare Azure PowerShell nel computer locale, seguire le istruzioni in [Installare il modulo Azure PowerShell](install-az-ps.md).

## <a name="sign-in-to-azure"></a>Accedere ad Azure

Accedere in modo interattivo con il cmdlet `Connect-AzAccount`. Ignorare questo passaggio se si usa Cloud Shell: La sessione di Auzre Cloud Shell è già autenticata per l'ambiente, la sottoscrizione e il tenant che ha avviato la sessione Cloud Shell.

```azurepowershell-interactive
Connect-AzAccount
```

Se si risiede in un'area non degli Stati Uniti, usare il parametro `-Environment` per l'accesso. Recuperare il nome dell'ambiente per la propria area con il cmdlet [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment). Ad esempio, per accedere ad Azure Cina 21Vianet:

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

Si otterrà un token da usare in https://microsoft.com/devicelogin. Aprire questa pagina nel browser e immettere il token, quindi accedere con le credenziali dell'account Azure e autorizzare Azure PowerShell. 

Dopo aver effettuato l'accesso è possibile usare i cmdlet di Azure PowerShell per l'accesso e la gestione delle risorse nella sottoscrizione. Per altre informazioni sul processo di accesso e i metodi di autenticazione, vedere [Accedere con Azure PowerShell](authenticate-azureps.md).

## <a name="find-commands"></a>Trovare i comandi

I cmdlet di Azure PowerShell seguono una convenzione di denominazione standard per PowerShell, `VERB-NOUN`. Il verbo descrive l'azione (alcuni esempi includono `Create`, `Get`, `Set`, `Delete`) e il nome descrive il tipo di risorsa (alcuni esempi includono `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`). I nomi in Azure PowerShell iniziano sempre con il prefisso `Az`. Per l'elenco completo dei verbi standard, vedere [Verbi approvati per i comandi di PowerShell](/powershell/developer/cmdlet/approved-verbs-for-windows-powershell-commands).

Conoscere i nomi, i verbi e i moduli di Azure PowerShell disponibili consente di trovare i comandi con il cmdlet [Get-Command](/powershell/module/microsoft.powershell.core/get-command). Ad esempio, per trovare tutti i comandi correlati alla macchina virtuale che usano il verbo `Get`:

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

Per trovare i comandi comuni, questa tabella elenca il tipo di risorsa, il modulo di Azure PowerShell corrispondente e il prefisso del nome da usare con `Get-Command`:

| Tipo di risorsa | Modulo di Azure PowerShell | Prefisso del nome |
|---------------|-------------------------|----------------|
| [Gruppo di risorse](/azure/azure-resource-manager/resource-group-overview) | [Az.Resources](/powershell/module/az.resources#resources) | `AzResourceGroup` |
| [Macchine virtuali](/azure/virtual-machines) | [Az.Compute](/powershell/module/az.compute#virtual_machines) | `AzVM` |
| [Account di archiviazione](/azure/storage/common/storage-introduction) | [Az.Storage](/powershell/module/az.storage/) | `AzStorageAccount` |
| [Insieme di credenziali di chiave](/azure/key-vault/key-vault-whatis) | [Az.KeyVault](/powershell/module/az.keyvault) | `AzKeyVault` |
| [Applicazioni Web](/azure/app-service) | [Az.Websites](/powershell/module/az.websites) | `AzWebApp` |
| [Database SQL](/azure/sql-database) | [Az.Sql](/powershell/module/az.sql) | `AzSqlDatabase` |

Per un elenco completo dei moduli di Azure PowerShell, vedere l'[elenco di moduli di Azure PowerShell](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) ospitato in GitHub.

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a>Guide introduttive ed esercitazioni per apprendere le nozioni di base di Azure PowerShell

Per iniziare a usare Azure PowerShell, provare un'esercitazione dettagliata per la configurazione delle macchine virtuali e per imparare a eseguire query nelle stesse.

> [!div class="nextstepaction"]
> [Creare macchine virtuali con Azure PowerShell](azureps-vm-tutorial.yml)

Sono disponibili anche guide introduttive di Azure PowerShell per altri servizi di Azure più diffusi:

* [Creare un account di archiviazione](/azure/storage/common/storage-quickstart-create-account?tabs=azure-powershell)
* [Trasferire oggetti da e verso Archiviazione BLOB di Azure](/azure/storage/blobs/storage-quickstart-blobs-powershell)
* [Creare e recuperare segreti da Azure Key Vault](/azure/key-vault/quick-create-powershell)
* [Creare un database SQL di Azure e un firewall](/azure/sql-database/scripts/sql-database-create-and-configure-database-powershell)
* [Eseguire un contenitore in Istanze di Azure Container](/azure/container-instances/container-instances-quickstart-powershell)
* [Creare un set di scalabilità di macchine virtuali](/azure/virtual-machine-scale-sets/quick-create-powershell)
* [Creare un'istanza di Load Balancer Standard](/azure/load-balancer/quickstart-create-standard-load-balancer-powershell)

## <a name="next-steps"></a>Passaggi successivi

* [Accedere con Azure PowerShell](authenticate-azureps.md)
* [Gestire le sottoscrizioni di Azure con Azure PowerShell](manage-subscriptions-azureps.md)
* [Creare entità servizio di Azure con Azure PowerShell](create-azure-service-principal-azureps.md)
* Ottenere informazioni dalla community:
  * [Forum Azure su MSDN](http://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [Stacki Overflow](http://go.microsoft.com/fwlink/?LinkId=320213)
