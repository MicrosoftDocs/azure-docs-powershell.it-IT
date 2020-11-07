---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsecret
schema: 2.0.0
ms.openlocfilehash: 70342620aeab42ba7236091e8aacc32ea44354ef
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866771"
---
# Add-AzureRmVMSecret

## Sinossi
Aggiunge un segreto a una macchina virtuale.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
Add-AzureRmVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Add-AzureRmVMSecret** aggiunge un segreto a una macchina virtuale.
Questo valore consente di aggiungere un certificato alla macchina virtuale.
Il segreto deve essere archiviato in un caveau chiave.
Per altre informazioni su Key Vault, vedere [cos'è Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).
Per altre informazioni sui cmdlet, vedere cmdlet di [Key Vault di Azure](https://msdn.microsoft.com/library/azure/dn868052.aspx) nella raccolta di reti Microsoft Developer o nel cmdlet [set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) .

## ESEMPI

### Esempio 1: aggiungere un segreto a una macchina virtuale
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzureRmVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

Il primo comando crea un oggetto macchina virtuale e lo archivia nella variabile $VirtualMachine.
Il comando assegna un nome e una dimensione alla macchina virtuale.

Il secondo comando crea un oggetto Credential usando il cmdlet Get-Credential e quindi archivia il risultato nella variabile $Credential.
Il comando richiede un nome utente e una password.
Per altre informazioni, digitare `Get-Help Get-Credential` .

Il terzo comando usa il cmdlet **set-AzureRmVMOperatingSystem** per configurare la macchina virtuale archiviata in $virtualmachine.

Il quarto comando assegna un ID di archiviazione di origine alla variabile $SourceVaultId per un uso successivo.
Il comando presuppone che la variabile $SubscriptionId abbia un valore appropriato.

Il quinto comando assegna un valore alla variabile $CertificateStore 01 per un uso successivo.

Il sesto comando assegna un URL per un archivio certificati.

Il settimo comando aggiunge un segreto alla macchina virtuale archiviata in $VirtualMachine.
Il parametro SourceVaultId specifica il Vault chiave.
Il comando specifica il nome dell'archivio certificati e l'URL del certificato.
Puoi eseguire ripetutamente il **componente aggiuntivo AzureRmVMSecret** per aggiungere segreti ad altri certificati.

## PARAMETRI

### -CertificateStore
Specifica il nome di un archivio certificati nella macchina virtuale che esegue il sistema operativo Windows.
Questo cmdlet aggiunge il certificato allo Store specificato da questo parametro.
Puoi specificare questo parametro solo per le macchine virtuali che eseguono il sistema operativo Windows.

```yaml
Type: String
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

Il certificato è la codifica Base64 dell'oggetto JSON (JavaScript Object Notation) seguente, codificato in UTF-8:

{"data": " \<Base64-encoded-file\> ", "tipo di dati": " \<file-format\> ", "password": " \<pfx-file-password\> "}


Attualmente, il tipo di dati accetta solo i file PFX.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceVaultId
Specifica l'ID risorsa del Vault chiave che contiene i certificati che è possibile aggiungere alla macchina virtuale.
Questo valore funge anche da chiave per l'aggiunta di più certificati.
Questo significa che puoi usare lo stesso valore per *SourceVaultId* quando Aggiungi più certificati dallo stesso Vault chiave.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Specifica l'oggetto macchina virtuale modificato da questo cmdlet.
Per ottenere un oggetto macchina virtuale, usare il cmdlet [Get-AzureRmVM](./Get-AzureRmVM.md) .
Puoi usare il cmdlet [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) per creare un oggetto macchina virtuale.

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### PSVirtualMachine
Il parametro ' VM ' accetta il valore di tipo ' PSVirtualMachine ' dalla pipeline

## OUTPUT

### Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmVM](./Get-AzureRmVM.md)

[New-AzureRmVMConfig](./New-AzureRmVMConfig.md)

[Set-AzureRmVMOperatingSystem](./Set-AzureRmVMOperatingSystem.md)
