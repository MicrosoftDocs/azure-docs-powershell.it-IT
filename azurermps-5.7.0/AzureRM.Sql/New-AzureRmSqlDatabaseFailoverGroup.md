---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 71f4796e33ec512f9d0aa2eb27f78ba615eefef1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507851"
---
# <span data-ttu-id="d8cff-101">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d8cff-101">New-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="d8cff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d8cff-102">SYNOPSIS</span></span>
<span data-ttu-id="d8cff-103">Questo comando crea un nuovo gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="d8cff-103">This command creates a new Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8cff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d8cff-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> -FailoverGroupName <String>
 [-PartnerResourceGroupName <String>] -PartnerServerName <String> [-FailoverPolicy <FailoverPolicy>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8cff-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8cff-105">DESCRIPTION</span></span>
<span data-ttu-id="d8cff-106">Crea un nuovo gruppo di failover di database SQL di Azure per i server specificati.</span><span class="sxs-lookup"><span data-stu-id="d8cff-106">Creates a new Azure SQL Database Failover Group for the specified servers.</span></span>

<span data-ttu-id="d8cff-107">Due endpoint TDS di database SQL di Azure vengono creati in FailoverGroupName. SqlDatabaseDnsSuffix (ad esempio, FailoverGroupName.database.windows.net) e FailoverGroupName. Secondary. SqlDatabaseDnsSuffix.</span><span class="sxs-lookup"><span data-stu-id="d8cff-107">Two Azure SQL Database TDS endpoints are created at FailoverGroupName.SqlDatabaseDnsSuffix (for example, FailoverGroupName.database.windows.net) and FailoverGroupName.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="d8cff-108">Questi endpoint possono essere usati per connettersi rispettivamente ai server primari e secondari nel gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="d8cff-108">These endpoints may be used to connect to the primary and secondary servers in the Failover Group, respectively.</span></span> <span data-ttu-id="d8cff-109">Se il server primario è influenzato da un'interruzione, il failover automatico degli endpoint e dei database viene attivato come dettato dai criteri di failover e dal periodo di tolleranza del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="d8cff-109">If the primary server is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Failover Group's failover policy and grace period.</span></span>

<span data-ttu-id="d8cff-110">I gruppi di failover appena creati non contengono database.</span><span class="sxs-lookup"><span data-stu-id="d8cff-110">Newly created Failover Groups do not contain any databases.</span></span> <span data-ttu-id="d8cff-111">Per controllare il set di database in un gruppo di failover, usare i cmdlet "Add-AzureRmSqlDatabaseToFailoverGroup" e "Remove-AzureRmSqlDatabaseFromFailoverGroup".</span><span class="sxs-lookup"><span data-stu-id="d8cff-111">To control the set of databases in a Failover Group, use the 'Add-AzureRmSqlDatabaseToFailoverGroup' and 'Remove-AzureRmSqlDatabaseFromFailoverGroup' cmdlets.</span></span>

<span data-ttu-id="d8cff-112">Durante l'anteprima della caratteristica gruppi di failover, per il parametro '-GracePeriodWithDataLossHours ' sono supportati solo i valori maggiori o uguali a 1 ora.</span><span class="sxs-lookup"><span data-stu-id="d8cff-112">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="d8cff-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d8cff-113">EXAMPLES</span></span>

### <span data-ttu-id="d8cff-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d8cff-114">Example 1</span></span>
```
C:\> $failoverGroup = New-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -PartnerServerName secondaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="d8cff-115">Questo comando crea un nuovo gruppo di failover con il criterio di failover "automatico" per due server nello stesso gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d8cff-115">This command creates a new Failover Group with failover policy 'Automatic' for two servers in the same resource group.</span></span>

### <span data-ttu-id="d8cff-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d8cff-116">Example 2</span></span>
```
C:\> $failoverGroup = New-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg1 -ServerName primaryserver -PartnerResourceGroupName rg2 -PartnerServerName secondaryserver1 -FailoverGroupName fg -FailoverPolicy Manual
```

<span data-ttu-id="d8cff-117">Questo comando crea un nuovo gruppo di failover con i criteri di failover "manuale" per due server in gruppi di risorse diversi.</span><span class="sxs-lookup"><span data-stu-id="d8cff-117">This command creates a new Failover Group with failover policy 'Manual' for two servers in different resource groups.</span></span>

## <span data-ttu-id="d8cff-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d8cff-118">PARAMETERS</span></span>

### <span data-ttu-id="d8cff-119">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="d8cff-119">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="d8cff-120">Se un'interruzione nel server secondario deve attivare il failover automatico dell'endpoint di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="d8cff-120">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="d8cff-121">Questa caratteristica non è ancora supportata.</span><span class="sxs-lookup"><span data-stu-id="d8cff-121">This feature is not yet supported.</span></span>

```yaml
Type: AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8cff-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8cff-122">-DefaultProfile</span></span>
<span data-ttu-id="d8cff-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d8cff-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8cff-124">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="d8cff-124">-FailoverGroupName</span></span>
<span data-ttu-id="d8cff-125">Il nome del gruppo di failover di database SQL di Azure da creare.</span><span class="sxs-lookup"><span data-stu-id="d8cff-125">The name of the Azure SQL Database Failover Group to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8cff-126">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="d8cff-126">-FailoverPolicy</span></span>
<span data-ttu-id="d8cff-127">Criteri di failover del gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="d8cff-127">The failover policy of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: Automatic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8cff-128">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="d8cff-128">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="d8cff-129">Intervallo prima che venga avviato il failover automatico se si verifica un'interruzione nel server primario e non è possibile completare il failover senza perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="d8cff-129">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8cff-130">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8cff-130">-PartnerResourceGroupName</span></span>
<span data-ttu-id="d8cff-131">Il nome del gruppo di risorse secondarie del gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="d8cff-131">The name of the secondary resource group of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8cff-132">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="d8cff-132">-PartnerServerName</span></span>
<span data-ttu-id="d8cff-133">Nome del server secondario del gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="d8cff-133">The name of the secondary server of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8cff-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8cff-134">-ResourceGroupName</span></span>
<span data-ttu-id="d8cff-135">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d8cff-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="d8cff-136">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="d8cff-136">-ServerName</span></span>
<span data-ttu-id="d8cff-137">Nome del server di database SQL di Azure principale del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="d8cff-137">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="d8cff-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8cff-138">CommonParameters</span></span>
<span data-ttu-id="d8cff-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8cff-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8cff-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8cff-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8cff-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d8cff-141">INPUTS</span></span>

### <span data-ttu-id="d8cff-142">System. String</span><span class="sxs-lookup"><span data-stu-id="d8cff-142">System.String</span></span>

## <span data-ttu-id="d8cff-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d8cff-143">OUTPUTS</span></span>

### <span data-ttu-id="d8cff-144">System. Object</span><span class="sxs-lookup"><span data-stu-id="d8cff-144">System.Object</span></span>

## <span data-ttu-id="d8cff-145">Note</span><span class="sxs-lookup"><span data-stu-id="d8cff-145">NOTES</span></span>

## <span data-ttu-id="d8cff-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d8cff-146">RELATED LINKS</span></span>

[<span data-ttu-id="d8cff-147">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d8cff-147">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d8cff-148">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d8cff-148">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d8cff-149">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d8cff-149">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="d8cff-150">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d8cff-150">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="d8cff-151">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d8cff-151">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d8cff-152">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d8cff-152">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d8cff-153">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="d8cff-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
