---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: E771D1F2-A06B-44BB-AAFF-9459DC6303E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 273edfe08e4d2476cd4c1baa2967a829ec1bbcc2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023406"
---
# Select-AzureStorSimpleResource

## Sinossi
Imposta una risorsa come risorsa corrente.

## SINTASSI

```
Select-AzureStorSimpleResource -ResourceName <String> [-RegistrationKey <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Descrizione
Il cmdlet **Select-AzureStorSimpleResource** imposta una risorsa come risorsa corrente.
Dopo aver selezionato una risorsa, gli altri cmdlet si applicano all'interno del contesto della risorsa.

## ESEMPI

### Esempio 1: selezionare una risorsa per la prima volta
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa" -RegistrationKey "<your registration key>"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

Questo comando consente di selezionare la risorsa denominata Contoso64-Tsqa come contesto corrente.
In questo esempio il computer non ha avuto questo contesto inizializzato in precedenza e, pertanto, devi specificare un valore per il parametro *RegistrationKey* .

### Esempio 2: tentativo di selezione di una risorsa
```
This command gets the current context for this computer by using the **Get-AzureStorSimpleResourceContext** cmdlet. The current selected resource is Contoso64-Tsqa. This is consistent with the previous example. 
PS C:\>Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa 

This command attempts to reset the resource to be Contoso02-Resource. For this example, this resource has not been previously selected. The registration key is not saved or included in the command. The command cannot select the resource. 
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso02-Resource"
Select-AzureStorSimpleResource : Could not find the persisted secret. Please use Select-AzureStorSimpleResource and
provide the Registration key once again.
```

### Esempio 3: selezionare una risorsa selezionata in precedenza
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

Questo comando consente di selezionare la risorsa denominata Contoso64-Tsqa come contesto corrente.
In questo esempio, il contesto è stato selezionato in precedenza e, pertanto, non è necessario specificare un valore per il parametro *RegistrationKey* .

## PARAMETRI

### -Profile
Specifica un profilo Azure.

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

### -RegistrationKey
Specifica una chiave di registrazione.
Specificare una chiave per la prima volta che si seleziona una risorsa.
Quando questo cmdlet seleziona la risorsa corrente, i cmdlet usano questa chiave, se necessario.
Per altre informazioni, vedere [ottenere la chiave di registrazione del servizio](https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx)  ( https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx) nella rete Microsoft Developer Network.

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

### -ResourceName
Specifica il nome della risorsa da selezionare come risorsa corrente.

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

## OUTPUT

### StorSimpleResourceContext
Questo cmdlet restituisce un oggetto **StorSimpleResourceContext** che contiene dettagli per il contesto della risorsa.

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureStorSimpleResource](./Get-AzureStorSimpleResource.md)

[Get-AzureStorSimpleResourceContext](./Get-AzureStorSimpleResourceContext.md)


