---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqlelasticpoolfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlElasticPoolFailover.md
ms.openlocfilehash: 631a8edcc3709e80b36a3ff8661b7ea6027b9f78
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193618"
---
# <span data-ttu-id="dae15-101">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="dae15-101">Invoke-AzSqlElasticPoolFailover</span></span>

## <span data-ttu-id="dae15-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dae15-102">SYNOPSIS</span></span>
<span data-ttu-id="dae15-103">Failover di un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="dae15-103">Failovers an elastic pool.</span></span>

## <span data-ttu-id="dae15-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dae15-104">SYNTAX</span></span>

```
Invoke-AzSqlElasticPoolFailover [-ElasticPoolName] <String> [-AsJob] [-PassThru] [-Force]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dae15-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dae15-105">DESCRIPTION</span></span>
<span data-ttu-id="dae15-106">Il cmdlet Invoke-AzSqlElasticPoolFailover failover di un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="dae15-106">The Invoke-AzSqlElasticPoolFailover cmdlet failovers an elastic pool.</span></span> <span data-ttu-id="dae15-107">Dopo l'uso di questo cmdlet, il failover si verificherà in tutti i database del pool elastico.</span><span class="sxs-lookup"><span data-stu-id="dae15-107">Failover will occur on all databases in the elastic pool after running this cmdlet.</span></span>

## <span data-ttu-id="dae15-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dae15-108">EXAMPLES</span></span>

### <span data-ttu-id="dae15-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dae15-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlElasticPoolFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="dae15-110">Questo comando eseguirà il failover del pool elastico denominato "ElasticPool01" sul server denominato "Server01".</span><span class="sxs-lookup"><span data-stu-id="dae15-110">This command will failover the elastic pool named "ElasticPool01" on the server named "Server01".</span></span>  <span data-ttu-id="dae15-111">Questo significa che il failover si verificherà in tutti i database nel pool elastico denominato "ElasticPool01".</span><span class="sxs-lookup"><span data-stu-id="dae15-111">This means failover will occur on all databases in the elastic pool named "ElasticPool01".</span></span>

## <span data-ttu-id="dae15-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dae15-112">PARAMETERS</span></span>

### <span data-ttu-id="dae15-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dae15-113">-AsJob</span></span>
<span data-ttu-id="dae15-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="dae15-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dae15-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dae15-115">-DefaultProfile</span></span>
<span data-ttu-id="dae15-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dae15-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dae15-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="dae15-117">-ElasticPoolName</span></span>
<span data-ttu-id="dae15-118">Nome del pool di Azure SQL Elastic da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="dae15-118">The name of the Azure SQL Elastic Pool to remove.</span></span>

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

### <span data-ttu-id="dae15-119">-Force</span><span class="sxs-lookup"><span data-stu-id="dae15-119">-Force</span></span>
<span data-ttu-id="dae15-120">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="dae15-120">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="dae15-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dae15-121">-PassThru</span></span>
<span data-ttu-id="dae15-122">Per l'esecuzione corretta, restituisce vero.</span><span class="sxs-lookup"><span data-stu-id="dae15-122">On Successful execution, returns true.</span></span>  <span data-ttu-id="dae15-123">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="dae15-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dae15-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dae15-124">-ResourceGroupName</span></span>
<span data-ttu-id="dae15-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dae15-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="dae15-126">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="dae15-126">-ServerName</span></span>
<span data-ttu-id="dae15-127">Nome di Azure SQL Server in cui è presente il pool di elastici.</span><span class="sxs-lookup"><span data-stu-id="dae15-127">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="dae15-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dae15-128">-Confirm</span></span>
<span data-ttu-id="dae15-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dae15-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dae15-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dae15-130">-WhatIf</span></span>
<span data-ttu-id="dae15-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dae15-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dae15-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dae15-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dae15-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dae15-133">CommonParameters</span></span>
<span data-ttu-id="dae15-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dae15-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dae15-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dae15-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dae15-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dae15-136">INPUTS</span></span>

### <span data-ttu-id="dae15-137">System. String</span><span class="sxs-lookup"><span data-stu-id="dae15-137">System.String</span></span>

## <span data-ttu-id="dae15-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dae15-138">OUTPUTS</span></span>

## <span data-ttu-id="dae15-139">Note</span><span class="sxs-lookup"><span data-stu-id="dae15-139">NOTES</span></span>

## <span data-ttu-id="dae15-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dae15-140">RELATED LINKS</span></span>

[<span data-ttu-id="dae15-141">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="dae15-141">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="dae15-142">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="dae15-142">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="dae15-143">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="dae15-143">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="dae15-144">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="dae15-144">Invoke-AzSqlDatabaseFailover</span></span>](./Invoke-AzSqlDatabaseFailover.md)

[<span data-ttu-id="dae15-145">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="dae15-145">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="dae15-146">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="dae15-146">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="dae15-147">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="dae15-147">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="dae15-148">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="dae15-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)