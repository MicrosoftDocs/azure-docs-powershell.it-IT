---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
ms.openlocfilehash: 7019fc7345b4296d9c35f11c6acec5bf5a42d966
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520596"
---
# <span data-ttu-id="ee9ba-101">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="ee9ba-101">New-AzureRmSqlDatabaseCopy</span></span>

## <span data-ttu-id="ee9ba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ee9ba-102">SYNOPSIS</span></span>
<span data-ttu-id="ee9ba-103">Crea una copia di un database SQL che usa lo snapshot in corrispondenza dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="ee9ba-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee9ba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee9ba-104">SYNTAX</span></span>

### <span data-ttu-id="ee9ba-105">DtuBasedDatabase (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ee9ba-105">DtuBasedDatabase (Default)</span></span>
```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>]
 -CopyDatabaseName <String> [-AsJob] [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ee9ba-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="ee9ba-106">VcoreBasedDatabase</span></span>
```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-Tags <Hashtable>] [-CopyResourceGroupName <String>]
 [-CopyServerName <String>] -CopyDatabaseName <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee9ba-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee9ba-107">DESCRIPTION</span></span>
<span data-ttu-id="ee9ba-108">Il cmdlet **New-AzureRmSqlDatabaseCopy** crea una copia di un database SQL di Azure che usa lo snapshot dei dati in corrispondenza dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="ee9ba-108">The **New-AzureRmSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="ee9ba-109">Usa questo cmdlet invece del cmdlet Start-AzureSqlDatabaseCopy per creare una copia di un database unica.</span><span class="sxs-lookup"><span data-stu-id="ee9ba-109">Use this cmdlet instead of the Start-AzureSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="ee9ba-110">Questo cmdlet restituisce l'oggetto di **database** della copia.</span><span class="sxs-lookup"><span data-stu-id="ee9ba-110">This cmdlet returns the **Database** object of the copy.</span></span>
<span data-ttu-id="ee9ba-111">Nota: usare il cmdlet New-AzureRmSqlDatabaseSecondary per configurare la replica geografica per un database.</span><span class="sxs-lookup"><span data-stu-id="ee9ba-111">Note: Use the New-AzureRmSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>
<span data-ttu-id="ee9ba-112">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="ee9ba-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ee9ba-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee9ba-113">EXAMPLES</span></span>

## <span data-ttu-id="ee9ba-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ee9ba-114">PARAMETERS</span></span>

### <span data-ttu-id="ee9ba-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee9ba-115">-AsJob</span></span>
<span data-ttu-id="ee9ba-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ee9ba-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ee9ba-117">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="ee9ba-117">-ComputeGeneration</span></span>
<span data-ttu-id="ee9ba-118">Generazione di Compute da assegnare alla nuova copia.</span><span class="sxs-lookup"><span data-stu-id="ee9ba-118">The compute generation to assign to the new copy.</span></span>

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

### <span data-ttu-id="ee9ba-119">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="ee9ba-119">-CopyDatabaseName</span></span>
<span data-ttu-id="ee9ba-120">Specifica il nome della copia del database SQL.</span><span class="sxs-lookup"><span data-stu-id="ee9ba-120">Specifies the name of the SQL Database copy.</span></span>

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

### <span data-ttu-id="ee9ba-121">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee9ba-121">-CopyResourceGroupName</span></span>
<span data-ttu-id="ee9ba-122">Specifica il nome del gruppo di risorse Azure in cui assegnare la copia.</span><span class="sxs-lookup"><span data-stu-id="ee9ba-122">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

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

### <span data-ttu-id="ee9ba-123">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="ee9ba-123">-CopyServerName</span></span>
<span data-ttu-id="ee9ba-124">Specifica il nome di SQL Server che ospita la copia.</span><span class="sxs-lookup"><span data-stu-id="ee9ba-124">Specifies the name of the SQL Server which hosts the copy.</span></span>

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

### <span data-ttu-id="ee9ba-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ee9ba-125">-DatabaseName</span></span>
<span data-ttu-id="ee9ba-126">Specifica il nome del database SQL da copiare.</span><span class="sxs-lookup"><span data-stu-id="ee9ba-126">Specifies the name of the SQL Database to copy.</span></span>

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

### <span data-ttu-id="ee9ba-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee9ba-127">-DefaultProfile</span></span>
<span data-ttu-id="ee9ba-128">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ee9ba-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee9ba-129">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="ee9ba-129">-ElasticPoolName</span></span>
<span data-ttu-id="ee9ba-130">Specifica il nome del pool elastico in cui assegnare la copia.</span><span class="sxs-lookup"><span data-stu-id="ee9ba-130">Specifies the name of the elastic pool in which to assign the copy.</span></span>

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

### <span data-ttu-id="ee9ba-131">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ee9ba-131">-LicenseType</span></span>
<span data-ttu-id="ee9ba-132">Tipo di licenza per il database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="ee9ba-132">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="ee9ba-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee9ba-133">-ResourceGroupName</span></span>
<span data-ttu-id="ee9ba-134">Specifica il nome del gruppo di risorse che contiene il database da copiare.</span><span class="sxs-lookup"><span data-stu-id="ee9ba-134">Specifies the name of the Resource Group that contains the database to copy.</span></span>

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

### <span data-ttu-id="ee9ba-135">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="ee9ba-135">-ServerName</span></span>
<span data-ttu-id="ee9ba-136">Specifica il nome di SQL Server che contiene il database da copiare.</span><span class="sxs-lookup"><span data-stu-id="ee9ba-136">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

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

### <span data-ttu-id="ee9ba-137">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="ee9ba-137">-ServiceObjectiveName</span></span>
<span data-ttu-id="ee9ba-138">Specifica il nome dell'obiettivo del servizio da assegnare alla copia.</span><span class="sxs-lookup"><span data-stu-id="ee9ba-138">Specifies the name of the service objective to assign to the copy.</span></span>

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

### <span data-ttu-id="ee9ba-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="ee9ba-139">-Tags</span></span>
<span data-ttu-id="ee9ba-140">Specifica le coppie chiave-valore nella forma di una tabella hash da associare alla copia del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="ee9ba-140">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="ee9ba-141">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ee9ba-141">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ee9ba-142">-VCore</span><span class="sxs-lookup"><span data-stu-id="ee9ba-142">-VCore</span></span>
<span data-ttu-id="ee9ba-143">I numeri Vcore della copia del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="ee9ba-143">The Vcore numbers of the Azure Sql Database copy.</span></span>

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

### <span data-ttu-id="ee9ba-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ee9ba-144">-Confirm</span></span>
<span data-ttu-id="ee9ba-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee9ba-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee9ba-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee9ba-146">-WhatIf</span></span>
<span data-ttu-id="ee9ba-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee9ba-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee9ba-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee9ba-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee9ba-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee9ba-149">CommonParameters</span></span>
<span data-ttu-id="ee9ba-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee9ba-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee9ba-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee9ba-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee9ba-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ee9ba-152">INPUTS</span></span>

### <span data-ttu-id="ee9ba-153">System. String</span><span class="sxs-lookup"><span data-stu-id="ee9ba-153">System.String</span></span>

## <span data-ttu-id="ee9ba-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee9ba-154">OUTPUTS</span></span>

### <span data-ttu-id="ee9ba-155">Microsoft. Azure. Commands. SQL. Replication. Model. AzureSqlDatabaseCopyModel</span><span class="sxs-lookup"><span data-stu-id="ee9ba-155">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>

## <span data-ttu-id="ee9ba-156">Note</span><span class="sxs-lookup"><span data-stu-id="ee9ba-156">NOTES</span></span>

## <span data-ttu-id="ee9ba-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee9ba-157">RELATED LINKS</span></span>

[<span data-ttu-id="ee9ba-158">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ee9ba-158">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="ee9ba-159">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="ee9ba-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
