---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 79D64D7C-6671-4F03-8776-70A716F36512
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2bc0525ee7238de421842b74f52f7dd4fa59df1a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029723"
---
# Import-AzurePublishSettingsFile

## Sinossi
Importa un file di impostazioni di pubblicazione che consente di gestire gli account di Azure in Windows PowerShell.

## SINTASSI

```
Import-AzurePublishSettingsFile -PublishSettingsFile <String> [-Environment <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Import-AzurePublishSettingsFile** importa un file di impostazioni di pubblicazione (*. publishsettings) che contiene informazioni sugli account di Azure e salva un file di dati di sottoscrizione nel computer.
Al termine del cmdlet, è possibile gestire gli account di Azure in Windows PowerShell.

Prima di eseguire **Import-AzurePublishSettingsFile** , Esegui **Get-AzurePublishSettingsFile** , che Scarica e salva il file delle impostazioni di pubblicazione in modo da poterlo importare.

Per rendere l'account di Azure disponibile per Windows PowerShell, è possibile usare un file di impostazioni di pubblicazione o il cmdlet **Add-AzureAccount** .
I file di impostazioni di pubblicazione consentono di preparare la sessione in anticipo, in modo da poter eseguire script e processi in background incustoditi.
Tuttavia, non tutti i servizi supportano i file delle impostazioni di pubblicazione.
Ad esempio, il modulo **AzureResourceManager** non supporta i file delle impostazioni di pubblicazione.

**Nota sulla sicurezza:** I file delle impostazioni di pubblicazione contengono un certificato di gestione codificato, ma non crittografato.
Se gli utenti malintenzionati accedono al file delle impostazioni di pubblicazione, potrebbero essere in grado di modificare, creare ed eliminare i servizi di Azure.
Come procedura consigliata per la sicurezza, salvare il file in un percorso nella cartella download o documenti e quindi eliminarlo dopo avere usato il cmdlet **Import-AzurePublishSettingsFile** per importare le impostazioni.

## ESEMPI

### Esempio 1: importare un file
```
PS C:\> Import-AzurePublishSettingsFile -PublishSettingsFile C:\Temp\MyAccount.publishsettings
```

Questo comando importa il file "C:\Temp\MyAccount.publishsettings".

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
Accept pipeline input: False
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

### -PublishSettingsFile
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

### Nessuno
Questo cmdlet non genera alcun output.

## Note
* Un file di impostazioni di pubblicazione è un file XML con estensione publishsettings. Il file contiene un certificato codificato che fornisce le credenziali di gestione per gli abbonamenti di Azure. Dopo aver importato il file, eliminarlo per evitare rischi per la sicurezza.
* Un "file di dati di sottoscrizione" è un file XML che può essere salvato nel computer in modo sicuro. Per impostazione predefinita, viene salvato nel profilo utente roaming ($home/AppData/Roaming).

## COLLEGAMENTI CORRELATI

[Come installare e configurare Azure PowerShell](https://azure.microsoft.com/documentation/articles/install-configure-powershell/)

[Add-AzureAccount](./Add-AzureAccount.md)

[Get-AzurePublishSettingsFile](./Get-AzurePublishSettingsFile.md)


