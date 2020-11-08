---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 3005E411-9466-4602-8E07-F4EF8804AB2A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22bff485bf49e0ec5f482e1325af661862583605
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023710"
---
# <span data-ttu-id="b242f-101">Start-AzureSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="b242f-101">Start-AzureSqlDatabaseExport</span></span>

## <span data-ttu-id="b242f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b242f-102">SYNOPSIS</span></span>
<span data-ttu-id="b242f-103">Avvia un'operazione di esportazione da un database SQL di Azure all'archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="b242f-103">Starts an export operation from an Azure SQL Database to Blob storage.</span></span>

## <span data-ttu-id="b242f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b242f-104">SYNTAX</span></span>

### <span data-ttu-id="b242f-105">ByContainerObject</span><span class="sxs-lookup"><span data-stu-id="b242f-105">ByContainerObject</span></span>
```
Start-AzureSqlDatabaseExport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContainer <AzureStorageContainer> -DatabaseName <String> -BlobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b242f-106">ByContainerName</span><span class="sxs-lookup"><span data-stu-id="b242f-106">ByContainerName</span></span>
```
Start-AzureSqlDatabaseExport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContext <IStorageContext> -StorageContainerName <String> -DatabaseName <String> -BlobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b242f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b242f-107">DESCRIPTION</span></span>
<span data-ttu-id="b242f-108">Il cmdlet **Start-AzureSqlDatabaseExport** avvia un'operazione di esportazione da un database SQL di Azure all'archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="b242f-108">The **Start-AzureSqlDatabaseExport** cmdlet starts an export operation from an Azure SQL Database to Blob storage.</span></span>
<span data-ttu-id="b242f-109">L'operazione richiede un contesto di connessione del server di database.</span><span class="sxs-lookup"><span data-stu-id="b242f-109">The operation requires a database server connection context.</span></span>
<span data-ttu-id="b242f-110">Usa il cmdlet Get-AzureSqlDatabaseImportExportStatus per ottenere lo stato dell'operazione di esportazione.</span><span class="sxs-lookup"><span data-stu-id="b242f-110">Use the Get-AzureSqlDatabaseImportExportStatus cmdlet to get the status of the export operation.</span></span>

## <span data-ttu-id="b242f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b242f-111">EXAMPLES</span></span>

### <span data-ttu-id="b242f-112">Esempio 1: esportare un database</span><span class="sxs-lookup"><span data-stu-id="b242f-112">Example 1: Export a database</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> $SqlContext = New-AzureSqlDatabaseServerContext -ServerName $ServerName -Credential $Credential
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName $StorageName -StorageAccountKey $StorageKey
PS C:\> $Container = Get-AzureStorageContainer -Name $ContainerName -Context $StorageContext
PS C:\> $exportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
```

<span data-ttu-id="b242f-113">Questo esempio avvia un processo di esportazione dal database SQL di Azure con il nome archiviato nella variabile $DatabaseName per l'archiviazione BLOB archiviati nella variabile $BlobName.</span><span class="sxs-lookup"><span data-stu-id="b242f-113">This example initiates an export process from the Azure SQL Database that has the name stored in the $DatabaseName variable to the Blob storage stored in the $BlobName variable.</span></span>

## <span data-ttu-id="b242f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b242f-114">PARAMETERS</span></span>

### <span data-ttu-id="b242f-115">-Blobname</span><span class="sxs-lookup"><span data-stu-id="b242f-115">-BlobName</span></span>
<span data-ttu-id="b242f-116">Specifica il nome dell'archiviazione BLOB di Azure in cui questo cmdlet Esporta il database.</span><span class="sxs-lookup"><span data-stu-id="b242f-116">Specifies the name of the Azure Blob storage into which this cmdlet exports the database.</span></span>

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

### <span data-ttu-id="b242f-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b242f-117">-DatabaseName</span></span>
<span data-ttu-id="b242f-118">Specifica il nome del database da cui questo cmdlet Esporta i dati.</span><span class="sxs-lookup"><span data-stu-id="b242f-118">Specifies the name of the database from which this cmdlet exports data.</span></span>

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

### <span data-ttu-id="b242f-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="b242f-119">-Profile</span></span>
<span data-ttu-id="b242f-120">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b242f-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b242f-121">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="b242f-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b242f-122">-SqlConnectionContext</span><span class="sxs-lookup"><span data-stu-id="b242f-122">-SqlConnectionContext</span></span>
<span data-ttu-id="b242f-123">Specifica il contesto di connessione di un server che contiene il database.</span><span class="sxs-lookup"><span data-stu-id="b242f-123">Specifies the connection context of a server that contains the database.</span></span>

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

### <span data-ttu-id="b242f-124">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="b242f-124">-StorageContainer</span></span>
<span data-ttu-id="b242f-125">Specifica il contenitore di archiviazione contenente il BLOB in cui questo cmdlet esporta un database.</span><span class="sxs-lookup"><span data-stu-id="b242f-125">Specifies the storage container that contains the Blob into which this cmdlet export a database.</span></span>

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

### <span data-ttu-id="b242f-126">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="b242f-126">-StorageContainerName</span></span>
<span data-ttu-id="b242f-127">Specifica il nome del contenitore di archiviazione contenente il BLOB in cui questo cmdlet esporta un database.</span><span class="sxs-lookup"><span data-stu-id="b242f-127">Specifies the name of the storage container that contains the Blob into which this cmdlet exports a database.</span></span>

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

### <span data-ttu-id="b242f-128">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="b242f-128">-StorageContext</span></span>
<span data-ttu-id="b242f-129">Specifica il contesto del contenitore di archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="b242f-129">Specifies the context of the Blob storage container.</span></span>

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

### <span data-ttu-id="b242f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b242f-130">CommonParameters</span></span>
<span data-ttu-id="b242f-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b242f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b242f-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b242f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b242f-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b242f-133">INPUTS</span></span>

## <span data-ttu-id="b242f-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b242f-134">OUTPUTS</span></span>

### <span data-ttu-id="b242f-135">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. ImportExportRequest</span><span class="sxs-lookup"><span data-stu-id="b242f-135">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.ImportExportRequest</span></span>

## <span data-ttu-id="b242f-136">Note</span><span class="sxs-lookup"><span data-stu-id="b242f-136">NOTES</span></span>

## <span data-ttu-id="b242f-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b242f-137">RELATED LINKS</span></span>

[<span data-ttu-id="b242f-138">Database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="b242f-138">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="b242f-139">Esporta database</span><span class="sxs-lookup"><span data-stu-id="b242f-139">Export Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn781282.aspx)

[<span data-ttu-id="b242f-140">Operazioni per i database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="b242f-140">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="b242f-141">Get-AzureSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="b242f-141">Get-AzureSqlDatabaseImportExportStatus</span></span>](./Get-AzureSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="b242f-142">Start-AzureSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="b242f-142">Start-AzureSqlDatabaseImport</span></span>](./Start-AzureSqlDatabaseImport.md)


