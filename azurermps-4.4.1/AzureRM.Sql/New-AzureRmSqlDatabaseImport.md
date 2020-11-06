---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A1327BC6-F090-490E-8DC2-2CC48A21C2C0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseImport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseImport.md
ms.openlocfilehash: 8ebe1cecc42d8ee01c270b994e1e10de4f402c1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514655"
---
# <span data-ttu-id="45022-101">New-AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="45022-101">New-AzureRmSqlDatabaseImport</span></span>

## <span data-ttu-id="45022-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="45022-102">SYNOPSIS</span></span>
<span data-ttu-id="45022-103">Importa un file con estensione bacpac e crea un nuovo database nel server.</span><span class="sxs-lookup"><span data-stu-id="45022-103">Imports a .bacpac file and create a new database on the server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45022-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="45022-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseImport -DatabaseName <String> -Edition <DatabaseEdition> -ServiceObjectiveName <String>
 -DatabaseMaxSizeBytes <Int64> [-ServerName] <String> -StorageKeyType <StorageKeyType> -StorageKey <String>
 -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45022-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45022-105">DESCRIPTION</span></span>
<span data-ttu-id="45022-106">Il cmdlet **New-AzureRmSqlDatabaseImport** importa un file BACPAC da un account di archiviazione di Azure in un nuovo database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="45022-106">The **New-AzureRmSqlDatabaseImport** cmdlet imports a bacpac file from an Azure storage account to a new Azure SQL Database.</span></span>
<span data-ttu-id="45022-107">Per recuperare le informazioni sullo stato della richiesta, è possibile che venga inviata la richiesta di stato del database di importazione.</span><span class="sxs-lookup"><span data-stu-id="45022-107">The get import database status request may be sent to retrieve status information for this request.</span></span>

## <span data-ttu-id="45022-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="45022-108">EXAMPLES</span></span>

### <span data-ttu-id="45022-109">Esempio 1: creare una richiesta di importazione per un file BACPAC</span><span class="sxs-lookup"><span data-stu-id="45022-109">Example 1: Create an import request for a bacpac file</span></span>
```
PS C:\>New-AzureRmSqlDatabaseImport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword $SecureString -Edition Standard -ServiceObjectiveName S0 -DatabaseMaxSizeBytes 5000000
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

<span data-ttu-id="45022-110">Questo comando crea una richiesta di importazione per importare un BACPAC in un nuovo database.</span><span class="sxs-lookup"><span data-stu-id="45022-110">This command creates an import request to import a .bacpac to a new database.</span></span>

## <span data-ttu-id="45022-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="45022-111">PARAMETERS</span></span>

### <span data-ttu-id="45022-112">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="45022-112">-AdministratorLogin</span></span>
<span data-ttu-id="45022-113">Specifica il nome dell'amministratore di SQL.</span><span class="sxs-lookup"><span data-stu-id="45022-113">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="45022-114">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="45022-114">-AdministratorLoginPassword</span></span>
<span data-ttu-id="45022-115">Specifica la password dell'amministratore di SQL.</span><span class="sxs-lookup"><span data-stu-id="45022-115">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="45022-116">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="45022-116">-AuthenticationType</span></span>
<span data-ttu-id="45022-117">Specifica il tipo di autenticazione usato per accedere al server.</span><span class="sxs-lookup"><span data-stu-id="45022-117">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="45022-118">Questo parametro imposta come predefinito SQL se non è impostato alcun tipo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="45022-118">This parameter defaults to SQL if no authentication type is set.</span></span>

<span data-ttu-id="45022-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="45022-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="45022-120">SQL.</span><span class="sxs-lookup"><span data-stu-id="45022-120">SQL.</span></span>
<span data-ttu-id="45022-121">Autenticazione SQL.</span><span class="sxs-lookup"><span data-stu-id="45022-121">SQL authentication.</span></span>
<span data-ttu-id="45022-122">Imposta i parametri *AdministratorLogin* e *AdministratorLoginPassword* sul nome utente e la password di amministratore SQL.</span><span class="sxs-lookup"><span data-stu-id="45022-122">Set the *AdministratorLogin* and *AdministratorLoginPassword* parameters to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="45022-123">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="45022-123">ADPassword.</span></span>
<span data-ttu-id="45022-124">Autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="45022-124">Azure Active Directory authentication.</span></span>
<span data-ttu-id="45022-125">Impostare *AdministratorLogin* e *AdministratorLoginPassword* sul nome utente e la password di amministratore di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="45022-125">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure Active Directory administrator username and password.</span></span>

<span data-ttu-id="45022-126">Questo parametro è disponibile solo nei server SQL database V12.</span><span class="sxs-lookup"><span data-stu-id="45022-126">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="45022-127">-DatabaseMaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="45022-127">-DatabaseMaxSizeBytes</span></span>
<span data-ttu-id="45022-128">Specifica le dimensioni massime per il database appena importato.</span><span class="sxs-lookup"><span data-stu-id="45022-128">Specifies the maximum size for the newly imported database.</span></span>

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

### <span data-ttu-id="45022-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="45022-129">-DatabaseName</span></span>
<span data-ttu-id="45022-130">Specifica il nome del database SQL.</span><span class="sxs-lookup"><span data-stu-id="45022-130">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="45022-131">-Edition</span><span class="sxs-lookup"><span data-stu-id="45022-131">-Edition</span></span>
<span data-ttu-id="45022-132">Specifica l'edizione del nuovo database da importare.</span><span class="sxs-lookup"><span data-stu-id="45022-132">Specifies the edition of the new database to import to.</span></span>

<span data-ttu-id="45022-133">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="45022-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="45022-134">Premium</span><span class="sxs-lookup"><span data-stu-id="45022-134">Premium</span></span>
- <span data-ttu-id="45022-135">Base</span><span class="sxs-lookup"><span data-stu-id="45022-135">Basic</span></span>
- <span data-ttu-id="45022-136">Standard</span><span class="sxs-lookup"><span data-stu-id="45022-136">Standard</span></span>
- <span data-ttu-id="45022-137">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="45022-137">DataWarehouse</span></span>
- <span data-ttu-id="45022-138">Gratuito</span><span class="sxs-lookup"><span data-stu-id="45022-138">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45022-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45022-139">-ResourceGroupName</span></span>
<span data-ttu-id="45022-140">Specifica il nome del gruppo di risorse per il server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="45022-140">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="45022-141">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="45022-141">-ServerName</span></span>
<span data-ttu-id="45022-142">Specifica il nome del server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="45022-142">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="45022-143">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="45022-143">-ServiceObjectiveName</span></span>
<span data-ttu-id="45022-144">Specifica il nome dell'obiettivo del servizio da assegnare al database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="45022-144">Specifies the name of the service objective to assign to the Azure SQL Database.</span></span>

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

### <span data-ttu-id="45022-145">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="45022-145">-StorageKey</span></span>
<span data-ttu-id="45022-146">Specifica il tasto di scelta per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="45022-146">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="45022-147">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="45022-147">-StorageKeyType</span></span>
<span data-ttu-id="45022-148">Specifica il tipo di chiave di accesso per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="45022-148">Specifies the type of access key for the storage account.</span></span>

<span data-ttu-id="45022-149">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="45022-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="45022-150">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="45022-150">StorageAccessKey.</span></span>
<span data-ttu-id="45022-151">Usa la chiave dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="45022-151">Uses the storage account key.</span></span> 
- <span data-ttu-id="45022-152">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="45022-152">SharedAccessKey.</span></span>
<span data-ttu-id="45022-153">Usa la chiave della firma di accesso condiviso (SAS).</span><span class="sxs-lookup"><span data-stu-id="45022-153">Uses the Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="45022-154">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="45022-154">-StorageUri</span></span>
<span data-ttu-id="45022-155">Specifica l'URI BLOB del file BACPAC.</span><span class="sxs-lookup"><span data-stu-id="45022-155">Specifies the blob URI of the .bacpac file.</span></span>

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

### <span data-ttu-id="45022-156">-Confermare</span><span class="sxs-lookup"><span data-stu-id="45022-156">-Confirm</span></span>
<span data-ttu-id="45022-157">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45022-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45022-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45022-158">-WhatIf</span></span>
<span data-ttu-id="45022-159">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45022-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45022-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45022-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45022-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45022-161">-DefaultProfile</span></span>
<span data-ttu-id="45022-162">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="45022-162">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45022-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45022-163">CommonParameters</span></span>
<span data-ttu-id="45022-164">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45022-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45022-165">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45022-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45022-166">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="45022-166">INPUTS</span></span>

## <span data-ttu-id="45022-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="45022-167">OUTPUTS</span></span>

### <span data-ttu-id="45022-168">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="45022-168">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="45022-169">Note</span><span class="sxs-lookup"><span data-stu-id="45022-169">NOTES</span></span>
* <span data-ttu-id="45022-170">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="45022-170">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="45022-171">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="45022-171">RELATED LINKS</span></span>

[<span data-ttu-id="45022-172">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="45022-172">Get-AzureRmSqlDatabaseImportExportStatus</span></span>](./Get-AzureRmSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="45022-173">New-AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="45022-173">New-AzureRmSqlDatabaseExport</span></span>](./New-AzureRmSqlDatabaseExport.md)

[<span data-ttu-id="45022-174">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="45022-174">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

