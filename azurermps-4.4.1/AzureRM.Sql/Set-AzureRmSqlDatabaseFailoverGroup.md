---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 05f2de37ebeb477d45f96c415759ead3080a9e60
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514651"
---
# <span data-ttu-id="9f0d4-101">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9f0d4-101">Set-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="9f0d4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9f0d4-102">SYNOPSIS</span></span>
<span data-ttu-id="9f0d4-103">Modifica la configurazione di un gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="9f0d4-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f0d4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9f0d4-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f0d4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9f0d4-105">DESCRIPTION</span></span>
<span data-ttu-id="9f0d4-106">Questo comando consente di modificare la configurazione di un gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="9f0d4-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>

<span data-ttu-id="9f0d4-107">Il server principale del gruppo di failover deve essere usato per eseguire il comando.</span><span class="sxs-lookup"><span data-stu-id="9f0d4-107">The Failover Group's primary server should be used to execute the command.</span></span>

<span data-ttu-id="9f0d4-108">Per controllare il set di database nel gruppo, USA invece ' Add-AzureRmSqlDatabaseToFailoverGroup ' è Remove-AzureRmSqlDatabaseFromFailoverGroup '.</span><span class="sxs-lookup"><span data-stu-id="9f0d4-108">To control the set of databases in the group, use 'Add-AzureRmSqlDatabaseToFailoverGroup' and 'Remove-AzureRmSqlDatabaseFromFailoverGroup' instead.</span></span>

<span data-ttu-id="9f0d4-109">Durante l'anteprima della caratteristica gruppi di failover, per il parametro '-GracePeriodWithDataLossHours ' sono supportati solo i valori maggiori o uguali a 1 ora.</span><span class="sxs-lookup"><span data-stu-id="9f0d4-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="9f0d4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9f0d4-110">EXAMPLES</span></span>

### <span data-ttu-id="9f0d4-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9f0d4-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="9f0d4-112">Imposta i criteri di failover di un gruppo di failover su "automatico".</span><span class="sxs-lookup"><span data-stu-id="9f0d4-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="9f0d4-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9f0d4-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzureRmSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="9f0d4-114">Imposta i criteri di failover di un gruppo di failover su "manuale" tramite il piping nel gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="9f0d4-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="9f0d4-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9f0d4-115">PARAMETERS</span></span>

### <span data-ttu-id="9f0d4-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="9f0d4-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="9f0d4-117">Se le interruzioni nel server secondario devono attivare il failover automatico dell'endpoint di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="9f0d4-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="9f0d4-118">Questa caratteristica non è ancora supportata.</span><span class="sxs-lookup"><span data-stu-id="9f0d4-118">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="9f0d4-119">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="9f0d4-119">-FailoverGroupName</span></span>
<span data-ttu-id="9f0d4-120">Nome del gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="9f0d4-120">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="9f0d4-121">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="9f0d4-121">-FailoverPolicy</span></span>
<span data-ttu-id="9f0d4-122">Criteri di failover del gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="9f0d4-122">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="9f0d4-123">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="9f0d4-123">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="9f0d4-124">Intervallo prima che venga avviato il failover automatico se si verifica un'interruzione nel server primario e non è possibile completare il failover senza perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="9f0d4-124">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="9f0d4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f0d4-125">-ResourceGroupName</span></span>
<span data-ttu-id="9f0d4-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9f0d4-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="9f0d4-127">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="9f0d4-127">-ServerName</span></span>
<span data-ttu-id="9f0d4-128">Nome del server di database SQL di Azure principale del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="9f0d4-128">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="9f0d4-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f0d4-129">-DefaultProfile</span></span>
<span data-ttu-id="9f0d4-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9f0d4-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f0d4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f0d4-131">CommonParameters</span></span>
<span data-ttu-id="9f0d4-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f0d4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f0d4-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f0d4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f0d4-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9f0d4-134">INPUTS</span></span>

### <span data-ttu-id="9f0d4-135">System. String</span><span class="sxs-lookup"><span data-stu-id="9f0d4-135">System.String</span></span>

## <span data-ttu-id="9f0d4-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9f0d4-136">OUTPUTS</span></span>

### <span data-ttu-id="9f0d4-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="9f0d4-137">System.Object</span></span>

## <span data-ttu-id="9f0d4-138">Note</span><span class="sxs-lookup"><span data-stu-id="9f0d4-138">NOTES</span></span>

## <span data-ttu-id="9f0d4-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9f0d4-139">RELATED LINKS</span></span>

[<span data-ttu-id="9f0d4-140">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9f0d4-140">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9f0d4-141">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9f0d4-141">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9f0d4-142">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9f0d4-142">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="9f0d4-143">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9f0d4-143">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="9f0d4-144">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9f0d4-144">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9f0d4-145">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9f0d4-145">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9f0d4-146">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="9f0d4-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
