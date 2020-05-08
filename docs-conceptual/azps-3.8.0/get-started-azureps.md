---
title: guida introduttiva ad Azure PowerShell
description: ''
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: get-started-article
ms.date: 04/24/2020
ms.openlocfilehash: 70f74cf4d3c2465dac88d694f9b373e43c48f64c
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/05/2020
ms.locfileid: "82587974"
---
# <a name="get-started-with-azure-powershell"></a>guida introduttiva ad Azure PowerShell

Azure PowerShell è progettato per la gestione e l'amministrazione delle risorse di Azure dalla riga di comando.
Usare Azure PowerShell quando si vogliono creare strumenti automatizzati che usano il modello di Azure Resource Manager. È possibile provarlo nel browser con [Azure Cloud Shell](/azure/cloud-shell/overview) oppure installarlo nel computer locale.

Questo articolo consente di iniziare a usare Azure PowerShell e ne illustra i concetti fondamentali.

## <a name="install-or-run-in-azure-cloud-shell"></a>Installazione o esecuzione in Azure Cloud Shell

Il modo più semplice per iniziare a usare Azure PowerShell è provarlo in un ambiente Azure Cloud Shell. Per iniziare subito a usare Azure Cloud Shell, vedere [Guida introduttiva a PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell). Cloud Shell esegue PowerShell in un contenitore Linux, per cui le funzionalità specifiche di Windows non sono disponibili.

Quando si è pronti per installare Azure PowerShell nel computer locale, seguire le istruzioni in [Installare il modulo Azure PowerShell](install-az-ps.md).

## <a name="sign-in-to-azure"></a>Accedere ad Azure

Per accedere in modo interattivo, usare il cmdlet [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount). Ignorare questo passaggio se si usa Cloud Shell. La sessione di Azure Cloud Shell è già autenticata per l'ambiente, la sottoscrizione e il tenant che ha avviato la sessione Cloud Shell.

```azurepowershell-interactive
Connect-AzAccount
```

I servizi cloud di Azure offrono ambienti conformi alle normative di gestione dei dati a livello di area. Per gli account in un cloud a livello di area, usare il parametro **Environment** per accedere. Per recuperare il nome dell'ambiente per la propria area, usare il cmdlet [Get-AzEnvironment](/powershell/module/Az.Accounts/Get-AzEnvironment).
Ad esempio, per accedere ad Azure Cina 21Vianet:

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

Negli ambienti di Windows PowerShell 5.1 verrà visualizzata una finestra di dialogo di accesso in cui specificare un nome utente e una password per l'account Azure. In tutte le altre versioni di PowerShell si otterrà un token da usare in [microsoft.com/devicelogin](https://microsoft.com/devicelogin). Aprire questa pagina nel browser e immettere il token, quindi accedere con le credenziali dell'account Azure e autorizzare Azure PowerShell.

Dopo aver effettuato l'accesso, verrà visualizzato un messaggio indicante quale sottoscrizione di Azure è attiva. Se l'account include più sottoscrizioni di Azure e se ne vuole selezionare una diversa, recuperare le sottoscrizioni disponibili con [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) e usare il cmdlet [Set-AzContext](/powershell/module/az.accounts/set-azcontext) con l'ID sottoscrizione. Per altre informazioni sulla gestione delle sottoscrizioni di Azure in Azure PowerShell, vedere [Usare più sottoscrizioni di Azure](manage-subscriptions-azureps.md).

Dopo aver effettuato l'accesso è possibile usare i cmdlet di Azure PowerShell per l'accesso e la gestione delle risorse nella sottoscrizione. Per altre informazioni sul processo di accesso e i metodi di autenticazione, vedere [Accedere con Azure PowerShell](authenticate-azureps.md).

## <a name="find-commands"></a>Trovare i comandi

I cmdlet di Azure PowerShell seguono una convenzione di denominazione standard per PowerShell, `Verb-Noun`. Il verbo descrive l'azione (alcuni esempi includono `New`, `Get`, `Set`, `Remove`) e il nome descrive il tipo di risorsa (alcuni esempi includono `AzVM`, `AzKeyVaultCertificate`, `AzFirewall`, `AzVirtualNetworkGateway`). I nomi in Azure PowerShell iniziano sempre con il prefisso `Az`. Per l'elenco completo dei verbi standard, vedere [Verbi approvati per i comandi di PowerShell](/powershell/scripting/developer/cmdlet/approved-verbs-for-windows-powershell-commands).

Conoscere i nomi, i verbi e i moduli di Azure PowerShell disponibili consente di trovare i comandi con il cmdlet [Get-Command](/powershell/module/microsoft.powershell.core/get-command). Ad esempio, per trovare tutti i comandi correlati alla macchina virtuale che usano il verbo `Get`:

```powershell-interactive
Get-Command -Verb Get -Noun AzVM* -Module Az.Compute
```

Per facilitare la ricerca di comandi comuni, questa tabella elenca il tipo di risorsa, il modulo di Azure PowerShell corrispondente e il prefisso del nome da usare con `Get-Command`:

|                              Tipo di risorsa                              |                   Modulo di Azure PowerShell                    |    Prefisso del nome     |
| ----------------------------------------------------------------------- | ------------------------------------------------------------ | ------------------ |
| [Gruppo di risorse](/azure/azure-resource-manager/resource-group-overview) | [Az.Resources](/powershell/module/az.resources#resources)    | `AzResourceGroup`  |
| [Macchine virtuali](/azure/virtual-machines)                             | [Az.Compute](/powershell/module/az.compute#virtual_machines) | `AzVM`             |
| [Account di archiviazione](/azure/storage/common/storage-introduction)          | [Az.Storage](/powershell/module/az.storage/)                 | `AzStorageAccount` |
| [Insieme di credenziali di chiave](/azure/key-vault/key-vault-whatis)                          | [Az.KeyVault](/powershell/module/az.keyvault)                | `AzKeyVault`       |
| [Applicazioni Web](/azure/app-service)                                  | [Az.Websites](/powershell/module/az.websites)                | `AzWebApp`         |
| [Database SQL](/azure/sql-database)                                    | [Az.Sql](/powershell/module/az.sql)                          | `AzSqlDatabase`    |

Per un elenco completo dei moduli di Azure PowerShell, vedere l'[elenco di moduli di Azure PowerShell](https://github.com/Azure/azure-powershell/blob/master/documentation/azure-powershell-modules.md) ospitato in GitHub.

## <a name="telemetry"></a>Telemetria

Azure PowerShell raccoglie automaticamente i dati di telemetria per impostazione predefinita. Microsoft aggrega i dati raccolti per identificare i modelli di utilizzo e i problemi comuni, nonché per migliorare l'esperienza di Azure PowerShell. Microsoft Azure PowerShell non raccoglie dati privati o personali. Per disabilitare la raccolta dei dati, è necessario rifiutarla esplicitamente eseguendo [Disable-AzDataCollection](/powershell/module/az.accounts/disable-azdatacollection).

## <a name="learn-azure-powershell-basics-with-quickstarts-and-tutorials"></a>Modelli di avvio rapido ed esercitazioni per apprendere le nozioni di base di Azure PowerShell

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
  * [Forum Azure su MSDN](https://go.microsoft.com/fwlink/p/?LinkId=320212)
  * [Stack Overflow](https://go.microsoft.com/fwlink/?LinkId=320213)
