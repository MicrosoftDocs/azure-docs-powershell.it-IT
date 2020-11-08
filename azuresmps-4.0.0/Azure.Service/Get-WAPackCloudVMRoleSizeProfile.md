---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 453AEA42-E29C-4FF2-9210-0DD88B77DC07
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29c7f8bc814ddf5295064d89eeaf34c8e7274916
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029970"
---
# Get-WAPackCloudVMRoleSizeProfile

## Sinossi
Ottiene gli oggetti del profilo di dimensione del ruolo Cloud VM.

## SINTASSI

### Empty (impostazione predefinita)
```
Get-WAPackCloudVMRoleSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromName
```
Get-WAPackCloudVMRoleSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Get-WAPackCloudVMRoleSizeProfile** ottiene gli oggetti del profilo delle dimensioni del ruolo Cloud VM per le macchine virtuali.

## ESEMPI

### Esempio 1: ottenere un profilo di dimensione del ruolo di VM cloud usando un nome
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile -Name "Small"
```

Questo comando consente di ottenere il profilo delle dimensioni denominato Small.

### Esempio 2: ottenere tutti i profili delle dimensioni del ruolo Cloud VM
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile
```

Questo comando ottiene tutti i profili di dimensione.

## PARAMETRI

### -Nome
Specifica il nome di un profilo di dimensione del ruolo di VM cloud.

```yaml
Type: String
Parameter Sets: FromName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

## OUTPUT

## Note

## COLLEGAMENTI CORRELATI

[Get-WAPackVM](./Get-WAPackVM.md)


