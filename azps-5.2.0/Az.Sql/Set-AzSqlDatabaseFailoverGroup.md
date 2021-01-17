---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 8b78cfc7a2934b4670702562941ea0e00c2a70c8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354787"
---
# <span data-ttu-id="d6897-101">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d6897-101">Set-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="d6897-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d6897-102">SYNOPSIS</span></span>
<span data-ttu-id="d6897-103">Modifica la configurazione di un gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="d6897-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="d6897-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d6897-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6897-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6897-105">DESCRIPTION</span></span>
<span data-ttu-id="d6897-106">Questo comando consente di modificare la configurazione di un gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="d6897-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>
<span data-ttu-id="d6897-107">Il server principale del gruppo di failover deve essere usato per eseguire il comando.</span><span class="sxs-lookup"><span data-stu-id="d6897-107">The Failover Group's primary server should be used to execute the command.</span></span>
<span data-ttu-id="d6897-108">Per controllare il set di database nel gruppo, USA invece ' Add-AzSqlDatabaseToFailoverGroup ' è Remove-AzSqlDatabaseFromFailoverGroup '.</span><span class="sxs-lookup"><span data-stu-id="d6897-108">To control the set of databases in the group, use 'Add-AzSqlDatabaseToFailoverGroup' and 'Remove-AzSqlDatabaseFromFailoverGroup' instead.</span></span>
<span data-ttu-id="d6897-109">Durante l'anteprima della caratteristica gruppi di failover, per il parametro '-GracePeriodWithDataLossHours ' sono supportati solo i valori maggiori o uguali a 1 ora.</span><span class="sxs-lookup"><span data-stu-id="d6897-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="d6897-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d6897-110">EXAMPLES</span></span>

### <span data-ttu-id="d6897-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d6897-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="d6897-112">Imposta i criteri di failover di un gruppo di failover su "automatico".</span><span class="sxs-lookup"><span data-stu-id="d6897-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="d6897-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d6897-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="d6897-114">Imposta i criteri di failover di un gruppo di failover su "manuale" tramite il piping nel gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="d6897-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="d6897-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d6897-115">PARAMETERS</span></span>

### <span data-ttu-id="d6897-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="d6897-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="d6897-117">Se le interruzioni nel server secondario devono attivare il failover automatico dell'endpoint di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="d6897-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

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

### <span data-ttu-id="d6897-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6897-118">-DefaultProfile</span></span>
<span data-ttu-id="d6897-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d6897-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6897-120">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="d6897-120">-FailoverGroupName</span></span>
<span data-ttu-id="d6897-121">Nome del gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="d6897-121">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="d6897-122">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="d6897-122">-FailoverPolicy</span></span>
<span data-ttu-id="d6897-123">Criteri di failover del gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="d6897-123">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="d6897-124">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="d6897-124">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="d6897-125">Intervallo prima che venga avviato il failover automatico se si verifica un'interruzione nel server primario.</span><span class="sxs-lookup"><span data-stu-id="d6897-125">Interval before automatic failover is initiated if an outage occurs on the primary server.</span></span> <span data-ttu-id="d6897-126">Ciò indica che il database SQL di Azure non avvierà il failover automatico prima che scada il periodo di tolleranza.</span><span class="sxs-lookup"><span data-stu-id="d6897-126">This indicates that Azure SQL Database will not initiate automatic failover before the grace period expires.</span></span> <span data-ttu-id="d6897-127">Tieni presente che l'operazione di failover con l'opzione AllowDataLoss può causare la perdita di dati a causa della natura della sincronizzazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="d6897-127">Please note that failover operation with AllowDataLoss option might cause data loss due to the nature of asynchronous synchronization.</span></span>

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

### <span data-ttu-id="d6897-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6897-128">-ResourceGroupName</span></span>
<span data-ttu-id="d6897-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d6897-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="d6897-130">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="d6897-130">-ServerName</span></span>
<span data-ttu-id="d6897-131">Nome del server di database SQL di Azure principale del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="d6897-131">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="d6897-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6897-132">CommonParameters</span></span>
<span data-ttu-id="d6897-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6897-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6897-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d6897-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6897-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d6897-135">INPUTS</span></span>

### <span data-ttu-id="d6897-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d6897-136">System.String</span></span>

## <span data-ttu-id="d6897-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d6897-137">OUTPUTS</span></span>

### <span data-ttu-id="d6897-138">Microsoft. Azure. Commands. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="d6897-138">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="d6897-139">Note</span><span class="sxs-lookup"><span data-stu-id="d6897-139">NOTES</span></span>

## <span data-ttu-id="d6897-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d6897-140">RELATED LINKS</span></span>

[<span data-ttu-id="d6897-141">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d6897-141">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d6897-142">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d6897-142">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d6897-143">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d6897-143">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="d6897-144">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d6897-144">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="d6897-145">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d6897-145">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d6897-146">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d6897-146">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d6897-147">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="d6897-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
