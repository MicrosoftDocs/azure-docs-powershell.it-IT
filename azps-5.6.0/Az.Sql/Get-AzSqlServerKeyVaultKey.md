---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 523192b1632bf6ed67dff170b2ac94374c443299
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997301"
---
# Get-AzSqlServerKeyVaultKey

## SYNOPSIS
Ottiene le chiavi SQL Vault delle chiavi del server.

## SINTASSI

```
Get-AzSqlServerKeyVaultKey [[-KeyId] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIZIONE
Il cmdlet Get-AzSqlServerKeyVaultKey cmdlet ottiene informazioni sulle chiavi del Vault delle chiavi in un SQL server.
È possibile visualizzare tutte le chiavi in un server o una chiave specifica fornendo il valore di KeyId.

## ESEMPI

### Esempio 1: Ottenere tutte le chiavi del Vault chiave
```
PS C:\> Get-AzSqlServerKeyVaultKey -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

Questo comando recupera tutte le chiavi del Vault delle chiavi in un SQL server.
ResourceGroupName : ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey_01234567890123456789012345678901 Type : AzureKeyVault Uri : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint : 112233445566778990011223344556677889900 CreationDate : 1/1/2017 12:00:00:00 AM ResourceDateGroupName : ContosoResourceGroup ServerName : ContosoServer ServerKeyName : contoso_contosokey2_01234567890123456789012345678901 Type : AzureKeyVault Uri : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint : 00998877665544322110099887665544332211 CreationDate : 1/1/2017 12:00:00 AM

### Esempio 2: Ottenere una chiave specifica del Vault delle chiavi
```
PS C:\> $MyServerKeyVaultKey = Get-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

Questo comando ottiene la chiave del Vault chiave con ID ' ' e quindi la archivia https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 nella variabile $MyServerKeyVaultKey chiave.
È possibile esaminare le proprietà dei $MyServerKeyVaultKey per ottenere informazioni dettagliate sul vault delle chiavi.

## PARAMETERS

### -DefaultProfile
Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure

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

### -KeyId
KeyId della chiave del Vault di Azure.

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

### -ResourceGroupName
Nome del gruppo di risorse

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

### -ServerName
Nome del server SQL di Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## INPUT

### System.String

## OUTPUT

### Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel

## NOTE

## COLLEGAMENTI CORRELATI

[documentazione SQL database](https://docs.microsoft.com/azure/sql-database/)
