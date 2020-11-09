---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 71bd8ca26755118a4bb9c075ae89bad765922f3d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296472"
---
# Set-AzVmssOsProfile

## Sinossi
Imposta le proprietà del profilo del sistema operativo VMSS.

## SINTASSI

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **set-AzVmssOsProfile** imposta la scala della macchina virtuale imposta le proprietà del profilo del sistema operativo.

## ESEMPI

### Esempio 1: impostare le proprietà del profilo del sistema operativo per un VMSS
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

Questo comando imposta le proprietà del profilo del sistema operativo per le macchine virtuali che appartengono al VMSS denominato ContosoVMSS.
Il comando imposta il prefisso del nome computer per tutte le istanze della macchina virtuale in VMSS per testare e fornire il nome utente e la password dell'amministratore.

## PARAMETRI

### -AdditionalUnattendContent
Specifica un oggetto contenuto non presidiato.
Puoi usare la Add-AzVMAdditionalUnattendContent per creare l'oggetto.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AdminPassword
Specifica la password di amministratore da usare per tutte le istanze della macchina virtuale in VMSS.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AdminUsername
Specifica il nome dell'account di amministratore da usare per tutte le istanze della macchina virtuale in VMSS. <br>
**Restrizione solo per Windows:** Non può terminare \" .\" <br>
**Valori non consentiti:** \" Administrator \" , \" admin \" , \" User \" , \" User1 \" , \" test \" , \" User2 \" , \" test1 \" , \" User3 \" , \" Admin1 \" , \" 1 \" , \" 123 \" , \" a \" , \" ACTUser \" , \" adm \" , \" Amministratore2 \" , \" ASPNET \" , \" backup \" , \" console \" , \" David \" , \" Guest \" , \" John \" , \" owner \" , \" root \" , \" server \" , \" SQL \" , \" support \" , \" Support_388945a0 \" , \" sys \" , \" test2 \" , \" test3 \" , \" User4 \" , \" User5 \" . <br>
**Lunghezza minima (Linux):** 1 carattere <br>
**Lunghezza max (Linux):** 64 caratteri <br>
**Lunghezza max (Windows):** 20 caratteri  <br>
<li> Per l'accesso root alla VM Linux, vedere [uso dei privilegi di root nelle macchine virtuali Linux in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).<br>
<li> Per un elenco di utenti di sistema predefiniti su Linux che non devono essere usati in questo campo, vedere [selezione di nomi utente per Linux in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ComputerNamePrefix
Specifica il prefisso del nome computer per tutte le istanze della macchina virtuale in VMSS.
I nomi dei computer devono essere lunghi da 1 a 15 caratteri.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CustomData
Specifica una stringa codificata di base-64 di dati personalizzati.
Questa operazione viene decodificata in una matrice binaria che viene salvata come file nella macchina virtuale.
La lunghezza massima della matrice binaria è di 65535 byte. <br>
Per usare cloud-init per la tua VM, Vedi [uso di cloud-init per personalizzare una VM di Linux durante la creazione](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).

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

### -LinuxConfigurationDisablePasswordAuthentication
Indica che questo cmdlet disabilita l'autenticazione tramite password.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Listener
Specifica i listener di gestione remota (WinRM) di Windows.
In questo modo viene abilitato Windows PowerShell remoto.
Puoi usare il cmdlet Add-AzVmssWinRMListener per creare il listener.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.WinRMListener[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicKey
Specifica l'oggetto chiave pubblica Secure Shell (SSH).
Puoi usare il cmdlet Add-AzVMSshPublicKey per creare l'oggetto.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.SshPublicKey[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Segreto
Specifica l'oggetto Secrets che contiene i riferimenti di certificato da posizionare nella macchina virtuale.
Puoi usare il cmdlet Add-AzVmssSecret per creare l'oggetto Secrets.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TimeZone
Specifica il fuso orario della macchina virtuale. ad esempio \" ora solare Pacifico \" . <br>
I valori possibili possono essere [TimeZoneInfo.ID](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) valore da fusi orari restituiti da [TimeZoneInfo. GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Specifica l'oggetto VMSS.
Puoi usare il cmdlet New-AzVmssConfig per creare l'oggetto.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WindowsConfigurationEnableAutomaticUpdate
Indica se le macchine virtuali in VMSS sono abilitate per gli aggiornamenti automatici.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WindowsConfigurationProvisionVMAgent
Indica se l'agente macchina virtuale deve essere eseguito il provisioning sulle macchine virtuali in VMSS.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito. Il cmdlet non viene eseguito.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INGRESSI

### Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet

### System. String

### System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

### Microsoft. Azure. Management. Compute. Models. AdditionalUnattendContent []

### Microsoft. Azure. Management. Compute. Models. WinRMListener []

### Microsoft. Azure. Management. Compute. Models. SshPublicKey []

### Microsoft. Azure. Management. Compute. Models. VaultSecretGroup []

## OUTPUT

### Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet

## Note

## COLLEGAMENTI CORRELATI

[Add-AzVMAdditionalUnattendContent](./Add-AzVMAdditionalUnattendContent.md)

[Add-AzVmssWinRMListener](./Add-AzVmssWinRMListener.md)

[Add-AzVMSshPublicKey](./Add-AzVMSshPublicKey.md)

[Add-AzVmssSecret](./Add-AzVmssSecret.md)

[New-AzVmssConfig](./New-AzVmssConfig.md)


