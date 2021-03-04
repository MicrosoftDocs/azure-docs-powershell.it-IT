---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccount.md
ms.openlocfilehash: 0a5ccfaec396f4dc79c877da38112a5bfa575e09
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993200"
---
# New-AzStorageAccount

## SYNOPSIS
Crea un account di archiviazione.

## SINTASSI

### AzureActiveDirectoryDomainServicesForFile (impostazione predefinita)
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableAzureActiveDirectoryDomainServicesForFile <Boolean>]
 [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>] [-PublishInternetEndpoint <Boolean>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AllowSharedKeyAccess <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

### ActiveDirectoryDomainServicesForFile
```
New-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Location] <String>
 [-Kind <String>] [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>]
 [-Tag <Hashtable>] [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-EnableHierarchicalNamespace <Boolean>] [-EnableLargeFileShare] [-PublishMicrosoftEndpoint <Boolean>]
 [-PublishInternetEndpoint <Boolean>] [-EnableActiveDirectoryDomainServicesForFile <Boolean>]
 [-ActiveDirectoryDomainName <String>] [-ActiveDirectoryNetBiosDomainName <String>]
 [-ActiveDirectoryForestName <String>] [-ActiveDirectoryDomainGuid <String>]
 [-ActiveDirectoryDomainSid <String>] [-ActiveDirectoryAzureStorageSid <String>] [-AsJob]
 [-EncryptionKeyTypeForTable <String>] [-EncryptionKeyTypeForQueue <String>] [-RequireInfrastructureEncryption]
 [-AllowBlobPublicAccess <Boolean>] [-MinimumTlsVersion <String>] [-AllowSharedKeyAccess <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-RoutingChoice <String>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **New-AzStorageAccount** crea un account di archiviazione di Azure.

## ESEMPI

### Esempio 1: Creare un account di archiviazione
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS
```

Questo comando crea un account di archiviazione per il gruppo di risorse denominato MyResourceGroup.

### Esempio 2: Creare un account di archiviazione BLOB con BlobStorage Kind e AccessTier a scelta rapida
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind BlobStorage -AccessTier Hot
```

Questo comando crea un account di Archiviazione BLOB con BlobStorage Kind e AccessTier a scelta rapida

### Esempio 3: Creare un account di archiviazione con Kind StorageV2 e generare e assegnare un'identità per Azure KeyVault.
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -SkuName Standard_GRS -Kind StorageV2 -AssignIdentity
```

Questo comando crea un account di archiviazione con Kind StorageV2.  Genera e assegna anche un'identità che può essere usata per gestire le chiavi dell'account tramite Azure KeyVault.

### Esempio 4: Creare un account di archiviazione con NetworkRuleSet da JSON
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName MyResourceGroup -AccountName mystorageaccount -Location westus -Type Standard_LRS -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="Deny"})
```

Questo comando crea un account di archiviazione con la proprietà NetworkRuleSet da JSON

### Esempio 5: Creare un account di archiviazione con spazio dei nomi gerarchico abilitato.
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "US West" -SkuName "Standard_GRS" -Kind StorageV2  -EnableHierarchicalNamespace $true
```

Questo comando crea un account di archiviazione con Spazio dei nomi gerarchico abilitato.

### Esempio 6: Creare un account di archiviazione con l'autenticazione AAD DS dei file di Azure e abilitare una condivisione file di grandi dimensioni.
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableAzureActiveDirectoryDomainServicesForFile $true -EnableLargeFileShare
```

Questo comando crea un account di archiviazione con l'autenticazione DS AAD dei file di Azure e abilita una condivisione file di grandi dimensioni.

### Esempio 7: Creare un account di archiviazione con abilitare l'autenticazione di File Active Directory Domain Service.
```
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EnableActiveDirectoryDomainServicesForFile $true `
        -ActiveDirectoryDomainName "mydomain.com" `
        -ActiveDirectoryNetBiosDomainName "mydomain.com" `
        -ActiveDirectoryForestName "mydomain.com" `
        -ActiveDirectoryDomainGuid "12345678-1234-1234-1234-123456789012" `
        -ActiveDirectoryDomainSid "S-1-5-21-1234567890-1234567890-1234567890" `
        -ActiveDirectoryAzureStorageSid "S-1-5-21-1234567890-1234567890-1234567890-1234"
```

Questo comando crea un account di archiviazione con l'autenticazione di Servizi di dominio Active Directory per File.

### Esempio 8: Creare un account di archiviazione con i servizi di coda e tabella con chiave di crittografia con ambito account e Richiedere la crittografia dell'infrastruttura.
```powershell
PS C:\>New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2  -EncryptionKeyTypeForTable Account -EncryptionKeyTypeForQueue Account -RequireInfrastructureEncryption

PS C:\>$account = get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName

PS C:\>$account.Encryption.Services.Queue

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\>$account.Encryption.Services.Table

Enabled LastEnabledTime     KeyType
------- ---------------     -------
   True 1/9/2020 6:09:11 AM Account

PS C:\> $account.Encryption.RequireInfrastructureEncryption
True
```

Questo comando crea un account di archiviazione con Coda e Servizio tabelle con chiave di crittografia con ambito account e Richiedi crittografia infrastruttura, quindi Coda e Tabella useranno la stessa chiave di crittografia con il servizio BLOB e file e il servizio applicherà un livello secondario di crittografia con chiavi gestite della piattaforma per i dati in archivio.
Ottenere quindi le proprietà dell'account di archiviazione e visualizzare il tipo di chiave di crittografia di Servizio coda e tabella e il valore RequireInfrastructureEncryption.

### Esempio 9: Creare un account MinimumTlsVersion e AllowBlobPublicAccess e disabilitare l'accesso SharedKey
```
PS C:\> $account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -Kind StorageV2 -MinimumTlsVersion TLS1_1 -AllowBlobPublicAccess $false -AllowSharedKeyAccess $false

PS C:\> $account.MinimumTlsVersion
TLS1_1

PS C:\> $account.AllowBlobPublicAccess
False

PS C:\> $a.AllowSharedKeyAccess
False
```

Il comando crea account con MinimumTlsVersion, AllowBlobPublicAccess e disabilita l'accesso SharedKey all'account, quindi mostra le 3 proprietà dell'account creato 

### Esempio 10: Creare un account di archiviazione con l'impostazione RoutingPreference
```powershell
PS C:\>$account = New-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Location "eastus2euap" -SkuName "Standard_LRS" -PublishMicrosoftEndpoint $true -PublishInternetEndpoint $true -RoutingChoice MicrosoftRouting

PS C:\>$account.RoutingPreference

RoutingChoice    PublishMicrosoftEndpoints PublishInternetEndpoints
-------------    ------------------------- ------------------------
MicrosoftRouting                     True                     True

PS C:\>$account.PrimaryEndpoints

Blob               : https://mystorageaccount.blob.core.windows.net/
Queue              : https://mystorageaccount.queue.core.windows.net/
Table              : https://mystorageaccount.table.core.windows.net/
File               : https://mystorageaccount.file.core.windows.net/
Web                : https://mystorageaccount.z2.web.core.windows.net/
Dfs                : https://mystorageaccount.dfs.core.windows.net/
MicrosoftEndpoints : {"Blob":"https://mystorageaccount-microsoftrouting.blob.core.windows.net/","Queue":"https://mystorageaccount-microsoftrouting.queue.core.windows.net/","Table":"https://mystorageaccount-microsoftrouting.table.core.windows.net/","File":"ht
                     tps://mystorageaccount-microsoftrouting.file.core.windows.net/","Web":"https://mystorageaccount-microsoftrouting.z2.web.core.windows.net/","Dfs":"https://mystorageaccount-microsoftrouting.dfs.core.windows.net/"}
InternetEndpoints  : {"Blob":"https://mystorageaccount-internetrouting.blob.core.windows.net/","File":"https://mystorageaccount-internetrouting.file.core.windows.net/","Web":"https://mystorageaccount-internetrouting.z2.web.core.windows.net/","Dfs":"https://w
                     eirp3-internetrouting.dfs.core.windows.net/"}
```

Questo comando crea un account di archiviazione con l'impostazione RoutingPreference: PublishMicrosoftEndpoint e PublishInternetEndpoint come true e RoutingChoice come MicrosoftRouting.

## PARAMETERS

### -AccessTier
Specifica il livello di accesso dell'account di archiviazione creato da questo cmdlet.
I valori accettabili per questo parametro sono: Hot e Cool.
Se si specifica un valore di BlobStorage per il *parametro Kind,* è necessario specificare un valore per il *parametro AccessTier.* Se si specifica un valore di Archiviazione per il parametro *kind,* non specificare il *parametro AccessTier.*

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryAzureStorageSid
Specifica l'identificatore di sicurezza (SID) per Archiviazione di Azure. Questo parametro deve essere impostato quando -EnableActiveDirectoryDomainServicesForFile è impostato su true.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryDomainGuid
Specifica il GUID del dominio. Questo parametro deve essere impostato quando -EnableActiveDirectoryDomainServicesForFile è impostato su true.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryDomainName
Specifica il dominio primario per cui è autorevole il server DNS di Active Directory. Questo parametro deve essere impostato quando -EnableActiveDirectoryDomainServicesForFile è impostato su true.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryDomainSid
Specifica l'identificatore di sicurezza (SID). Questo parametro deve essere impostato quando -EnableActiveDirectoryDomainServicesForFile è impostato su true.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryForestName
Specifica la foresta di Active Directory da recuperare. Questo parametro deve essere impostato quando -EnableActiveDirectoryDomainServicesForFile è impostato su true.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryNetDomainName
Specifica il nome di dominio Net PIÙ.ER. Questo parametro deve essere impostato quando -EnableActiveDirectoryDomainServicesForFile è impostato su true.

```yaml
Type: System.String
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowBlobPublicAccess
Consentire l'accesso pubblico a tutti i BLOB o contenitori nell'account di archiviazione. L'interpretazione predefinita è vera per questa proprietà.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowSharedKeyAccess
Indica se l'account di archiviazione consente di autorizzare le richieste con la chiave di accesso dell'account tramite chiave condivisa. Se false, tutte le richieste, incluse le firme di accesso condiviso, devono essere autorizzate con Azure Active Directory (Azure AD). Il valore predefinito è Null, che equivale a true.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
Eseguire il cmdlet in background

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

### -AssignIdentity
Generare e assegnare una nuova identità dell'account di archiviazione per questo account di archiviazione da usare con servizi di gestione delle chiavi come Azure KeyVault.

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

### -CustomDomainName
Specifica il nome del dominio personalizzato dell'account di archiviazione.
Il valore predefinito è Archiviazione.

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

### -EnableActiveDirectoryDomainServicesForFile
Abilitare l'autenticazione di Active Directory Domain Service per i file di Azure per l'account di archiviazione.

```yaml
Type: System.Boolean
Parameter Sets: ActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAzureActiveDirectoryDomainServicesForFile
Abilitare l'autenticazione di Azure Active Directory Domain Service per i file di Azure per l'account di archiviazione.

```yaml
Type: System.Boolean
Parameter Sets: AzureActiveDirectoryDomainServicesForFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableHierarchicalZone
Indica se l'account di archiviazione abilita o meno lo spazio dei nomi gerarchico.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableHttpsTrafficOnly
Indica se l'account di archiviazione abilita o meno solo il traffico HTTPS.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableLargeFileShare
Indica se l'account di archiviazione può supportare condivisioni file di grandi dimensioni con una capacità superiore a 5 TB. Una volta abilitato l'account, la funzionalità non può essere disabilitata. Attualmente supportato solo per i tipi di replica LRS e ZRS, pertanto non sarebbe possibile eseguire la conversione degli account in account geo-ridondanti. Scopri di più in https://go.microsoft.com/fwlink/?linkid=2086047

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

### -EncryptionKeyTypeForQueue
Impostare il tipo di chiave di crittografia per la coda. Il valore predefinito è Servizio.
-Account: la coda verrà crittografata con una chiave di crittografia con ambito account. -Service: La coda sarà sempre crittografata con Service-Managed chiavi. 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionKeyTypeForTable
Impostare Il tipo di chiave di crittografia per la tabella. Il valore predefinito è Servizio.
- Account: la tabella verrà crittografata con una chiave di crittografia con ambito account. 
- Servizio: la tabella sarà sempre crittografata con Service-Managed chiavi. 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Service, Account

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kind
Specifica il tipo di account di archiviazione creato da questo cmdlet.
I valori accettabili per questo parametro sono:
- Spazio di archiviazione. Account di archiviazione generico che supporta l'archiviazione di BLOB, tabelle, code, file e dischi.
- StorageV2. Account di archiviazione generico versione 2 (GPv2) che supporta BLOB, tabelle, code, file e dischi, con caratteristiche avanzate come il livelli dei dati.
- BlobStorage. Account di Archiviazione BLOB che supporta solo l'archiviazione di BLOB.
- BlockBlobStorage. Bloccare l'account di Archiviazione BLOB che supporta solo l'archiviazione di BLOB di blocco.
- FileStorage. Account di archiviazione file che supporta solo l'archiviazione di file.
Il valore predefinito è StorageV2.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Storage, StorageV2, BlobStorage, BlockBlobStorage, FileStorage

Required: False
Position: Named
Default value: StorageV2
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
Specifica la posizione dell'account di archiviazione da creare.

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

### -MinimumTlsVersion
La versione minima di TLS da poter usare per le richieste di archiviazione. L'interpretazione predefinita è TLS 1.0 per questa proprietà.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TLS1_0, TLS1_1, TLS1_2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifica il nome dell'account di archiviazione da creare.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NetworkRuleSet
NetworkRuleSet viene usato per definire un set di regole di configurazione per firewall e reti virtuali, nonché per impostare i valori per le proprietà di rete, ad esempio i servizi autorizzati a ignorare le regole e come gestire le richieste che non corrispondono a nessuna delle regole definite.

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublishInternetEndpoint
Indica se gli endpoint di archiviazione del routing Internet devono essere pubblicati

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublishMicrosoftEndpoint
Indica se gli endpoint di archiviazione del routing Microsoft devono essere pubblicati

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequireInfrastructureEncryption
Il servizio applicherà un livello secondario di crittografia con chiavi gestite della piattaforma per i dati in archivio.

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

### -ResourceGroupName
Specifica il nome del gruppo di risorse in cui aggiungere l'account di archiviazione.

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

### -RoutingChoice
Routing Choice definisce il tipo di routing di rete scelto dall'utente. I valori possibili includono: 'MicrosoftRouting', 'InternetRouting'

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MicrosoftRouting, InternetRouting

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SKUName
Specifica il nome SKU dell'account di archiviazione creato dal cmdlet.
I valori accettabili per questo parametro sono:
- Standard_LRS. Archiviazione ridondante in locale.
- Standard_ZRS. Spazio di archiviazione ridondante.
- Standard_GRS. Archiviazione geo-ridondante.
- Standard_RAGRS. Archiviazione geo-ridondante di accesso in lettura.
- Premium_LRS. Spazio di archiviazione premium ridondante in locale.
- Premium_ZRS. Spazio di archiviazione premium con ridondanza in zona.
- Standard_GZRS: archiviazione con ridondanza geografica e con ridondanza d'area.
- Standard_RAGZRS - Accesso in lettura con accesso geo-ridondante e archiviazione ridondante.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS, Premium_ZRS, Standard_GZRS, Standard_RAGZRS

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Coppie chiave-valore sotto forma di tabella hash impostata come tag nel server. Ad esempio: @{key0="value0";key1=$null;key2="value2"}

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

### -UseSubDomain
Indica se abilitare la convalida indiretta di CName.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### System.String

## OUTPUT

### Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount

## NOTE

## COLLEGAMENTI CORRELATI

[Get-AzStorageAccount](./Get-AzStorageAccount.md)

[Remove-AzStorageAccount](./Remove-AzStorageAccount.md)

[Set-AzStorageAccount](./Set-AzStorageAccount.md)
