---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/invoke-azsqlelasticpoolfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
ms.openlocfilehash: 0af12c967dbbc65b37619ed837da1b8f778ab1db
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977741"
---
# <span data-ttu-id="e8a17-101">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="e8a17-101">Invoke-AzSqlElasticPoolFailover</span></span>

## <span data-ttu-id="e8a17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8a17-102">SYNOPSIS</span></span>
<span data-ttu-id="e8a17-103">Failover di un pool flessibile.</span><span class="sxs-lookup"><span data-stu-id="e8a17-103">Failovers an elastic pool.</span></span>

## <span data-ttu-id="e8a17-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8a17-104">SYNTAX</span></span>

```
Invoke-AzSqlElasticPoolFailover [-ElasticPoolName] <String> [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8a17-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e8a17-105">DESCRIPTION</span></span>
<span data-ttu-id="e8a17-106">Il Invoke-AzSqlElasticPoolFailover cmdlet failover di un pool flessibile.</span><span class="sxs-lookup"><span data-stu-id="e8a17-106">The Invoke-AzSqlElasticPoolFailover cmdlet failovers an elastic pool.</span></span> <span data-ttu-id="e8a17-107">Il failover si verificherà in tutti i database nel pool elastico dopo l'esecuzione di questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8a17-107">Failover will occur on all databases in the elastic pool after running this cmdlet.</span></span>

## <span data-ttu-id="e8a17-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8a17-108">EXAMPLES</span></span>

### <span data-ttu-id="e8a17-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e8a17-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlElasticPoolFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="e8a17-110">Questo comando failoverrà il pool elastico denominato "ElasticPool01" nel server denominato "Server01".</span><span class="sxs-lookup"><span data-stu-id="e8a17-110">This command will failover the elastic pool named "ElasticPool01" on the server named "Server01".</span></span>  <span data-ttu-id="e8a17-111">Questo significa che il failover si verificherà in tutti i database nel pool elastico denominato "ElasticPool01".</span><span class="sxs-lookup"><span data-stu-id="e8a17-111">This means failover will occur on all databases in the elastic pool named "ElasticPool01".</span></span>

## <span data-ttu-id="e8a17-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8a17-112">PARAMETERS</span></span>

### <span data-ttu-id="e8a17-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8a17-113">-AsJob</span></span>
<span data-ttu-id="e8a17-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e8a17-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e8a17-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8a17-115">-DefaultProfile</span></span>
<span data-ttu-id="e8a17-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e8a17-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8a17-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="e8a17-117">-ElasticPoolName</span></span>
<span data-ttu-id="e8a17-118">Nome del pool SQL Azure da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="e8a17-118">The name of the Azure SQL Elastic Pool to remove.</span></span>

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

### <span data-ttu-id="e8a17-119">-Force</span><span class="sxs-lookup"><span data-stu-id="e8a17-119">-Force</span></span>
<span data-ttu-id="e8a17-120">Ignora messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="e8a17-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="e8a17-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8a17-121">-PassThru</span></span>
<span data-ttu-id="e8a17-122">In caso di esecuzione riuscita, restituisce true.</span><span class="sxs-lookup"><span data-stu-id="e8a17-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="e8a17-123">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="e8a17-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e8a17-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8a17-124">-ResourceGroupName</span></span>
<span data-ttu-id="e8a17-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e8a17-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="e8a17-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e8a17-126">-ServerName</span></span>
<span data-ttu-id="e8a17-127">Il nome del gruppo di SQL Server Azure in cui si trova il pool flessibile.</span><span class="sxs-lookup"><span data-stu-id="e8a17-127">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="e8a17-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8a17-128">-Confirm</span></span>
<span data-ttu-id="e8a17-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8a17-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8a17-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8a17-130">-WhatIf</span></span>
<span data-ttu-id="e8a17-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e8a17-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8a17-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e8a17-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8a17-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8a17-133">CommonParameters</span></span>
<span data-ttu-id="e8a17-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8a17-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8a17-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e8a17-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8a17-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="e8a17-136">INPUTS</span></span>

### <span data-ttu-id="e8a17-137">System.String</span><span class="sxs-lookup"><span data-stu-id="e8a17-137">System.String</span></span>

## <span data-ttu-id="e8a17-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8a17-138">OUTPUTS</span></span>

## <span data-ttu-id="e8a17-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="e8a17-139">NOTES</span></span>

## <span data-ttu-id="e8a17-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8a17-140">RELATED LINKS</span></span>

[<span data-ttu-id="e8a17-141">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e8a17-141">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="e8a17-142">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="e8a17-142">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="e8a17-143">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="e8a17-143">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="e8a17-144">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="e8a17-144">Invoke-AzSqlDatabaseFailover</span></span>](./Invoke-AzSqlDatabaseFailover.md)

[<span data-ttu-id="e8a17-145">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e8a17-145">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="e8a17-146">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e8a17-146">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="e8a17-147">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e8a17-147">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="e8a17-148">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="e8a17-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)