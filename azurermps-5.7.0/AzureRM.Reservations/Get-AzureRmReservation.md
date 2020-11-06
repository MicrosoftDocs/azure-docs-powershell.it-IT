---
external help file: Microsoft.Azure.Commands.Reservations.dll-Help.xml
Module Name: AzureRM.Reservations
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.reservations/get-azurermreservation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Reservations/Commands.Reservations/help/Get-AzureRmReservation.md
ms.openlocfilehash: 443f7c161cf2e3e44b2e080ef5adbc27665833bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508003"
---
# Get-AzureRmReservation

## Sinossi
Ottenere `Reservation` s in un ordine di prenotazione specifico

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### CommandLine (impostazione predefinita)
```
Get-AzureRmReservation -ReservationOrderId <String> [-ReservationId <String>] [<CommonParameters>]
```

### PipeObject
```
Get-AzureRmReservation [-ReservationOrder <PSReservationOrder>]
 [-ReservationOrderPage <PSReservationOrderPage>] [<CommonParameters>]
```

## Descrizione
Elenco `Reservation` s all'interno di un singolo `ReservationOrder` .

## ESEMPI

### Esempio 1
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff"
```

Elenco `Reservation` s all'interno dell'oggetto specificato `ReservationOrder` .

### Esempio 2
```
PS C:\> Get-AzureRmReservation -ReservationOrderId "1111aaaa-b1b2-c0c2-d0d2-00000fffff" -ReservationId "11111111-1111-1111-1111-1111111111"
```

Ottenere `Reservation` dettagli specifici.

## PARAMETRI

### -ReservationId
ID dell'interfaccia `Reservation` da esaminare

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ReservationOrder
Parametro oggetto pipe per `ReservationOrder`

```yaml
Type: PSReservationOrder
Parameter Sets: PipeObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ReservationOrderId
ID dell' `ReservationOrder` che contiene `Reservation` . Obbligatorio.

```yaml
Type: String
Parameter Sets: CommandLine
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ReservationOrderPage
Parametro oggetto pipe per `ReservationOrder`

```yaml
Type: PSReservationOrderPage
Parameter Sets: PipeObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### System. String
Microsoft. Azure. Commands. reservations. Models. PSReservationOrder Microsoft. Azure. Commands. reservations. Models. PSReservationOrderPage

## OUTPUT

### Microsoft. Azure. Commands. reservations. Models. PSReservationPage
Microsoft. Azure. Commands. reservations. Models. PSReservation

## Note

## COLLEGAMENTI CORRELATI

