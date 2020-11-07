---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseCopy.md
ms.openlocfilehash: a962ca86c3d65cd11da4169626ed932bb78653b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688219"
---
# <span data-ttu-id="69fd1-101">New-AzureRmSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="69fd1-101">New-AzureRmSqlDatabaseCopy</span></span>

## <span data-ttu-id="69fd1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="69fd1-102">SYNOPSIS</span></span>
<span data-ttu-id="69fd1-103">Crea una copia di un database SQL che usa lo snapshot in corrispondenza dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="69fd1-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69fd1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="69fd1-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>]
 -CopyDatabaseName <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69fd1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69fd1-105">DESCRIPTION</span></span>
<span data-ttu-id="69fd1-106">Il cmdlet **New-AzureRmSqlDatabaseCopy** crea una copia di un database SQL di Azure che usa lo snapshot dei dati in corrispondenza dell'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="69fd1-106">The **New-AzureRmSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="69fd1-107">Usa questo cmdlet invece del cmdlet Start-AzureSqlDatabaseCopy per creare una copia di un database unica.</span><span class="sxs-lookup"><span data-stu-id="69fd1-107">Use this cmdlet instead of the Start-AzureSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="69fd1-108">Questo cmdlet restituisce l'oggetto di **database** della copia.</span><span class="sxs-lookup"><span data-stu-id="69fd1-108">This cmdlet returns the **Database** object of the copy.</span></span>

<span data-ttu-id="69fd1-109">Nota: usare il cmdlet New-AzureRmSqlDatabaseSecondary per configurare la replica geografica per un database.</span><span class="sxs-lookup"><span data-stu-id="69fd1-109">Note: Use the New-AzureRmSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>

<span data-ttu-id="69fd1-110">Questo cmdlet è supportato anche dal servizio database stretch di SQL Server in Azure.</span><span class="sxs-lookup"><span data-stu-id="69fd1-110">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="69fd1-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="69fd1-111">EXAMPLES</span></span>

## <span data-ttu-id="69fd1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="69fd1-112">PARAMETERS</span></span>

### <span data-ttu-id="69fd1-113">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="69fd1-113">-CopyDatabaseName</span></span>
<span data-ttu-id="69fd1-114">Specifica il nome della copia del database SQL.</span><span class="sxs-lookup"><span data-stu-id="69fd1-114">Specifies the name of the SQL Database copy.</span></span>

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

### <span data-ttu-id="69fd1-115">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69fd1-115">-CopyResourceGroupName</span></span>
<span data-ttu-id="69fd1-116">Specifica il nome del gruppo di risorse Azure in cui assegnare la copia.</span><span class="sxs-lookup"><span data-stu-id="69fd1-116">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

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

### <span data-ttu-id="69fd1-117">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="69fd1-117">-CopyServerName</span></span>
<span data-ttu-id="69fd1-118">Specifica il nome di SQL Server che ospita la copia.</span><span class="sxs-lookup"><span data-stu-id="69fd1-118">Specifies the name of the SQL Server which hosts the copy.</span></span>

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

### <span data-ttu-id="69fd1-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="69fd1-119">-DatabaseName</span></span>
<span data-ttu-id="69fd1-120">Specifica il nome del database SQL da copiare.</span><span class="sxs-lookup"><span data-stu-id="69fd1-120">Specifies the name of the SQL Database to copy.</span></span>

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

### <span data-ttu-id="69fd1-121">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="69fd1-121">-ElasticPoolName</span></span>
<span data-ttu-id="69fd1-122">Specifica il nome del pool elastico in cui assegnare la copia.</span><span class="sxs-lookup"><span data-stu-id="69fd1-122">Specifies the name of the elastic pool in which to assign the copy.</span></span>

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

### <span data-ttu-id="69fd1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69fd1-123">-ResourceGroupName</span></span>
<span data-ttu-id="69fd1-124">Specifica il nome del gruppo di risorse a cui questo cmdlet assegna il database copiato.</span><span class="sxs-lookup"><span data-stu-id="69fd1-124">Specifies the name of the  Resource Group to which this cmdlet assigns the copied database.</span></span>

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

### <span data-ttu-id="69fd1-125">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="69fd1-125">-ServerName</span></span>
<span data-ttu-id="69fd1-126">Specifica il nome di SQL Server che contiene il database da copiare.</span><span class="sxs-lookup"><span data-stu-id="69fd1-126">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

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

### <span data-ttu-id="69fd1-127">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="69fd1-127">-ServiceObjectiveName</span></span>
<span data-ttu-id="69fd1-128">Specifica il nome dell'obiettivo del servizio da assegnare alla copia.</span><span class="sxs-lookup"><span data-stu-id="69fd1-128">Specifies the name of the service objective to assign to the copy.</span></span>

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

### <span data-ttu-id="69fd1-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="69fd1-129">-Tags</span></span>
<span data-ttu-id="69fd1-130">Specifica le coppie chiave-valore nella forma di una tabella hash da associare alla copia del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="69fd1-130">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="69fd1-131">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="69fd1-131">For example:</span></span>

<span data-ttu-id="69fd1-132">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="69fd1-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="69fd1-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="69fd1-133">-Confirm</span></span>
<span data-ttu-id="69fd1-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69fd1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69fd1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69fd1-135">-WhatIf</span></span>
<span data-ttu-id="69fd1-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="69fd1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69fd1-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="69fd1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69fd1-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69fd1-138">-DefaultProfile</span></span>
<span data-ttu-id="69fd1-139">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="69fd1-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69fd1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69fd1-140">CommonParameters</span></span>
<span data-ttu-id="69fd1-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69fd1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69fd1-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69fd1-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69fd1-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="69fd1-143">INPUTS</span></span>

## <span data-ttu-id="69fd1-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="69fd1-144">OUTPUTS</span></span>

### <span data-ttu-id="69fd1-145">Microsoft. Azure. Commands. SQL. Replication. Model. AzureSqlDatabaseCopyModel</span><span class="sxs-lookup"><span data-stu-id="69fd1-145">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>
<span data-ttu-id="69fd1-146">Questo cmdlet restituisce un oggetto di **database** che rappresenta il database copiato.</span><span class="sxs-lookup"><span data-stu-id="69fd1-146">This cmdlet returns a **Database** object that represents the copied database.</span></span>

## <span data-ttu-id="69fd1-147">Note</span><span class="sxs-lookup"><span data-stu-id="69fd1-147">NOTES</span></span>

## <span data-ttu-id="69fd1-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="69fd1-148">RELATED LINKS</span></span>

[<span data-ttu-id="69fd1-149">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="69fd1-149">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="69fd1-150">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="69fd1-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
