---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 4136A0EF-2682-4B17-BC37-53CD43F5940B
online version: ''
schema: 2.0.0
ms.openlocfilehash: e7b884da0395313ddc8aa4d0e301b37849ec3d57
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029784"
---
# Get-AzureRemoteAppOperationResult

## Sinossi
Recupera il risultato di un'operazione RemoteApp di Azure.

## SINTASSI

```
Get-AzureRemoteAppOperationResult [-TrackingId] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-AzureRemoteAppOperationResult** Recupera il risultato di un'operazione RemoteApp di Azure a esecuzione prolungata.
Azure RemoteApp USA operazioni a esecuzione prolungata per molte azioni che richiedono l'elaborazione da parte del servizio e non possono tornare immediatamente.
Esempi di cmdlet che restituiscono gli ID di rilevamento includono **Update-AzureRemoteAppCollection** , **set-AzureRemoteAppWorkspace** , **Disconnect-AzureRemoteAppSession** e altri.

## ESEMPI

### Esempio 1: usare un ID di rilevamento per ottenere un risultato dell'operazione
```
PS C:\> $result = New-AzureRemoteAppCollection -CollectionName Contoso -ImageName "Windows Server 2012 R2" -Plan Standard -Location "West US" -Description CloudOnly
PS C:\> Get-AzureRemoteAppOperationResult -TrackingId $result.Tracking
```

Questo comando Salva l'ID di rilevamento restituito da un'operazione RemoteApp di Azure.
L'ID di rilevamento viene passato a **Get-AzureRemoteAppOperationResult** nel comando seguente.

## PARAMETRI

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

### -TrackingId
Specifica l'ID di rilevamento di un'operazione.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[Disconnetti-AzureRemoteAppSession](./Disconnect-AzureRemoteAppSession.md)

[Set-AzureRemoteAppWorkspace](./Set-AzureRemoteAppWorkspace.md)

[Update-AzureRemoteAppCollection](./Update-AzureRemoteAppCollection.md)


