---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: f7dbffffe9a51d35ced8861894373322898fd0f8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020426"
---
# <span data-ttu-id="251bd-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="251bd-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="251bd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="251bd-102">SYNOPSIS</span></span>
<span data-ttu-id="251bd-103">Crea un database secondario per un database esistente e avvia la replica dei dati.</span><span class="sxs-lookup"><span data-stu-id="251bd-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="251bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="251bd-104">SYNTAX</span></span>

### <span data-ttu-id="251bd-105">DtuBasedDatabase (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="251bd-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="251bd-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="251bd-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="251bd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="251bd-107">DESCRIPTION</span></span>
<span data-ttu-id="251bd-108">Il cmdlet **New-AzSqlDatabaseSecondary** sostituisce il cmdlet Start-AzSqlDatabaseCopy quando viene usato per configurare la Geo-replica per un database.</span><span class="sxs-lookup"><span data-stu-id="251bd-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="251bd-109">Viene restituito l'oggetto link di Geo-replica dal database principale a quello secondario.</span><span class="sxs-lookup"><span data-stu-id="251bd-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="251bd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="251bd-110">EXAMPLES</span></span>

### <span data-ttu-id="251bd-111">1: stabilire Geo-Replication attive</span><span class="sxs-lookup"><span data-stu-id="251bd-111">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

### <span data-ttu-id="251bd-112">2: stabilire Geo-Replication attivi e specificare il nome del database partner in modo che sia diverso dal nome del database di origine</span><span class="sxs-lookup"><span data-stu-id="251bd-112">2: Establish Active Geo-Replication and specify the partner database name to be different than the source database name</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -PartnerDatabaseName $secondarydatabasename -AllowConnections "All"
```

## <span data-ttu-id="251bd-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="251bd-113">PARAMETERS</span></span>

### <span data-ttu-id="251bd-114">-AllowConnections nella</span><span class="sxs-lookup"><span data-stu-id="251bd-114">-AllowConnections</span></span>
<span data-ttu-id="251bd-115">Specifica lo scopo di lettura del database SQL secondario di Azure.</span><span class="sxs-lookup"><span data-stu-id="251bd-115">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="251bd-116">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="251bd-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="251bd-117">Non</span><span class="sxs-lookup"><span data-stu-id="251bd-117">No</span></span>
- <span data-ttu-id="251bd-118">Tutti</span><span class="sxs-lookup"><span data-stu-id="251bd-118">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Replication.Model.AllowConnections
Parameter Sets: (All)
Aliases:
Accepted values: No, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="251bd-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="251bd-119">-AsJob</span></span>
<span data-ttu-id="251bd-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="251bd-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="251bd-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="251bd-121">-DatabaseName</span></span>
<span data-ttu-id="251bd-122">Specifica il nome del database che funge da principale.</span><span class="sxs-lookup"><span data-stu-id="251bd-122">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="251bd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="251bd-123">-DefaultProfile</span></span>
<span data-ttu-id="251bd-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="251bd-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="251bd-125">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="251bd-125">-LicenseType</span></span>
<span data-ttu-id="251bd-126">Tipo di licenza per il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="251bd-126">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="251bd-127">-PartnerDatabaseName</span><span class="sxs-lookup"><span data-stu-id="251bd-127">-PartnerDatabaseName</span></span>
<span data-ttu-id="251bd-128">Nome del database secondario da creare.</span><span class="sxs-lookup"><span data-stu-id="251bd-128">The name of the secondary database to create.</span></span>

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

### <span data-ttu-id="251bd-129">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="251bd-129">-PartnerResourceGroupName</span></span>
<span data-ttu-id="251bd-130">Specifica il nome del gruppo di risorse Azure a cui questo cmdlet assegna il database secondario.</span><span class="sxs-lookup"><span data-stu-id="251bd-130">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="251bd-131">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="251bd-131">-PartnerServerName</span></span>
<span data-ttu-id="251bd-132">Specifica il nome del server di database SQL di Azure che funge da secondario.</span><span class="sxs-lookup"><span data-stu-id="251bd-132">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="251bd-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="251bd-133">-ResourceGroupName</span></span>
<span data-ttu-id="251bd-134">Specifica il nome del gruppo di risorse Azure a cui questo cmdlet assegna il database primario.</span><span class="sxs-lookup"><span data-stu-id="251bd-134">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="251bd-135">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="251bd-135">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="251bd-136">La generazione di calcolo del database SQL di Azure secondario.</span><span class="sxs-lookup"><span data-stu-id="251bd-136">The compute generation of the Azure Sql Database secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="251bd-137">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="251bd-137">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="251bd-138">Specifica il nome del pool elastico in cui inserire il database secondario.</span><span class="sxs-lookup"><span data-stu-id="251bd-138">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="251bd-139">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="251bd-139">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="251bd-140">Specifica il nome dell'obiettivo del servizio da assegnare al database secondario.</span><span class="sxs-lookup"><span data-stu-id="251bd-140">Specifies the name of the service objective to assign to the secondary database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="251bd-141">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="251bd-141">-SecondaryVCore</span></span>
<span data-ttu-id="251bd-142">I numeri Vcore del database SQL di Azure secondario.</span><span class="sxs-lookup"><span data-stu-id="251bd-142">The Vcore numbers of the Azure Sql Database secondary.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="251bd-143">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="251bd-143">-ServerName</span></span>
<span data-ttu-id="251bd-144">Specifica il nome di SQL Server del database SQL primario.</span><span class="sxs-lookup"><span data-stu-id="251bd-144">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="251bd-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="251bd-145">-Tags</span></span>
<span data-ttu-id="251bd-146">Specifica le coppie chiave-valore nella forma di una tabella hash da associare al collegamento alla replica di database SQL.</span><span class="sxs-lookup"><span data-stu-id="251bd-146">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="251bd-147">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="251bd-147">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="251bd-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="251bd-148">-Confirm</span></span>
<span data-ttu-id="251bd-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="251bd-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="251bd-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="251bd-150">-WhatIf</span></span>
<span data-ttu-id="251bd-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="251bd-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="251bd-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="251bd-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="251bd-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="251bd-153">CommonParameters</span></span>
<span data-ttu-id="251bd-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="251bd-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="251bd-155">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="251bd-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="251bd-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="251bd-156">INPUTS</span></span>

### <span data-ttu-id="251bd-157">System. String</span><span class="sxs-lookup"><span data-stu-id="251bd-157">System.String</span></span>

## <span data-ttu-id="251bd-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="251bd-158">OUTPUTS</span></span>

### <span data-ttu-id="251bd-159">Microsoft. Azure. Commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="251bd-159">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="251bd-160">Note</span><span class="sxs-lookup"><span data-stu-id="251bd-160">NOTES</span></span>

## <span data-ttu-id="251bd-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="251bd-161">RELATED LINKS</span></span>

[<span data-ttu-id="251bd-162">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="251bd-162">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="251bd-163">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="251bd-163">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="251bd-164">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="251bd-164">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
