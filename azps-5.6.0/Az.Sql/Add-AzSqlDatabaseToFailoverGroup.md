---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/add-azsqldatabasetofailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
ms.openlocfilehash: 5c06c8e95d85e6a2b9f7c8449859edd94d9568b0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961549"
---
# <span data-ttu-id="39cb6-101">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="39cb6-101">Add-AzSqlDatabaseToFailoverGroup</span></span>

## <span data-ttu-id="39cb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39cb6-102">SYNOPSIS</span></span>
<span data-ttu-id="39cb6-103">Aggiunge uno o più database a un gruppo di failover SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="39cb6-103">Adds one or more databases to an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="39cb6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39cb6-104">SYNTAX</span></span>

```
Add-AzSqlDatabaseToFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39cb6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="39cb6-105">DESCRIPTION</span></span>
<span data-ttu-id="39cb6-106">Aggiunge uno o più database in un server SQL di failover del database di Azure a tale gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="39cb6-106">Adds one or more databases on a Azure SQL Database Failover Group's primary server to that Failover Group.</span></span> <span data-ttu-id="39cb6-107">I database non devono essere database secondari nelle relazioni di replica esistenti.</span><span class="sxs-lookup"><span data-stu-id="39cb6-107">The databases must not be secondary databases in existing replication relationships.</span></span> <span data-ttu-id="39cb6-108">Il comando avvia la replica geografica di tutti i database aggiunti al server secondario del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="39cb6-108">The command will start geo-replication of any added databases to the Failover Group's secondary server.</span></span>
<span data-ttu-id="39cb6-109">Per ottenere oggetti di database con cui popolare il parametro '-Database', usare, ad esempio, il cmdlet Get-AzSqlDatabase database.</span><span class="sxs-lookup"><span data-stu-id="39cb6-109">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="39cb6-110">Per eseguire il comando, è necessario usare il server primario del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="39cb6-110">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="39cb6-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39cb6-111">EXAMPLES</span></span>

### <span data-ttu-id="39cb6-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="39cb6-112">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Add-AzSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="39cb6-113">Questo comando aggiunge un database a un gruppo di failover tramite piping.</span><span class="sxs-lookup"><span data-stu-id="39cb6-113">This command adds one database to a Failover Group by piping it in.</span></span>

### <span data-ttu-id="39cb6-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="39cb6-114">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Add-AzSqlDatabaseToFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="39cb6-115">Questo comando aggiunge tutti i database di un server a un gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="39cb6-115">This command adds all databases in a server to a Failover Group.</span></span>

### <span data-ttu-id="39cb6-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="39cb6-116">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Add-AzSqlDatabaseToFailoverGroup -Database $databases
```

<span data-ttu-id="39cb6-117">Questo comando aggiunge tutti i database di un pool elastico a un gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="39cb6-117">This command adds all databases in an Elastic Pool to a Failover Group.</span></span>

## <span data-ttu-id="39cb6-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39cb6-118">PARAMETERS</span></span>

### <span data-ttu-id="39cb6-119">-Database</span><span class="sxs-lookup"><span data-stu-id="39cb6-119">-Database</span></span>
<span data-ttu-id="39cb6-120">Uno o più database SQL Azure nel server primario del gruppo di failover da aggiungere al gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="39cb6-120">One or more Azure SQL Databases on the Failover Group's primary server to be added to the Failover Group.</span></span>

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

### <span data-ttu-id="39cb6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39cb6-121">-DefaultProfile</span></span>
<span data-ttu-id="39cb6-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="39cb6-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="39cb6-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="39cb6-123">-FailoverGroupName</span></span>
<span data-ttu-id="39cb6-124">Nome del gruppo di failover del database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="39cb6-124">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="39cb6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39cb6-125">-ResourceGroupName</span></span>
<span data-ttu-id="39cb6-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="39cb6-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="39cb6-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="39cb6-127">-ServerName</span></span>
<span data-ttu-id="39cb6-128">Nome del server di database SQL Azure primario del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="39cb6-128">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="39cb6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39cb6-129">CommonParameters</span></span>
<span data-ttu-id="39cb6-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39cb6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39cb6-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="39cb6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39cb6-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="39cb6-132">INPUTS</span></span>

### <span data-ttu-id="39cb6-133">System.String</span><span class="sxs-lookup"><span data-stu-id="39cb6-133">System.String</span></span>

### <span data-ttu-id="39cb6-134">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="39cb6-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="39cb6-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39cb6-135">OUTPUTS</span></span>

### <span data-ttu-id="39cb6-136">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="39cb6-136">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="39cb6-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="39cb6-137">NOTES</span></span>

## <span data-ttu-id="39cb6-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39cb6-138">RELATED LINKS</span></span>

[<span data-ttu-id="39cb6-139">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="39cb6-139">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="39cb6-140">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="39cb6-140">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="39cb6-141">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="39cb6-141">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="39cb6-142">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="39cb6-142">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="39cb6-143">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="39cb6-143">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="39cb6-144">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="39cb6-144">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="39cb6-145">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="39cb6-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
