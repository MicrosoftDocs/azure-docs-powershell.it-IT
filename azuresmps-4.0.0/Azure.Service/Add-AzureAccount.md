---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 03EAFFB2-EA64-4227-A33B-D24EB4A75F71
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac88bc2494bad975c6169262edd05c7b821061bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029858"
---
# Add-AzureAccount

## Sinossi
Aggiunge l'account di Azure a Windows PowerShell.

## SINTASSI

### Utente (impostazione predefinita)
```
Add-AzureAccount [-Environment <String>] [-Credential <PSCredential>] [-Tenant <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ServicePrincipal
```
Add-AzureAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Add-AzureAccount** rende disponibile l'account Azure e le relative sottoscrizioni in Windows PowerShell.
È come accedere all'account di Azure in Windows PowerShell.
Per disconnettersi dall'account, usare il cmdlet **Remove-AzureAccount** .

**Add-AzureAccount** Scarica le informazioni relative all'account di Azure e la Salva in un file di dati di sottoscrizione nel profilo utente mobile.
Viene inoltre ottenuto un token di accesso che consente a Windows PowerShell di accedere all'account di Azure per conto dell'utente.
Al termine del comando, puoi gestire l'account di Azure in Windows PowerShell.

Esistono due modi diversi per rendere l'account di Azure disponibile per Windows PowerShell.
Puoi usare il cmdlet **Add-AzureAccount** , che usa i token di accesso per l'autenticazione di Azure Active Directory (Azure ad) o **Import-AzurePublishSettingsFile** , che usa un certificato di gestione.
Per informazioni su quale metodo usare, vedere [procedura: connettersi all'abbonamento](https://azure.microsoft.com/documentation/articles/install-configure-powershell) ( https://azure.microsoft.com/documentation/articles/install-configure-powershell/#Connect) .

Quando si esegue **Add-AzureAccount** , viene visualizzata una finestra interattiva in cui viene richiesto di accedere all'account di Azure.
Questo accesso è valido fino alla scadenza del token di Access.
Quando scade, i cmdlet che richiedono l'accesso all'account ti chiedono di eseguire di nuovo l'esecuzione di **Add-AzureAccount** .

Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.
Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .

## ESEMPI

### Esempio 1: aggiungere un account
```
PS C:\> Add-AzureAccount
```

Questo comando aggiunge un account di Azure a Windows PowerShell.
Quando si esegue il comando, viene visualizzata una finestra per richiedere il nome utente e la password dell'account.

### Esempio 2: usare un file di dati alternativo per l'abbonamento
```
PS C:\> Add-AzureAccount -SubscriptionDataFile C:\Testing\SDF.xml
```

Questo comando usa il parametro **SubscriptionDataFile** per indirizzare **Add-AzureAccount** per archiviare i dati dell'account nel file C:\Testing\SDF.xml, invece che nel file predefinito.

## PARAMETRI

### -Credenziale
```yaml
Type: PSCredential
Parameter Sets: User
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -ServicePrincipal
```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tenant
```yaml
Type: String
Parameter Sets: User
Aliases: TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno
Non è possibile reindirizzare l'input a questo cmdlet

## OUTPUT

### Nessuno
Questo cmdlet non restituisce alcun output.

## Note
* **Add-AzureAccount** (e il metodo di autenticazione di Azure ad) hanno la precedenza su **Import-AzurePublishSettings** (e il metodo del certificato di gestione). Se si usa **Add-AzureAccount** anche una volta nel proprio account, viene usato il metodo di autenticazione di Azure ad e il certificato di gestione viene ignorato. Per rimuovere il token Azure AD e ripristinare il metodo di gestione del certificato, usare il cmdlet **Remove-AzureAccount** . Per altre informazioni, digitare: **Get-Help Remove-AzureAccount**.
* Errore "le credenziali sono scadute. Usare Add-AzureAccount per accedere di nuovo. indica che il token di accesso è scaduto e che Windows PowerShell non può accedere all'account di Azure. Per ripristinare l'accesso al proprio account, eseguire di nuovo **Add-AzureAccount** .
* I cmdlet di account e abbonamento di Azure PowerShell ottengono i loro dati dal file di dati dell'abbonamento, non dall'account di Azure Live. Se si modifica l'account o gli abbonamenti all'esterno di Windows PowerShell, ad esempio tramite il portale di gestione di Azure, eseguire di nuovo **Add-AzureAccount** per aggiornare il file di dati dell'abbonamento.

## COLLEGAMENTI CORRELATI

[Add-AzureEnvironment](./Add-AzureEnvironment.md)

[Get-AzureEnvironment](./Get-AzureEnvironment.md)

[Import-AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[Get-AzureAccount](./Get-AzureAccount.md)

[Remove-AzureAccount](./Remove-AzureAccount.md)


