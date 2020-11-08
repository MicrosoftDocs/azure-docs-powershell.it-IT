---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 3CD1A989-902C-48B3-81E9-7B78EDA5F880
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7003abf263fd4c669956f65c990246295cf7158d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023828"
---
# Remove-AzureAccount

## Sinossi
Elimina un account Azure da Windows PowerShell.

## SINTASSI

```
Remove-AzureAccount -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Remove-AzureAccount** Elimina un account Azure e i relativi abbonamenti dal file di dati dell'abbonamento nel profilo utente mobile.
Non elimina l'account da Microsoft Azure o modifica l'account effettivo in alcun modo.

L'uso di questo cmdlet è molto simile alla disconnessione dall'account di Azure.
Se si vuole accedere di nuovo all'account, usare il **componente aggiuntivo AzureAccount** o **Import-AzurePublishSettingsFile** per aggiungere di nuovo l'account a Windows PowerShell.

Puoi anche usare il cmdlet **Remove-AzureAccount** per cambiare il modo in cui i cmdlet di PowerShell di Azure si iscrivono all'account di Azure.
Se l'account include sia un certificato di gestione da **Import-AzurePublishSettingsFile** che un token di accesso da **Add-AzureAccount** , i cmdlet di PowerShell di Azure usano solo il token di accesso. ignorano il certificato di gestione.
Per usare il certificato di gestione, eseguire **Remove-AzureAccount**.
Quando **Remove-AzureAccount** trova sia un certificato di gestione che un token di accesso, Elimina solo il token di accesso anziché eliminare l'account.
Il certificato di gestione è ancora presente, quindi l'account è ancora disponibile per Windows PowerShell.

Questo argomento descrive il cmdlet nella versione 0.8.10 del modulo PowerShell di Microsoft Azure.
Per ottenere la versione del modulo che si sta usando, nella console di PowerShell di Azure digitare `(Get-Module -Name Azure).Version` .

## ESEMPI

### Esempio 1: rimuovere un account
```
PS C:\> Remove-AzureAccount -Name admin@contoso.com
```

Questo comando rimuove admin@contoso.com dal file di dati dell'abbonamento.
Al termine del comando, l'account non è più disponibile per Windows PowerShell.

## PARAMETRI

### -Force
Elimina la richiesta di conferma.
Per impostazione predefinita, **Remove-AzureAccount** richiede prima di rimuovere l'account da Windows PowerShell.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Specifica il nome dell'account da rimuovere.
Il valore del parametro fa distinzione tra maiuscole e minuscole.
I caratteri jolly non sono supportati.

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

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno
È possibile reindirizzare l'input a questo cmdlet in base al nome della proprietà, ma non in base al valore.

## OUTPUT

### None o System. Boolean
Se si usa il parametro *PassThru* , questo cmdlet restituisce un valore booleano.
In caso contrario, non restituirà alcun output.

## Note

## COLLEGAMENTI CORRELATI

[Add-AzureAccount](./Add-AzureAccount.md)

[Get-AzureAccount](./Get-AzureAccount.md)


