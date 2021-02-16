---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqldatabasefailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
ms.openlocfilehash: e5cd2c2e6e903afd5afeafe2ca5fcdc70551e582
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201463"
---
# <span data-ttu-id="08613-101">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="08613-101">Invoke-AzSqlDatabaseFailover</span></span>

## <span data-ttu-id="08613-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08613-102">SYNOPSIS</span></span>
<span data-ttu-id="08613-103">Failover di un database.</span><span class="sxs-lookup"><span data-stu-id="08613-103">Failovers a database.</span></span>

## <span data-ttu-id="08613-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="08613-104">SYNTAX</span></span>

```
Invoke-AzSqlDatabaseFailover [-DatabaseName] <String> [-ReadableSecondary] [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08613-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="08613-105">DESCRIPTION</span></span>
<span data-ttu-id="08613-106">Il cmdlet Invoke-AzSqlDatabaseFailover failover di un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="08613-106">The Invoke-AzSqlDatabaseFailover cmdlet failovers an Azure SQL database.</span></span> <span data-ttu-id="08613-107">Se il database si trova in un pool flessibile, questo comando failoverrà il database specificato senza influire sugli altri database nello stesso pool flessibile.</span><span class="sxs-lookup"><span data-stu-id="08613-107">If the database is in an elastic pool, this command will failover the given database without affecting the other databases in the same elastic pool.</span></span>

## <span data-ttu-id="08613-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="08613-108">EXAMPLES</span></span>

### <span data-ttu-id="08613-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="08613-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="08613-110">Questo comando failoverrà la replica primaria del database denominato "Database01" nel server denominato "Server01"</span><span class="sxs-lookup"><span data-stu-id="08613-110">This command will failover the primary replica of the database named "Database01" on the server named "Server01"</span></span>

### <span data-ttu-id="08613-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="08613-111">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -ReadableSecondary
```

<span data-ttu-id="08613-112">Questo comando failoverrà la replica secondaria leggibile del database denominato "Database01" nel server denominato "Server01"</span><span class="sxs-lookup"><span data-stu-id="08613-112">This command will failover the readable secondary replica of the database named "Database01" on the server named "Server01"</span></span>

## <span data-ttu-id="08613-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08613-113">PARAMETERS</span></span>

### <span data-ttu-id="08613-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08613-114">-AsJob</span></span>
<span data-ttu-id="08613-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="08613-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="08613-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="08613-116">-DatabaseName</span></span>
<span data-ttu-id="08613-117">Il nome del database SQL Azure per il failover.</span><span class="sxs-lookup"><span data-stu-id="08613-117">The name of the Azure SQL Database to failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08613-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08613-118">-DefaultProfile</span></span>
<span data-ttu-id="08613-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="08613-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08613-120">-Force</span><span class="sxs-lookup"><span data-stu-id="08613-120">-Force</span></span>
<span data-ttu-id="08613-121">Ignora messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="08613-121">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="08613-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08613-122">-PassThru</span></span>
<span data-ttu-id="08613-123">Se l'esecuzione riesce, restituisce true.</span><span class="sxs-lookup"><span data-stu-id="08613-123">On Successful execution, returns true.</span></span>  <span data-ttu-id="08613-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="08613-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="08613-125">-ReadableSecondary</span><span class="sxs-lookup"><span data-stu-id="08613-125">-ReadableSecondary</span></span>
<span data-ttu-id="08613-126">Eseguire il failover della replica secondaria leggibile anziché della replica primaria predefinita</span><span class="sxs-lookup"><span data-stu-id="08613-126">Failover the readable secondary replica instead of the default primary replica</span></span>

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

### <span data-ttu-id="08613-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08613-127">-ResourceGroupName</span></span>
<span data-ttu-id="08613-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="08613-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="08613-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="08613-129">-ServerName</span></span>
<span data-ttu-id="08613-130">Nome del server di SQL Azure in cui si trova il database.</span><span class="sxs-lookup"><span data-stu-id="08613-130">The name of the Azure SQL Database Server the database is in.</span></span>

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

### <span data-ttu-id="08613-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="08613-131">-Confirm</span></span>
<span data-ttu-id="08613-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08613-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08613-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08613-133">-WhatIf</span></span>
<span data-ttu-id="08613-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="08613-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="08613-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="08613-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08613-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08613-136">CommonParameters</span></span>
<span data-ttu-id="08613-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08613-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08613-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="08613-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08613-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="08613-139">INPUTS</span></span>

### <span data-ttu-id="08613-140">System.String</span><span class="sxs-lookup"><span data-stu-id="08613-140">System.String</span></span>

## <span data-ttu-id="08613-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="08613-141">OUTPUTS</span></span>

## <span data-ttu-id="08613-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="08613-142">NOTES</span></span>

## <span data-ttu-id="08613-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="08613-143">RELATED LINKS</span></span>

[<span data-ttu-id="08613-144">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="08613-144">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="08613-145">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="08613-145">Invoke-AzSqlElasticPoolFailover</span></span>](./Invoke-AzSqlElasticPoolFailover.md)

[<span data-ttu-id="08613-146">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="08613-146">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="08613-147">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="08613-147">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="08613-148">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="08613-148">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="08613-149">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="08613-149">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="08613-150">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="08613-150">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="08613-151">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="08613-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
