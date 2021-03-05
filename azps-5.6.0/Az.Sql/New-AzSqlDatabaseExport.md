---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabaseexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
ms.openlocfilehash: 198692c73609f6e3e88be0ccbe270c60bc679020
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979213"
---
# <span data-ttu-id="3e6d6-101">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="3e6d6-101">New-AzSqlDatabaseExport</span></span>

## <span data-ttu-id="3e6d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e6d6-102">SYNOPSIS</span></span>
<span data-ttu-id="3e6d6-103">Esporta un database SQL Azure come file con estensione bacpac in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3e6d6-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

## <span data-ttu-id="3e6d6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e6d6-104">SYNTAX</span></span>

```
New-AzSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-UseNetworkIsolation <Boolean>]
 [-StorageAccountResourceIdForPrivateLink <String>] [-SqlServerResourceIdForPrivateLink <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e6d6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3e6d6-105">DESCRIPTION</span></span>
<span data-ttu-id="3e6d6-106">Il cmdlet **New-AzSqlDatabaseExport** esporta un database di SQL azure come file con estensione bacpac in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3e6d6-106">The **New-AzSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="3e6d6-107">È possibile che venga inviata la richiesta di stato di recupero del database di recupero delle informazioni sullo stato per questa richiesta.</span><span class="sxs-lookup"><span data-stu-id="3e6d6-107">The get export database status request may be sent to retrieve status information for this request.</span></span>
<span data-ttu-id="3e6d6-108">Questo cmdlet è supportato anche dal servizio SQL Server stretch database in Azure.</span><span class="sxs-lookup"><span data-stu-id="3e6d6-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3e6d6-109">Per usare questo cmdlet, il firewall nel SQL Server azure dovrà essere configurato su "Consenti ai servizi e alle risorse di Azure di accedere al server".</span><span class="sxs-lookup"><span data-stu-id="3e6d6-109">In order to make use of this cmdlet the firewall on the Azure SQL Server will need to be configured to "Allow Azure services and resources to access this server".</span></span> <span data-ttu-id="3e6d6-110">Se questa configurazione non è configurata, verranno visualizzati gli errori di GatewayTimeout.</span><span class="sxs-lookup"><span data-stu-id="3e6d6-110">If this is not configured then GatewayTimeout errors will be experienced.</span></span>

## <span data-ttu-id="3e6d6-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e6d6-111">EXAMPLES</span></span>

### <span data-ttu-id="3e6d6-112">Esempio 1: Creare una richiesta di esportazione per un database</span><span class="sxs-lookup"><span data-stu-id="3e6d6-112">Example 1: Create an export request for a database</span></span>
```
PS C:\>New-AzSqlDatabaseExport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword "secure password"
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

<span data-ttu-id="3e6d6-113">Questo comando crea una richiesta di esportazione per il database specificato.</span><span class="sxs-lookup"><span data-stu-id="3e6d6-113">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="3e6d6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e6d6-114">PARAMETERS</span></span>

### <span data-ttu-id="3e6d6-115">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="3e6d6-115">-AdministratorLogin</span></span>
<span data-ttu-id="3e6d6-116">Specifica il nome dell'SQL amministratore.</span><span class="sxs-lookup"><span data-stu-id="3e6d6-116">Specifies the name of the SQL administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e6d6-117">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="3e6d6-117">-AdministratorLoginPassword</span></span>
<span data-ttu-id="3e6d6-118">Specifica la password dell'SQL amministratore.</span><span class="sxs-lookup"><span data-stu-id="3e6d6-118">Specifies the password of the SQL administrator.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e6d6-119">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="3e6d6-119">-AuthenticationType</span></span>
<span data-ttu-id="3e6d6-120">Specifica il tipo di autenticazione usato per accedere al server.</span><span class="sxs-lookup"><span data-stu-id="3e6d6-120">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="3e6d6-121">Il valore predefinito è SQL se non è impostato alcun tipo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="3e6d6-121">The default value is SQL if no authentication type is set.</span></span>
<span data-ttu-id="3e6d6-122">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="3e6d6-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3e6d6-123">Sql.</span><span class="sxs-lookup"><span data-stu-id="3e6d6-123">Sql.</span></span>
<span data-ttu-id="3e6d6-124">SQL autenticazione.</span><span class="sxs-lookup"><span data-stu-id="3e6d6-124">SQL authentication.</span></span>
<span data-ttu-id="3e6d6-125">Impostare *AdministratorLogin e* *AdministratorLoginPassword* sul nome utente e la password SQL'amministratore.</span><span class="sxs-lookup"><span data-stu-id="3e6d6-125">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="3e6d6-126">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="3e6d6-126">ADPassword.</span></span>
<span data-ttu-id="3e6d6-127">Autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3e6d6-127">Azure Active Directory authentication.</span></span>
<span data-ttu-id="3e6d6-128">Impostare *AdministratorLogin e* *AdministratorLoginPassword sul* nome utente e la password di amministratore di Azure AD.</span><span class="sxs-lookup"><span data-stu-id="3e6d6-128">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>
<span data-ttu-id="3e6d6-129">Questo parametro è disponibile solo nei server SQL Database V12.</span><span class="sxs-lookup"><span data-stu-id="3e6d6-129">This parameter is only available on SQL Database V12 servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ImportExport.Model.AuthenticationType
Parameter Sets: (All)
Aliases:
Accepted values: None, Sql, AdPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e6d6-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3e6d6-130">-DatabaseName</span></span>
<span data-ttu-id="3e6d6-131">Specifica il nome dell'SQL database.</span><span class="sxs-lookup"><span data-stu-id="3e6d6-131">Specifies the name of the SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e6d6-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e6d6-132">-DefaultProfile</span></span>
<span data-ttu-id="3e6d6-133">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3e6d6-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e6d6-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e6d6-134">-ResourceGroupName</span></span>
<span data-ttu-id="3e6d6-135">Specifica il nome del gruppo di risorse per il server SQL database.</span><span class="sxs-lookup"><span data-stu-id="3e6d6-135">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="3e6d6-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3e6d6-136">-ServerName</span></span>
<span data-ttu-id="3e6d6-137">Specifica il nome del server di SQL database.</span><span class="sxs-lookup"><span data-stu-id="3e6d6-137">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="3e6d6-138">-SqlServerResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="3e6d6-138">-SqlServerResourceIdForPrivateLink</span></span>
<span data-ttu-id="3e6d6-139">ID di risorsa di SQL Server per creare un collegamento privato</span><span class="sxs-lookup"><span data-stu-id="3e6d6-139">The sql server resource id to create private link</span></span>

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

### <span data-ttu-id="3e6d6-140">-StorageAccountResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="3e6d6-140">-StorageAccountResourceIdForPrivateLink</span></span>
<span data-ttu-id="3e6d6-141">ID di risorsa dell'account di archiviazione per creare un collegamento privato</span><span class="sxs-lookup"><span data-stu-id="3e6d6-141">The storage account resource id to create private link</span></span>

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

### <span data-ttu-id="3e6d6-142">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="3e6d6-142">-StorageKey</span></span>
<span data-ttu-id="3e6d6-143">Specifica la chiave di accesso per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3e6d6-143">Specifies the access key for the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e6d6-144">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="3e6d6-144">-StorageKeyType</span></span>
<span data-ttu-id="3e6d6-145">Specifica il tipo di chiave di accesso per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3e6d6-145">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="3e6d6-146">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="3e6d6-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3e6d6-147">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="3e6d6-147">StorageAccessKey.</span></span>
<span data-ttu-id="3e6d6-148">Questo valore usa una chiave dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3e6d6-148">This value uses a storage account key.</span></span> 
- <span data-ttu-id="3e6d6-149">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="3e6d6-149">SharedAccessKey.</span></span>
<span data-ttu-id="3e6d6-150">Questo valore usa una chiave di firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="3e6d6-150">This value uses a Shared Access Signature (SAS) key.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ImportExport.Model.StorageKeyType
Parameter Sets: (All)
Aliases:
Accepted values: StorageAccessKey, SharedAccessKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e6d6-151">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="3e6d6-151">-StorageUri</span></span>
<span data-ttu-id="3e6d6-152">Specifica il collegamento BLOB, come URL, al file con estensione bacpac.</span><span class="sxs-lookup"><span data-stu-id="3e6d6-152">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e6d6-153">-UseNetworkIsolation</span><span class="sxs-lookup"><span data-stu-id="3e6d6-153">-UseNetworkIsolation</span></span>
<span data-ttu-id="3e6d6-154">Se impostato, creerà un collegamento privato per l'account di archiviazione e/o SQL server</span><span class="sxs-lookup"><span data-stu-id="3e6d6-154">If set, will create private link for storage account and/or SQL server</span></span>

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

### <span data-ttu-id="3e6d6-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e6d6-155">-Confirm</span></span>
<span data-ttu-id="3e6d6-156">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e6d6-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e6d6-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e6d6-157">-WhatIf</span></span>
<span data-ttu-id="3e6d6-158">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e6d6-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e6d6-159">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e6d6-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e6d6-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e6d6-160">CommonParameters</span></span>
<span data-ttu-id="3e6d6-161">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e6d6-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e6d6-162">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3e6d6-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e6d6-163">INPUT</span><span class="sxs-lookup"><span data-stu-id="3e6d6-163">INPUTS</span></span>

### <span data-ttu-id="3e6d6-164">System.String</span><span class="sxs-lookup"><span data-stu-id="3e6d6-164">System.String</span></span>

## <span data-ttu-id="3e6d6-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e6d6-165">OUTPUTS</span></span>

### <span data-ttu-id="3e6d6-166">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="3e6d6-166">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="3e6d6-167">NOTE</span><span class="sxs-lookup"><span data-stu-id="3e6d6-167">NOTES</span></span>
* <span data-ttu-id="3e6d6-168">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, sql, database, mssql</span><span class="sxs-lookup"><span data-stu-id="3e6d6-168">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="3e6d6-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e6d6-169">RELATED LINKS</span></span>

[<span data-ttu-id="3e6d6-170">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="3e6d6-170">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="3e6d6-171">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="3e6d6-171">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="3e6d6-172">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="3e6d6-172">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
