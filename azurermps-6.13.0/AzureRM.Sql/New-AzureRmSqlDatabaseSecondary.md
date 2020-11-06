---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: d2af2095198cf0a1102e3422716013f2f2e02fc6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513371"
---
# <span data-ttu-id="4b43e-101">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="4b43e-101">New-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="4b43e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4b43e-102">SYNOPSIS</span></span>
<span data-ttu-id="4b43e-103">Crea un database secondario per un database esistente e avvia la replica dei dati.</span><span class="sxs-lookup"><span data-stu-id="4b43e-103">Creates a secondary database for an existing database and starts data replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b43e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4b43e-104">SYNTAX</span></span>

### <span data-ttu-id="4b43e-105">DtuBasedDatabase (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4b43e-105">DtuBasedDatabase (Default)</span></span>
```
New-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob] [-LicenseType <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b43e-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="4b43e-106">VcoreBasedDatabase</span></span>
```
New-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4b43e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b43e-107">DESCRIPTION</span></span>
<span data-ttu-id="4b43e-108">Il cmdlet **New-AzureRMSqlDatabaseSecondary** sostituisce il cmdlet Start-AzureSqlDatabaseCopy quando viene usato per configurare la Geo-replica per un database.</span><span class="sxs-lookup"><span data-stu-id="4b43e-108">The **New-AzureRMSqlDatabaseSecondary** cmdlet replaces the Start-AzureSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="4b43e-109">Viene restituito l'oggetto link di Geo-replica dal database principale a quello secondario.</span><span class="sxs-lookup"><span data-stu-id="4b43e-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="4b43e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4b43e-110">EXAMPLES</span></span>

### <span data-ttu-id="4b43e-111">1: stabilire Geo-Replication attive</span><span class="sxs-lookup"><span data-stu-id="4b43e-111">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzureRmSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzureRmSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

## <span data-ttu-id="4b43e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4b43e-112">PARAMETERS</span></span>

### <span data-ttu-id="4b43e-113">-AllowConnections nella</span><span class="sxs-lookup"><span data-stu-id="4b43e-113">-AllowConnections</span></span>
<span data-ttu-id="4b43e-114">Specifica lo scopo di lettura del database SQL secondario di Azure.</span><span class="sxs-lookup"><span data-stu-id="4b43e-114">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="4b43e-115">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4b43e-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4b43e-116">Non</span><span class="sxs-lookup"><span data-stu-id="4b43e-116">No</span></span>
- <span data-ttu-id="4b43e-117">Tutti</span><span class="sxs-lookup"><span data-stu-id="4b43e-117">All</span></span>

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

### <span data-ttu-id="4b43e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4b43e-118">-AsJob</span></span>
<span data-ttu-id="4b43e-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4b43e-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4b43e-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4b43e-120">-DatabaseName</span></span>
<span data-ttu-id="4b43e-121">Specifica il nome del database che funge da principale.</span><span class="sxs-lookup"><span data-stu-id="4b43e-121">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="4b43e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b43e-122">-DefaultProfile</span></span>
<span data-ttu-id="4b43e-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4b43e-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b43e-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="4b43e-124">-LicenseType</span></span>
<span data-ttu-id="4b43e-125">Tipo di licenza per il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4b43e-125">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="4b43e-126">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b43e-126">-PartnerResourceGroupName</span></span>
<span data-ttu-id="4b43e-127">Specifica il nome del gruppo di risorse Azure a cui questo cmdlet assegna il database secondario.</span><span class="sxs-lookup"><span data-stu-id="4b43e-127">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="4b43e-128">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="4b43e-128">-PartnerServerName</span></span>
<span data-ttu-id="4b43e-129">Specifica il nome del server di database SQL di Azure che funge da secondario.</span><span class="sxs-lookup"><span data-stu-id="4b43e-129">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="4b43e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b43e-130">-ResourceGroupName</span></span>
<span data-ttu-id="4b43e-131">Specifica il nome del gruppo di risorse Azure a cui questo cmdlet assegna il database primario.</span><span class="sxs-lookup"><span data-stu-id="4b43e-131">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="4b43e-132">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="4b43e-132">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="4b43e-133">La generazione di calcolo del database SQL di Azure secondario.</span><span class="sxs-lookup"><span data-stu-id="4b43e-133">The compute generation of teh Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="4b43e-134">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="4b43e-134">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="4b43e-135">Specifica il nome del pool elastico in cui inserire il database secondario.</span><span class="sxs-lookup"><span data-stu-id="4b43e-135">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="4b43e-136">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="4b43e-136">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="4b43e-137">Specifica il nome dell'obiettivo del servizio da assegnare al database secondario.</span><span class="sxs-lookup"><span data-stu-id="4b43e-137">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="4b43e-138">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="4b43e-138">-SecondaryVCore</span></span>
<span data-ttu-id="4b43e-139">I numeri Vcore del database SQL di Azure secondario.</span><span class="sxs-lookup"><span data-stu-id="4b43e-139">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="4b43e-140">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="4b43e-140">-ServerName</span></span>
<span data-ttu-id="4b43e-141">Specifica il nome di SQL Server del database SQL primario.</span><span class="sxs-lookup"><span data-stu-id="4b43e-141">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="4b43e-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="4b43e-142">-Tags</span></span>
<span data-ttu-id="4b43e-143">Specifica le coppie chiave-valore nella forma di una tabella hash da associare al collegamento alla replica di database SQL.</span><span class="sxs-lookup"><span data-stu-id="4b43e-143">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="4b43e-144">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="4b43e-144">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4b43e-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4b43e-145">-Confirm</span></span>
<span data-ttu-id="4b43e-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b43e-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b43e-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b43e-147">-WhatIf</span></span>
<span data-ttu-id="4b43e-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4b43e-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b43e-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4b43e-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b43e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b43e-150">CommonParameters</span></span>
<span data-ttu-id="4b43e-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b43e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b43e-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b43e-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b43e-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4b43e-153">INPUTS</span></span>

### <span data-ttu-id="4b43e-154">System. String</span><span class="sxs-lookup"><span data-stu-id="4b43e-154">System.String</span></span>

## <span data-ttu-id="4b43e-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4b43e-155">OUTPUTS</span></span>

### <span data-ttu-id="4b43e-156">Microsoft. Azure. Commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="4b43e-156">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="4b43e-157">Note</span><span class="sxs-lookup"><span data-stu-id="4b43e-157">NOTES</span></span>

## <span data-ttu-id="4b43e-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4b43e-158">RELATED LINKS</span></span>

[<span data-ttu-id="4b43e-159">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="4b43e-159">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="4b43e-160">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="4b43e-160">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="4b43e-161">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="4b43e-161">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
