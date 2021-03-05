---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1327BC6-F090-490E-8DC2-2CC48A21C2C0
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabaseimport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
ms.openlocfilehash: e0f23e1d41e27e7e16cf9a1cbead42a979f73eed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979197"
---
# <span data-ttu-id="db67d-101">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="db67d-101">New-AzSqlDatabaseImport</span></span>

## <span data-ttu-id="db67d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db67d-102">SYNOPSIS</span></span>
<span data-ttu-id="db67d-103">Importa un file con estensione bacpac e crea un nuovo database nel server.</span><span class="sxs-lookup"><span data-stu-id="db67d-103">Imports a .bacpac file and create a new database on the server.</span></span>

## <span data-ttu-id="db67d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db67d-104">SYNTAX</span></span>

```
New-AzSqlDatabaseImport -DatabaseName <String> -Edition <DatabaseEdition> -ServiceObjectiveName <String>
 -DatabaseMaxSizeBytes <Int64> [-ServerName] <String> -StorageKeyType <StorageKeyType> -StorageKey <String>
 -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-UseNetworkIsolation <Boolean>]
 [-StorageAccountResourceIdForPrivateLink <String>] [-SqlServerResourceIdForPrivateLink <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db67d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="db67d-105">DESCRIPTION</span></span>
<span data-ttu-id="db67d-106">Il cmdlet **New-AzSqlDatabaseImport** importa un file bacpac da un account di archiviazione di Azure in un nuovo database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="db67d-106">The **New-AzSqlDatabaseImport** cmdlet imports a bacpac file from an Azure storage account to a new Azure SQL Database.</span></span>
<span data-ttu-id="db67d-107">La richiesta di stato di recupera database di importazione può essere inviata per recuperare informazioni sullo stato per questa richiesta.</span><span class="sxs-lookup"><span data-stu-id="db67d-107">The get import database status request may be sent to retrieve status information for this request.</span></span>

## <span data-ttu-id="db67d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db67d-108">EXAMPLES</span></span>

### <span data-ttu-id="db67d-109">Esempio 1: Creare una richiesta di importazione per un file bacpac</span><span class="sxs-lookup"><span data-stu-id="db67d-109">Example 1: Create an import request for a bacpac file</span></span>
```
PS C:\>New-AzSqlDatabaseImport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword $SecureString -Edition Standard -ServiceObjectiveName S0 -DatabaseMaxSizeBytes 5000000
ResourceGroupName          : RG01
ServerName                 : Server01
DatabaseName               : Database01
StorageKeyType             : StorageAccessKey
StorageKey                 : 
StorageUri                 : http://account01.blob.core.contoso.net/bacpacs/database01.bacpac
AdministratorLogin         : User
AdministratorLoginPassword : 
AuthenticationType         : None
OperationStatusLink        : https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-00
                             0-0000-0000-000000000000?api-version=2014-04-01
Status                     : InProgress
ErrorMessage               :
```

<span data-ttu-id="db67d-110">Questo comando crea una richiesta di importazione per importare un file con estensione bacpac in un nuovo database.</span><span class="sxs-lookup"><span data-stu-id="db67d-110">This command creates an import request to import a .bacpac to a new database.</span></span>

## <span data-ttu-id="db67d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db67d-111">PARAMETERS</span></span>

### <span data-ttu-id="db67d-112">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="db67d-112">-AdministratorLogin</span></span>
<span data-ttu-id="db67d-113">Specifica il nome dell'SQL amministratore.</span><span class="sxs-lookup"><span data-stu-id="db67d-113">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="db67d-114">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="db67d-114">-AdministratorLoginPassword</span></span>
<span data-ttu-id="db67d-115">Specifica la password dell'SQL amministratore.</span><span class="sxs-lookup"><span data-stu-id="db67d-115">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="db67d-116">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="db67d-116">-AuthenticationType</span></span>
<span data-ttu-id="db67d-117">Specifica il tipo di autenticazione usato per accedere al server.</span><span class="sxs-lookup"><span data-stu-id="db67d-117">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="db67d-118">Per impostazione predefinita, questo parametro SQL se non è impostato alcun tipo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="db67d-118">This parameter defaults to SQL if no authentication type is set.</span></span>
<span data-ttu-id="db67d-119">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="db67d-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="db67d-120">SQL.</span><span class="sxs-lookup"><span data-stu-id="db67d-120">SQL.</span></span>
<span data-ttu-id="db67d-121">SQL autenticazione.</span><span class="sxs-lookup"><span data-stu-id="db67d-121">SQL authentication.</span></span>
<span data-ttu-id="db67d-122">Impostare i *parametri AdministratorLogin* *e AdministratorLoginPassword* sul nome utente e la password SQL'amministratore.</span><span class="sxs-lookup"><span data-stu-id="db67d-122">Set the *AdministratorLogin* and *AdministratorLoginPassword* parameters to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="db67d-123">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="db67d-123">ADPassword.</span></span>
<span data-ttu-id="db67d-124">Autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="db67d-124">Azure Active Directory authentication.</span></span>
<span data-ttu-id="db67d-125">Impostare *AdministratorLogin e* *AdministratorLoginPassword sul* nome utente e la password di amministratore di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="db67d-125">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure Active Directory administrator username and password.</span></span>
<span data-ttu-id="db67d-126">Questo parametro è disponibile solo nei server SQL Database V12.</span><span class="sxs-lookup"><span data-stu-id="db67d-126">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="db67d-127">-DatabaseMaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="db67d-127">-DatabaseMaxSizeBytes</span></span>
<span data-ttu-id="db67d-128">Specifica le dimensioni massime per il database appena importato.</span><span class="sxs-lookup"><span data-stu-id="db67d-128">Specifies the maximum size for the newly imported database.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db67d-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="db67d-129">-DatabaseName</span></span>
<span data-ttu-id="db67d-130">Specifica il nome dell'SQL database.</span><span class="sxs-lookup"><span data-stu-id="db67d-130">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="db67d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db67d-131">-DefaultProfile</span></span>
<span data-ttu-id="db67d-132">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="db67d-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db67d-133">-Edition</span><span class="sxs-lookup"><span data-stu-id="db67d-133">-Edition</span></span>
<span data-ttu-id="db67d-134">Specifica l'edizione del nuovo database in cui eseguire l'importazione.</span><span class="sxs-lookup"><span data-stu-id="db67d-134">Specifies the edition of the new database to import to.</span></span>
<span data-ttu-id="db67d-135">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="db67d-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="db67d-136">Premium</span><span class="sxs-lookup"><span data-stu-id="db67d-136">Premium</span></span>
- <span data-ttu-id="db67d-137">Di base</span><span class="sxs-lookup"><span data-stu-id="db67d-137">Basic</span></span>
- <span data-ttu-id="db67d-138">Standard</span><span class="sxs-lookup"><span data-stu-id="db67d-138">Standard</span></span>
- <span data-ttu-id="db67d-139">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="db67d-139">DataWarehouse</span></span>
- <span data-ttu-id="db67d-140">Gratis</span><span class="sxs-lookup"><span data-stu-id="db67d-140">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS, GeneralPurpose, BusinessCritical, Hyperscale

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db67d-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db67d-141">-ResourceGroupName</span></span>
<span data-ttu-id="db67d-142">Specifica il nome del gruppo di risorse per il server SQL database.</span><span class="sxs-lookup"><span data-stu-id="db67d-142">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="db67d-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="db67d-143">-ServerName</span></span>
<span data-ttu-id="db67d-144">Specifica il nome del server di SQL database.</span><span class="sxs-lookup"><span data-stu-id="db67d-144">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="db67d-145">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="db67d-145">-ServiceObjectiveName</span></span>
<span data-ttu-id="db67d-146">Specifica il nome dell'obiettivo del servizio da assegnare al database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="db67d-146">Specifies the name of the service objective to assign to the Azure SQL Database.</span></span>

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

### <span data-ttu-id="db67d-147">-SqlServerResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="db67d-147">-SqlServerResourceIdForPrivateLink</span></span>
<span data-ttu-id="db67d-148">ID di risorsa di SQL Server per creare un collegamento privato</span><span class="sxs-lookup"><span data-stu-id="db67d-148">The sql server resource id to create private link</span></span>

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

### <span data-ttu-id="db67d-149">-StorageAccountResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="db67d-149">-StorageAccountResourceIdForPrivateLink</span></span>
<span data-ttu-id="db67d-150">ID di risorsa dell'account di archiviazione per creare un collegamento privato</span><span class="sxs-lookup"><span data-stu-id="db67d-150">The storage account resource id to create private link</span></span>

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

### <span data-ttu-id="db67d-151">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="db67d-151">-StorageKey</span></span>
<span data-ttu-id="db67d-152">Specifica la chiave di accesso per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="db67d-152">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="db67d-153">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="db67d-153">-StorageKeyType</span></span>
<span data-ttu-id="db67d-154">Specifica il tipo di chiave di accesso per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="db67d-154">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="db67d-155">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="db67d-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="db67d-156">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="db67d-156">StorageAccessKey.</span></span>
<span data-ttu-id="db67d-157">Usa la chiave dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="db67d-157">Uses the storage account key.</span></span> 
- <span data-ttu-id="db67d-158">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="db67d-158">SharedAccessKey.</span></span>
<span data-ttu-id="db67d-159">Usa la chiave di firma di accesso condiviso.</span><span class="sxs-lookup"><span data-stu-id="db67d-159">Uses the Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="db67d-160">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="db67d-160">-StorageUri</span></span>
<span data-ttu-id="db67d-161">Specifica l'URI BLOB del file con estensione bacpac.</span><span class="sxs-lookup"><span data-stu-id="db67d-161">Specifies the blob URI of the .bacpac file.</span></span>

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

### <span data-ttu-id="db67d-162">-UseNetworkIsolation</span><span class="sxs-lookup"><span data-stu-id="db67d-162">-UseNetworkIsolation</span></span>
<span data-ttu-id="db67d-163">Se impostato, creerà un collegamento privato per l'account di archiviazione e/o SQL server</span><span class="sxs-lookup"><span data-stu-id="db67d-163">If set, will create private link for storage account and/or SQL server</span></span>

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

### <span data-ttu-id="db67d-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db67d-164">-Confirm</span></span>
<span data-ttu-id="db67d-165">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db67d-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db67d-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db67d-166">-WhatIf</span></span>
<span data-ttu-id="db67d-167">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db67d-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db67d-168">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db67d-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db67d-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db67d-169">CommonParameters</span></span>
<span data-ttu-id="db67d-170">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db67d-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db67d-171">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="db67d-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db67d-172">INPUT</span><span class="sxs-lookup"><span data-stu-id="db67d-172">INPUTS</span></span>

### <span data-ttu-id="db67d-173">System.String</span><span class="sxs-lookup"><span data-stu-id="db67d-173">System.String</span></span>

## <span data-ttu-id="db67d-174">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db67d-174">OUTPUTS</span></span>

### <span data-ttu-id="db67d-175">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="db67d-175">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="db67d-176">NOTE</span><span class="sxs-lookup"><span data-stu-id="db67d-176">NOTES</span></span>
* <span data-ttu-id="db67d-177">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, sql, database, mssql</span><span class="sxs-lookup"><span data-stu-id="db67d-177">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="db67d-178">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db67d-178">RELATED LINKS</span></span>

[<span data-ttu-id="db67d-179">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="db67d-179">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="db67d-180">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="db67d-180">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="db67d-181">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="db67d-181">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

