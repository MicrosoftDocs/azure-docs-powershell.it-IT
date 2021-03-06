---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 753c1de5b2f967ad321334231c77e379e11bc2ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031852"
---
# Set-AzVMSqlServerExtension

## Sinossi
Imposta l'estensione di Azure SQL Server in una macchina virtuale.

## SINTASSI

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzVMSqlServerExtension** imposta l'estensione del server AzureSQL in una macchina virtuale.

## ESEMPI

### Esempio 1: impostare le impostazioni di correzione automatica in una macchina virtuale
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

Il primo comando crea un oggetto Configuration usando il cmdlet **New-AzVMSqlServerAutoPatchingConfig** .
Il comando Archivia la configurazione nella variabile $AutoPatchingConfig.
Il secondo comando consente di ottenere la macchina virtuale denominata VirtualMachine11 nel servizio denominato Service02 usando il cmdlet Get-AzVM.
Il comando passa l'oggetto al cmdlet corrente usando l'operatore pipeline.
Il cmdlet corrente imposta le impostazioni di correzione automatica in $AutoPatchingConfig per la macchina virtuale.
Il comando passa la macchina virtuale al cmdlet Update-AzVM.

### Esempio 2: impostare le impostazioni di backup automatico in una macchina virtuale
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

Il primo comando crea un oggetto Configuration usando il cmdlet **New-AzVMSqlServerAutoBackupConfig** .
Il comando Archivia la configurazione nella variabile $AutoBackupConfig.
Il secondo comando consente di ottenere la macchina virtuale denominata VirtualMachine11 nel servizio denominato Service02 e quindi di passarla al cmdlet corrente.
Il cmdlet Current imposta le impostazioni di backup automatico in $AutoBackupConfig per la macchina virtuale.
Il comando passa la macchina virtuale al cmdlet Update-AzVM.

### Esempio 3: disabilitare un'estensione di SQL Server in una macchina virtuale
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

Questo comando consente di ottenere una macchina virtuale denominata VirtualMachine08 in Service03 e quindi di passarla al cmdlet corrente.
Il comando Disabilita l'estensione della macchina virtuale di SQL Server in quella macchina virtuale.

### Esempio 4: disinstallare un'estensione di SQL Server in una specifica macchina virtuale
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

Questo comando consente di ottenere una macchina virtuale denominata VirtualMachine08 in Service03 e quindi di passarla al cmdlet corrente.
Il comando disinstalla un'estensione della macchina virtuale di SQL Server in quella macchina virtuale.

## PARAMETRI

### -AutoBackupSettings
Specifica le impostazioni di backup automatico di SQL Server.
Per creare un oggetto **AutoBackupSettings** , usa il cmdlet New-AzVMSqlServerAutoBackupConfig.

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoBackupSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutoPatchingSettings
Specifica le impostazioni di correzione automatica di SQL Server.
Per creare un oggetto **AutoPatchingSettings** , usa il cmdlet New-AzVMSqlServerAutoPatchingConfig.

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoPatchingSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVaultCredentialSettings
```yaml
Type: Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Posizione
Specifica la posizione della macchina virtuale.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Specifica il nome dell'estensione di SQL Server.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome del gruppo di risorse della macchina virtuale.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Versione
Specifica la versione dell'estensione di SQL Server.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Specifica il nome della macchina virtuale in cui questo cmdlet imposta l'estensione di SQL Server.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### System. String

### Microsoft. Azure. Commands. Compute. AutoPatchingSettings

### Microsoft. Azure. Commands. Compute. AutoBackupSettings

### Microsoft. Azure. Commands. Compute. KeyVaultCredentialSettings

## OUTPUT

### Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse

## Note

## COLLEGAMENTI CORRELATI

[Get-AzVM](./Get-AzVM.md)

[Get-AzVMSqlServerExtension](./Get-AzVMSqlServerExtension.md)

[New-AzVMSqlServerAutoPatchingConfig](./New-AzVMSqlServerAutoPatchingConfig.md)

[New-AzVMSqlServerAutoBackupConfig](./New-AzVMSqlServerAutoBackupConfig.md)

[Remove-AzVMSqlServerExtension](./Remove-AzVMSqlServerExtension.md)

[Update-AzVM](./Update-AzVM.md)


