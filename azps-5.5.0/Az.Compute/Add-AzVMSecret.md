---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
ms.openlocfilehash: 059aedf6ca3b5c229092f9ce536d23a8fc602830
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199359"
---
# Add-AzVMSecret

## SYNOPSIS
Aggiunge un segreto a una macchina virtuale.

## SINTASSI

```
Add-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Add-AzVMSecret** aggiunge un segreto a una macchina virtuale.
Questo valore consente di aggiungere un certificato alla macchina virtuale.
Il segreto deve essere archiviato in un Vault chiave.
Per altre informazioni sul Vault delle chiavi, vedere [Che cos'è il Vault delle chiavi di Azure?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).
Per altre informazioni sui cmdlet, vedere i cmdlet del Vault delle chiavi di [Azure](/powershell/module/az.keyvault) o il cmdlet [Set-AzKeyVaultSecret.](/powershell/module/az.keyvault/set-azkeyvaultsecret)

## ESEMPI

### Esempio 1: Aggiungere un segreto a una macchina virtuale
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

Il primo comando crea un oggetto macchina virtuale e quindi lo archivia nella $VirtualMachine variabile.
Il comando assegna un nome e le dimensioni alla macchina virtuale.
Il secondo comando crea un oggetto credenziali usando il cmdlet Get-Credential e quindi archivia il risultato nella $Credential variabile.
Il comando chiede di specificare un nome utente e una password.
Per altre informazioni, digitare `Get-Help Get-Credential` .
Il terzo comando usa il cmdlet **Set-AzVMOperatingSystem** per configurare la macchina virtuale archiviata in $VirtualMachine.
Il quarto comando assegna un ID vault di origine alla variabile $SourceVaultId per un uso futuro.
Il comando presuppone che la $SubscriptionId variabile abbia un valore appropriato.
Il quinto comando assegna un valore alla variabile $CertificateStore 01 per un uso futuro.
Il sesto comando assegna un URL a un archivio certificati.
Il settimo comando aggiunge un segreto alla macchina virtuale archiviata in $VirtualMachine.
Il parametro SourceVaultId specifica il Vault delle chiavi.
Il comando specifica il nome dell'archivio certificati e l'URL del certificato.
È possibile eseguire **Add-AzVMSecret** più volte per aggiungere informazioni segrete per altri certificati.

## PARAMETERS

### -CertificateStore
Specifica il nome di un archivio certificati nella macchina virtuale che esegue il sistema operativo Windows.
Questo cmdlet aggiunge il certificato all'archivio specificato da questo parametro.
È possibile specificare questo parametro solo per le macchine virtuali che eseguono il sistema operativo Windows.

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

### -CertificateUrl
Specifica l'URL che punta a un segreto del Vault chiave che contiene un certificato.
Il certificato è la codifica Base64 dell'oggetto JSON (JavaScript Object Notation) seguente, codificato in UTF-8: { "data": " \<Base64-encoded-file\> ", "dataType": " \<file-format\> ", "password": " " } Attualmente, dataType accetta solo file \<pfx-file-password\> PFX.

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

### -SourceVaultId
Specifica l'ID della risorsa del Vault delle chiavi che contiene i certificati che è possibile aggiungere alla macchina virtuale.
Questo valore funge anche da chiave per l'aggiunta di più certificati.
Questo significa che è possibile usare lo stesso valore per *SourceVaultId* quando si aggiungono più certificati dallo stesso Vault delle chiavi.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Specifica l'oggetto della macchina virtuale modificato dal cmdlet.
Per ottenere un oggetto macchina virtuale, usare il cmdlet [Get-AzVM.](./Get-AzVM.md)
È possibile usare il cmdlet [New-AzVMConfig](./New-AzVMConfig.md) per creare un oggetto macchina virtuale.

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

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.String

## OUTPUT

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AZVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)

[Set-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)
