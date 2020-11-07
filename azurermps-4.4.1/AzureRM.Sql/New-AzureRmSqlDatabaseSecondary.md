---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: 226910b81da287c04adb05574b77713e97c6a045
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685652"
---
# <span data-ttu-id="fb6a5-101">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="fb6a5-101">New-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="fb6a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fb6a5-102">SYNOPSIS</span></span>
<span data-ttu-id="fb6a5-103">Crea un database secondario per un database esistente e avvia la replica dei dati.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-103">Creates a secondary database for an existing database and starts data replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb6a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fb6a5-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fb6a5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb6a5-105">DESCRIPTION</span></span>
<span data-ttu-id="fb6a5-106">Il cmdlet **New-AzureRMSqlDatabaseSecondary** sostituisce il cmdlet Start-AzureSqlDatabaseCopy quando viene usato per configurare la Geo-replica per un database.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-106">The **New-AzureRMSqlDatabaseSecondary** cmdlet replaces the Start-AzureSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="fb6a5-107">Viene restituito l'oggetto link di Geo-replica dal database principale a quello secondario.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-107">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="fb6a5-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fb6a5-108">EXAMPLES</span></span>

### <span data-ttu-id="fb6a5-109">1: stabilire Geo-Replication attive</span><span class="sxs-lookup"><span data-stu-id="fb6a5-109">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzureRmSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzureRmSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

## <span data-ttu-id="fb6a5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fb6a5-110">PARAMETERS</span></span>

### <span data-ttu-id="fb6a5-111">-AllowConnections nella</span><span class="sxs-lookup"><span data-stu-id="fb6a5-111">-AllowConnections</span></span>
<span data-ttu-id="fb6a5-112">Specifica lo scopo di lettura del database SQL secondario di Azure.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-112">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="fb6a5-113">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="fb6a5-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fb6a5-114">Non</span><span class="sxs-lookup"><span data-stu-id="fb6a5-114">No</span></span>
- <span data-ttu-id="fb6a5-115">Tutti</span><span class="sxs-lookup"><span data-stu-id="fb6a5-115">All</span></span>

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

### <span data-ttu-id="fb6a5-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fb6a5-116">-DatabaseName</span></span>
<span data-ttu-id="fb6a5-117">Specifica il nome del database che funge da principale.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-117">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="fb6a5-118">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb6a5-118">-PartnerResourceGroupName</span></span>
<span data-ttu-id="fb6a5-119">Specifica il nome del gruppo di risorse Azure a cui questo cmdlet assegna il database secondario.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-119">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="fb6a5-120">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="fb6a5-120">-PartnerServerName</span></span>
<span data-ttu-id="fb6a5-121">Specifica il nome del server di database SQL di Azure che funge da secondario.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-121">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="fb6a5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb6a5-122">-ResourceGroupName</span></span>
<span data-ttu-id="fb6a5-123">Specifica il nome del gruppo di risorse Azure a cui questo cmdlet assegna il database primario.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-123">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="fb6a5-124">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="fb6a5-124">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="fb6a5-125">Specifica il nome del pool elastico in cui inserire il database secondario.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-125">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="fb6a5-126">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="fb6a5-126">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="fb6a5-127">Specifica il nome dell'obiettivo del servizio da assegnare al database secondario.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-127">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="fb6a5-128">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="fb6a5-128">-ServerName</span></span>
<span data-ttu-id="fb6a5-129">Specifica il nome di SQL Server del database SQL primario.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-129">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="fb6a5-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="fb6a5-130">-Tags</span></span>
<span data-ttu-id="fb6a5-131">Specifica le coppie chiave-valore nella forma di una tabella hash da associare al collegamento alla replica di database SQL.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-131">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="fb6a5-132">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="fb6a5-132">For example:</span></span>

<span data-ttu-id="fb6a5-133">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="fb6a5-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="fb6a5-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fb6a5-134">-Confirm</span></span>
<span data-ttu-id="fb6a5-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb6a5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb6a5-136">-WhatIf</span></span>
<span data-ttu-id="fb6a5-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb6a5-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb6a5-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb6a5-139">-DefaultProfile</span></span>
<span data-ttu-id="fb6a5-140">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb6a5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb6a5-141">CommonParameters</span></span>
<span data-ttu-id="fb6a5-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb6a5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb6a5-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb6a5-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb6a5-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fb6a5-144">INPUTS</span></span>

## <span data-ttu-id="fb6a5-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fb6a5-145">OUTPUTS</span></span>

### <span data-ttu-id="fb6a5-146">Microsoft. Azure. Commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="fb6a5-146">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>
<span data-ttu-id="fb6a5-147">Questo cmdlet restituisce gli oggetti **ReplicationLink** .</span><span class="sxs-lookup"><span data-stu-id="fb6a5-147">This cmdlet returns **ReplicationLink** objects.</span></span>

## <span data-ttu-id="fb6a5-148">Note</span><span class="sxs-lookup"><span data-stu-id="fb6a5-148">NOTES</span></span>

## <span data-ttu-id="fb6a5-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fb6a5-149">RELATED LINKS</span></span>

[<span data-ttu-id="fb6a5-150">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="fb6a5-150">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="fb6a5-151">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="fb6a5-151">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="fb6a5-152">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="fb6a5-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
