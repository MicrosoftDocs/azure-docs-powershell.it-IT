---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: c1164f7c4875d6cdd00ca13236c1d8e6d4b07cb3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191047"
---
# <span data-ttu-id="29a9a-101">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="29a9a-101">New-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="29a9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29a9a-102">SYNOPSIS</span></span>
<span data-ttu-id="29a9a-103">Questo comando crea un nuovo gruppo di failover SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="29a9a-103">This command creates a new Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="29a9a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="29a9a-104">SYNTAX</span></span>

```
New-AzSqlDatabaseFailoverGroup [-ServerName] <String> -FailoverGroupName <String>
 [-PartnerResourceGroupName <String>] -PartnerServerName <String> [-FailoverPolicy <FailoverPolicy>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29a9a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="29a9a-105">DESCRIPTION</span></span>
<span data-ttu-id="29a9a-106">Crea un nuovo gruppo di failover SQL database di Azure per i server specificati.</span><span class="sxs-lookup"><span data-stu-id="29a9a-106">Creates a new Azure SQL Database Failover Group for the specified servers.</span></span>
<span data-ttu-id="29a9a-107">Vengono creati due endpoint TDS del database di Azure SQL in FailoverGroupName.SqlDatabaseDnsSuffix, ad esempio FailoverGroupName.database.windows.net, e FailoverGroupName.secondary.SqlDatabaseDnsSuffix.</span><span class="sxs-lookup"><span data-stu-id="29a9a-107">Two Azure SQL Database TDS endpoints are created at FailoverGroupName.SqlDatabaseDnsSuffix (for example, FailoverGroupName.database.windows.net) and FailoverGroupName.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="29a9a-108">Questi endpoint possono essere usati, rispettivamente, per connettersi ai server primario e secondario nel gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="29a9a-108">These endpoints may be used to connect to the primary and secondary servers in the Failover Group, respectively.</span></span> <span data-ttu-id="29a9a-109">Se il server primario è interessato da un'interruzione, il failover automatico degli endpoint e dei database verrà attivato in base ai criteri di failover e al periodo di tolleranza del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="29a9a-109">If the primary server is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Failover Group's failover policy and grace period.</span></span>
<span data-ttu-id="29a9a-110">I gruppi di failover appena creati non contengono database.</span><span class="sxs-lookup"><span data-stu-id="29a9a-110">Newly created Failover Groups do not contain any databases.</span></span> <span data-ttu-id="29a9a-111">Per controllare il set di database in un gruppo di failover, usare i cmdlet 'Add-AzSqlDatabaseToFailoverGroup' e 'Remove-AzSqlDatabaseFromFailoverGroup'.</span><span class="sxs-lookup"><span data-stu-id="29a9a-111">To control the set of databases in a Failover Group, use the 'Add-AzSqlDatabaseToFailoverGroup' and 'Remove-AzSqlDatabaseFromFailoverGroup' cmdlets.</span></span>
<span data-ttu-id="29a9a-112">Per il parametro '-GracePeriodWithDataLossHours' sono supportati solo i valori maggiori o uguali a 1 ora.</span><span class="sxs-lookup"><span data-stu-id="29a9a-112">Only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="29a9a-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="29a9a-113">EXAMPLES</span></span>

### <span data-ttu-id="29a9a-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="29a9a-114">Example 1</span></span>
```
C:\> $failoverGroup = New-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -PartnerServerName secondaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="29a9a-115">Questo comando crea un nuovo gruppo di failover con criterio di failover "Automatico" per due server nello stesso gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="29a9a-115">This command creates a new Failover Group with failover policy 'Automatic' for two servers in the same resource group.</span></span>

### <span data-ttu-id="29a9a-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="29a9a-116">Example 2</span></span>
```
C:\> $failoverGroup = New-AzSqlDatabaseFailoverGroup -ResourceGroupName rg1 -ServerName primaryserver -PartnerResourceGroupName rg2 -PartnerServerName secondaryserver1 -FailoverGroupName fg -FailoverPolicy Manual
```

<span data-ttu-id="29a9a-117">Questo comando crea un nuovo gruppo di failover con criteri di failover "Manuale" per due server in gruppi di risorse diversi.</span><span class="sxs-lookup"><span data-stu-id="29a9a-117">This command creates a new Failover Group with failover policy 'Manual' for two servers in different resource groups.</span></span>

## <span data-ttu-id="29a9a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29a9a-118">PARAMETERS</span></span>

### <span data-ttu-id="29a9a-119">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="29a9a-119">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="29a9a-120">Se un'interruzione nel server secondario deve attivare il failover automatico dell'endpoint di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="29a9a-120">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="29a9a-121">Questa funzionalità non è ancora supportata.</span><span class="sxs-lookup"><span data-stu-id="29a9a-121">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="29a9a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29a9a-122">-DefaultProfile</span></span>
<span data-ttu-id="29a9a-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="29a9a-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29a9a-124">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="29a9a-124">-FailoverGroupName</span></span>
<span data-ttu-id="29a9a-125">Nome del gruppo di failover del database SQL Azure da creare.</span><span class="sxs-lookup"><span data-stu-id="29a9a-125">The name of the Azure SQL Database Failover Group to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29a9a-126">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="29a9a-126">-FailoverPolicy</span></span>
<span data-ttu-id="29a9a-127">Criteri di failover del gruppo di failover SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="29a9a-127">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="29a9a-128">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="29a9a-128">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="29a9a-129">Intervallo prima dell'avvio del failover automatico se si verifica un'interruzione nel server principale e il failover non può essere completato senza perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="29a9a-129">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="29a9a-130">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29a9a-130">-PartnerResourceGroupName</span></span>
<span data-ttu-id="29a9a-131">Nome del gruppo di risorse secondario del gruppo di failover del SQL di failover del database di Azure.</span><span class="sxs-lookup"><span data-stu-id="29a9a-131">The name of the secondary resource group of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29a9a-132">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="29a9a-132">-PartnerServerName</span></span>
<span data-ttu-id="29a9a-133">Nome del server secondario del gruppo di failover del SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="29a9a-133">The name of the secondary server of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29a9a-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29a9a-134">-ResourceGroupName</span></span>
<span data-ttu-id="29a9a-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="29a9a-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="29a9a-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="29a9a-136">-ServerName</span></span>
<span data-ttu-id="29a9a-137">Nome del server di database SQL Azure primario del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="29a9a-137">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="29a9a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29a9a-138">CommonParameters</span></span>
<span data-ttu-id="29a9a-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29a9a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29a9a-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="29a9a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29a9a-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="29a9a-141">INPUTS</span></span>

### <span data-ttu-id="29a9a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="29a9a-142">System.String</span></span>

## <span data-ttu-id="29a9a-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="29a9a-143">OUTPUTS</span></span>

### <span data-ttu-id="29a9a-144">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="29a9a-144">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="29a9a-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="29a9a-145">NOTES</span></span>

## <span data-ttu-id="29a9a-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="29a9a-146">RELATED LINKS</span></span>

[<span data-ttu-id="29a9a-147">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="29a9a-147">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="29a9a-148">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="29a9a-148">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="29a9a-149">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="29a9a-149">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="29a9a-150">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="29a9a-150">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="29a9a-151">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="29a9a-151">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="29a9a-152">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="29a9a-152">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="29a9a-153">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="29a9a-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
