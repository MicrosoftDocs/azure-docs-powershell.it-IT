---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseExport.md
ms.openlocfilehash: f7ede8432f8e833b3d309925daab591889836257
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688216"
---
# <span data-ttu-id="85321-101">New-AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="85321-101">New-AzureRmSqlDatabaseExport</span></span>

## <span data-ttu-id="85321-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="85321-102">SYNOPSIS</span></span>
<span data-ttu-id="85321-103">Esporta un database SQL di Azure come file con estensione bacpac in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="85321-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85321-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85321-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85321-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85321-105">DESCRIPTION</span></span>
<span data-ttu-id="85321-106">Il cmdlet **New-AzureRmSqlDatabaseExport** esporta un database SQL di Azure come file con estensione bacpac in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="85321-106">The **New-AzureRmSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="85321-107">Per recuperare le informazioni sullo stato della richiesta, è possibile che venga inviata la richiesta di stato del database di esportazione.</span><span class="sxs-lookup"><span data-stu-id="85321-107">The get export database status request may be sent to retrieve status information for this request.</span></span>

<span data-ttu-id="85321-108">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="85321-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="85321-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85321-109">EXAMPLES</span></span>

### <span data-ttu-id="85321-110">Esempio 1: creare una richiesta di esportazione per un database</span><span class="sxs-lookup"><span data-stu-id="85321-110">Example 1: Create an export request for a database</span></span>
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

<span data-ttu-id="85321-111">Questo comando crea una richiesta di esportazione per il database specificato.</span><span class="sxs-lookup"><span data-stu-id="85321-111">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="85321-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="85321-112">PARAMETERS</span></span>

### <span data-ttu-id="85321-113">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="85321-113">-AdministratorLogin</span></span>
<span data-ttu-id="85321-114">Specifica il nome dell'amministratore di SQL.</span><span class="sxs-lookup"><span data-stu-id="85321-114">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="85321-115">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="85321-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="85321-116">Specifica la password dell'amministratore di SQL.</span><span class="sxs-lookup"><span data-stu-id="85321-116">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="85321-117">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="85321-117">-AuthenticationType</span></span>
<span data-ttu-id="85321-118">Specifica il tipo di autenticazione usato per accedere al server.</span><span class="sxs-lookup"><span data-stu-id="85321-118">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="85321-119">Il valore predefinito è SQL se non è impostato alcun tipo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="85321-119">The default value is SQL if no authentication type is set.</span></span>

<span data-ttu-id="85321-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="85321-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="85321-121">SQL.</span><span class="sxs-lookup"><span data-stu-id="85321-121">Sql.</span></span>
<span data-ttu-id="85321-122">Autenticazione SQL.</span><span class="sxs-lookup"><span data-stu-id="85321-122">SQL authentication.</span></span>
<span data-ttu-id="85321-123">Imposta *AdministratorLogin* e *AdministratorLoginPassword* sul nome utente e la password di amministratore SQL.</span><span class="sxs-lookup"><span data-stu-id="85321-123">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="85321-124">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="85321-124">ADPassword.</span></span>
<span data-ttu-id="85321-125">Autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="85321-125">Azure Active Directory authentication.</span></span>
<span data-ttu-id="85321-126">Imposta *AdministratorLogin* e *AdministratorLoginPassword* sul nome utente e la password dell'amministratore di Azure ad.</span><span class="sxs-lookup"><span data-stu-id="85321-126">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>

<span data-ttu-id="85321-127">Questo parametro è disponibile solo nei server SQL database V12.</span><span class="sxs-lookup"><span data-stu-id="85321-127">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="85321-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="85321-128">-DatabaseName</span></span>
<span data-ttu-id="85321-129">Specifica il nome del database SQL.</span><span class="sxs-lookup"><span data-stu-id="85321-129">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="85321-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85321-130">-ResourceGroupName</span></span>
<span data-ttu-id="85321-131">Specifica il nome del gruppo di risorse per il server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="85321-131">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="85321-132">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="85321-132">-ServerName</span></span>
<span data-ttu-id="85321-133">Specifica il nome del server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="85321-133">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="85321-134">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="85321-134">-StorageKey</span></span>
<span data-ttu-id="85321-135">Specifica il tasto di scelta per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="85321-135">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="85321-136">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="85321-136">-StorageKeyType</span></span>
<span data-ttu-id="85321-137">Specifica il tipo di chiave di accesso per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="85321-137">Specifies the type of access key for the storage account.</span></span>

<span data-ttu-id="85321-138">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="85321-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="85321-139">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="85321-139">StorageAccessKey.</span></span>
<span data-ttu-id="85321-140">Questo valore usa una chiave dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="85321-140">This value uses a storage account key.</span></span> 
- <span data-ttu-id="85321-141">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="85321-141">SharedAccessKey.</span></span>
<span data-ttu-id="85321-142">Questo valore usa una chiave SAS (Shared Access Signature).</span><span class="sxs-lookup"><span data-stu-id="85321-142">This value uses a Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="85321-143">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="85321-143">-StorageUri</span></span>
<span data-ttu-id="85321-144">Specifica il collegamento BLOB, come URL, al file BACPAC.</span><span class="sxs-lookup"><span data-stu-id="85321-144">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

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

### <span data-ttu-id="85321-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="85321-145">-Confirm</span></span>
<span data-ttu-id="85321-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85321-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85321-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85321-147">-WhatIf</span></span>
<span data-ttu-id="85321-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85321-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85321-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85321-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85321-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85321-150">-DefaultProfile</span></span>
<span data-ttu-id="85321-151">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="85321-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85321-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85321-152">CommonParameters</span></span>
<span data-ttu-id="85321-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85321-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85321-154">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85321-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85321-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="85321-155">INPUTS</span></span>

## <span data-ttu-id="85321-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85321-156">OUTPUTS</span></span>

### <span data-ttu-id="85321-157">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="85321-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="85321-158">Note</span><span class="sxs-lookup"><span data-stu-id="85321-158">NOTES</span></span>
* <span data-ttu-id="85321-159">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="85321-159">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="85321-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85321-160">RELATED LINKS</span></span>

[<span data-ttu-id="85321-161">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="85321-161">Get-AzureRmSqlDatabaseImportExportStatus</span></span>](./Get-AzureRmSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="85321-162">New-AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="85321-162">New-AzureRmSqlDatabaseImport</span></span>](./New-AzureRmSqlDatabaseImport.md)

[<span data-ttu-id="85321-163">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="85321-163">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
