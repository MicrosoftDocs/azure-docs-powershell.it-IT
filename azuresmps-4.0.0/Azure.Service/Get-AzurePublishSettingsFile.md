---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: A5419F76-B85E-445D-84EA-CC695B175C8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1364cf1bbec1fdca2a8c9901556d38de0b620358
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023591"
---
# Get-AzurePublishSettingsFile

## Sinossi
Scarica il file delle impostazioni di pubblicazione per un abbonamento a Azure.

## SINTASSI

```
Get-AzurePublishSettingsFile [-Environment <String>] [-Realm <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzurePublishSettingsFile** Scarica un file di impostazioni di pubblicazione per un abbonamento nell'account.
Al termine del comando, è possibile usare il cmdlet **Import-PublishSettingsFile** per rendere le impostazioni del file disponibili per Windows PowerShell.

Per rendere l'account di Azure disponibile per Windows PowerShell, è possibile usare un file di impostazioni di pubblicazione o il cmdlet **Add-AzureAccount** .
I file di impostazioni di pubblicazione consentono di preparare la sessione in anticipo, in modo da poter eseguire script e processi in background incustoditi.
Tuttavia, non tutti i servizi supportano i file delle impostazioni di pubblicazione.
Ad esempio, il modulo **AzureResourceManager** non supporta i file delle impostazioni di pubblicazione.

Quando si esegue **Get-AzurePublishSettingsFile** , viene aperto il browser predefinito e viene chiesto di accedere all'account di Azure, selezionare un abbonamento e selezionare un percorso di file System per il file delle impostazioni di pubblicazione.
Quindi, Scarica il file delle impostazioni di pubblicazione per l'abbonamento nel file selezionato.

Un file di impostazioni di pubblicazione è un file XML con estensione publishsettings.
Il file contiene un certificato codificato che fornisce le credenziali di gestione per gli abbonamenti di Azure.

**Nota sulla sicurezza:** I file delle impostazioni di pubblicazione contengono le credenziali usate per amministrare gli abbonamenti e i servizi di Azure.
Se gli utenti malintenzionati accedono al file delle impostazioni di pubblicazione, possono modificare, creare ed eliminare i servizi di Azure.
Come procedura consigliata per la sicurezza, salvare il file in un percorso nella cartella download o documenti e quindi eliminarlo dopo avere usato il cmdlet **Import-AzurePublishSettingsFile** per importare le impostazioni.

Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.
Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .

## ESEMPI

### Esempio 1: scaricare un file di impostazioni di pubblicazione
```
PS C:\> Get-AzurePublishSettingsFile
```

Questo comando apre il browser predefinito, si connette all'account di Windows Azure e quindi Scarica il file con estensione publishsettings per l'account.

### Esempio 2: specificare un Realm
```
PS C:\> Get-AzurePublishSettingsFile -Realm contoso.com -Passthru
```

Questo comando Scarica il file delle impostazioni di pubblicazione per un account nel dominio contoso.com.
Usare un comando con il parametro **Realm** quando si accede a Azure con un account aziendale, invece di un account Microsoft.

## PARAMETRI

### -Ambiente
Specifica un ambiente Azure.

Un ambiente Azure una distribuzione indipendente di Microsoft Azure, ad esempio AzureCloud per Azure globale e AzureChinaCloud per Azure gestito da 21Vianet in Cina.
Puoi anche creare ambienti Azure locali usando Azure Pack e i cmdlet WAPack.
Per altre informazioni, vedere [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Restituisce $True se il comando riesce e $False se non riesce.
Per impostazione predefinita, questo cmdlet non restituisce alcun output.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profile
Specifica il profilo Azure da cui viene letto il cmdlet. Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Realm
Specifica l'organizzazione in un ID organizzativo.
Ad esempio, se si accede a Azure As admin@contoso.com , il valore del parametro **Realm** è contoso.com.
Usa questo parametro quando usi un ID organizzazione per accedere a Azure Portal.
Questo parametro non è necessario quando si usa un account Microsoft, ad esempio un account di outlook.com o live.com.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno
È possibile reindirizzare l'input a questo cmdlet in base al nome della proprietà, ma non in base al valore.

## OUTPUT

### None o System. Boolean
Quando si usa il parametro *PassThru* , questo cmdlet restituisce un valore booleano.
In caso contrario, questo cmdlet non restituisce alcun output

## Note

## COLLEGAMENTI CORRELATI

[Add-AzureAccount](./Add-AzureAccount.md)

[Import-AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)


