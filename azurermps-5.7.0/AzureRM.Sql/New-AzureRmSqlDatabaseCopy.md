---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
ms.openlocfilehash: 4e9d33691cfd09681bb115c89d0eaf351ef14f13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507856"
---
# <span data-ttu-id="00b7d-101">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="00b7d-101">New-AzureRmSqlDatabaseCopy</span></span>

## <span data-ttu-id="00b7d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="00b7d-102">SYNOPSIS</span></span>
<span data-ttu-id="00b7d-103">Crea una copia di un database SQL che usa lo snapshot in corrispondenza dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="00b7d-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00b7d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="00b7d-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>]
 -CopyDatabaseName <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00b7d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00b7d-105">DESCRIPTION</span></span>
<span data-ttu-id="00b7d-106">Il cmdlet **New-AzureRmSqlDatabaseCopy** crea una copia di un database SQL di Azure che usa lo snapshot dei dati in corrispondenza dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="00b7d-106">The **New-AzureRmSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="00b7d-107">Usa questo cmdlet invece del cmdlet Start-AzureSqlDatabaseCopy per creare una copia di un database unica.</span><span class="sxs-lookup"><span data-stu-id="00b7d-107">Use this cmdlet instead of the Start-AzureSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="00b7d-108">Questo cmdlet restituisce l'oggetto di **database** della copia.</span><span class="sxs-lookup"><span data-stu-id="00b7d-108">This cmdlet returns the **Database** object of the copy.</span></span>

<span data-ttu-id="00b7d-109">Nota: usare il cmdlet New-AzureRmSqlDatabaseSecondary per configurare la replica geografica per un database.</span><span class="sxs-lookup"><span data-stu-id="00b7d-109">Note: Use the New-AzureRmSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>

<span data-ttu-id="00b7d-110">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="00b7d-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="00b7d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="00b7d-111">EXAMPLES</span></span>

## <span data-ttu-id="00b7d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="00b7d-112">PARAMETERS</span></span>

### <span data-ttu-id="00b7d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00b7d-113">-AsJob</span></span>
<span data-ttu-id="00b7d-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="00b7d-114">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="00b7d-115">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="00b7d-115">-CopyDatabaseName</span></span>
<span data-ttu-id="00b7d-116">Specifica il nome della copia del database SQL.</span><span class="sxs-lookup"><span data-stu-id="00b7d-116">Specifies the name of the SQL Database copy.</span></span>

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

### <span data-ttu-id="00b7d-117">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00b7d-117">-CopyResourceGroupName</span></span>
<span data-ttu-id="00b7d-118">Specifica il nome del gruppo di risorse Azure in cui assegnare la copia.</span><span class="sxs-lookup"><span data-stu-id="00b7d-118">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

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

### <span data-ttu-id="00b7d-119">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="00b7d-119">-CopyServerName</span></span>
<span data-ttu-id="00b7d-120">Specifica il nome di SQL Server che ospita la copia.</span><span class="sxs-lookup"><span data-stu-id="00b7d-120">Specifies the name of the SQL Server which hosts the copy.</span></span>

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

### <span data-ttu-id="00b7d-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="00b7d-121">-DatabaseName</span></span>
<span data-ttu-id="00b7d-122">Specifica il nome del database SQL da copiare.</span><span class="sxs-lookup"><span data-stu-id="00b7d-122">Specifies the name of the SQL Database to copy.</span></span>

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

### <span data-ttu-id="00b7d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00b7d-123">-DefaultProfile</span></span>
<span data-ttu-id="00b7d-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="00b7d-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00b7d-125">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="00b7d-125">-ElasticPoolName</span></span>
<span data-ttu-id="00b7d-126">Specifica il nome del pool elastico in cui assegnare la copia.</span><span class="sxs-lookup"><span data-stu-id="00b7d-126">Specifies the name of the elastic pool in which to assign the copy.</span></span>

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

### <span data-ttu-id="00b7d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00b7d-127">-ResourceGroupName</span></span>
<span data-ttu-id="00b7d-128">Specifica il nome del gruppo di risorse che contiene il database da copiare.</span><span class="sxs-lookup"><span data-stu-id="00b7d-128">Specifies the name of the Resource Group that contains the database to copy.</span></span>

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

### <span data-ttu-id="00b7d-129">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="00b7d-129">-ServerName</span></span>
<span data-ttu-id="00b7d-130">Specifica il nome di SQL Server che contiene il database da copiare.</span><span class="sxs-lookup"><span data-stu-id="00b7d-130">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

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

### <span data-ttu-id="00b7d-131">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="00b7d-131">-ServiceObjectiveName</span></span>
<span data-ttu-id="00b7d-132">Specifica il nome dell'obiettivo del servizio da assegnare alla copia.</span><span class="sxs-lookup"><span data-stu-id="00b7d-132">Specifies the name of the service objective to assign to the copy.</span></span>

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

### <span data-ttu-id="00b7d-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="00b7d-133">-Tags</span></span>
<span data-ttu-id="00b7d-134">Specifica le coppie chiave-valore nella forma di una tabella hash da associare alla copia del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="00b7d-134">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="00b7d-135">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="00b7d-135">For example:</span></span>

<span data-ttu-id="00b7d-136">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="00b7d-136">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="00b7d-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="00b7d-137">-Confirm</span></span>
<span data-ttu-id="00b7d-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00b7d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00b7d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00b7d-139">-WhatIf</span></span>
<span data-ttu-id="00b7d-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="00b7d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00b7d-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="00b7d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00b7d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00b7d-142">CommonParameters</span></span>
<span data-ttu-id="00b7d-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00b7d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00b7d-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00b7d-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00b7d-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="00b7d-145">INPUTS</span></span>

### <span data-ttu-id="00b7d-146">Nessuno</span><span class="sxs-lookup"><span data-stu-id="00b7d-146">None</span></span>
<span data-ttu-id="00b7d-147">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="00b7d-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="00b7d-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="00b7d-148">OUTPUTS</span></span>

### <span data-ttu-id="00b7d-149">Microsoft. Azure. Commands. SQL. Replication. Model. AzureSqlDatabaseCopyModel</span><span class="sxs-lookup"><span data-stu-id="00b7d-149">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>
<span data-ttu-id="00b7d-150">Questo cmdlet restituisce un oggetto di **database** che rappresenta il database copiato.</span><span class="sxs-lookup"><span data-stu-id="00b7d-150">This cmdlet returns a **Database** object that represents the copied database.</span></span>

## <span data-ttu-id="00b7d-151">Note</span><span class="sxs-lookup"><span data-stu-id="00b7d-151">NOTES</span></span>

## <span data-ttu-id="00b7d-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="00b7d-152">RELATED LINKS</span></span>

[<span data-ttu-id="00b7d-153">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="00b7d-153">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="00b7d-154">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="00b7d-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
