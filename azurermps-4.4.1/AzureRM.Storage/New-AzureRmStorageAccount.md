---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: A3DA1205-B8FB-4B4C-9C40-AD303D038EDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/New-AzureRmStorageAccount.md
ms.openlocfilehash: 50384630658f7626ee02ca1dee223e82bf122ef1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688486"
---
# New-AzureRmStorageAccount

## Sinossi
Crea un account di archiviazione.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
New-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Location] <String> [[-Kind] <String>] [[-AccessTier] <String>] [[-CustomDomainName] <String>]
 [[-UseSubDomain] <Boolean>] [[-EnableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureRmStorageAccount** crea un account di archiviazione di Azure.

## ESEMPI

### Esempio 1: creare un account di archiviazione
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "US West" -SkuName "Standard_GRS"
```

Questo comando crea un account di archiviazione per il nome del gruppo di risorse MyResourceGroup.

### Esempio 2: creare un account di archiviazione BLOB che usa la crittografia del servizio di archiviazione
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "US West" -SkuName "Standard_GRS" -EnableEncryptionService Blob -Kind "BlobStorage" -AccessTier Hot
```

Questo comando crea un account di archiviazione BLOB che usa il tipo di accesso caldo.
L'account ha abilitato la crittografia del servizio di archiviazione nel servizio BLOB.

### Esempio 3: creare un account di archiviazione che consente la crittografia del servizio di archiviazione su BLOB e servizi file e generare e assegnare un'identità per il Vault di Azure.
```
PS C:\>New-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Location "US West" -SkuName "Standard_GRS" -EnableEncryptionService "Blob,File" -AssignIdentity
```

Questo comando crea un account di archiviazione che ha abilitato la crittografia del servizio di archiviazione su BLOB e servizi file.  Viene inoltre generata e assegnata un'identità che può essere usata per gestire le chiavi dell'account tramite Azure Key Vault.

## PARAMETRI

### -AccessTier
Specifica il livello di accesso dell'account di archiviazione creato da questo cmdlet.
I valori accettabili per questo parametro sono: caldo e freddo.

Se specifichi un valore di BlobStorage per il parametro *Kind* , devi specificare un valore per il parametro *AccessTier* .

Se specifichi un valore di spazio di archiviazione per questo parametro di *tipo* , non specificare il parametro *AccessTier* .

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AssignIdentity
Genera e assegna una nuova identità dell'account di archiviazione per l'account di archiviazione per l'uso con i servizi di gestione delle chiavi, ad esempio Azure Key Vault.

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
Il valore predefinito è lo spazio di archiviazione.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableEncryptionService
Indica se questo cmdlet Abilita la crittografia del servizio di archiviazione nel servizio di archiviazione.
Sono supportati i servizi file Azure BLOB e Azure.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Storage.StorageAccountBaseCmdlet+EncryptionSupportServiceEnum]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableHttpsTrafficOnly
Indica se l'account di archiviazione consente o meno solo il traffico HTTPS.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InformationAction
Specifica il modo in cui questo cmdlet risponde a un evento informativo.

I valori accettabili per questo parametro sono i seguenti:

- Continuare
- Ignora
- Informarsi
- SilentlyContinue
- Stop
- Sospensione

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Specifica una variabile di informazioni.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tipo
Specifica il tipo di account di archiviazione creato da questo cmdlet.
I valori accettabili per questo parametro sono i seguenti:

- Archiviazione.
Account di archiviazione di uso generale che supporta l'archiviazione di BLOB, tabelle, code, file e dischi.
 
- BlobStorage.
Account di archiviazione BLOB che supporta l'archiviazione solo di BLOB.
 

Il valore predefinito è lo spazio di archiviazione.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Posizione
Specifica la posizione dell'account di archiviazione da creare.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nome
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
NetworkRuleSet account di archiviazione

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

### -SkuName
Specifica il nome SKU dell'account di archiviazione creato da questo cmdlet.
I valori accettabili per questo parametro sono i seguenti:

- Standard_LRS.
Spazio di archiviazione locale ridondante. 
- Standard_ZRS.
Area-archiviazione ridondante.
- Standard_GRS.
Spazio di archiviazione Geo-ridondante. 
- Standard_RAGRS.
Accesso in lettura archiviazione Geo-ridondante. 
- Premium_LRS.
Spazio di archiviazione locale ridondante Premium.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Se specifichi un valore di BlobStorage per il parametro *Kind* , devi specificare un valore per il parametro *AccessTier* .

Se specifichi un valore di spazio di archiviazione per questo parametro di *tipo* , non specificare il parametro *AccessTier* .

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseSubDomain
Indica se abilitare la convalida CName indiretta.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
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

## Note

## COLLEGAMENTI CORRELATI

[Get-AzureRmStorageAccount](./Get-AzureRmStorageAccount.md)

[Remove-AzureRmStorageAccount](./Remove-AzureRmStorageAccount.md)

[Set-AzureRmStorageAccount](./Set-AzureRmStorageAccount.md)


