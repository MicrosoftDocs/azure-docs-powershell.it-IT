---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqldatabasetofailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
ms.openlocfilehash: aaf2063d82e0140e9abe07b7343a2c314e2fbd7f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677042"
---
# <span data-ttu-id="41ac4-101">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="41ac4-101">Add-AzSqlDatabaseToFailoverGroup</span></span>

## <span data-ttu-id="41ac4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="41ac4-102">SYNOPSIS</span></span>
<span data-ttu-id="41ac4-103">Aggiunge uno o più database a un gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="41ac4-103">Adds one or more databases to an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="41ac4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="41ac4-104">SYNTAX</span></span>

```
Add-AzSqlDatabaseToFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41ac4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41ac4-105">DESCRIPTION</span></span>
<span data-ttu-id="41ac4-106">Aggiunge uno o più database in un server primario di Azure SQL database per il gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="41ac4-106">Adds one or more databases on a Azure SQL Database Failover Group's primary server to that Failover Group.</span></span> <span data-ttu-id="41ac4-107">I database non devono essere database secondari nelle relazioni di replica esistenti.</span><span class="sxs-lookup"><span data-stu-id="41ac4-107">The databases must not be secondary databases in existing replication relationships.</span></span> <span data-ttu-id="41ac4-108">Il comando avvierà la Geo-replicazione di qualsiasi database aggiunto al server secondario del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="41ac4-108">The command will start geo-replication of any added databases to the Failover Group's secondary server.</span></span>
<span data-ttu-id="41ac4-109">Per ottenere gli oggetti di database con cui inserire il parametro "-database", usare (ad esempio) il cmdlet Get-AzSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="41ac4-109">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="41ac4-110">Il server principale del gruppo di failover deve essere usato per eseguire il comando.</span><span class="sxs-lookup"><span data-stu-id="41ac4-110">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="41ac4-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="41ac4-111">EXAMPLES</span></span>

### <span data-ttu-id="41ac4-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="41ac4-112">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Add-AzSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="41ac4-113">Questo comando aggiunge un database a un gruppo di failover eseguendo il piping.</span><span class="sxs-lookup"><span data-stu-id="41ac4-113">This command adds one database to a Failover Group by piping it in.</span></span>

### <span data-ttu-id="41ac4-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="41ac4-114">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Add-AzSqlDatabaseToFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="41ac4-115">Questo comando aggiunge tutti i database di un server a un gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="41ac4-115">This command adds all databases in a server to a Failover Group.</span></span>

### <span data-ttu-id="41ac4-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="41ac4-116">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Add-AzSqlDatabaseToFailoverGroup -Database $databases
```

<span data-ttu-id="41ac4-117">Questo comando aggiunge tutti i database in un pool elastico a un gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="41ac4-117">This command adds all databases in an Elastic Pool to a Failover Group.</span></span>

## <span data-ttu-id="41ac4-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="41ac4-118">PARAMETERS</span></span>

### <span data-ttu-id="41ac4-119">-Database</span><span class="sxs-lookup"><span data-stu-id="41ac4-119">-Database</span></span>
<span data-ttu-id="41ac4-120">Uno o più database SQL di Azure nel server principale del gruppo di failover da aggiungere al gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="41ac4-120">One or more Azure SQL Databases on the Failover Group's primary server to be added to the Failover Group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41ac4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41ac4-121">-DefaultProfile</span></span>
<span data-ttu-id="41ac4-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="41ac4-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41ac4-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="41ac4-123">-FailoverGroupName</span></span>
<span data-ttu-id="41ac4-124">Nome del gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="41ac4-124">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="41ac4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41ac4-125">-ResourceGroupName</span></span>
<span data-ttu-id="41ac4-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="41ac4-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="41ac4-127">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="41ac4-127">-ServerName</span></span>
<span data-ttu-id="41ac4-128">Nome del server di database SQL di Azure principale del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="41ac4-128">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="41ac4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41ac4-129">CommonParameters</span></span>
<span data-ttu-id="41ac4-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41ac4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41ac4-131">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41ac4-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41ac4-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="41ac4-132">INPUTS</span></span>

### <span data-ttu-id="41ac4-133">System. String</span><span class="sxs-lookup"><span data-stu-id="41ac4-133">System.String</span></span>

### <span data-ttu-id="41ac4-134">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel, Microsoft. Azure. PowerShell. cmdlet. SQL, Version = 1.3.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="41ac4-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="41ac4-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="41ac4-135">OUTPUTS</span></span>

### <span data-ttu-id="41ac4-136">Microsoft. Azure. Commands. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="41ac4-136">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="41ac4-137">Note</span><span class="sxs-lookup"><span data-stu-id="41ac4-137">NOTES</span></span>

## <span data-ttu-id="41ac4-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="41ac4-138">RELATED LINKS</span></span>

[<span data-ttu-id="41ac4-139">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="41ac4-139">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="41ac4-140">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="41ac4-140">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="41ac4-141">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="41ac4-141">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="41ac4-142">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="41ac4-142">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="41ac4-143">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="41ac4-143">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="41ac4-144">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="41ac4-144">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="41ac4-145">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="41ac4-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)