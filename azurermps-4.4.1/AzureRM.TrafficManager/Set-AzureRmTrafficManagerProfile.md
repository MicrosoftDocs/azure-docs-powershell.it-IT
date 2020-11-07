---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: e8baf033131442f23a0db63339673018b209f140
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686542"
---
# Set-AzureRmTrafficManagerProfile

## Sinossi
Aggiorna un profilo di gestione traffico.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Set-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzureRmTrafficManagerProfile** aggiorna un profilo di Azure Traffic Manager.
Questo cmdlet aggiorna le impostazioni del profilo da un oggetto profilo locale.
Puoi specificare l'oggetto profile usando il parametro *TrafficManagerProfile* o usando la pipeline.

Puoi ottenere un oggetto locale che rappresenta un profilo usando il cmdlet Get-AzureRmTrafficManagerProfile.
Modificare l'oggetto localmente e quindi usare **set-AzureRmTrafficManagerProfile** per eseguire il commit delle modifiche.

## ESEMPI

### Esempio 1: aggiornare un profilo
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

Il primo comando ottiene un profilo di Azure Traffic Manager usando il cmdlet Get-AzureRmTrafficManagerProfile.
Il comando Archivia il profilo localmente nella variabile $TrafficManagerProfile.

Il secondo comando cambia il profilo localmente.
Questo comando Disabilita il profilo.

Il terzo comando Aggiorna il profilo di Traffic Manager denominato ContosoProfile in base al valore locale in $TrafficManagerProfile.

## PARAMETRI

### -TrafficManagerProfile
Specifica un oggetto **TrafficManagerProfile** locale.
Questo cmdlet aggiorna Traffic Manager in base a questo oggetto locale.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Microsoft. Azure. Commands. Network. TrafficManagerProfile
Questo cmdlet accetta un oggetto **TrafficManagerProfile** .

## OUTPUT

### Microsoft. Azure. Commands. Network. TrafficManagerProfile
Questo cmdlet restituisce un oggetto **TrafficManagerProfile** .

## Note

## COLLEGAMENTI CORRELATI

[Add-AzureRmTrafficManagerEndpointConfig](./Add-AzureRmTrafficManagerEndpointConfig.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerProfile.md)

[New-AzureRmTrafficManagerProfile](./New-AzureRmTrafficManagerProfile.md)

[Remove-AzureRmTrafficManagerEndpointConfig](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[Remove-AzureRmTrafficManagerProfile](./Remove-AzureRmTrafficManagerProfile.md)


