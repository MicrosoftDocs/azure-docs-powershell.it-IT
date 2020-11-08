---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 53580FF1-D905-40FD-A5F0-D5FBCD036E0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: a51fd8210d2fe7fb224ed43650a354e383ed4e54
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023734"
---
# Start-AzureStorSimpleDeviceFailoverJob

## Sinossi
Avvia un'operazione di failover dei gruppi di contenitori di volumi.

## SINTASSI

### Empty (impostazione predefinita)
```
Start-AzureStorSimpleDeviceFailoverJob
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyById
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceId <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByName
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceName <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceName <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Start-AzureStorSimpleDeviceFailoverJob** avvia un'operazione di failover di uno o più gruppi di contenitori di volumi da un dispositivo a un altro.

## ESEMPI

### Esempio 1: avviare un processo di failover per un dispositivo denominato e un dispositivo di destinazione denominato
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Start-AzureStorSimpleDeviceFailoverJob -DeviceName "ChewD_App7" -TargetDeviceName "Fuller05" -Force
a3d902be-8ffb-42a4-bbf8-0a1b30db71b2_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

Questo comando ottiene i contenitori del volume di failover per il dispositivo denominato ChewD_App7 usando il cmdlet **Get-AzureStorSimpleFailoverVolumeContainers** .
Il comando passa i risultati al cmdlet **Where-Object** , che elimina i contenitori che hanno un valore diverso da $true per la proprietà **IsDCGroupEligibleForDR** .
Per altre informazioni, digitare `Get-Help Where-Object` .
Il cmdlet corrente avvia i processi di failover per i contenitori del volume di failover rimanenti.
Il comando specifica il nome del dispositivo e il nome del dispositivo di destinazione.
Il comando restituisce l'ID istanza del processo che viene avviato dal cmdlet.

### Esempio 2: avviare un processo di failover per un dispositivo e un dispositivo di destinazione specificato da ID
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Select-Object -First 1 | Start-AzureStorSimpleDeviceFailoverJob -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925" -TargetDeviceId "0ee59ae9-0293-46e2-ae56-bc308c8e5520" -Force
4c5ac0d0-4b66-465c-98f5-aec90505ad12_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

Questo comando ottiene i contenitori del volume di failover per il dispositivo denominato ChewD_App7 tramite **Get-AzureStorSimpleFailoverVolumeContainers**.
Il comando passa i risultati a **Where-Object** , che elimina i containers che hanno un valore diverso da $true per la proprietà **IsDCGroupEligibleForDR** .
Il cmdlet passa i risultati al cmdlet **Select-Object** , che seleziona il primo oggetto da passare al cmdlet corrente.
Per altre informazioni, digitare `Get-Help Select-Object` .
Il cmdlet corrente avvia i processi di failover per il contenitore del volume di failover selezionato.
Il comando specifica l'ID del dispositivo e l'ID del dispositivo di destinazione.
Il comando restituisce l'ID istanza del processo che viene avviato dal cmdlet.

## PARAMETRI

### -DeviceId
Specifica l'ID istanza del dispositivo StorSimple in cui sono presenti i gruppi di contenitori del volume.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Specifica il nome del dispositivo StorSimple in cui sono presenti i gruppi di contenitori del volume.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Impone l'esecuzione del comando senza richiedere la conferma dell'utente.

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

### -TargetDeviceId
Specifica l'ID istanza del dispositivo StorSimple a cui il cmdlet non riesce sui gruppi di contenitori del volume.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDeviceName
Specifica il nome del dispositivo StorSimple a cui questo cmdlet ha esito negativo sui gruppi di contenitori del volume.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VolumecontainerGroups
Specifica l'elenco dei gruppi di contenitori di volumi a cui il cmdlet esegue il failover su un altro dispositivo.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Elenco\<DataContainerGroup\>
È possibile reindirizzare un elenco di gruppi di contenitori di volumi a questo cmdlet.

## OUTPUT

### Stringa

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureStorSimpleFailoverVolumeContainers](./Get-AzureStorSimpleFailoverVolumeContainers.md)


