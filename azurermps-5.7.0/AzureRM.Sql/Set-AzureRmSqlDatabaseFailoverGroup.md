---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: e5452ef5b6d8b2e5535c5388d5d42698aa7c261f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512156"
---
# <span data-ttu-id="b63cf-101">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b63cf-101">Set-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="b63cf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b63cf-102">SYNOPSIS</span></span>
<span data-ttu-id="b63cf-103">Modifica la configurazione di un gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="b63cf-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b63cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b63cf-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b63cf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b63cf-105">DESCRIPTION</span></span>
<span data-ttu-id="b63cf-106">Questo comando consente di modificare la configurazione di un gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="b63cf-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>

<span data-ttu-id="b63cf-107">Il server principale del gruppo di failover deve essere usato per eseguire il comando.</span><span class="sxs-lookup"><span data-stu-id="b63cf-107">The Failover Group's primary server should be used to execute the command.</span></span>

<span data-ttu-id="b63cf-108">Per controllare il set di database nel gruppo, USA invece ' Add-AzureRmSqlDatabaseToFailoverGroup ' è Remove-AzureRmSqlDatabaseFromFailoverGroup '.</span><span class="sxs-lookup"><span data-stu-id="b63cf-108">To control the set of databases in the group, use 'Add-AzureRmSqlDatabaseToFailoverGroup' and 'Remove-AzureRmSqlDatabaseFromFailoverGroup' instead.</span></span>

<span data-ttu-id="b63cf-109">Durante l'anteprima della caratteristica gruppi di failover, per il parametro '-GracePeriodWithDataLossHours ' sono supportati solo i valori maggiori o uguali a 1 ora.</span><span class="sxs-lookup"><span data-stu-id="b63cf-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="b63cf-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b63cf-110">EXAMPLES</span></span>

### <span data-ttu-id="b63cf-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b63cf-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="b63cf-112">Imposta i criteri di failover di un gruppo di failover su "automatico".</span><span class="sxs-lookup"><span data-stu-id="b63cf-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="b63cf-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b63cf-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzureRmSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="b63cf-114">Imposta i criteri di failover di un gruppo di failover su "manuale" tramite il piping nel gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="b63cf-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="b63cf-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b63cf-115">PARAMETERS</span></span>

### <span data-ttu-id="b63cf-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="b63cf-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="b63cf-117">Se le interruzioni nel server secondario devono attivare il failover automatico dell'endpoint di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="b63cf-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="b63cf-118">Questa caratteristica non è ancora supportata.</span><span class="sxs-lookup"><span data-stu-id="b63cf-118">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="b63cf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b63cf-119">-DefaultProfile</span></span>
<span data-ttu-id="b63cf-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b63cf-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b63cf-121">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="b63cf-121">-FailoverGroupName</span></span>
<span data-ttu-id="b63cf-122">Nome del gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="b63cf-122">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="b63cf-123">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="b63cf-123">-FailoverPolicy</span></span>
<span data-ttu-id="b63cf-124">Criteri di failover del gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="b63cf-124">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="b63cf-125">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="b63cf-125">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="b63cf-126">Intervallo prima che venga avviato il failover automatico se si verifica un'interruzione nel server primario.</span><span class="sxs-lookup"><span data-stu-id="b63cf-126">Interval before automatic failover is initiated if an outage occurs on the primary server.</span></span> <span data-ttu-id="b63cf-127">Ciò indica che il database SQL di Azure non avvierà il failover automatico prima che scada il periodo di tolleranza.</span><span class="sxs-lookup"><span data-stu-id="b63cf-127">This indicates that Azure SQL Database will not initiate automatic failover before the grace period expires.</span></span> <span data-ttu-id="b63cf-128">Tieni presente che l'operazione di failover con l'opzione AllowDataLoss può causare la perdita di dati a causa della natura della sincronizzazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="b63cf-128">Please note that failover operation with AllowDataLoss option might cause data loss due to the nature of asynchronous synchronization.</span></span>

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

### <span data-ttu-id="b63cf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b63cf-129">-ResourceGroupName</span></span>
<span data-ttu-id="b63cf-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b63cf-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="b63cf-131">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="b63cf-131">-ServerName</span></span>
<span data-ttu-id="b63cf-132">Nome del server di database SQL di Azure principale del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="b63cf-132">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="b63cf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b63cf-133">CommonParameters</span></span>
<span data-ttu-id="b63cf-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b63cf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b63cf-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b63cf-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b63cf-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b63cf-136">INPUTS</span></span>

### <span data-ttu-id="b63cf-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b63cf-137">System.String</span></span>

## <span data-ttu-id="b63cf-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b63cf-138">OUTPUTS</span></span>

### <span data-ttu-id="b63cf-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="b63cf-139">System.Object</span></span>

## <span data-ttu-id="b63cf-140">Note</span><span class="sxs-lookup"><span data-stu-id="b63cf-140">NOTES</span></span>

## <span data-ttu-id="b63cf-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b63cf-141">RELATED LINKS</span></span>

[<span data-ttu-id="b63cf-142">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b63cf-142">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="b63cf-143">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b63cf-143">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="b63cf-144">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b63cf-144">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="b63cf-145">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b63cf-145">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="b63cf-146">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b63cf-146">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="b63cf-147">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="b63cf-147">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="b63cf-148">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="b63cf-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
