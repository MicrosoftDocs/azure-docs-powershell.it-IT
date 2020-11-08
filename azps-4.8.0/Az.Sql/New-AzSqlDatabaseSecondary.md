---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 0b0934ffe9a5721ff08438ca7a24d97e2b4a34cd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032111"
---
# <span data-ttu-id="6f89a-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6f89a-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="6f89a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6f89a-102">SYNOPSIS</span></span>
<span data-ttu-id="6f89a-103">Crea un database secondario per un database esistente e avvia la replica dei dati.</span><span class="sxs-lookup"><span data-stu-id="6f89a-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="6f89a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6f89a-104">SYNTAX</span></span>

### <span data-ttu-id="6f89a-105">DtuBasedDatabase (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6f89a-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f89a-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="6f89a-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f89a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6f89a-107">DESCRIPTION</span></span>
<span data-ttu-id="6f89a-108">Il cmdlet **New-AzSqlDatabaseSecondary** sostituisce il cmdlet Start-AzSqlDatabaseCopy quando viene usato per configurare la Geo-replica per un database.</span><span class="sxs-lookup"><span data-stu-id="6f89a-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="6f89a-109">Viene restituito l'oggetto link di Geo-replica dal database principale a quello secondario.</span><span class="sxs-lookup"><span data-stu-id="6f89a-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="6f89a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6f89a-110">EXAMPLES</span></span>

### <span data-ttu-id="6f89a-111">Esempio 1: stabilire Geo-Replication attivi</span><span class="sxs-lookup"><span data-stu-id="6f89a-111">Example 1: Establish Active Geo-Replication</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

### <span data-ttu-id="6f89a-112">Esempio 2: stabilire Geo-Replication attivi e specificare il nome del database partner in modo che sia diverso dal nome del database di origine</span><span class="sxs-lookup"><span data-stu-id="6f89a-112">Example 2: Establish Active Geo-Replication and specify the partner database name to be different than the source database name</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -PartnerDatabaseName $secondarydatabasename -AllowConnections "All"
```

## <span data-ttu-id="6f89a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6f89a-113">PARAMETERS</span></span>

### <span data-ttu-id="6f89a-114">-AllowConnections nella</span><span class="sxs-lookup"><span data-stu-id="6f89a-114">-AllowConnections</span></span>
<span data-ttu-id="6f89a-115">Specifica lo scopo di lettura del database SQL secondario di Azure.</span><span class="sxs-lookup"><span data-stu-id="6f89a-115">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="6f89a-116">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="6f89a-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6f89a-117">Non</span><span class="sxs-lookup"><span data-stu-id="6f89a-117">No</span></span>
- <span data-ttu-id="6f89a-118">Tutti</span><span class="sxs-lookup"><span data-stu-id="6f89a-118">All</span></span>

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

### <span data-ttu-id="6f89a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f89a-119">-AsJob</span></span>
<span data-ttu-id="6f89a-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6f89a-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6f89a-121">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="6f89a-121">-BackupStorageRedundancy</span></span>
<span data-ttu-id="6f89a-122">Ridondanza dello spazio di archiviazione di backup utilizzata per archiviare i backup per il database SQL.</span><span class="sxs-lookup"><span data-stu-id="6f89a-122">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="6f89a-123">Le opzioni disponibili sono: locale, zona e geo.</span><span class="sxs-lookup"><span data-stu-id="6f89a-123">Options are: Local, Zone and Geo.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f89a-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6f89a-124">-DatabaseName</span></span>
<span data-ttu-id="6f89a-125">Specifica il nome del database che funge da principale.</span><span class="sxs-lookup"><span data-stu-id="6f89a-125">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="6f89a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f89a-126">-DefaultProfile</span></span>
<span data-ttu-id="6f89a-127">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6f89a-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f89a-128">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="6f89a-128">-LicenseType</span></span>
<span data-ttu-id="6f89a-129">Tipo di licenza per il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="6f89a-129">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="6f89a-130">-PartnerDatabaseName</span><span class="sxs-lookup"><span data-stu-id="6f89a-130">-PartnerDatabaseName</span></span>
<span data-ttu-id="6f89a-131">Nome del database secondario da creare.</span><span class="sxs-lookup"><span data-stu-id="6f89a-131">The name of the secondary database to create.</span></span>

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

### <span data-ttu-id="6f89a-132">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f89a-132">-PartnerResourceGroupName</span></span>
<span data-ttu-id="6f89a-133">Specifica il nome del gruppo di risorse Azure a cui questo cmdlet assegna il database secondario.</span><span class="sxs-lookup"><span data-stu-id="6f89a-133">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="6f89a-134">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="6f89a-134">-PartnerServerName</span></span>
<span data-ttu-id="6f89a-135">Specifica il nome del server di database SQL di Azure che funge da secondario.</span><span class="sxs-lookup"><span data-stu-id="6f89a-135">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="6f89a-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f89a-136">-ResourceGroupName</span></span>
<span data-ttu-id="6f89a-137">Specifica il nome del gruppo di risorse Azure a cui questo cmdlet assegna il database primario.</span><span class="sxs-lookup"><span data-stu-id="6f89a-137">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="6f89a-138">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="6f89a-138">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="6f89a-139">La generazione di calcolo del database SQL di Azure secondario.</span><span class="sxs-lookup"><span data-stu-id="6f89a-139">The compute generation of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="6f89a-140">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="6f89a-140">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="6f89a-141">Specifica il nome del pool elastico in cui inserire il database secondario.</span><span class="sxs-lookup"><span data-stu-id="6f89a-141">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="6f89a-142">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="6f89a-142">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="6f89a-143">Specifica il nome dell'obiettivo del servizio da assegnare al database secondario.</span><span class="sxs-lookup"><span data-stu-id="6f89a-143">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="6f89a-144">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="6f89a-144">-SecondaryVCore</span></span>
<span data-ttu-id="6f89a-145">I numeri Vcore del database SQL di Azure secondario.</span><span class="sxs-lookup"><span data-stu-id="6f89a-145">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="6f89a-146">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="6f89a-146">-ServerName</span></span>
<span data-ttu-id="6f89a-147">Specifica il nome di SQL Server del database SQL primario.</span><span class="sxs-lookup"><span data-stu-id="6f89a-147">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="6f89a-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="6f89a-148">-Tags</span></span>
<span data-ttu-id="6f89a-149">Specifica le coppie chiave-valore nella forma di una tabella hash da associare al collegamento alla replica di database SQL.</span><span class="sxs-lookup"><span data-stu-id="6f89a-149">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="6f89a-150">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="6f89a-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6f89a-151">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6f89a-151">-Confirm</span></span>
<span data-ttu-id="6f89a-152">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f89a-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f89a-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f89a-153">-WhatIf</span></span>
<span data-ttu-id="6f89a-154">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6f89a-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f89a-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6f89a-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f89a-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f89a-156">CommonParameters</span></span>
<span data-ttu-id="6f89a-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f89a-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f89a-158">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f89a-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f89a-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6f89a-159">INPUTS</span></span>

### <span data-ttu-id="6f89a-160">System. String</span><span class="sxs-lookup"><span data-stu-id="6f89a-160">System.String</span></span>

## <span data-ttu-id="6f89a-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6f89a-161">OUTPUTS</span></span>

### <span data-ttu-id="6f89a-162">Microsoft. Azure. Commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="6f89a-162">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="6f89a-163">Note</span><span class="sxs-lookup"><span data-stu-id="6f89a-163">NOTES</span></span>

## <span data-ttu-id="6f89a-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6f89a-164">RELATED LINKS</span></span>

[<span data-ttu-id="6f89a-165">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6f89a-165">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="6f89a-166">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="6f89a-166">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="6f89a-167">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="6f89a-167">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
