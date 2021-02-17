---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 8b78cfc7a2934b4670702562941ea0e00c2a70c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207875"
---
# <span data-ttu-id="9e187-101">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e187-101">Set-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="9e187-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e187-102">SYNOPSIS</span></span>
<span data-ttu-id="9e187-103">Modifica la configurazione di un gruppo di failover del SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="9e187-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="9e187-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e187-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e187-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9e187-105">DESCRIPTION</span></span>
<span data-ttu-id="9e187-106">Questo comando modifica la configurazione di un gruppo di failover del SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="9e187-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>
<span data-ttu-id="9e187-107">Il server primario del gruppo di failover deve essere usato per eseguire il comando.</span><span class="sxs-lookup"><span data-stu-id="9e187-107">The Failover Group's primary server should be used to execute the command.</span></span>
<span data-ttu-id="9e187-108">Per controllare il set di database nel gruppo, usare invece "Add-AzSqlDatabaseToFailoverGroup" e "Remove-AzSqlDatabaseFromFailoverGroup".</span><span class="sxs-lookup"><span data-stu-id="9e187-108">To control the set of databases in the group, use 'Add-AzSqlDatabaseToFailoverGroup' and 'Remove-AzSqlDatabaseFromFailoverGroup' instead.</span></span>
<span data-ttu-id="9e187-109">Durante l'anteprima della funzionalità Gruppi di failover, sono supportati solo i valori maggiori o uguali a 1 ora per il parametro '-GracePeriodWithDataLossHours'.</span><span class="sxs-lookup"><span data-stu-id="9e187-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="9e187-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e187-110">EXAMPLES</span></span>

### <span data-ttu-id="9e187-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9e187-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="9e187-112">Imposta il criterio di failover di un gruppo di failover su "Automatico".</span><span class="sxs-lookup"><span data-stu-id="9e187-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="9e187-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9e187-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="9e187-114">Imposta il criterio di failover di un gruppo di failover su "Manuale" tramite piping nel gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="9e187-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="9e187-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e187-115">PARAMETERS</span></span>

### <span data-ttu-id="9e187-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="9e187-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="9e187-117">Se le interruzioni nel server secondario devono attivare il failover automatico dell'endpoint di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="9e187-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e187-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e187-118">-DefaultProfile</span></span>
<span data-ttu-id="9e187-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="9e187-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e187-120">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="9e187-120">-FailoverGroupName</span></span>
<span data-ttu-id="9e187-121">Nome del gruppo di failover del database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="9e187-121">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="9e187-122">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="9e187-122">-FailoverPolicy</span></span>
<span data-ttu-id="9e187-123">Criteri di failover del gruppo di failover SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="9e187-123">The failover policy of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: Automatic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e187-124">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="9e187-124">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="9e187-125">Intervallo prima dell'avvio del failover automatico se si verifica un'interruzione nel server primario.</span><span class="sxs-lookup"><span data-stu-id="9e187-125">Interval before automatic failover is initiated if an outage occurs on the primary server.</span></span> <span data-ttu-id="9e187-126">Questo significa che Il database SQL Azure non avvierà il failover automatico prima della scadenza del periodo di tolleranza.</span><span class="sxs-lookup"><span data-stu-id="9e187-126">This indicates that Azure SQL Database will not initiate automatic failover before the grace period expires.</span></span> <span data-ttu-id="9e187-127">Tenere presente che l'operazione di failover con l'opzione AllowDataLoss potrebbe causare la perdita di dati a causa della natura della sincronizzazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="9e187-127">Please note that failover operation with AllowDataLoss option might cause data loss due to the nature of asynchronous synchronization.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e187-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e187-128">-ResourceGroupName</span></span>
<span data-ttu-id="9e187-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9e187-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="9e187-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9e187-130">-ServerName</span></span>
<span data-ttu-id="9e187-131">Nome del server di database SQL Azure primario del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="9e187-131">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="9e187-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e187-132">CommonParameters</span></span>
<span data-ttu-id="9e187-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e187-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e187-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9e187-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e187-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="9e187-135">INPUTS</span></span>

### <span data-ttu-id="9e187-136">System.String</span><span class="sxs-lookup"><span data-stu-id="9e187-136">System.String</span></span>

## <span data-ttu-id="9e187-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e187-137">OUTPUTS</span></span>

### <span data-ttu-id="9e187-138">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="9e187-138">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="9e187-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="9e187-139">NOTES</span></span>

## <span data-ttu-id="9e187-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e187-140">RELATED LINKS</span></span>

[<span data-ttu-id="9e187-141">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e187-141">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9e187-142">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e187-142">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9e187-143">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e187-143">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="9e187-144">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e187-144">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="9e187-145">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e187-145">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9e187-146">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9e187-146">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9e187-147">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="9e187-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
