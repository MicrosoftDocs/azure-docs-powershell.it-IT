---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaseexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
ms.openlocfilehash: c5b0295458d0efe443dc20ab069ccfb62a44eb49
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199998"
---
# <span data-ttu-id="cc686-101">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="cc686-101">New-AzSqlDatabaseExport</span></span>

## <span data-ttu-id="cc686-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cc686-102">SYNOPSIS</span></span>
<span data-ttu-id="cc686-103">Esporta un database SQL di Azure come file con estensione bacpac in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cc686-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

## <span data-ttu-id="cc686-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cc686-104">SYNTAX</span></span>

```
New-AzSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-UseNetworkIsolation <Boolean>]
 [-StorageAccountResourceIdForPrivateLink <String>] [-SqlServerResourceIdForPrivateLink <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cc686-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc686-105">DESCRIPTION</span></span>
<span data-ttu-id="cc686-106">Il cmdlet **New-AzSqlDatabaseExport** esporta un database SQL di Azure come file con estensione bacpac in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cc686-106">The **New-AzSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="cc686-107">Per recuperare le informazioni sullo stato della richiesta, è possibile che venga inviata la richiesta di stato del database di esportazione.</span><span class="sxs-lookup"><span data-stu-id="cc686-107">The get export database status request may be sent to retrieve status information for this request.</span></span>
<span data-ttu-id="cc686-108">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="cc686-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="cc686-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cc686-109">EXAMPLES</span></span>

### <span data-ttu-id="cc686-110">Esempio 1: creare una richiesta di esportazione per un database</span><span class="sxs-lookup"><span data-stu-id="cc686-110">Example 1: Create an export request for a database</span></span>
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

<span data-ttu-id="cc686-111">Questo comando crea una richiesta di esportazione per il database specificato.</span><span class="sxs-lookup"><span data-stu-id="cc686-111">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="cc686-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cc686-112">PARAMETERS</span></span>

### <span data-ttu-id="cc686-113">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="cc686-113">-AdministratorLogin</span></span>
<span data-ttu-id="cc686-114">Specifica il nome dell'amministratore di SQL.</span><span class="sxs-lookup"><span data-stu-id="cc686-114">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="cc686-115">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="cc686-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="cc686-116">Specifica la password dell'amministratore di SQL.</span><span class="sxs-lookup"><span data-stu-id="cc686-116">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="cc686-117">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="cc686-117">-AuthenticationType</span></span>
<span data-ttu-id="cc686-118">Specifica il tipo di autenticazione usato per accedere al server.</span><span class="sxs-lookup"><span data-stu-id="cc686-118">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="cc686-119">Il valore predefinito è SQL se non è impostato alcun tipo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="cc686-119">The default value is SQL if no authentication type is set.</span></span>
<span data-ttu-id="cc686-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="cc686-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cc686-121">SQL.</span><span class="sxs-lookup"><span data-stu-id="cc686-121">Sql.</span></span>
<span data-ttu-id="cc686-122">Autenticazione SQL.</span><span class="sxs-lookup"><span data-stu-id="cc686-122">SQL authentication.</span></span>
<span data-ttu-id="cc686-123">Imposta *AdministratorLogin* e *AdministratorLoginPassword* sul nome utente e la password di amministratore SQL.</span><span class="sxs-lookup"><span data-stu-id="cc686-123">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="cc686-124">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="cc686-124">ADPassword.</span></span>
<span data-ttu-id="cc686-125">Autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cc686-125">Azure Active Directory authentication.</span></span>
<span data-ttu-id="cc686-126">Imposta *AdministratorLogin* e *AdministratorLoginPassword* sul nome utente e la password dell'amministratore di Azure ad.</span><span class="sxs-lookup"><span data-stu-id="cc686-126">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>
<span data-ttu-id="cc686-127">Questo parametro è disponibile solo nei server SQL database V12.</span><span class="sxs-lookup"><span data-stu-id="cc686-127">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="cc686-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cc686-128">-DatabaseName</span></span>
<span data-ttu-id="cc686-129">Specifica il nome del database SQL.</span><span class="sxs-lookup"><span data-stu-id="cc686-129">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="cc686-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc686-130">-DefaultProfile</span></span>
<span data-ttu-id="cc686-131">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="cc686-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc686-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc686-132">-ResourceGroupName</span></span>
<span data-ttu-id="cc686-133">Specifica il nome del gruppo di risorse per il server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="cc686-133">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="cc686-134">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="cc686-134">-ServerName</span></span>
<span data-ttu-id="cc686-135">Specifica il nome del server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="cc686-135">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="cc686-136">-SqlServerResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="cc686-136">-SqlServerResourceIdForPrivateLink</span></span>
<span data-ttu-id="cc686-137">ID risorsa di SQL Server per creare un collegamento privato</span><span class="sxs-lookup"><span data-stu-id="cc686-137">The sql server resource id to create private link</span></span>

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

### <span data-ttu-id="cc686-138">-StorageAccountResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="cc686-138">-StorageAccountResourceIdForPrivateLink</span></span>
<span data-ttu-id="cc686-139">ID risorsa account di archiviazione per creare un collegamento privato</span><span class="sxs-lookup"><span data-stu-id="cc686-139">The storage account resource id to create private link</span></span>

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

### <span data-ttu-id="cc686-140">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="cc686-140">-StorageKey</span></span>
<span data-ttu-id="cc686-141">Specifica il tasto di scelta per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cc686-141">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="cc686-142">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="cc686-142">-StorageKeyType</span></span>
<span data-ttu-id="cc686-143">Specifica il tipo di chiave di accesso per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cc686-143">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="cc686-144">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="cc686-144">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cc686-145">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="cc686-145">StorageAccessKey.</span></span>
<span data-ttu-id="cc686-146">Questo valore usa una chiave dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cc686-146">This value uses a storage account key.</span></span> 
- <span data-ttu-id="cc686-147">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="cc686-147">SharedAccessKey.</span></span>
<span data-ttu-id="cc686-148">Questo valore usa una chiave SAS (Shared Access Signature).</span><span class="sxs-lookup"><span data-stu-id="cc686-148">This value uses a Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="cc686-149">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="cc686-149">-StorageUri</span></span>
<span data-ttu-id="cc686-150">Specifica il collegamento BLOB, come URL, al file BACPAC.</span><span class="sxs-lookup"><span data-stu-id="cc686-150">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

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

### <span data-ttu-id="cc686-151">-UseNetworkIsolation</span><span class="sxs-lookup"><span data-stu-id="cc686-151">-UseNetworkIsolation</span></span>
<span data-ttu-id="cc686-152">Se impostato, creerà un collegamento privato per l'account di archiviazione e/o SQL Server</span><span class="sxs-lookup"><span data-stu-id="cc686-152">If set, will create private link for storage account and/or SQL server</span></span>

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

### <span data-ttu-id="cc686-153">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cc686-153">-Confirm</span></span>
<span data-ttu-id="cc686-154">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc686-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc686-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc686-155">-WhatIf</span></span>
<span data-ttu-id="cc686-156">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cc686-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc686-157">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cc686-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc686-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc686-158">CommonParameters</span></span>
<span data-ttu-id="cc686-159">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc686-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc686-160">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc686-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc686-161">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cc686-161">INPUTS</span></span>

### <span data-ttu-id="cc686-162">System. String</span><span class="sxs-lookup"><span data-stu-id="cc686-162">System.String</span></span>

## <span data-ttu-id="cc686-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cc686-163">OUTPUTS</span></span>

### <span data-ttu-id="cc686-164">Microsoft. Azure. Commands. SQL. ImportExport. Model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="cc686-164">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="cc686-165">Note</span><span class="sxs-lookup"><span data-stu-id="cc686-165">NOTES</span></span>
* <span data-ttu-id="cc686-166">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="cc686-166">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="cc686-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cc686-167">RELATED LINKS</span></span>

[<span data-ttu-id="cc686-168">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="cc686-168">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="cc686-169">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="cc686-169">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="cc686-170">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="cc686-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
