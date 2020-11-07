---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasefromfailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
ms.openlocfilehash: 4a39cd97936ef72615e30072de1988304fc5ad09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93856809"
---
# <span data-ttu-id="2d80f-101">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="2d80f-101">Remove-AzSqlDatabaseFromFailoverGroup</span></span>

## <span data-ttu-id="2d80f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2d80f-102">SYNOPSIS</span></span>
<span data-ttu-id="2d80f-103">Rimuove uno o più database da un gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d80f-103">Removes one or more databases from an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="2d80f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2d80f-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFromFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Force] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2d80f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d80f-105">DESCRIPTION</span></span>
<span data-ttu-id="2d80f-106">Rimuove uno o più database dal gruppo di failover di database SQL di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="2d80f-106">Removes one or more databases from the specified Azure SQL Database Failover Group.</span></span> <span data-ttu-id="2d80f-107">I database e le relazioni di replica rimangono intatti, ma non saranno più accessibili tramite gli endpoint del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="2d80f-107">The databases and replication relationships are left intact, but they will no longer be accessible through the Failover Group endpoints.</span></span>
<span data-ttu-id="2d80f-108">Per ottenere gli oggetti di database con cui inserire il parametro "-database", usare (ad esempio) il cmdlet Get-AzSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="2d80f-108">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="2d80f-109">Il server principale del gruppo di failover deve essere usato per eseguire il comando.</span><span class="sxs-lookup"><span data-stu-id="2d80f-109">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="2d80f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2d80f-110">EXAMPLES</span></span>

### <span data-ttu-id="2d80f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2d80f-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Remove-AzSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="2d80f-112">Questo comando rimuove un database da un gruppo di failover eseguendo il piping.</span><span class="sxs-lookup"><span data-stu-id="2d80f-112">This command removes one database from a Failover Group by piping it in.</span></span>

### <span data-ttu-id="2d80f-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2d80f-113">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Remove-AzSqlDatabaseFromFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="2d80f-114">Questo comando rimuove tutti i database da un gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="2d80f-114">This command removes all databases from a Failover Group.</span></span>

### <span data-ttu-id="2d80f-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="2d80f-115">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Remove-AzSqlDatabaseFromFailoverGroup -Database $databases
```

<span data-ttu-id="2d80f-116">Questo comando rimuove tutti i database in un pool elastico da un gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="2d80f-116">This command removes all databases in an Elastic Pool from a Failover Group.</span></span>

## <span data-ttu-id="2d80f-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2d80f-117">PARAMETERS</span></span>

### <span data-ttu-id="2d80f-118">-Database</span><span class="sxs-lookup"><span data-stu-id="2d80f-118">-Database</span></span>
<span data-ttu-id="2d80f-119">Uno o più database SQL di Azure nel server principale del gruppo di failover da rimuovere dal gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="2d80f-119">One or more Azure SQL Databases on the Failover Group's primary server to be removed from the Failover Group.</span></span>

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

### <span data-ttu-id="2d80f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d80f-120">-DefaultProfile</span></span>
<span data-ttu-id="2d80f-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2d80f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d80f-122">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="2d80f-122">-FailoverGroupName</span></span>
<span data-ttu-id="2d80f-123">Nome del gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d80f-123">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="2d80f-124">-Force</span><span class="sxs-lookup"><span data-stu-id="2d80f-124">-Force</span></span>
<span data-ttu-id="2d80f-125">Ignorare il messaggio di conferma per l'esecuzione dell'azione.</span><span class="sxs-lookup"><span data-stu-id="2d80f-125">Skip confirmation message for performing the action.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d80f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d80f-126">-ResourceGroupName</span></span>
<span data-ttu-id="2d80f-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2d80f-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="2d80f-128">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="2d80f-128">-ServerName</span></span>
<span data-ttu-id="2d80f-129">Nome del server di database SQL di Azure principale del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="2d80f-129">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="2d80f-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2d80f-130">-Confirm</span></span>
<span data-ttu-id="2d80f-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d80f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d80f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d80f-132">-WhatIf</span></span>
<span data-ttu-id="2d80f-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2d80f-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d80f-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2d80f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d80f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d80f-135">CommonParameters</span></span>
<span data-ttu-id="2d80f-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d80f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d80f-137">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d80f-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d80f-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2d80f-138">INPUTS</span></span>

### <span data-ttu-id="2d80f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2d80f-139">System.String</span></span>

### <span data-ttu-id="2d80f-140">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel, Microsoft. Azure. PowerShell. cmdlet. SQL, Version = 1.3.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2d80f-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2d80f-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2d80f-141">OUTPUTS</span></span>

### <span data-ttu-id="2d80f-142">Microsoft. Azure. Commands. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="2d80f-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="2d80f-143">Note</span><span class="sxs-lookup"><span data-stu-id="2d80f-143">NOTES</span></span>

## <span data-ttu-id="2d80f-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2d80f-144">RELATED LINKS</span></span>

[<span data-ttu-id="2d80f-145">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="2d80f-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="2d80f-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="2d80f-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="2d80f-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="2d80f-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="2d80f-148">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="2d80f-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="2d80f-149">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="2d80f-149">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="2d80f-150">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="2d80f-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="2d80f-151">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="2d80f-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
