---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 98a6ceafed2c7c62301c63ff1c8b3028c46e1201
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511440"
---
# <span data-ttu-id="9af7d-101">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9af7d-101">Set-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="9af7d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9af7d-102">SYNOPSIS</span></span>
<span data-ttu-id="9af7d-103">Modifica la configurazione di un gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="9af7d-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9af7d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9af7d-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9af7d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9af7d-105">DESCRIPTION</span></span>
<span data-ttu-id="9af7d-106">Questo comando consente di modificare la configurazione di un gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="9af7d-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>
<span data-ttu-id="9af7d-107">Il server principale del gruppo di failover deve essere usato per eseguire il comando.</span><span class="sxs-lookup"><span data-stu-id="9af7d-107">The Failover Group's primary server should be used to execute the command.</span></span>
<span data-ttu-id="9af7d-108">Per controllare il set di database nel gruppo, USA invece ' Add-AzureRmSqlDatabaseToFailoverGroup ' è Remove-AzureRmSqlDatabaseFromFailoverGroup '.</span><span class="sxs-lookup"><span data-stu-id="9af7d-108">To control the set of databases in the group, use 'Add-AzureRmSqlDatabaseToFailoverGroup' and 'Remove-AzureRmSqlDatabaseFromFailoverGroup' instead.</span></span>
<span data-ttu-id="9af7d-109">Durante l'anteprima della caratteristica gruppi di failover, per il parametro '-GracePeriodWithDataLossHours ' sono supportati solo i valori maggiori o uguali a 1 ora.</span><span class="sxs-lookup"><span data-stu-id="9af7d-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="9af7d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9af7d-110">EXAMPLES</span></span>

### <span data-ttu-id="9af7d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9af7d-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="9af7d-112">Imposta i criteri di failover di un gruppo di failover su "automatico".</span><span class="sxs-lookup"><span data-stu-id="9af7d-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="9af7d-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9af7d-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzureRmSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="9af7d-114">Imposta i criteri di failover di un gruppo di failover su "manuale" tramite il piping nel gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="9af7d-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="9af7d-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9af7d-115">PARAMETERS</span></span>

### <span data-ttu-id="9af7d-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="9af7d-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="9af7d-117">Se le interruzioni nel server secondario devono attivare il failover automatico dell'endpoint di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="9af7d-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="9af7d-118">Questa caratteristica non è ancora supportata.</span><span class="sxs-lookup"><span data-stu-id="9af7d-118">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="9af7d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9af7d-119">-DefaultProfile</span></span>
<span data-ttu-id="9af7d-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9af7d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af7d-121">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="9af7d-121">-FailoverGroupName</span></span>
<span data-ttu-id="9af7d-122">Nome del gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="9af7d-122">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="9af7d-123">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="9af7d-123">-FailoverPolicy</span></span>
<span data-ttu-id="9af7d-124">Criteri di failover del gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="9af7d-124">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="9af7d-125">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="9af7d-125">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="9af7d-126">Intervallo prima che venga avviato il failover automatico se si verifica un'interruzione nel server primario.</span><span class="sxs-lookup"><span data-stu-id="9af7d-126">Interval before automatic failover is initiated if an outage occurs on the primary server.</span></span> <span data-ttu-id="9af7d-127">Ciò indica che il database SQL di Azure non avvierà il failover automatico prima che scada il periodo di tolleranza.</span><span class="sxs-lookup"><span data-stu-id="9af7d-127">This indicates that Azure SQL Database will not initiate automatic failover before the grace period expires.</span></span> <span data-ttu-id="9af7d-128">Tieni presente che l'operazione di failover con l'opzione AllowDataLoss può causare la perdita di dati a causa della natura della sincronizzazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="9af7d-128">Please note that failover operation with AllowDataLoss option might cause data loss due to the nature of asynchronous synchronization.</span></span>

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

### <span data-ttu-id="9af7d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9af7d-129">-ResourceGroupName</span></span>
<span data-ttu-id="9af7d-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9af7d-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="9af7d-131">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="9af7d-131">-ServerName</span></span>
<span data-ttu-id="9af7d-132">Nome del server di database SQL di Azure principale del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="9af7d-132">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="9af7d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9af7d-133">CommonParameters</span></span>
<span data-ttu-id="9af7d-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9af7d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9af7d-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9af7d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9af7d-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9af7d-136">INPUTS</span></span>

### <span data-ttu-id="9af7d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="9af7d-137">System.String</span></span>

## <span data-ttu-id="9af7d-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9af7d-138">OUTPUTS</span></span>

### <span data-ttu-id="9af7d-139">Microsoft. Azure. Commands. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="9af7d-139">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="9af7d-140">Note</span><span class="sxs-lookup"><span data-stu-id="9af7d-140">NOTES</span></span>

## <span data-ttu-id="9af7d-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9af7d-141">RELATED LINKS</span></span>

[<span data-ttu-id="9af7d-142">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9af7d-142">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9af7d-143">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9af7d-143">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9af7d-144">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9af7d-144">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="9af7d-145">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9af7d-145">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="9af7d-146">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9af7d-146">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9af7d-147">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9af7d-147">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9af7d-148">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="9af7d-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
