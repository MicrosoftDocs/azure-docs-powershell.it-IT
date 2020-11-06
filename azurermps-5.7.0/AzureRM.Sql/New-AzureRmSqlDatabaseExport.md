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
# <span data-ttu-id="1f061-101">New-AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="1f061-101">New-AzureRmSqlDatabaseExport</span></span>

## <span data-ttu-id="1f061-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1f061-102">SYNOPSIS</span></span>
<span data-ttu-id="1f061-103">Esporta un database SQL di Azure come file con estensione bacpac in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1f061-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f061-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f061-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f061-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f061-105">DESCRIPTION</span></span>
<span data-ttu-id="1f061-106">Il cmdlet **New-AzureRmSqlDatabaseExport** esporta un database SQL di Azure come file con estensione bacpac in un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1f061-106">The **New-AzureRmSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="1f061-107">Per recuperare le informazioni sullo stato della richiesta, è possibile che venga inviata la richiesta di stato del database di esportazione.</span><span class="sxs-lookup"><span data-stu-id="1f061-107">The get export database status request may be sent to retrieve status information for this request.</span></span>

<span data-ttu-id="1f061-108">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="1f061-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="1f061-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f061-109">EXAMPLES</span></span>

### <span data-ttu-id="1f061-110">Esempio 1: creare una richiesta di esportazione per un database</span><span class="sxs-lookup"><span data-stu-id="1f061-110">Example 1: Create an export request for a database</span></span>
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

<span data-ttu-id="1f061-111">Questo comando crea una richiesta di esportazione per il database specificato.</span><span class="sxs-lookup"><span data-stu-id="1f061-111">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="1f061-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f061-112">PARAMETERS</span></span>

### <span data-ttu-id="1f061-113">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="1f061-113">-AdministratorLogin</span></span>
<span data-ttu-id="1f061-114">Specifica il nome dell'amministratore di SQL.</span><span class="sxs-lookup"><span data-stu-id="1f061-114">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="1f061-115">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="1f061-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="1f061-116">Specifica la password dell'amministratore di SQL.</span><span class="sxs-lookup"><span data-stu-id="1f061-116">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="1f061-117">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="1f061-117">-AuthenticationType</span></span>
<span data-ttu-id="1f061-118">Specifica il tipo di autenticazione usato per accedere al server.</span><span class="sxs-lookup"><span data-stu-id="1f061-118">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="1f061-119">Il valore predefinito è SQL se non è impostato alcun tipo di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="1f061-119">The default value is SQL if no authentication type is set.</span></span>

<span data-ttu-id="1f061-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="1f061-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1f061-121">SQL.</span><span class="sxs-lookup"><span data-stu-id="1f061-121">Sql.</span></span>
<span data-ttu-id="1f061-122">Autenticazione SQL.</span><span class="sxs-lookup"><span data-stu-id="1f061-122">SQL authentication.</span></span>
<span data-ttu-id="1f061-123">Imposta *AdministratorLogin* e *AdministratorLoginPassword* sul nome utente e la password di amministratore SQL.</span><span class="sxs-lookup"><span data-stu-id="1f061-123">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="1f061-124">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="1f061-124">ADPassword.</span></span>
<span data-ttu-id="1f061-125">Autenticazione di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1f061-125">Azure Active Directory authentication.</span></span>
<span data-ttu-id="1f061-126">Imposta *AdministratorLogin* e *AdministratorLoginPassword* sul nome utente e la password dell'amministratore di Azure ad.</span><span class="sxs-lookup"><span data-stu-id="1f061-126">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>

<span data-ttu-id="1f061-127">Questo parametro è disponibile solo nei server SQL database V12.</span><span class="sxs-lookup"><span data-stu-id="1f061-127">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="1f061-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1f061-128">-DatabaseName</span></span>
<span data-ttu-id="1f061-129">Specifica il nome del database SQL.</span><span class="sxs-lookup"><span data-stu-id="1f061-129">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="1f061-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f061-130">-DefaultProfile</span></span>
<span data-ttu-id="1f061-131">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1f061-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f061-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f061-132">-ResourceGroupName</span></span>
<span data-ttu-id="1f061-133">Specifica il nome del gruppo di risorse per il server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="1f061-133">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="1f061-134">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="1f061-134">-ServerName</span></span>
<span data-ttu-id="1f061-135">Specifica il nome del server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="1f061-135">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="1f061-136">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="1f061-136">-StorageKey</span></span>
<span data-ttu-id="1f061-137">Specifica il tasto di scelta per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1f061-137">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="1f061-138">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="1f061-138">-StorageKeyType</span></span>
<span data-ttu-id="1f061-139">Specifica il tipo di chiave di accesso per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1f061-139">Specifies the type of access key for the storage account.</span></span>

<span data-ttu-id="1f061-140">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="1f061-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1f061-141">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="1f061-141">StorageAccessKey.</span></span>
<span data-ttu-id="1f061-142">Questo valore usa una chiave dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1f061-142">This value uses a storage account key.</span></span> 
- <span data-ttu-id="1f061-143">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="1f061-143">SharedAccessKey.</span></span>
<span data-ttu-id="1f061-144">Questo valore usa una chiave SAS (Shared Access Signature).</span><span class="sxs-lookup"><span data-stu-id="1f061-144">This value uses a Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="1f061-145">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="1f061-145">-StorageUri</span></span>
<span data-ttu-id="1f061-146">Specifica il collegamento BLOB, come URL, al file BACPAC.</span><span class="sxs-lookup"><span data-stu-id="1f061-146">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

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

### <span data-ttu-id="1f061-147">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1f061-147">-Confirm</span></span>
<span data-ttu-id="1f061-148">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f061-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f061-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f061-149">-WhatIf</span></span>
<span data-ttu-id="1f061-150">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f061-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f061-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f061-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f061-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f061-152">CommonParameters</span></span>
<span data-ttu-id="1f061-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f061-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f061-154">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f061-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f061-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1f061-155">INPUTS</span></span>

### <span data-ttu-id="1f061-156">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1f061-156">None</span></span>
<span data-ttu-id="1f061-157">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="1f061-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1f061-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f061-158">OUTPUTS</span></span>

### <span data-ttu-id="1f061-159">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="1f061-159">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="1f061-160">Note</span><span class="sxs-lookup"><span data-stu-id="1f061-160">NOTES</span></span>
* <span data-ttu-id="1f061-161">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="1f061-161">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="1f061-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f061-162">RELATED LINKS</span></span>

[<span data-ttu-id="1f061-163">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="1f061-163">Get-AzureRmSqlDatabaseImportExportStatus</span></span>](./Get-AzureRmSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="1f061-164">New-AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="1f061-164">New-AzureRmSqlDatabaseImport</span></span>](./New-AzureRmSqlDatabaseImport.md)

[<span data-ttu-id="1f061-165">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="1f061-165">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
