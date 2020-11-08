---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 56026A74-A6DC-47A5-9643-5828C3D0E83B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 32219154f2036ee028b05a369c46be1d8e1def87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029755"
---
# <span data-ttu-id="19328-101">Get-AzureSqlDatabaseOperation</span><span class="sxs-lookup"><span data-stu-id="19328-101">Get-AzureSqlDatabaseOperation</span></span>

## <span data-ttu-id="19328-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="19328-102">SYNOPSIS</span></span>
<span data-ttu-id="19328-103">Ottiene lo stato delle operazioni di database in un server Azure.</span><span class="sxs-lookup"><span data-stu-id="19328-103">Gets the status of database operations on an Azure server.</span></span>

## <span data-ttu-id="19328-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="19328-104">SYNTAX</span></span>

### <span data-ttu-id="19328-105">ByConnectionContext (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="19328-105">ByConnectionContext (Default)</span></span>
```
Get-AzureSqlDatabaseOperation -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="19328-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="19328-106">ByServerName</span></span>
```
Get-AzureSqlDatabaseOperation -ServerName <String> [-Database <Database>] [-DatabaseName <String>]
 [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="19328-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19328-107">DESCRIPTION</span></span>
<span data-ttu-id="19328-108">Il cmdlet **Get-AzureSqlDatabaseOperation** ottiene lo stato delle operazioni di database nel server Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="19328-108">The **Get-AzureSqlDatabaseOperation** cmdlet gets the status of database operations on the specified Azure server.</span></span>
<span data-ttu-id="19328-109">Se specifichi solo il parametro *ServerName* o *ConnectionContext* , il cmdlet ottiene tutte le operazioni di database per il server.</span><span class="sxs-lookup"><span data-stu-id="19328-109">If you specify only the *ServerName* or *ConnectionContext* parameter, the cmdlet gets all the database operations for the server.</span></span>
<span data-ttu-id="19328-110">Se si specifica anche un database tramite il parametro *database* o *DatabaseName* , questo cmdlet ottiene tutte le operazioni per il database specificato.</span><span class="sxs-lookup"><span data-stu-id="19328-110">If you also specify a database by using the *Database* or *DatabaseName* parameter, this cmdlet gets all the operations for the specified database.</span></span>
<span data-ttu-id="19328-111">Se si specifica un GUID dell'operazione e *ServerName* o *ConnectionContext* , il cmdlet ottiene una singola operazione di database.</span><span class="sxs-lookup"><span data-stu-id="19328-111">If you specify an operation GUID, and *ServerName* or *ConnectionContext* , the cmdlet gets a single database operation.</span></span>

## <span data-ttu-id="19328-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="19328-112">EXAMPLES</span></span>

### <span data-ttu-id="19328-113">Esempio 1: ottenere lo stato di tutte le operazioni di database per un database</span><span class="sxs-lookup"><span data-stu-id="19328-113">Example 1: Get the status of all database operations for a database</span></span>
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context -DatabaseName "Database17"
```

<span data-ttu-id="19328-114">Questo comando consente di ottenere lo stato di tutte le operazioni di database nel database denominato Database17 nel server specificato dal contesto di connessione $Context.</span><span class="sxs-lookup"><span data-stu-id="19328-114">This command gets the status of all database operations on the database named Database17 on the server that the connection context $Context specifies.</span></span>

### <span data-ttu-id="19328-115">Esempio 2: ottenere lo stato di tutte le operazioni di database per un server</span><span class="sxs-lookup"><span data-stu-id="19328-115">Example 2: Get the status of all database operations for a server</span></span>
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context
```

<span data-ttu-id="19328-116">Questo comando consente di ottenere lo stato di tutte le operazioni di database nel server che il contesto di connessione $Context specifica.</span><span class="sxs-lookup"><span data-stu-id="19328-116">This command gets the status of all database operations on the server that the connection context $Context specifies.</span></span>

## <span data-ttu-id="19328-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="19328-117">PARAMETERS</span></span>

### <span data-ttu-id="19328-118">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="19328-118">-ConnectionContext</span></span>
<span data-ttu-id="19328-119">Specifica il contesto di connessione di un server.</span><span class="sxs-lookup"><span data-stu-id="19328-119">Specifies the connection context of a server.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19328-120">-Database</span><span class="sxs-lookup"><span data-stu-id="19328-120">-Database</span></span>
<span data-ttu-id="19328-121">Specifica un oggetto che rappresenta un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="19328-121">Specifies an object that represents an Azure SQL Database.</span></span>
<span data-ttu-id="19328-122">Se specifichi questo parametro, devi specificare il parametro *ServerName* o il parametro *ConnectionContext* .</span><span class="sxs-lookup"><span data-stu-id="19328-122">If you specify this parameter, you must specify the *ServerName* parameter or *ConnectionContext* parameter.</span></span>

```yaml
Type: Database
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19328-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="19328-123">-DatabaseName</span></span>
<span data-ttu-id="19328-124">Specifica il nome di un database.</span><span class="sxs-lookup"><span data-stu-id="19328-124">Specifies the name of a database.</span></span>
<span data-ttu-id="19328-125">Se specifichi questo parametro, devi specificare il parametro *ServerName* o il parametro *ConnectionContext* .</span><span class="sxs-lookup"><span data-stu-id="19328-125">If you specify this parameter, you must specify the *ServerName* parameter or the *ConnectionContext* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19328-126">-OperationGuid</span><span class="sxs-lookup"><span data-stu-id="19328-126">-OperationGuid</span></span>
<span data-ttu-id="19328-127">Specifica l'ID operazione che rappresenta un'operazione specifica del database per cui questo cmdlet ottiene lo stato.</span><span class="sxs-lookup"><span data-stu-id="19328-127">Specifies the operation ID that represents a specific database operation for which this cmdlet gets status.</span></span>
<span data-ttu-id="19328-128">Puoi ottenere gli ID operazione richiedendo tutte le operazioni di database per un server o un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="19328-128">You can obtain operation IDs by requesting all the database operations for a Azure SQL Database or server.</span></span>
<span data-ttu-id="19328-129">Se specifichi questo parametro, devi specificare il parametro *ServerName* o il parametro *ConnectionContext* .</span><span class="sxs-lookup"><span data-stu-id="19328-129">If you specify this parameter, you must specify the *ServerName* parameter or the *ConnectionContext* parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19328-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="19328-130">-Profile</span></span>
<span data-ttu-id="19328-131">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19328-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="19328-132">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="19328-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="19328-133">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="19328-133">-ServerName</span></span>
<span data-ttu-id="19328-134">Specifica il nome di un server.</span><span class="sxs-lookup"><span data-stu-id="19328-134">Specifies the name of a server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19328-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19328-135">CommonParameters</span></span>
<span data-ttu-id="19328-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19328-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19328-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19328-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19328-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="19328-138">INPUTS</span></span>

### <span data-ttu-id="19328-139">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. database</span><span class="sxs-lookup"><span data-stu-id="19328-139">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

### <span data-ttu-id="19328-140">Microsoft. WindowsAzure. Commands. SqlDatabase. Model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="19328-140">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

### <span data-ttu-id="19328-141">System. Guid</span><span class="sxs-lookup"><span data-stu-id="19328-141">System.Guid</span></span>

## <span data-ttu-id="19328-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="19328-142">OUTPUTS</span></span>

### <span data-ttu-id="19328-143">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. database. DatabaseOperationResponseList []</span><span class="sxs-lookup"><span data-stu-id="19328-143">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database.DatabaseOperationResponseList[]</span></span>
<span data-ttu-id="19328-144">Questo cmdlet restituisce una matrice di oggetti **DatabaseOperationResponseList** se si ottengono più operazioni.</span><span class="sxs-lookup"><span data-stu-id="19328-144">This cmdlet returns an array of **DatabaseOperationResponseList** objects if you get multiple operations.</span></span>

### <span data-ttu-id="19328-145">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. database. DatabaseOperationResponse</span><span class="sxs-lookup"><span data-stu-id="19328-145">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database.DatabaseOperationResponse</span></span>

## <span data-ttu-id="19328-146">Note</span><span class="sxs-lookup"><span data-stu-id="19328-146">NOTES</span></span>

## <span data-ttu-id="19328-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="19328-147">RELATED LINKS</span></span>

[<span data-ttu-id="19328-148">Database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="19328-148">Azure SQL Database</span></span>](https://msdn.microsoft.com/library/ee336279.aspx)

[<span data-ttu-id="19328-149">Stato operazione database</span><span class="sxs-lookup"><span data-stu-id="19328-149">Database Operation Status</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn720371.aspx)

[<span data-ttu-id="19328-150">Operazioni per i database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="19328-150">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="19328-151">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="19328-151">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="19328-152">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="19328-152">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


