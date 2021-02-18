---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: 61125ae7d9fa78ec9f121cc9b60610258ad2c67c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405398"
---
# Add-AzKeyVaultKey

## SYNOPSIS
Crea una chiave in un vault delle chiavi o importa una chiave in un vault delle chiavi.

## SINTASSI

### InteractiveCreate (impostazione predefinita)
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InteractiveImport
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmInteractiveCreate
```
Add-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String> [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmInteractiveImport
```
Add-AzKeyVaultKey -HsmName <String> [-Name] <String> -KeyFilePath <String> [-KeyFilePassword <SecureString>]
 [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectCreate
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InputObjectImport
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmInputObjectCreate
```
Add-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String>
 [-CurveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmInputObjectImport
```
Add-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ResourceIdCreate
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ResourceIdImport
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmResourceIdCreate
```
Add-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String>
 [-CurveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HsmResourceIdImport
```
Add-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **Add-AzKeyVaultKey** crea una chiave in un vault delle chiavi nel Vault delle chiavi di Azure oppure importa una chiave in un vault delle chiavi.
Usare questo cmdlet per aggiungere le chiavi usando uno dei metodi seguenti:
- Creare una chiave in un modulo di sicurezza hardware (HSM) nel servizio Vault delle chiavi.
- Creare una chiave nel software nel servizio Vault delle chiavi.
- Importare una chiave dal proprio modulo di sicurezza hardware (HSM) a un sistema HMS nel servizio Vault delle chiavi.
- Importare una chiave da un file PFX nel computer.
- Importare una chiave da un file PFX nel computer nei moduli di sicurezza hardware (HMS) nel servizio Vault delle chiavi.
Per una di queste operazioni, è possibile fornire attributi chiave o accettare le impostazioni predefinite.
Se si crea o si importa una chiave con lo stesso nome di una chiave esistente nel vault delle chiavi, la chiave originale viene aggiornata con i valori specificati per la nuova chiave. È possibile accedere ai valori precedenti usando l'URI specifico della versione per tale versione della chiave. Per informazioni sulle versioni principali e sulla struttura DELL'URI, vedere [Informazioni sulle](http://go.microsoft.com/fwlink/?linkid=518560) chiavi e i segreti nella documentazione dell'API REST del Vault delle chiavi.
Nota: per importare una chiave dal modulo di sicurezza hardware, è necessario generare prima un pacchetto BYOK (un file con estensione byok) usando il set di strumenti BYOK del Vault delle chiavi di Azure. Per altre informazioni, vedere Come generare e trasferire le chiavi [HSM-Protected per il Vault delle chiavi di Azure.](http://go.microsoft.com/fwlink/?LinkId=522252)
Come procedura consigliata, eseguire il backup della chiave dopo che è stata creata o aggiornata, usando il cmdlet Backup-AzKeyVaultKey. Non sono disponibili funzionalità di annullamento dell'eliminazione, quindi se si elimina accidentalmente la chiave o la si elimina e quindi si cambia idea, la chiave non può essere recuperata a meno che non si abbia un backup che è possibile ripristinare.

## ESEMPI

### Esempio 1: Creare una chiave
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITSoftware' -Destination 'Software'

Vault Name     : contoso
Name           : ITSoftware
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

Questo comando crea una chiave protetta dal software denominata ITSoftware nella chiave vault denominata Contoso.

### Esempio 2: Creare una chiave protetta da HSM
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsm' -Destination 'HSM'

Vault Name     : contoso
Name           : ITHsm
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

Questo comando crea una chiave protetta da HSM nella chiave vault denominata Contoso.

### Esempio 3: Creare una chiave con valori non predefiniti
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

Vault Name     : contoso
Name           : ITHsmNonDefault
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITHsmNonDefault/929bfc14db84439b823ffd1bedadaf5f
Enabled        : False
Expires        : 5/21/2020 11:12:43 PM
Not Before     : 5/21/2018 11:12:50 PM
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

Il primo comando archivia i valori decrittografa e verifica nella $KeyOperations variabile.
Il secondo comando crea un **oggetto DateTime,** definito in UTC, usando il cmdlet **Get-Date.**
L'oggetto specifica un periodo di tempo futuro di due anni. Il comando archivia tale data nella $Expires variabile. Per altre informazioni, digitare `Get-Help Get-Date` .
Il terzo comando crea un **oggetto DateTime** usando il cmdlet **Get-Date.** Questo oggetto specifica l'ora UTC corrente. Il comando archivia tale data nella $NotBefore variabile.
Il comando finale crea una chiave denominata ITHsmNonDefault che è una chiave protetta da HSM. Il comando specifica i valori per le operazioni chiave consentite $KeyOperations. Il comando specifica gli orari per i parametri *Expires* e *NotBefore* creati nei comandi precedenti e i tag per un livello di gravità elevato e per l'IT. La nuova chiave viene disabilitata. È possibile abilitarlo usando il cmdlet **Set-AzKeyVaultKey.**

### Esempio 4: Importare una chiave protetta da HSM
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'

Vault Name     : contoso
Name           : ITByok
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITByok/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

Questo comando importa la chiave denominata ITByok dalla posizione specificata dal parametro *KeyFilePath.* La chiave importata è una chiave protetta da HSM.
Per importare una chiave dal proprio modulo di sicurezza hardware, è necessario generare prima un pacchetto BYOK (un file con estensione byok) usando il set di strumenti BYOK del Vault delle chiavi di Azure.
Per altre informazioni, vedere Come generare e trasferire le chiavi [HSM-Protected per il Vault delle chiavi di Azure.](http://go.microsoft.com/fwlink/?LinkId=522252)

### Esempio 5: Importare una chiave protetta da software
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password

Vault Name     : contoso
Name           : ITPfx
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITPfx/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

Il primo comando converte una stringa in una stringa sicura usando il cmdlet **ConvertTo-SecureString** e quindi archivia la stringa nella $Password variabile. Per altre informazioni, digitare `Get-Help
ConvertTo-SecureString` .
Il secondo comando crea una password software nel vault della chiave Contoso. Il comando specifica il percorso della chiave e la password archiviati in $Password.

### Esempio 6: Importare una chiave e assegnare attributi
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = "true" }
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags

Vault Name     : contoso
Name           : ITPfxToHSM
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITPfxToHSM/929bfc14db84439b823ffd1bedadaf5f
Enabled        : True
Expires        : 5/21/2020 11:12:43 PM
Not Before     :
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

Il primo comando converte una stringa in una stringa sicura usando il cmdlet **ConvertTo-SecureString** e quindi archivia la stringa nella $Password variabile.
Il secondo comando crea un **oggetto DateTime** usando il cmdlet **Get-Date** e quindi archivia l'oggetto nella $Expires variabile.
Il terzo comando crea la $tags variabile per impostare tag di gravità elevata e it.
Il comando finale importa una chiave come chiave HSM dalla posizione specificata. Il comando specifica la scadenza archiviata in $Expires e la password archiviati in $Password e applica i tag archiviati in $tags.

### Esempio 7: Generare una chiave di exchange chiave (KEK) per la caratteristica BYOK (Bring Your Own Key)

```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName $vaultName -Name $keyName -Destination HSM -Size 2048 -KeyOps "import"
```

Genera una chiave (denominata chiave di scambio delle chiavi, Key Exchange Key, KEK). La chiave KEK deve essere una chiave RSA-HSM che include solo l'operazione di importazione della chiave. Solo lo SKU di Vault delle chiavi Premium supporta le chiavi RSA-HSM.
Per maggiori dettagli, consulta https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys

## PARAMETERS

### -CurveName
Specifica il nome della curva di crittografia della curva ellit. Questo valore è valido quando KeyType è EC.

```yaml
Type: System.String
Parameter Sets: InteractiveImport, HsmInteractiveCreate, InputObjectImport, HsmInputObjectCreate, ResourceIdImport, HsmResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure

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

### -Destination
Specifica se aggiungere la chiave come chiave protetta dal software o come chiave protetta da HSM nel servizio Vault delle chiavi.
I valori validi sono HSM e Software.
Nota: per usare HSM come destinazione, è necessario avere un vault delle chiavi che supporti gli HMS. Per altre informazioni sui livelli di servizio e sulle funzionalità per il Vault delle chiavi di Azure, vedere il sito [Web prezzi del Vault delle chiavi di Azure.](http://go.microsoft.com/fwlink/?linkid=512521)
Questo parametro è obbligatorio quando si crea una nuova chiave. Se si importa una chiave usando il *parametro KeyFilePath,* questo parametro è facoltativo:
- Se non si specifica questo parametro e questo cmdlet importa una chiave con estensione byok, la importa come chiave protetta da HSM. Il cmdlet non può importare la chiave come chiave protetta da software.
- Se non si specifica questo parametro e questo cmdlet importa una chiave con estensione pfx, la importa come chiave protetta dal software.

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Disable
Indica che la chiave che si sta aggiungendo è impostata sullo stato iniziale Disabilitato. Qualsiasi tentativo di usare la chiave non riuscirà. Usare questo parametro se si precaricano chiavi che si intende abilitare in un secondo momento.

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
Specifica la scadenza, come oggetto **DateTime,** per la chiave aggiunta da questo cmdlet. Questo parametro usa l'ora UTC (Coordinated Universal Time). Per ottenere un **oggetto DateTime,** usare il cmdlet **Get-Date.** Per altre informazioni, digitare `Get-Help Get-Date` . Se non si specifica questo parametro, la chiave non scade.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HsmName
Nome HSM. Il cmdlet crea l'FQDN di un servizio HSM gestito in base al nome e all'ambiente attualmente selezionato.

```yaml
Type: System.String
Parameter Sets: HsmInteractiveCreate, HsmInteractiveImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HsmObject
Oggetto HSM.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: HsmInputObjectCreate, HsmInputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -HsmResourceId
ID risorsa di HSM.

```yaml
Type: System.String
Parameter Sets: HsmResourceIdCreate, HsmResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InputObject
Oggetto Vault.

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -KeyFilePassword
Specifica una password per il file importato come **oggetto SecureString.** Per ottenere un **oggetto SecureString,** usare il cmdlet **ConvertTo-SecureString.** Per altre informazioni, digitare `Get-Help ConvertTo-SecureString` . È necessario specificare questa password per importare un file con estensione pfx.

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, HsmInteractiveImport, InputObjectImport, HsmInputObjectImport, ResourceIdImport, HsmResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyFilePath
Specifica il percorso di un file locale che contiene il materiale chiave importato da questo cmdlet.
Le estensioni di file valide sono byok e pfx.
- Se il file è byok, la chiave viene protetta automaticamente dai messaggi hMS dopo l'importazione e non è possibile ignorare questa impostazione predefinita.
- Se il file è un file PFX, la chiave viene protetta automaticamente dal software dopo l'importazione. Per ignorare questa impostazione predefinita, impostare *il parametro Destination* su HSM in modo che la chiave sia protetta da HSM.
Quando si specifica questo parametro, *il parametro Destination* è facoltativo.

```yaml
Type: System.String
Parameter Sets: InteractiveImport, HsmInteractiveImport, InputObjectImport, HsmInputObjectImport, ResourceIdImport, HsmResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyOps
Specifica una matrice di operazioni che possono essere eseguite usando la chiave aggiunta da questo cmdlet.
Se non si specifica questo parametro, è possibile eseguire tutte le operazioni.
I valori accettabili per questo parametro sono un elenco di operazioni chiave separate da virgole, come definito dalla specifica della chiave [Web JSON (JWK):](http://go.microsoft.com/fwlink/?LinkID=613300)
- crittografare
- decrittografare
- wrapKey
- unwrapKey
- segno
- verifica
- importare (solo per KEK, vedere l'esempio 7)

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyType
Specifica il tipo di chiave. Quando si importano le chiavi BYOK, per impostazione predefinita viene visualizzato "RSA".

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: HsmInteractiveCreate, HsmInputObjectCreate, HsmResourceIdCreate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifica il nome della chiave da aggiungere al vault delle chiavi. Questo cmdlet crea il nome di dominio completo (FQDN) di una chiave in base al nome specificato da questo parametro, al nome del vault delle chiavi e all'ambiente corrente. La lunghezza del nome deve essere di un massimo di 1 e 63 caratteri, contenente solo i caratteri 0-9, a-z, A-Z e - (il trattino).

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
Specifica l'ora, come oggetto **DateTime,** prima della quale non è possibile usare il tasto. Questo parametro usa utc. Per ottenere un **oggetto DateTime,** usare il cmdlet **Get-Date.** Se non si specifica questo parametro, la chiave può essere usata immediatamente.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
ID risorsa Vault.

```yaml
Type: System.String
Parameter Sets: ResourceIdCreate, ResourceIdImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Size
Dimensioni della chiave RSA, in bit. Se non è specificato, il servizio fornirà un valore predefinito sicuro.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, HsmInteractiveCreate, InputObjectCreate, HsmInputObjectCreate, ResourceIdCreate, HsmResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Coppie chiave-valore sotto forma di tabella hash. Ad esempio: @{key0="value0";key1=$null;key2="value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
Specifica il nome del vault della chiave a cui il cmdlet aggiunge la chiave. Questo cmdlet crea l'FQDN di un vault delle chiavi in base al nome specificato da questo parametro e all'ambiente corrente.

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InteractiveImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Chiede conferma prima di eseguire il cmdlet.

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
Mostra cosa accadrebbe se il cmdlet viene eseguito.
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

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault

### System.String

## OUTPUT

### Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey

## NOTE

## COLLEGAMENTI CORRELATI

[Backup-AzKeyVaultKey](./Backup-AzKeyVaultKey.md)

[Get-AzKeyVaultKey](./Get-AzKeyVaultKey.md)

[Remove-AzKeyVaultKey](./Remove-AzKeyVaultKey.md)

