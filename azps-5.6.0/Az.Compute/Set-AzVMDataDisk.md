---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDataDisk.md
ms.openlocfilehash: da4455e7d2630ddb263c56aae96be79fe3cc7a20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964989"
---
# Set-AzVMDataDisk

## SYNOPSIS
Modifica le proprietà di un disco dati della macchina virtuale.

## SINTASSI

### ChangeWithName
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ChangeWithLun
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>]
 [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Set-AzVMDataDisk** modifica le proprietà di un disco dati della macchina virtuale.

## ESEMPI

### Esempio 1: Modificare la modalità di memorizzazione nella cache di un disco dati
```powershell
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzVM
```

Il primo comando recupera la macchina virtuale denominata ContosoVM07 tramite **Get-AzVM.**
Il comando lo archivia nella $VM variabile.
Il secondo comando modifica la modalità di memorizzazione nella cache per il disco dati denominato DataDisk01 nella macchina virtuale in $VM.
Il comando passa il risultato al cmdlet Update-AzVM, che implementa le modifiche.
Una modifica alla modalità di pagamento fa sì che la macchina virtuale venga riavviata.

### Esempio 2

Modifica le proprietà di un disco dati della macchina virtuale. (autogenerati)

```powershell <!-- Aladdin Generated Example --> 
Set-AzVMDataDisk -Caching None -Lun 1 -VM <PSVirtualMachine>
```

## PARAMETERS

### -Memorizzazione nella cache
Specifica la modalità di memorizzazione nella cache del disco.
I valori accettabili per questo parametro sono:
- ReadOnly
- ReadWrite Il valore predefinito è ReadWrite.
Se si modifica questo valore, la macchina virtuale viene riavviata.
Questa impostazione influisce sulla coerenza e sulle prestazioni del disco.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.

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

### -DiskEncryptionSetId
Specifica l'ID risorsa del set di crittografia del disco gestito dal cliente.  Può essere specificato solo per il disco gestito.

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

### -DiskSizeInGB
Specifica le dimensioni, in gigabyte, del disco dati.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Lun
Specifica il numero di unità logiche (LUN) del disco dati modificato dal cmdlet.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ChangeWithLun
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Specifica il nome del disco dati modificato dal cmdlet.

```yaml
Type: System.String
Parameter Sets: ChangeWithName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountType
Tipo di account del disco gestito dalla macchina virtuale.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Specifica la macchina virtuale per cui questo cmdlet modifica un disco dati.
Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzVM.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WriteAccelerator
Specifica se WriteAccelerator deve essere abilitato o disabilitato nel disco dati.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.String

### System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

## OUTPUT

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzVM](./Get-AzVM.md)

[Update-AZVM](./Update-AzVM.md)


