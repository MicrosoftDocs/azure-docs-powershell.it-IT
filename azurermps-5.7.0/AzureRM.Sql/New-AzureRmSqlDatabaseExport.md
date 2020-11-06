---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabaseexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseExport.md
ms.openlocfilehash: 324686ace908235e3b48fb150249d2bad22c169b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507855"
---
# New-AzureRmSqlDatabaseExport

## Sinossi
Esporta un database SQL di Azure come file con estensione bacpac in un account di archiviazione.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SINTASSI

```
New-AzureRmSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Descrizione
Il cmdlet **New-AzureRmSqlDatabaseExport** esporta un database SQL di Azure come file con estensione bacpac in un account di archiviazione.
Per recuperare le informazioni sullo stato della richiesta, è possibile che venga inviata la richiesta di stato del database di esportazione.

Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.

## ESEMPI

### Esempio 1: creare una richiesta di esportazione per un database
```
PS C:\>New-AzureRmSqlDatabaseExport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword "secure password"
ResourceGroupName          : RG01
ServerName                 : Server01
DatabaseName               : Database01
StorageKeyType             : StorageAccessKey
StorageKey                 : 
StorageUri                 : http://account01.blob.core.contoso.net/bacpacs/database01.bacpac
AdministratorLogin         : User
AdministratorLoginPassword : 
AuthenticationType         : None
OperationStatusLink        : https://management.azure.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-00
                             0-0000-0000-000000000000?api-version=2014-04-01
Status                     : InProgress
ErrorMessage               :
```

Questo comando crea una richiesta di esportazione per il database specificato.

## PARAMETRI

### -AdministratorLogin
Specifica il nome dell'amministratore di SQL.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AdministratorLoginPassword
Specifica la password dell'amministratore di SQL.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AuthenticationType
Specifica il tipo di autenticazione usato per accedere al server.
Il valore predefinito è SQL se non è impostato alcun tipo di autenticazione.

I valori accettabili per questo parametro sono i seguenti:

- SQL.
Autenticazione SQL.
Imposta *AdministratorLogin* e *AdministratorLoginPassword* sul nome utente e la password di amministratore SQL. 
- ADPassword.
Autenticazione di Azure Active Directory.
Imposta *AdministratorLogin* e *AdministratorLoginPassword* sul nome utente e la password dell'amministratore di Azure ad.

Questo parametro è disponibile solo nei server SQL database V12.

```yaml
Type: AuthenticationType
Parameter Sets: (All)
Aliases:
Accepted values: None, Sql, AdPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseName
Specifica il nome del database SQL.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

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

### -ResourceGroupName
Specifica il nome del gruppo di risorse per il server di database SQL.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nomeserver
Specifica il nome del server di database SQL.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageKey
Specifica il tasto di scelta per l'account di archiviazione.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageKeyType
Specifica il tipo di chiave di accesso per l'account di archiviazione.

I valori accettabili per questo parametro sono i seguenti:

- StorageAccessKey.
Questo valore usa una chiave dell'account di archiviazione. 
- SharedAccessKey.
Questo valore usa una chiave SAS (Shared Access Signature).

```yaml
Type: StorageKeyType
Parameter Sets: (All)
Aliases:
Accepted values: StorageAccessKey, SharedAccessKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageUri
Specifica il collegamento BLOB, come URL, al file BACPAC.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confermare
Richiede la conferma prima di eseguire il cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra cosa succede se il cmdlet viene eseguito.
Il cmdlet non viene eseguito.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable. Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## INGRESSI

### Nessuno
Questo cmdlet non accetta alcun input.

## OUTPUT

### Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseImportExportBaseModel

## Note
* Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, database, MSSQL

## COLLEGAMENTI CORRELATI

[Get-AzureRmSqlDatabaseImportExportStatus](./Get-AzureRmSqlDatabaseImportExportStatus.md)

[New-AzureRmSqlDatabaseImport](./New-AzureRmSqlDatabaseImport.md)

[Documentazione di database SQL](https://docs.microsoft.com/azure/sql-database/)
