---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://go.microsoft.com/fwlink/?LinkId=690295
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultKey.md
ms.openlocfilehash: 0046a1ed2b2580d1cafbdaa31d9fad53a09ea644
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522133"
---
# Add-AzureKeyVaultKey

## Sinossi
Crea una chiave in un Vault chiave o importa una chiave in un Vault chiave.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

### Crea (impostazione predefinita)
```
Add-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Importazione
```
Add-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **Add-AzureKeyVaultKey** crea una chiave in un Vault chiave in Azure Key Vault o importa una chiave in un Vault chiave.
Questo cmdlet consente di aggiungere chiavi utilizzando uno dei metodi seguenti:

- Creare una chiave in un modulo di sicurezza hardware (HSM) nel servizio Key Vault.
- Creare una chiave nel software nel servizio Key Vault.
- Importare una chiave da un modulo HSM (hardware Security Module) in HSM nel servizio Key Vault.
- Importare una chiave da un file con estensione pfx nel computer.
- Importare una chiave da un file PFX nel computer in moduli di sicurezza hardware (HSM) nel servizio Key Vault.

Per ognuna di queste operazioni, è possibile specificare gli attributi chiave o accettare le impostazioni predefinite.

Se si crea o si importa una chiave con lo stesso nome di una chiave esistente nel Vault chiave, la chiave originale viene aggiornata con i valori specificati per la nuova chiave. Puoi accedere ai valori precedenti usando l'URI specifico della versione per la versione della chiave. Per informazioni sulle versioni chiave e sulla struttura URI, vedere [informazioni sulle chiavi andSecrets](https://go.microsoft.com/fwlink/?linkid=518560) nella documentazione dell'API REST di Key Vault.

Nota: per importare una chiave dal modulo di sicurezza hardware, è necessario prima di tutto generare un pacchetto BYOK (un file con estensione BYOK) usando il set di strumenti di BYOK Key Vault di Azure. Per altre informazioni, vedere [come generare e trasferire HSM-Protected chiavi per Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).

Come procedura consigliata, eseguire il backup della chiave dopo la creazione o l'aggiornamento usando il cmdlet Backup-AzureKeyVaultKey. Non esiste alcuna funzionalità di annullamento dell'eliminazione, quindi se si elimina accidentalmente la chiave o la si elimina e quindi si cambia idea, la chiave non è recuperabile, a meno che non si disponga di un backup che è possibile ripristinare.

## ESEMPI

### Esempio 1: creare una chiave
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Destination 'Software'
```

Questo comando crea una chiave protetta dal software denominata ITSoftware nel caveau della chiave denominata Contoso.

### Esempio 2: creare un tasto protetto da HSM
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITHsm' -Destination 'HSM'
```

Questo comando crea una chiave con protezione HSM nel Vault chiave denominata Contoso.

### Esempio 3: creare una chiave con valori non predefiniti
```
PS C:\>$KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags
```

Con il primo comando vengono archiviati i valori decrittografati e verificati nella variabile $KeyOperations.

Il secondo comando crea un oggetto **DateTime** , definito in formato UTC, usando il cmdlet **get-date** .
L'oggetto specifica un periodo di due anni nel futuro. Il comando archivia tale data nella variabile $Expires. Per altre informazioni, digitare `Get-Help Get-Date` .

Il terzo comando crea un oggetto **DateTime** usando il cmdlet **get-date** . Tale oggetto specifica l'ora UTC corrente. Il comando archivia tale data nella variabile $NotBefore.

Il comando finale crea una chiave denominata ITHsmNonDefault che è una chiave protetta da HSM. Il comando specifica i valori per le operazioni chiave consentite archiviate $KeyOperations. Il comando specifica gli orari per i parametri *Expires* e *NotBefore* creati nei comandi precedenti e i tag per l'elevata gravità. La nuova chiave è disabilitata. Puoi abilitarlo usando il cmdlet **set-AzureKeyVaultKey** .

### Esempio 4: importare un tasto protetto da HSM
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'
```

Questo comando importa la chiave denominata ITByok dalla posizione specificata dal parametro *filePath* . La chiave importata è una chiave con protezione HSM.

Per importare una chiave dal modulo di sicurezza hardware, è necessario prima di tutto generare un pacchetto BYOK (un file con estensione BYOK) usando il set di strumenti di BYOK Key Vault di Azure.
Per altre informazioni, vedere [come generare e trasferire HSM-Protected chiavi per Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).

### Esempio 5: importare una chiave protetta dal software
```
PS C:\>$Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password
```

Il primo comando converte una stringa in una stringa sicura usando il cmdlet **ConvertTo-SecureString** e quindi archivia la stringa nella variabile $password. Per altre informazioni, digitare `Get-Help
ConvertTo-SecureString` .

Il secondo comando crea una password software nel caveau della chiave contoso. Il comando specifica la posizione per la chiave e la password archiviata in $Password.

### Esempio 6: importare una chiave e assegnare attributi
```
PS C:\>$Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = null }
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags
```

Il primo comando converte una stringa in una stringa sicura usando il cmdlet **ConvertTo-SecureString** e quindi archivia la stringa nella variabile $password.

Il secondo comando crea un oggetto **DateTime** usando il cmdlet **get-date** e quindi archivia tale oggetto nella variabile $Expires.

Il terzo comando crea la variabile $tags per impostare i contrassegni per l'elevata gravità.

Il comando finale importa una chiave come chiave HSM dalla posizione specificata. Il comando specifica la data di scadenza archiviata in $Expires e la password archiviata in $Password e applica i tag archiviati in $tags.

## PARAMETRI

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

### -Destinazione
Specifica se aggiungere la chiave come chiave protetta dal software o con una chiave protetta da HSM nel servizio Key Vault.
I valori validi sono: HSM e software.

Nota: per usare HSM come destinazione, è necessario disporre di un Vault Key che supporti HSM. Per altre informazioni sui livelli di servizio e sulle funzionalità per l'archiviazione delle chiavi di Azure, vedere il [sito Web di Azure Key Vault pricing](https://go.microsoft.com/fwlink/?linkid=512521).

Questo parametro è obbligatorio quando si crea una nuova chiave. Se si importa una chiave usando il parametro *filePath* , questo parametro è facoltativo:

- Se non specifichi questo parametro e questo cmdlet importa una chiave con estensione Byok, questa viene importata come chiave protetta da HSM. Il cmdlet non può importare la chiave come chiave protetta dal software.

- Se non specifichi questo parametro e questo cmdlet importa una chiave con estensione pfx, la chiave viene importata come chiave protetta dal software.

```yaml
Type: System.String
Parameter Sets: Create
Aliases: 
Accepted values: HSM, Software, HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Import
Aliases: 
Accepted values: HSM, Software, HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Disable
Indica che la chiave che si sta aggiungendo è impostata su uno stato iniziale di disabled. Qualsiasi tentativo di usare la chiave non riuscirà. Usare questo parametro se si precaricano le chiavi che si desidera abilitare in seguito.

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

### -Scadenza
Specifica la data di scadenza, come oggetto **DateTime** , per la chiave aggiunta da questo cmdlet. Questo parametro usa l'ora UTC (Coordinated Universal Time). Per ottenere un oggetto **DateTime** , usare il cmdlet **get-date** . Per altre informazioni, digitare `Get-Help Get-Date` . Se non specifichi questo parametro, la chiave non scade.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -KeyFilePassword
Specifica una password per il file importato come oggetto **SecureString** . Per ottenere un oggetto **SecureString** , usa il cmdlet **ConvertTo-SecureString** . Per altre informazioni, digitare `Get-Help ConvertTo-SecureString` . Devi specificare questa password per importare un file con estensione pfx.

```yaml
Type: System.Security.SecureString
Parameter Sets: Import
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FilePath
Specifica il percorso di un file locale che contiene il materiale chiave importato da questo cmdlet.
Le estensioni valide per i nomi di file sono Byok e PFX.

- Se il file è un file con estensione Byok, la chiave viene protetta automaticamente da HSM dopo l'importazione e non è possibile eseguire l'override di questa impostazione predefinita.

- Se il file è un file PFX, la chiave viene automaticamente protetta dal software dopo l'importazione. Per eseguire l'override di questo valore predefinito, imposta il parametro di *destinazione* su HSM in modo che la chiave sia protetta da HSM.

Quando specifichi questo parametro, il parametro di *destinazione* è facoltativo.

```yaml
Type: System.String
Parameter Sets: Import
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyOps
Specifica una matrice di operazioni che è possibile eseguire tramite la chiave aggiunta da questo cmdlet.
Se non specifichi questo parametro, tutte le operazioni possono essere eseguite.

I valori accettabili per questo parametro sono un elenco delimitato da virgole delle operazioni chiave definite dalla [specifica JSON Web Key (JWK)](https://go.microsoft.com/fwlink/?LinkID=613300):

- Crittografare
- Decrittografare
- A capo
- Annullare
- Segno
- Verificare
- Backup
- Ripristinare

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
Specifica il nome della chiave da aggiungere all'archivio della chiave. Questo cmdlet costruisce il nome di dominio completo (FQDN) di una chiave in base al nome specificato da questo parametro, il nome del Vault della chiave e l'ambiente corrente. Il nome deve essere una stringa da 1 a 63 caratteri di lunghezza che contiene solo 0-9, a-z, A-Z e-(il simbolo del trattino).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NotBefore
Specifica il tempo, come oggetto **DateTime** , prima del quale non è possibile usare la chiave. Questo parametro usa l'ora UTC. Per ottenere un oggetto **DateTime** , usare il cmdlet **get-date** . Se non specifichi questo parametro, la chiave può essere usata immediatamente.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Coppie chiave-valore in forma di tabella hash. Per esempio:

@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VAULTNAME
Specifica il nome del Vault chiave a cui questo cmdlet aggiunge la chiave. Questo cmdlet crea l'FQDN di un Vault chiave in base al nome specificato da questo parametro e all'ambiente corrente.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

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

## OUTPUT

### Microsoft. Azure. Commands. Vault. Models. bundle

## Note

## COLLEGAMENTI CORRELATI

[Backup-AzureKeyVaultKey](./Backup-AzureKeyVaultKey.md)

[Get-AzureKeyVaultKey](./Get-AzureKeyVaultKey.md)

[Remove-AzureKeyVaultKey](./Remove-AzureKeyVaultKey.md)

[Set-AzureKeyVaultKeyAttribute](./Set-AzureKeyVaultKeyAttribute.md)
