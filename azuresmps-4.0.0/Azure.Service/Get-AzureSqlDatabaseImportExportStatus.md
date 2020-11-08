---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 4661C479-6E3B-425D-B9D2-B36D7A83130C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3c55ebd22337a8078f3ae495b3901317f4201e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029756"
---
# <span data-ttu-id="4abd3-101">Get-AzureSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="4abd3-101">Get-AzureSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="4abd3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4abd3-102">SYNOPSIS</span></span>
<span data-ttu-id="4abd3-103">Ottiene lo stato di una richiesta di importazione o esportazione.</span><span class="sxs-lookup"><span data-stu-id="4abd3-103">Gets the status of an import or export request.</span></span>

## <span data-ttu-id="4abd3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4abd3-104">SYNTAX</span></span>

### <span data-ttu-id="4abd3-105">ByConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="4abd3-105">ByConnectionInfo</span></span>
```
Get-AzureSqlDatabaseImportExportStatus -Username <String> -Password <String> -ServerName <String>
 -RequestId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4abd3-106">ByRequestObject</span><span class="sxs-lookup"><span data-stu-id="4abd3-106">ByRequestObject</span></span>
```
Get-AzureSqlDatabaseImportExportStatus -Request <ImportExportRequest> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="4abd3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4abd3-107">DESCRIPTION</span></span>
<span data-ttu-id="4abd3-108">Il cmdlet **Get-AzureSqlDatabaseImportExportStatus** ottiene lo stato di una richiesta di importazione o esportazione.</span><span class="sxs-lookup"><span data-stu-id="4abd3-108">The **Get-AzureSqlDatabaseImportExportStatus** cmdlet gets the status of an import or export request.</span></span>
<span data-ttu-id="4abd3-109">Il cmdlet Start-AzureSqlDatabaseImport o Start-AzureSqlDatabaseExport avvia le richieste.</span><span class="sxs-lookup"><span data-stu-id="4abd3-109">The Start-AzureSqlDatabaseImport or Start-AzureSqlDatabaseExport cmdlet initiates requests.</span></span>
<span data-ttu-id="4abd3-110">Puoi specificare l'oggetto Request usando il parametro *Request* oppure puoi identificare la richiesta usando il parametro *RequestId* e i parametri *username* , *password* e *ServerName* .</span><span class="sxs-lookup"><span data-stu-id="4abd3-110">You can specify the request object by using the *Request* parameter, or you can identify the request by using the *RequestId* parameter and the *Username* , *Password* , and *ServerName* parameters.</span></span>

## <span data-ttu-id="4abd3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4abd3-111">EXAMPLES</span></span>

### <span data-ttu-id="4abd3-112">Esempio 1: ottenere lo stato di una richiesta di esportazione</span><span class="sxs-lookup"><span data-stu-id="4abd3-112">Example 1: Get the status of an export request</span></span>
```
PS C:\> $ExportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
PS C:\> Get-AzureSqlDatabaseImportExportStatus -Request $ExportRequest
```

<span data-ttu-id="4abd3-113">Il primo comando crea una richiesta di esportazione e la archivia nella variabile $ExportRequest.</span><span class="sxs-lookup"><span data-stu-id="4abd3-113">The first command creates an export request, and then stores it in the $ExportRequest variable.</span></span>

<span data-ttu-id="4abd3-114">Il secondo comando ottiene lo stato della richiesta di esportazione archiviata in $ExportRequest.</span><span class="sxs-lookup"><span data-stu-id="4abd3-114">The second command gets the status of the export request stored in $ExportRequest.</span></span>

## <span data-ttu-id="4abd3-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4abd3-115">PARAMETERS</span></span>

### <span data-ttu-id="4abd3-116">-Password</span><span class="sxs-lookup"><span data-stu-id="4abd3-116">-Password</span></span>
<span data-ttu-id="4abd3-117">Specifica la password necessaria per connettersi al server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4abd3-117">Specifies the password that is required to connect to the Azure SQL Database server.</span></span>
<span data-ttu-id="4abd3-118">Devi specificare questo parametro se hai specificato il parametro *RequestId* .</span><span class="sxs-lookup"><span data-stu-id="4abd3-118">You must specify this parameter if you specified the *RequestId* parameter.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4abd3-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="4abd3-119">-Profile</span></span>
<span data-ttu-id="4abd3-120">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4abd3-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4abd3-121">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="4abd3-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4abd3-122">-Request</span><span class="sxs-lookup"><span data-stu-id="4abd3-122">-Request</span></span>
<span data-ttu-id="4abd3-123">Specifica un oggetto **ImportExportRequest** .</span><span class="sxs-lookup"><span data-stu-id="4abd3-123">Specifies an **ImportExportRequest** object.</span></span>
<span data-ttu-id="4abd3-124">Per ottenere un oggetto di richiesta di importazione o esportazione, usare il cmdlet Start-AzureSqlDatabaseImport o Start-AzureSqlDatabaseExport.</span><span class="sxs-lookup"><span data-stu-id="4abd3-124">To obtain an import or export request object, use the Start-AzureSqlDatabaseImport or Start-AzureSqlDatabaseExport cmdlet.</span></span>

```yaml
Type: ImportExportRequest
Parameter Sets: ByRequestObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4abd3-125">-RequestId</span><span class="sxs-lookup"><span data-stu-id="4abd3-125">-RequestId</span></span>
<span data-ttu-id="4abd3-126">Specifica il GUID dell'operazione di importazione o esportazione per cui questo cmdlet ottiene lo stato.</span><span class="sxs-lookup"><span data-stu-id="4abd3-126">Specifies the GUID of the import or export operation for which this cmdlet gets status.</span></span>
<span data-ttu-id="4abd3-127">Se specifichi questo parametro, devi specificare il *nome utente* , la *password* e i parametri *ServerName* .</span><span class="sxs-lookup"><span data-stu-id="4abd3-127">If you specify this parameter, you must specify the *UserName* , *Password* , and *ServerName* parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4abd3-128">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="4abd3-128">-ServerName</span></span>
<span data-ttu-id="4abd3-129">Specifica il nome del server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4abd3-129">Specifies the name of the Azure SQL Database server.</span></span>
<span data-ttu-id="4abd3-130">Devi specificare questo parametro se hai specificato il parametro *RequestId* .</span><span class="sxs-lookup"><span data-stu-id="4abd3-130">You must specify this parameter if you specified the *RequestId* parameter.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4abd3-131">-Username</span><span class="sxs-lookup"><span data-stu-id="4abd3-131">-Username</span></span>
<span data-ttu-id="4abd3-132">Specifica il nome utente necessario per connettersi al server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4abd3-132">Specifies the user name required to connect to the Azure SQL Database server.</span></span>
<span data-ttu-id="4abd3-133">Devi specificare questo parametro se hai specificato il parametro *RequestId* .</span><span class="sxs-lookup"><span data-stu-id="4abd3-133">You must specify this parameter if you specified the *RequestId* parameter.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4abd3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4abd3-134">CommonParameters</span></span>
<span data-ttu-id="4abd3-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4abd3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4abd3-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4abd3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4abd3-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4abd3-137">INPUTS</span></span>

## <span data-ttu-id="4abd3-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4abd3-138">OUTPUTS</span></span>

### <span data-ttu-id="4abd3-139">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. ImportExport. StatusInfo</span><span class="sxs-lookup"><span data-stu-id="4abd3-139">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.ImportExport.StatusInfo</span></span>

## <span data-ttu-id="4abd3-140">Note</span><span class="sxs-lookup"><span data-stu-id="4abd3-140">NOTES</span></span>

## <span data-ttu-id="4abd3-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4abd3-141">RELATED LINKS</span></span>

[<span data-ttu-id="4abd3-142">Database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="4abd3-142">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="4abd3-143">Ottenere lo stato Import Export database</span><span class="sxs-lookup"><span data-stu-id="4abd3-143">Get Import Export Database Status</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn781289.aspx)

[<span data-ttu-id="4abd3-144">Operazioni per i database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="4abd3-144">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="4abd3-145">Start-AzureSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="4abd3-145">Start-AzureSqlDatabaseExport</span></span>](./Start-AzureSqlDatabaseExport.md)

[<span data-ttu-id="4abd3-146">Start-AzureSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="4abd3-146">Start-AzureSqlDatabaseImport</span></span>](./Start-AzureSqlDatabaseImport.md)


