---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabasefromfailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
ms.openlocfilehash: 556cece1b4fb22067918fb84dd1474c39d8c5aeb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961374"
---
# <span data-ttu-id="10318-101">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="10318-101">Remove-AzSqlDatabaseFromFailoverGroup</span></span>

## <span data-ttu-id="10318-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10318-102">SYNOPSIS</span></span>
<span data-ttu-id="10318-103">Rimuove uno o più database da un gruppo di failover SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="10318-103">Removes one or more databases from an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="10318-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="10318-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFromFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Force] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="10318-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="10318-105">DESCRIPTION</span></span>
<span data-ttu-id="10318-106">Rimuove uno o più database dal gruppo di failover del SQL azure specificato.</span><span class="sxs-lookup"><span data-stu-id="10318-106">Removes one or more databases from the specified Azure SQL Database Failover Group.</span></span> <span data-ttu-id="10318-107">I database e le relazioni di replica non vengono modificati, ma non saranno più accessibili tramite gli endpoint del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="10318-107">The databases and replication relationships are left intact, but they will no longer be accessible through the Failover Group endpoints.</span></span>
<span data-ttu-id="10318-108">Per ottenere oggetti di database con cui popolare il parametro '-Database', usare, ad esempio, il cmdlet Get-AzSqlDatabase database.</span><span class="sxs-lookup"><span data-stu-id="10318-108">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="10318-109">Per eseguire il comando, è necessario usare il server primario del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="10318-109">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="10318-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="10318-110">EXAMPLES</span></span>

### <span data-ttu-id="10318-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="10318-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Remove-AzSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="10318-112">Questo comando rimuove un database da un gruppo di failover tramite piping.</span><span class="sxs-lookup"><span data-stu-id="10318-112">This command removes one database from a Failover Group by piping it in.</span></span>

### <span data-ttu-id="10318-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="10318-113">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Remove-AzSqlDatabaseFromFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="10318-114">Questo comando rimuove tutti i database da un gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="10318-114">This command removes all databases from a Failover Group.</span></span>

### <span data-ttu-id="10318-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="10318-115">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Remove-AzSqlDatabaseFromFailoverGroup -Database $databases
```

<span data-ttu-id="10318-116">Questo comando rimuove tutti i database in un pool flessibile da un gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="10318-116">This command removes all databases in an Elastic Pool from a Failover Group.</span></span>

## <span data-ttu-id="10318-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10318-117">PARAMETERS</span></span>

### <span data-ttu-id="10318-118">-Database</span><span class="sxs-lookup"><span data-stu-id="10318-118">-Database</span></span>
<span data-ttu-id="10318-119">Uno o più database SQL Azure nel server primario del gruppo di failover da rimuovere dal gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="10318-119">One or more Azure SQL Databases on the Failover Group's primary server to be removed from the Failover Group.</span></span>

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

### <span data-ttu-id="10318-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10318-120">-DefaultProfile</span></span>
<span data-ttu-id="10318-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="10318-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10318-122">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="10318-122">-FailoverGroupName</span></span>
<span data-ttu-id="10318-123">Nome del gruppo di failover del database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="10318-123">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="10318-124">-Force</span><span class="sxs-lookup"><span data-stu-id="10318-124">-Force</span></span>
<span data-ttu-id="10318-125">Ignorare il messaggio di conferma per l'esecuzione dell'azione.</span><span class="sxs-lookup"><span data-stu-id="10318-125">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="10318-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10318-126">-ResourceGroupName</span></span>
<span data-ttu-id="10318-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="10318-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="10318-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="10318-128">-ServerName</span></span>
<span data-ttu-id="10318-129">Nome del server di database SQL Azure primario del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="10318-129">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="10318-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10318-130">-Confirm</span></span>
<span data-ttu-id="10318-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10318-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10318-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10318-132">-WhatIf</span></span>
<span data-ttu-id="10318-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="10318-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="10318-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="10318-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10318-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10318-135">CommonParameters</span></span>
<span data-ttu-id="10318-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10318-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10318-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="10318-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10318-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="10318-138">INPUTS</span></span>

### <span data-ttu-id="10318-139">System.String</span><span class="sxs-lookup"><span data-stu-id="10318-139">System.String</span></span>

### <span data-ttu-id="10318-140">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="10318-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="10318-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="10318-141">OUTPUTS</span></span>

### <span data-ttu-id="10318-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="10318-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="10318-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="10318-143">NOTES</span></span>

## <span data-ttu-id="10318-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="10318-144">RELATED LINKS</span></span>

[<span data-ttu-id="10318-145">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="10318-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="10318-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="10318-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="10318-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="10318-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="10318-148">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="10318-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="10318-149">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="10318-149">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="10318-150">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="10318-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="10318-151">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="10318-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
