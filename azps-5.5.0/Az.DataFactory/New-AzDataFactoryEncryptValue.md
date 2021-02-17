---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5BF24BC2-DEB6-4830-BDEA-841BAB070388
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactoryencryptvalue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryEncryptValue.md
ms.openlocfilehash: 0e69cfe7ae76be1d79bdd8cf0d7db193a05219d5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196590"
---
# New-AzDataFactoryEncryptValue

## SYNOPSIS
Crittografa i dati sensibili.

## SINTASSI

### ByFactoryName (Default)
```
New-AzDataFactoryEncryptValue [-DataFactoryName] <String> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByFactoryObject
```
New-AzDataFactoryEncryptValue [-DataFactory] <PSDataFactory> [[-Value] <SecureString>] [-GatewayName] <String>
 [[-Credential] <PSCredential>] [[-Type] <String>] [[-NonCredentialValue] <String>]
 [[-AuthenticationType] <String>] [[-Server] <String>] [[-Database] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet **New-AzDataFactoryEncryptValue** crittografa i dati riservati, ad esempio una password o una stringa di connessione Microsoft SQL Server e restituisce un valore crittografato.

## ESEMPI

### Esempio 1: Crittografare una stringa di connessione non ODBC
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;user id =user123;password=password123' -AsPlainText -Force 
PS C:\> New-AzDataFactoryEncryptValue -GatewayName "WikiGateway" -DataFactoryName "WikiAdf" -Value $value -ResourceGroupName "ADF" -Type OnPremisesSqlLinkedService
```

Il primo comando usa il cmdlet ConvertTo-SecureString per convertire la stringa di connessione specificata in un oggetto **SecureString** e quindi archivia l'oggetto nella $Value variabile.
Per altre informazioni, digitare `Get-Help ConvertTo-SecureString` .
Valori consentiti: SQL Server di connessione Oracle o una stringa di connessione Oracle.
Il secondo comando crea un valore crittografato per l'oggetto archiviato in $Value per il data factory, il gateway, il gruppo di risorse e il tipo di servizio collegato specificato.

### Esempio 2: Crittografare una stringa di connessione non ODBC che usa l'autenticazione di Windows.
```
PS C:\>$Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesSqlLinkedService $Value = ConvertTo-SecureString 'Data Source=ContosoServer;Initial Catalog=catalog;Integrated Security=True' -AsPlainText -Force
```

Il primo comando usa **ConvertTo-SecureString** per convertire la stringa di connessione specificata in un oggetto stringa sicura, quindi archivia l'oggetto nella $Value variabile.
Il secondo comando usa il cmdlet Get-Credential per raccogliere l'autenticazione di Windows (nome utente e password) e quindi archivia l'oggetto **PSCredential** nella variabile $Credential locale.
Per altre informazioni, digitare `Get-Help Get-Credential` .
Il terzo comando crea un valore crittografato per l'oggetto archiviato in $Value e $Credential per il data factory, il gateway, il gruppo di risorse e il tipo di servizio collegato specificato.

### Esempio 3: Crittografare il nome del server e le credenziali per il servizio collegato File system
```
PS C:\>$Value = ConvertTo-SecureString '\\servername' -AsPlainText -Force
PS C:\> $Credential = Get-Credential
PS C:\> New-AzDataFactoryEncryptValue -DataFactoryName "WikiADF" -GatewayName "WikiGateway" -ResourceGroupName "ADF" -Value $Value -Credential $Credential -Type OnPremisesFileSystemLinkedService
```

Il primo comando usa **ConvertTo-SecureString** per convertire la stringa specificata in una stringa sicura, quindi archivia l'oggetto nella $Value variabile.
Il secondo comando usa **Get-Credential** per raccogliere l'autenticazione di Windows (nome utente e password), quindi archivia l'oggetto **PSCredential** nella $Credential variabile.
Il terzo comando crea un valore crittografato per l'oggetto archiviato in $Value e $Credential per il data factory, il gateway, il gruppo di risorse e il tipo di servizio collegato specificato.

### Esempio 4: Crittografare le credenziali per il servizio collegato HDFS
```
PS C:\>$UserName = ConvertTo-SecureString "domain\\username" -AsPlainText -Force
$Password = ConvertTo-SecureString "password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ($UserName, $Password)
New-AzDataFactoryEncryptValue -DataFactoryName "MyDataFactory" -ResourceGroupName "MyResourceGroup" -GatewayName "MyDataManagementGateway" -Type HdfsLinkedService -AuthenticationType Windows -Credential $Credential -NonCredentialValue "http://server01.com:50070/webhdfs/v1/user/username"
```

Il **comando ConvertTo-SecureString** converte la stringa specificata in una stringa sicura.
Il **comando Nuovo oggetto crea** un oggetto PSCredential usando le stringhe di nome utente e password sicure.
È invece possibile usare il comando **Get-Credential** per raccogliere l'autenticazione di Windows (nome utente e password) e quindi archiviare l'oggetto **PSCredential** restituito nella variabile $credential, come illustrato negli esempi precedenti.
Il **comando New-AzDataFactoryEncryptValue** crea un valore crittografato per l'oggetto archiviato in $Credential per il data factory, il gateway, il gruppo di risorse e il tipo di servizio collegato specificato.

### Esempio 5: Crittografare le credenziali per il servizio collegato ODBC
```
PS C:\>$Content = ConvertTo-SecureString "UID=username@contoso;PWD=password;" -AsPlainText -Force
New-AzDataFactoryEncryptValue -ResourceGroupName $RGName -DataFactoryName $DFName -GatewayName $Gateway -Type OnPremisesOdbcLinkedService -AuthenticationType Basic -NonCredentialValue "Driver={SQL Server};Server=server01.database.contoso.net; Database=HDISScenarioTest;" -Value $content
```

Il **comando ConvertTo-SecureString** converte la stringa specificata in una stringa sicura.
Il **comando New-AzDataFactoryEncryptValue** crea un valore crittografato per l'oggetto archiviato in $Value per il data factory, il gateway, il gruppo di risorse e il tipo di servizio collegato specificato.

## PARAMETERS

### -AuthenticationType
Specifica il tipo di autenticazione da usare per connettersi all'origine dati.
I valori accettabili per questo parametro sono:
- Windows
- Di base
- Anonimo.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Basic, Anonymous

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
Specifica le credenziali di autenticazione di Windows (nome utente e password) da usare.
Questo cmdlet crittografa i dati delle credenziali specificati qui.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Database
Specifica il nome del database del servizio collegato.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataFactory
Specifica un **oggetto PSDataFactory.**
Questo cmdlet crittografa i dati del data factory specificati da questo parametro.

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataFactoryName
Specifica il nome di un data factory.
Questo cmdlet crittografa i dati del data factory specificati da questo parametro.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -GatewayName
Specifica il nome del gateway.
Questo cmdlet crittografa i dati per il gateway specificato da questo parametro.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NonCredentialValue
Specifica la parte non credenziali della stringa di connessione ODBC (Open Database Connectivity).
Questo parametro è valido solo per il servizio collegato ODBC.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Specifica il nome di un gruppo di risorse di Azure.
Questo cmdlet crittografa i dati per il gruppo specificato da questo parametro.

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Server
Specifica il nome del server del servizio collegato.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
Specifica il tipo di servizio collegato.
Questo cmdlet crittografa i dati per il tipo di servizio collegato specificato da questo parametro.
I valori accettabili per questo parametro sono:
- OnPremisesSqlLinkedService 
- OnPremisesFileSystemLinkedService 
- OnPremisesOracleLinkedService 
- OnPremisesOdbcLinkedService 
- OnPremisesPostgreSqlLinkedService 
- OnPremisesTeradataLinkedService 
- OnPremisesMySQLLinkedService 
- OnPremisesDB2LinkedService 
- OnPremisesSybaseLinkedService

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OnPremisesSqlLinkedService, OnPremisesFileSystemLinkedService, OnPremisesOracleLinkedService, OnPremisesOdbcLinkedService, OnPremisesPostgreSqlLinkedService, OnPremisesTeradataLinkedService, OnPremisesMySQLLinkedService, OnPremisesDB2LinkedService, OnPremisesSybaseLinkedService, HdfsLinkedService

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Value
Specifica il valore da crittografare.
Per un servizio collegato SQL Server locale e un servizio collegato Oracle locale, usare una stringa di connessione.
Per un servizio collegato ODBC locale, usare la parte delle credenziali della stringa di connessione.
Per il servizio collegato del file system locale, se il file system è locale al computer gateway, usare Local o localhost e, se il file system si trova in un server diverso dal computer gateway, usare \\ \\ servername.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## INPUT

### Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory

### System.String

## OUTPUT

### System.String

## NOTE
* Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori

## COLLEGAMENTI CORRELATI

[New-AzDataFactoryEncryptValue](./New-AzDataFactoryEncryptValue.md)


