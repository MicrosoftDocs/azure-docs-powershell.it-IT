---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasefromfailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFromFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFromFailoverGroup.md
ms.openlocfilehash: ba0203b328b1ae75b1f671ed3e9437a47657bb1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519836"
---
# <span data-ttu-id="a3b9b-101">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a3b9b-101">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>

## <span data-ttu-id="a3b9b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a3b9b-102">SYNOPSIS</span></span>
<span data-ttu-id="a3b9b-103">Rimuove uno o più database da un gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="a3b9b-103">Removes one or more databases from an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3b9b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a3b9b-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseFromFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Force] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a3b9b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3b9b-105">DESCRIPTION</span></span>
<span data-ttu-id="a3b9b-106">Rimuove uno o più database dal gruppo di failover di database SQL di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="a3b9b-106">Removes one or more databases from the specified Azure SQL Database Failover Group.</span></span> <span data-ttu-id="a3b9b-107">I database e le relazioni di replica rimangono intatti, ma non saranno più accessibili tramite gli endpoint del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="a3b9b-107">The databases and replication relationships are left intact, but they will no longer be accessible through the Failover Group endpoints.</span></span>

<span data-ttu-id="a3b9b-108">Per ottenere gli oggetti di database con cui inserire il parametro "-database", usare (ad esempio) il cmdlet Get-AzureRmSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="a3b9b-108">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzureRmSqlDatabase cmdlet.</span></span>

<span data-ttu-id="a3b9b-109">Il server principale del gruppo di failover deve essere usato per eseguire il comando.</span><span class="sxs-lookup"><span data-stu-id="a3b9b-109">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="a3b9b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a3b9b-110">EXAMPLES</span></span>

### <span data-ttu-id="a3b9b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a3b9b-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="a3b9b-112">Questo comando rimuove un database da un gruppo di failover eseguendo il piping.</span><span class="sxs-lookup"><span data-stu-id="a3b9b-112">This command removes one database from a Failover Group by piping it in.</span></span>

### <span data-ttu-id="a3b9b-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a3b9b-113">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzureRmSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Remove-AzureRmSqlDatabaseFromFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzureRmSqlDatabase)
```

<span data-ttu-id="a3b9b-114">Questo comando rimuove tutti i database da un gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="a3b9b-114">This command removes all databases from a Failover Group.</span></span>

### <span data-ttu-id="a3b9b-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="a3b9b-115">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Remove-AzureRMSqlDatabaseFromFailoverGroup -Database $databases
```

<span data-ttu-id="a3b9b-116">Questo comando rimuove tutti i database in un pool elastico da un gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="a3b9b-116">This command removes all databases in an Elastic Pool from a Failover Group.</span></span>

## <span data-ttu-id="a3b9b-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a3b9b-117">PARAMETERS</span></span>

### <span data-ttu-id="a3b9b-118">-Database</span><span class="sxs-lookup"><span data-stu-id="a3b9b-118">-Database</span></span>
<span data-ttu-id="a3b9b-119">Uno o più database SQL di Azure nel server principale del gruppo di failover da rimuovere dal gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="a3b9b-119">One or more Azure SQL Databases on the Failover Group's primary server to be removed from the Failover Group.</span></span>

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

### <span data-ttu-id="a3b9b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3b9b-120">-DefaultProfile</span></span>
<span data-ttu-id="a3b9b-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a3b9b-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3b9b-122">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="a3b9b-122">-FailoverGroupName</span></span>
<span data-ttu-id="a3b9b-123">Nome del gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="a3b9b-123">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="a3b9b-124">-Force</span><span class="sxs-lookup"><span data-stu-id="a3b9b-124">-Force</span></span>
<span data-ttu-id="a3b9b-125">Ignorare il messaggio di conferma per l'esecuzione dell'azione.</span><span class="sxs-lookup"><span data-stu-id="a3b9b-125">Skip confirmation message for performing the action.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b9b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3b9b-126">-ResourceGroupName</span></span>
<span data-ttu-id="a3b9b-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a3b9b-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="a3b9b-128">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="a3b9b-128">-ServerName</span></span>
<span data-ttu-id="a3b9b-129">Nome del server di database SQL di Azure principale del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="a3b9b-129">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="a3b9b-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a3b9b-130">-Confirm</span></span>
<span data-ttu-id="a3b9b-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3b9b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3b9b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3b9b-132">-WhatIf</span></span>
<span data-ttu-id="a3b9b-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a3b9b-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a3b9b-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a3b9b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3b9b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3b9b-135">CommonParameters</span></span>
<span data-ttu-id="a3b9b-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3b9b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3b9b-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3b9b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3b9b-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a3b9b-138">INPUTS</span></span>

### <span data-ttu-id="a3b9b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a3b9b-139">System.String</span></span>
<span data-ttu-id="a3b9b-140">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel, Microsoft. Azure. Commands. SQL, Version = 2.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a3b9b-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.Commands.Sql, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a3b9b-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a3b9b-141">OUTPUTS</span></span>

### <span data-ttu-id="a3b9b-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="a3b9b-142">System.Object</span></span>

## <span data-ttu-id="a3b9b-143">Note</span><span class="sxs-lookup"><span data-stu-id="a3b9b-143">NOTES</span></span>

## <span data-ttu-id="a3b9b-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a3b9b-144">RELATED LINKS</span></span>

[<span data-ttu-id="a3b9b-145">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a3b9b-145">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a3b9b-146">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a3b9b-146">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a3b9b-147">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a3b9b-147">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a3b9b-148">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a3b9b-148">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="a3b9b-149">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a3b9b-149">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a3b9b-150">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="a3b9b-150">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="a3b9b-151">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="a3b9b-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
