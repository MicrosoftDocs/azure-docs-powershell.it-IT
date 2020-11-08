---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/switch-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: d8eff694378f6145931a18a622f29bf88d99e1ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203046"
---
# <span data-ttu-id="4a260-101">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4a260-101">Switch-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="4a260-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4a260-102">SYNOPSIS</span></span>
<span data-ttu-id="4a260-103">Esegue un failover di un gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4a260-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="4a260-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a260-104">SYNTAX</span></span>

```
Switch-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4a260-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a260-105">DESCRIPTION</span></span>
<span data-ttu-id="4a260-106">Questo comando scambia i ruoli dei server in un gruppo di failover e passa tutti i database secondari al ruolo principale.</span><span class="sxs-lookup"><span data-stu-id="4a260-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="4a260-107">Tutte le nuove sessioni TDS vengono reinstradate automaticamente al server secondario dopo l'aggiornamento della cache del client DNS.</span><span class="sxs-lookup"><span data-stu-id="4a260-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="4a260-108">Quando il server primario originale è di nuovo online, tutti i database primari in precedenza verranno passati al ruolo secondario.</span><span class="sxs-lookup"><span data-stu-id="4a260-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>
<span data-ttu-id="4a260-109">Il server secondario del gruppo di failover deve essere usato per eseguire questo comando.</span><span class="sxs-lookup"><span data-stu-id="4a260-109">The Failover Group's secondary server must be used to execute this command.</span></span>
<span data-ttu-id="4a260-110">Se il parametro AllowDataLoss non è specificato, questo comando attende fino a quando non vengono cambiati entrambi i ruoli.</span><span class="sxs-lookup"><span data-stu-id="4a260-110">If the AllowDataLoss parameter is not specified, this command waits until both roles are switched.</span></span> <span data-ttu-id="4a260-111">Se il parametro AllowDataLoss è specificato, il comando attende solo fino a quando il nuovo primario non assumerà il ruolo.</span><span class="sxs-lookup"><span data-stu-id="4a260-111">If the AllowDataLoss parameter is specified, the command only waits until the new primary assumes its role.</span></span>

## <span data-ttu-id="4a260-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a260-112">EXAMPLES</span></span>

### <span data-ttu-id="4a260-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4a260-113">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="4a260-114">Eseguire un'operazione di failover per consentire la perdita dei dati tramite piping nel gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="4a260-114">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="4a260-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4a260-115">Example 2</span></span>
```
C:\> Switch-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="4a260-116">Eseguire un'operazione di failover ottimale dello sforzo che avrà esito positivo senza perdere dati o non riesce e ripristinare il rollback.</span><span class="sxs-lookup"><span data-stu-id="4a260-116">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="4a260-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4a260-117">PARAMETERS</span></span>

### <span data-ttu-id="4a260-118">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="4a260-118">-AllowDataLoss</span></span>
<span data-ttu-id="4a260-119">Completare il failover anche se tale operazione può causare una perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="4a260-119">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="4a260-120">In questo modo il failover verrà continuato anche se un database primario non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="4a260-120">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a260-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a260-121">-AsJob</span></span>
<span data-ttu-id="4a260-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4a260-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4a260-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a260-123">-DefaultProfile</span></span>
<span data-ttu-id="4a260-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4a260-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a260-125">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="4a260-125">-FailoverGroupName</span></span>
<span data-ttu-id="4a260-126">Nome del gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4a260-126">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a260-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a260-127">-ResourceGroupName</span></span>
<span data-ttu-id="4a260-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4a260-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="4a260-129">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="4a260-129">-ServerName</span></span>
<span data-ttu-id="4a260-130">Nome del server di database SQL di Azure secondario del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="4a260-130">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="4a260-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4a260-131">-Confirm</span></span>
<span data-ttu-id="4a260-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a260-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a260-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a260-133">-WhatIf</span></span>
<span data-ttu-id="4a260-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a260-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a260-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a260-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a260-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a260-136">CommonParameters</span></span>
<span data-ttu-id="4a260-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a260-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a260-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a260-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a260-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4a260-139">INPUTS</span></span>

### <span data-ttu-id="4a260-140">System. String</span><span class="sxs-lookup"><span data-stu-id="4a260-140">System.String</span></span>

## <span data-ttu-id="4a260-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a260-141">OUTPUTS</span></span>

### <span data-ttu-id="4a260-142">Microsoft. Azure. Commands. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="4a260-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="4a260-143">Note</span><span class="sxs-lookup"><span data-stu-id="4a260-143">NOTES</span></span>

## <span data-ttu-id="4a260-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a260-144">RELATED LINKS</span></span>

[<span data-ttu-id="4a260-145">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4a260-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4a260-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4a260-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4a260-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4a260-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4a260-148">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4a260-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="4a260-149">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4a260-149">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="4a260-150">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4a260-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4a260-151">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="4a260-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
