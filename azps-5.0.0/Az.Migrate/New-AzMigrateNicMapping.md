---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratenicmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
ms.openlocfilehash: 118e96747d3859a7b9132747052fb3407b7201ae
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202332"
---
# New-AzMigrateNicMapping

## Sinossi
Crea un oggetto per aggiornare le proprietà NIC di un server di replica.

## SINTASSI

```
New-AzMigrateNicMapping -NicID <String> [-TargetNicIP <String>] [-TargetNicSelectionType <String>]
 [-TargetNicSubnet <String>] [<CommonParameters>]
```

## Descrizione
Il cmdlet New-AzMigrateNicMapping crea un mapping della scheda NIC di origine collegata al server di cui eseguire la migrazione.
Questo oggetto viene fornito come input per il cmdlet Set-AzMigrateServerReplication per aggiornare la scheda NIC e le relative proprietà per un server di replica.

## ESEMPI

### Esempio 1: creare un oggetto NIC
```powershell
PS C:\> New-AzMigrateNicMapping -NicID a2399354-653a-464e-a567-d30ef5467a31 -TargetNicSelectionType primary -TargetNicIP "172.17.1.17"

IsPrimaryNic IsSelectedForMigration NicId                                TargetStaticIPAddress TargetSubnetName
------------ ---------------------- -----                                --------------------- ----------------
false        false                  a2399354-653a-464e-a567-d30ef5467a31
```

Crea un oggetto di aggiornamento di NIC.

## PARAMETRI

### -NicID
Specifica l'ID della scheda NIC da aggiornare.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetNicIP
Specifica l'IP all'interno della subnet di destinazione da usare per la scheda NIC.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetNicSelectionType
Specifica se il NIC da aggiornare sarà primario, secondario o non migrato.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetNicSubnet
Specifica il nome della subnet per la scheda NIC nella rete virtuale di destinazione a cui deve essere eseguita la migrazione del server.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

## OUTPUT

### Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180110. IVMwareCbtNicInput

## Note

ALIAS

## COLLEGAMENTI CORRELATI

