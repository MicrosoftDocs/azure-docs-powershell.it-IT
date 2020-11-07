---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/switch-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 15b0026158f3942ffbb9ff1d426104cffcb18a28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857697"
---
# <span data-ttu-id="02766-101">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="02766-101">Switch-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="02766-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="02766-102">SYNOPSIS</span></span>
<span data-ttu-id="02766-103">Esegue un failover di un gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="02766-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="02766-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="02766-104">SYNTAX</span></span>

```
Switch-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02766-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02766-105">DESCRIPTION</span></span>
<span data-ttu-id="02766-106">Questo comando scambia i ruoli dei server in un gruppo di failover e passa tutti i database secondari al ruolo principale.</span><span class="sxs-lookup"><span data-stu-id="02766-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="02766-107">Tutte le nuove sessioni TDS vengono reinstradate automaticamente al server secondario dopo l'aggiornamento della cache del client DNS.</span><span class="sxs-lookup"><span data-stu-id="02766-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="02766-108">Quando il server primario originale è di nuovo online, tutti i database primari in precedenza verranno passati al ruolo secondario.</span><span class="sxs-lookup"><span data-stu-id="02766-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>
<span data-ttu-id="02766-109">Il server secondario del gruppo di failover deve essere usato per eseguire questo comando.</span><span class="sxs-lookup"><span data-stu-id="02766-109">The Failover Group's secondary server must be used to execute this command.</span></span>

## <span data-ttu-id="02766-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="02766-110">EXAMPLES</span></span>

### <span data-ttu-id="02766-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="02766-111">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="02766-112">Eseguire un'operazione di failover per consentire la perdita dei dati tramite piping nel gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="02766-112">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="02766-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="02766-113">Example 2</span></span>
```
C:\> Switch-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="02766-114">Eseguire un'operazione di failover ottimale dello sforzo che avrà esito positivo senza perdere dati o non riesce e ripristinare il rollback.</span><span class="sxs-lookup"><span data-stu-id="02766-114">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="02766-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="02766-115">PARAMETERS</span></span>

### <span data-ttu-id="02766-116">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="02766-116">-AllowDataLoss</span></span>
<span data-ttu-id="02766-117">Completare il failover anche se tale operazione può causare una perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="02766-117">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="02766-118">In questo modo il failover verrà continuato anche se un database primario non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="02766-118">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="02766-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02766-119">-AsJob</span></span>
<span data-ttu-id="02766-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="02766-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02766-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02766-121">-DefaultProfile</span></span>
<span data-ttu-id="02766-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="02766-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="02766-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="02766-123">-FailoverGroupName</span></span>
<span data-ttu-id="02766-124">Nome del gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="02766-124">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="02766-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02766-125">-ResourceGroupName</span></span>
<span data-ttu-id="02766-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="02766-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="02766-127">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="02766-127">-ServerName</span></span>
<span data-ttu-id="02766-128">Nome del server di database SQL di Azure secondario del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="02766-128">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="02766-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="02766-129">-Confirm</span></span>
<span data-ttu-id="02766-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02766-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02766-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02766-131">-WhatIf</span></span>
<span data-ttu-id="02766-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="02766-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02766-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="02766-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02766-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02766-134">CommonParameters</span></span>
<span data-ttu-id="02766-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02766-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02766-136">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02766-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02766-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="02766-137">INPUTS</span></span>

### <span data-ttu-id="02766-138">System. String</span><span class="sxs-lookup"><span data-stu-id="02766-138">System.String</span></span>

## <span data-ttu-id="02766-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="02766-139">OUTPUTS</span></span>

### <span data-ttu-id="02766-140">Microsoft. Azure. Commands. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="02766-140">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="02766-141">Note</span><span class="sxs-lookup"><span data-stu-id="02766-141">NOTES</span></span>

## <span data-ttu-id="02766-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="02766-142">RELATED LINKS</span></span>

[<span data-ttu-id="02766-143">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="02766-143">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="02766-144">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="02766-144">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="02766-145">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="02766-145">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="02766-146">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="02766-146">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="02766-147">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="02766-147">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="02766-148">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="02766-148">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="02766-149">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="02766-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
