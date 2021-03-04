---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 983291eda139793b2cc5d0fe5cd213b5d8cd69a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982029"
---
# <span data-ttu-id="d0309-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d0309-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="d0309-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0309-102">SYNOPSIS</span></span>
<span data-ttu-id="d0309-103">Crea un database secondario per un database esistente e avvia la replica dei dati.</span><span class="sxs-lookup"><span data-stu-id="d0309-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="d0309-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0309-104">SYNTAX</span></span>

### <span data-ttu-id="d0309-105">DtuBasedDatabase (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d0309-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d0309-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="d0309-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d0309-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d0309-107">DESCRIPTION</span></span>
<span data-ttu-id="d0309-108">Il cmdlet **New-AzSqlDatabaseSecondary** sostituisce il cmdlet Start-AzSqlDatabaseCopy quando viene usato per configurare la replica geografica per un database.</span><span class="sxs-lookup"><span data-stu-id="d0309-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="d0309-109">Restituisce l'oggetto collegamento di replica geografica dal database primario al database secondario.</span><span class="sxs-lookup"><span data-stu-id="d0309-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="d0309-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0309-110">EXAMPLES</span></span>

### <span data-ttu-id="d0309-111">Esempio 1: Stabilire le Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="d0309-111">Example 1: Establish Active Geo-Replication</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

### <span data-ttu-id="d0309-112">Esempio 2: Stabilire la Geo-Replication e specificare che il nome del database partner sia diverso dal nome del database di origine</span><span class="sxs-lookup"><span data-stu-id="d0309-112">Example 2: Establish Active Geo-Replication and specify the partner database name to be different than the source database name</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -PartnerDatabaseName $secondarydatabasename -AllowConnections "All"
```

## <span data-ttu-id="d0309-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0309-113">PARAMETERS</span></span>

### <span data-ttu-id="d0309-114">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="d0309-114">-AllowConnections</span></span>
<span data-ttu-id="d0309-115">Specifica lo scopo di lettura del database SQL Azure secondario.</span><span class="sxs-lookup"><span data-stu-id="d0309-115">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="d0309-116">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="d0309-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d0309-117">No</span><span class="sxs-lookup"><span data-stu-id="d0309-117">No</span></span>
- <span data-ttu-id="d0309-118">Tutti</span><span class="sxs-lookup"><span data-stu-id="d0309-118">All</span></span>

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

### <span data-ttu-id="d0309-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0309-119">-AsJob</span></span>
<span data-ttu-id="d0309-120">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d0309-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d0309-121">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="d0309-121">-BackupStorageRedundancy</span></span>
<span data-ttu-id="d0309-122">Ridondanza di archiviazione di backup usata per archiviare i backup per SQL database.</span><span class="sxs-lookup"><span data-stu-id="d0309-122">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="d0309-123">Le opzioni disponibili sono: Locale, Area e Geo.</span><span class="sxs-lookup"><span data-stu-id="d0309-123">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="d0309-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d0309-124">-DatabaseName</span></span>
<span data-ttu-id="d0309-125">Specifica il nome del database da utilizzare come principale.</span><span class="sxs-lookup"><span data-stu-id="d0309-125">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="d0309-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0309-126">-DefaultProfile</span></span>
<span data-ttu-id="d0309-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="d0309-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0309-128">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="d0309-128">-LicenseType</span></span>
<span data-ttu-id="d0309-129">Il tipo di licenza per il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="d0309-129">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="d0309-130">-PartnerDatabaseName</span><span class="sxs-lookup"><span data-stu-id="d0309-130">-PartnerDatabaseName</span></span>
<span data-ttu-id="d0309-131">Nome del database secondario da creare.</span><span class="sxs-lookup"><span data-stu-id="d0309-131">The name of the secondary database to create.</span></span>

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

### <span data-ttu-id="d0309-132">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0309-132">-PartnerResourceGroupName</span></span>
<span data-ttu-id="d0309-133">Specifica il nome del gruppo di risorse di Azure a cui questo cmdlet assegna il database secondario.</span><span class="sxs-lookup"><span data-stu-id="d0309-133">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="d0309-134">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="d0309-134">-PartnerServerName</span></span>
<span data-ttu-id="d0309-135">Specifica il nome del server di database SQL Azure che deve agire come secondario.</span><span class="sxs-lookup"><span data-stu-id="d0309-135">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="d0309-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0309-136">-ResourceGroupName</span></span>
<span data-ttu-id="d0309-137">Specifica il nome del gruppo di risorse di Azure a cui questo cmdlet assegna il database primario.</span><span class="sxs-lookup"><span data-stu-id="d0309-137">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="d0309-138">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="d0309-138">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="d0309-139">Generazione di calcolo del database SQL di Azure secondario.</span><span class="sxs-lookup"><span data-stu-id="d0309-139">The compute generation of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="d0309-140">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="d0309-140">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="d0309-141">Specifica il nome del pool flessibile in cui inserire il database secondario.</span><span class="sxs-lookup"><span data-stu-id="d0309-141">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="d0309-142">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="d0309-142">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="d0309-143">Specifica il nome dell'obiettivo del servizio da assegnare al database secondario.</span><span class="sxs-lookup"><span data-stu-id="d0309-143">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="d0309-144">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="d0309-144">-SecondaryType</span></span>
<span data-ttu-id="d0309-145">Tipo secondario del database, se secondario.</span><span class="sxs-lookup"><span data-stu-id="d0309-145">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="d0309-146">I valori validi sono Geo e Denominato.</span><span class="sxs-lookup"><span data-stu-id="d0309-146">Valid values are Geo and Named.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Named, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0309-147">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="d0309-147">-SecondaryVCore</span></span>
<span data-ttu-id="d0309-148">Numeri Vcore del database SQL di Azure secondario.</span><span class="sxs-lookup"><span data-stu-id="d0309-148">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="d0309-149">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d0309-149">-ServerName</span></span>
<span data-ttu-id="d0309-150">Specifica il nome dell'SQL Server del database SQL primario.</span><span class="sxs-lookup"><span data-stu-id="d0309-150">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="d0309-151">-Tag</span><span class="sxs-lookup"><span data-stu-id="d0309-151">-Tags</span></span>
<span data-ttu-id="d0309-152">Specifica le coppie chiave-valore sotto forma di tabella hash da associare al collegamento di replica SQL database locale.</span><span class="sxs-lookup"><span data-stu-id="d0309-152">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="d0309-153">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="d0309-153">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d0309-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0309-154">-Confirm</span></span>
<span data-ttu-id="d0309-155">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0309-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0309-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0309-156">-WhatIf</span></span>
<span data-ttu-id="d0309-157">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0309-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0309-158">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0309-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0309-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0309-159">CommonParameters</span></span>
<span data-ttu-id="d0309-160">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0309-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0309-161">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d0309-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0309-162">INPUT</span><span class="sxs-lookup"><span data-stu-id="d0309-162">INPUTS</span></span>

### <span data-ttu-id="d0309-163">System.String</span><span class="sxs-lookup"><span data-stu-id="d0309-163">System.String</span></span>

## <span data-ttu-id="d0309-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0309-164">OUTPUTS</span></span>

### <span data-ttu-id="d0309-165">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="d0309-165">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="d0309-166">NOTE</span><span class="sxs-lookup"><span data-stu-id="d0309-166">NOTES</span></span>

## <span data-ttu-id="d0309-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0309-167">RELATED LINKS</span></span>

[<span data-ttu-id="d0309-168">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d0309-168">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="d0309-169">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d0309-169">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="d0309-170">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="d0309-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
