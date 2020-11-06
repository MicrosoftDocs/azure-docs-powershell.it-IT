---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: b23128d2ef55e971f20569e251601b410b218ec2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507852"
---
# <span data-ttu-id="0992d-101">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="0992d-101">New-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="0992d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0992d-102">SYNOPSIS</span></span>
<span data-ttu-id="0992d-103">Crea un database secondario per un database esistente e avvia la replica dei dati.</span><span class="sxs-lookup"><span data-stu-id="0992d-103">Creates a secondary database for an existing database and starts data replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0992d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0992d-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0992d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0992d-105">DESCRIPTION</span></span>
<span data-ttu-id="0992d-106">Il cmdlet **New-AzureRMSqlDatabaseSecondary** sostituisce il cmdlet Start-AzureSqlDatabaseCopy quando viene usato per configurare la Geo-replica per un database.</span><span class="sxs-lookup"><span data-stu-id="0992d-106">The **New-AzureRMSqlDatabaseSecondary** cmdlet replaces the Start-AzureSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="0992d-107">Viene restituito l'oggetto link di Geo-replica dal database principale a quello secondario.</span><span class="sxs-lookup"><span data-stu-id="0992d-107">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="0992d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0992d-108">EXAMPLES</span></span>

### <span data-ttu-id="0992d-109">1: stabilire Geo-Replication attive</span><span class="sxs-lookup"><span data-stu-id="0992d-109">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzureRmSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzureRmSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

## <span data-ttu-id="0992d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0992d-110">PARAMETERS</span></span>

### <span data-ttu-id="0992d-111">-AllowConnections nella</span><span class="sxs-lookup"><span data-stu-id="0992d-111">-AllowConnections</span></span>
<span data-ttu-id="0992d-112">Specifica lo scopo di lettura del database SQL secondario di Azure.</span><span class="sxs-lookup"><span data-stu-id="0992d-112">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="0992d-113">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0992d-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0992d-114">Non</span><span class="sxs-lookup"><span data-stu-id="0992d-114">No</span></span>
- <span data-ttu-id="0992d-115">Tutti</span><span class="sxs-lookup"><span data-stu-id="0992d-115">All</span></span>

```yaml
Type: AllowConnections
Parameter Sets: (All)
Aliases:
Accepted values: No, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0992d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0992d-116">-AsJob</span></span>
<span data-ttu-id="0992d-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="0992d-117">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0992d-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0992d-118">-DatabaseName</span></span>
<span data-ttu-id="0992d-119">Specifica il nome del database che funge da principale.</span><span class="sxs-lookup"><span data-stu-id="0992d-119">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="0992d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0992d-120">-DefaultProfile</span></span>
<span data-ttu-id="0992d-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0992d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0992d-122">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0992d-122">-PartnerResourceGroupName</span></span>
<span data-ttu-id="0992d-123">Specifica il nome del gruppo di risorse Azure a cui questo cmdlet assegna il database secondario.</span><span class="sxs-lookup"><span data-stu-id="0992d-123">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="0992d-124">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="0992d-124">-PartnerServerName</span></span>
<span data-ttu-id="0992d-125">Specifica il nome del server di database SQL di Azure che funge da secondario.</span><span class="sxs-lookup"><span data-stu-id="0992d-125">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="0992d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0992d-126">-ResourceGroupName</span></span>
<span data-ttu-id="0992d-127">Specifica il nome del gruppo di risorse Azure a cui questo cmdlet assegna il database primario.</span><span class="sxs-lookup"><span data-stu-id="0992d-127">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="0992d-128">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="0992d-128">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="0992d-129">Specifica il nome del pool elastico in cui inserire il database secondario.</span><span class="sxs-lookup"><span data-stu-id="0992d-129">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="0992d-130">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="0992d-130">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="0992d-131">Specifica il nome dell'obiettivo del servizio da assegnare al database secondario.</span><span class="sxs-lookup"><span data-stu-id="0992d-131">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="0992d-132">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="0992d-132">-ServerName</span></span>
<span data-ttu-id="0992d-133">Specifica il nome di SQL Server del database SQL primario.</span><span class="sxs-lookup"><span data-stu-id="0992d-133">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="0992d-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="0992d-134">-Tags</span></span>
<span data-ttu-id="0992d-135">Specifica le coppie chiave-valore nella forma di una tabella hash da associare al collegamento alla replica di database SQL.</span><span class="sxs-lookup"><span data-stu-id="0992d-135">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="0992d-136">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="0992d-136">For example:</span></span>

<span data-ttu-id="0992d-137">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="0992d-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0992d-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0992d-138">-Confirm</span></span>
<span data-ttu-id="0992d-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0992d-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0992d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0992d-140">-WhatIf</span></span>
<span data-ttu-id="0992d-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0992d-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0992d-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0992d-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0992d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0992d-143">CommonParameters</span></span>
<span data-ttu-id="0992d-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0992d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0992d-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0992d-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0992d-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0992d-146">INPUTS</span></span>

### <span data-ttu-id="0992d-147">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0992d-147">None</span></span>
<span data-ttu-id="0992d-148">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="0992d-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0992d-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0992d-149">OUTPUTS</span></span>

### <span data-ttu-id="0992d-150">Microsoft. Azure. Commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="0992d-150">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>
<span data-ttu-id="0992d-151">Questo cmdlet restituisce gli oggetti **ReplicationLink** .</span><span class="sxs-lookup"><span data-stu-id="0992d-151">This cmdlet returns **ReplicationLink** objects.</span></span>

## <span data-ttu-id="0992d-152">Note</span><span class="sxs-lookup"><span data-stu-id="0992d-152">NOTES</span></span>

## <span data-ttu-id="0992d-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0992d-153">RELATED LINKS</span></span>

[<span data-ttu-id="0992d-154">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="0992d-154">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="0992d-155">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="0992d-155">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="0992d-156">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="0992d-156">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
