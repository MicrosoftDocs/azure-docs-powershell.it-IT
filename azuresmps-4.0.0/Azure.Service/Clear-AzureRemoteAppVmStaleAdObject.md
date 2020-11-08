---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DA8EC1BD-1219-4B98-B661-40A28897271F
online version: ''
schema: 2.0.0
ms.openlocfilehash: dcbca5ab73d64bd0336f723d623c7f976237ecba
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023661"
---
# Clear-AzureRemoteAppVmStaleAdObject

## Sinossi
Rimuove gli oggetti in Azure Active Directory associati alle macchine virtuali di Azure RemoteApp che non esistono più.

## SINTASSI

```
Clear-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Clear-AzureRemoteAppVmStaleAdObject** rimuove gli oggetti in Azure Active Directory associati alle macchine virtuali di Azure RemoteApp che non esistono più.
È necessario utilizzare le credenziali con diritti per rimuovere gli oggetti di Azure Active Directory.
Se specifichi il parametro comune *verbose* , questo cmdlet Visualizza il nome di ogni oggetto che viene eliminato.

## ESEMPI

### Esempio 1: cancellare gli oggetti obsoleti per una raccolta
```
PS C:\> $AdminCredentials = Get-Credential
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso" -Credential $AdminCredentials
```

Il primo comando richiede un nome utente e una password utilizzando **Get-Credential**.
Il comando Archivia i risultati nella variabile $AdminCredentials.

Il secondo comando Cancella gli oggetti non aggiornati per la raccolta denominata Contoso.
Il comando usa le credenziali archiviate in $AdminCredentials variabile.
Affinché il comando abbia esito positivo, tali credenziali devono avere diritti appropriati.

## PARAMETRI

### -CollectionName
Specifica il nome della raccolta RemoteApp di Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Credenziale
Specifica una credenziale con diritti per eseguire questa azione.
Per ottenere un oggetto **PSCredential** , usare il cmdlet **Get-Credential** .
Se non specifichi questo parametro, questo cmdlet usa le credenziali utente correnti.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Specifica il profilo Azure da cui viene letto il cmdlet.
Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.

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

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRemoteAppVmStaleAdObject](./Get-AzureRemoteAppVmStaleAdObject.md)


