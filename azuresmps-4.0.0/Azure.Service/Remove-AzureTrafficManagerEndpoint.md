---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 50B83AEC-1B32-4089-9804-D388677C3F7E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7388841c48f2f7c6ba0752748b245cce1f8b5c4e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029554"
---
# Remove-AzureTrafficManagerEndpoint

## Sinossi
Rimuove un endpoint da un profilo di gestione traffico.

## SINTASSI

```
Remove-AzureTrafficManagerEndpoint -DomainName <String> [-Force]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Remove-AzureTrafficManagerEndpoint** consente di rimuovere un endpoint da un profilo di Microsoft Azure Traffic Manager.
Dopo aver rimosso un endpoint, passare il risultato al cmdlet **set-AzureTrafficManagerProfile** usando l'operatore pipeline.
Questo cmdlet si connette a Azure per salvare le modifiche.

## ESEMPI

### Esempio 1: rimuovere un endpoint da un profilo
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Remove-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" | Set-AzureTrafficManagerProfile
```

Il primo comando usa il cmdlet **Get-AzureTrafficManagerProfile** per ottenere il profilo denominato ContosoProfile e lo archivia nella variabile $TrafficManagerProfile.

Il secondo comando rimuove un endpoint con il nome di dominio Contoso02App.cloudapp.net dal profilo di Traffic Manager archiviato in $TrafficManagerProfile.
Il comando passa l'oggetto profile al cmdlet **set-AzureTrafficManagerProfile** per connettersi a Azure per salvare le modifiche.

## PARAMETRI

### -DomainName
Specifica il nome di dominio dell'endpoint da rimuovere.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
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

### -TrafficManagerProfile
Specifica l'oggetto profilo Traffic Manager da cui rimuovere l'endpoint.

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

### Microsoft. WindowsAzure. Commands. Utilities. TrafficManager. Models. IProfileWithDefinition
Questo cmdlet genera un oggetto profilo di Traffic Manager, che contiene informazioni sul profilo aggiornato.

## Note

## COLLEGAMENTI CORRELATI

[Add-AzureTrafficManagerEndpoint](./Add-AzureTrafficManagerEndpoint.md)

[Set-AzureTrafficManagerEndpoint](./Set-AzureTrafficManagerEndpoint.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


