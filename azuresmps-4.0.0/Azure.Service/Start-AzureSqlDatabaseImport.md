---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5EE936CA-DD9A-4BC6-B835-E22AE633B46D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bc7c8f39f1bdbd35cfffeb59b3b4f184f30845e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023385"
---
# <span data-ttu-id="63d0b-101">Start-AzureSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="63d0b-101">Start-AzureSqlDatabaseImport</span></span>

## <span data-ttu-id="63d0b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="63d0b-102">SYNOPSIS</span></span>
<span data-ttu-id="63d0b-103">Avvia un'operazione di importazione dall'archiviazione BLOB a un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="63d0b-103">Starts an import operation from blob storage to an Azure SQL Database.</span></span>

## <span data-ttu-id="63d0b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="63d0b-104">SYNTAX</span></span>

### <span data-ttu-id="63d0b-105">ByContainerObject</span><span class="sxs-lookup"><span data-stu-id="63d0b-105">ByContainerObject</span></span>
```
Start-AzureSqlDatabaseImport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContainer <AzureStorageContainer> -DatabaseName <String> -BlobName <String>
 [-Edition <DatabaseEdition>] [-DatabaseMaxSize <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="63d0b-106">ByContainerName</span><span class="sxs-lookup"><span data-stu-id="63d0b-106">ByContainerName</span></span>
```
Start-AzureSqlDatabaseImport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContext <IStorageContext> -StorageContainerName <String> -DatabaseName <String> -BlobName <String>
 [-Edition <DatabaseEdition>] [-DatabaseMaxSize <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="63d0b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63d0b-107">DESCRIPTION</span></span>
<span data-ttu-id="63d0b-108">Il cmdlet **Start-AzureSqlDatabaseImport** avvia un'operazione di importazione da archiviazione BLOB di Azure a un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="63d0b-108">The **Start-AzureSqlDatabaseImport** cmdlet starts an import operation from Azure Blob storage to an Azure SQL Database.</span></span>
<span data-ttu-id="63d0b-109">Se il database non esiste, questo cmdlet lo crea usando i valori di dimensioni e di edizione specificati.</span><span class="sxs-lookup"><span data-stu-id="63d0b-109">If the database does not exist, this cmdlet creates it by using the size and edition values that you specify.</span></span>
<span data-ttu-id="63d0b-110">L'operazione richiede un contesto di connessione del server di database.</span><span class="sxs-lookup"><span data-stu-id="63d0b-110">The operation requires a database server connection context.</span></span>
<span data-ttu-id="63d0b-111">Usa il cmdlet Get-AzureSqlDatabaseImportExportStatus per ottenere lo stato dell'operazione di importazione.</span><span class="sxs-lookup"><span data-stu-id="63d0b-111">Use the Get-AzureSqlDatabaseImportExportStatus cmdlet to get the status of the import operation.</span></span>

## <span data-ttu-id="63d0b-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="63d0b-112">EXAMPLES</span></span>

### <span data-ttu-id="63d0b-113">Esempio 1: importare un database</span><span class="sxs-lookup"><span data-stu-id="63d0b-113">Example 1: Import a database</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> $SqlContext = New-AzureSqlDatabaseServerContext -ServerName $ServerName -Credentials $Credential
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName $StorageName -StorageAccountKey $StorageKey
PS C:\> $Container = Get-AzureStorageContainer -Name $ContainerName -Context $StorageContext
PS C:\> $ImportRequest = Start-AzureSqlDatabaseImport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
```

<span data-ttu-id="63d0b-114">Questo esempio avvia un processo di importazione dallo spazio di archiviazione BLOB nella variabile $BlobName nel database SQL di Azure denominato DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="63d0b-114">This example initiates an import process from the Blob storage in the $BlobName variable into the Azure SQL Database named DatabaseName.</span></span>

## <span data-ttu-id="63d0b-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="63d0b-115">PARAMETERS</span></span>

### <span data-ttu-id="63d0b-116">-Blobname</span><span class="sxs-lookup"><span data-stu-id="63d0b-116">-BlobName</span></span>
<span data-ttu-id="63d0b-117">Specifica il nome dell'archiviazione BLOB di Azure da cui questo cmdlet importa il database.</span><span class="sxs-lookup"><span data-stu-id="63d0b-117">Specifies the name of the Azure Blob storage from which this cmdlet imports the database.</span></span>

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

### <span data-ttu-id="63d0b-118">-DatabaseMaxSize</span><span class="sxs-lookup"><span data-stu-id="63d0b-118">-DatabaseMaxSize</span></span>
<span data-ttu-id="63d0b-119">Specifica le dimensioni massime, in gigabyte, per il database.</span><span class="sxs-lookup"><span data-stu-id="63d0b-119">Specifies the maximum size, in gigabytes, for the database.</span></span>
<span data-ttu-id="63d0b-120">Se il database non esiste, questo cmdlet lo crea in base alle dimensioni massime.</span><span class="sxs-lookup"><span data-stu-id="63d0b-120">If the database does not exist, this cmdlet creates it based on this maximum size.</span></span>
<span data-ttu-id="63d0b-121">I valori accettabili variano in base all'edizione.</span><span class="sxs-lookup"><span data-stu-id="63d0b-121">The acceptable values differ based on edition.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d0b-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="63d0b-122">-DatabaseName</span></span>
<span data-ttu-id="63d0b-123">Specifica un nome per il database.</span><span class="sxs-lookup"><span data-stu-id="63d0b-123">Specifies a name for the database.</span></span>
<span data-ttu-id="63d0b-124">Se il database non esiste, questo cmdlet lo crea e assegna il nome specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="63d0b-124">If the database does not exist, this cmdlet creates it, and assigns the name that this parameter specifies.</span></span>

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

### <span data-ttu-id="63d0b-125">-Edition</span><span class="sxs-lookup"><span data-stu-id="63d0b-125">-Edition</span></span>
<span data-ttu-id="63d0b-126">Specifica l'edizione del database.</span><span class="sxs-lookup"><span data-stu-id="63d0b-126">Specifies the edition of the database.</span></span>
<span data-ttu-id="63d0b-127">Se il database non esiste, questo cmdlet lo crea come edizione.</span><span class="sxs-lookup"><span data-stu-id="63d0b-127">If the database does not exist, this cmdlet creates it as this edition.</span></span>
<span data-ttu-id="63d0b-128">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="63d0b-128">Valid values are:</span></span> 

- <span data-ttu-id="63d0b-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="63d0b-129">None</span></span>
- <span data-ttu-id="63d0b-130">Web</span><span class="sxs-lookup"><span data-stu-id="63d0b-130">Web</span></span> 
- <span data-ttu-id="63d0b-131">Business</span><span class="sxs-lookup"><span data-stu-id="63d0b-131">Business</span></span> 
- <span data-ttu-id="63d0b-132">Base</span><span class="sxs-lookup"><span data-stu-id="63d0b-132">Basic</span></span>
- <span data-ttu-id="63d0b-133">Standard</span><span class="sxs-lookup"><span data-stu-id="63d0b-133">Standard</span></span>
- <span data-ttu-id="63d0b-134">Premium</span><span class="sxs-lookup"><span data-stu-id="63d0b-134">Premium</span></span>

<span data-ttu-id="63d0b-135">Il valore predefinito è Web.</span><span class="sxs-lookup"><span data-stu-id="63d0b-135">The default is Web.</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d0b-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="63d0b-136">-Profile</span></span>
<span data-ttu-id="63d0b-137">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63d0b-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="63d0b-138">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="63d0b-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d0b-139">-SqlConnectionContext</span><span class="sxs-lookup"><span data-stu-id="63d0b-139">-SqlConnectionContext</span></span>
<span data-ttu-id="63d0b-140">Specifica il contesto di connessione di un server che contiene il database.</span><span class="sxs-lookup"><span data-stu-id="63d0b-140">Specifies the connection context of a server that contains the database.</span></span>

```yaml
Type: ISqlServerConnectionInformation
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d0b-141">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="63d0b-141">-StorageContainer</span></span>
<span data-ttu-id="63d0b-142">Specifica il contenitore di archiviazione contenente il BLOB da cui questo cmdlet importa un database.</span><span class="sxs-lookup"><span data-stu-id="63d0b-142">Specifies the storage container that contains the Blob from which this cmdlet imports a database.</span></span>

```yaml
Type: AzureStorageContainer
Parameter Sets: ByContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d0b-143">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="63d0b-143">-StorageContainerName</span></span>
<span data-ttu-id="63d0b-144">Specifica il nome del contenitore di archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="63d0b-144">Specifies the name of the Blob storage container.</span></span>

```yaml
Type: String
Parameter Sets: ByContainerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d0b-145">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="63d0b-145">-StorageContext</span></span>
<span data-ttu-id="63d0b-146">Specifica il contesto del contenitore di archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="63d0b-146">Specifies the context of the Blob storage container.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ByContainerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d0b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63d0b-147">CommonParameters</span></span>
<span data-ttu-id="63d0b-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63d0b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63d0b-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63d0b-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63d0b-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="63d0b-150">INPUTS</span></span>

## <span data-ttu-id="63d0b-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="63d0b-151">OUTPUTS</span></span>

### <span data-ttu-id="63d0b-152">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. ImportExportRequest</span><span class="sxs-lookup"><span data-stu-id="63d0b-152">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.ImportExportRequest</span></span>

## <span data-ttu-id="63d0b-153">Note</span><span class="sxs-lookup"><span data-stu-id="63d0b-153">NOTES</span></span>

## <span data-ttu-id="63d0b-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="63d0b-154">RELATED LINKS</span></span>

[<span data-ttu-id="63d0b-155">Database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="63d0b-155">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="63d0b-156">Importare database</span><span class="sxs-lookup"><span data-stu-id="63d0b-156">Import Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn781284.aspx)

[<span data-ttu-id="63d0b-157">Operazioni per i database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="63d0b-157">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="63d0b-158">Get-AzureSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="63d0b-158">Get-AzureSqlDatabaseImportExportStatus</span></span>](./Get-AzureSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="63d0b-159">Start-AzureSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="63d0b-159">Start-AzureSqlDatabaseExport</span></span>](./Start-AzureSqlDatabaseExport.md)


