---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 68e889f4da9555a4dc4ca7217bce65121d3a62c5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189330"
---
# <span data-ttu-id="c4bf8-101">Enable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="c4bf8-101">Enable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="c4bf8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c4bf8-102">SYNOPSIS</span></span>
<span data-ttu-id="c4bf8-103">Abilita suggerimenti per la sensitività sulle colonne (le raccomandazioni sono abilitate per impostazione predefinita in tutte le colonne) nel database.</span><span class="sxs-lookup"><span data-stu-id="c4bf8-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the database.</span></span>

## <span data-ttu-id="c4bf8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4bf8-104">SYNTAX</span></span>

### <span data-ttu-id="c4bf8-105">InputObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c4bf8-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4bf8-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4bf8-106">ColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4bf8-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4bf8-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4bf8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c4bf8-108">DESCRIPTION</span></span>
<span data-ttu-id="c4bf8-109">Il cmdlet Enable-AzSqlDatabaseSensitivityRecommendation consente di abilitare i consigli di sensitività sulle colonne del database.</span><span class="sxs-lookup"><span data-stu-id="c4bf8-109">The Enable-AzSqlDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="c4bf8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4bf8-110">EXAMPLES</span></span>

### <span data-ttu-id="c4bf8-111">Esempio 1: abilitare i consigli di sensitività per una determinata colonna in un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="c4bf8-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Enable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="c4bf8-112">Esempio 2: abilitare i suggerimenti per la sensitività in un database SQL di Column Azure specifico tramite piping.</span><span class="sxs-lookup"><span data-stu-id="c4bf8-112">Example 2: Enable sensitivity recommendations on a given column Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Enable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="c4bf8-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c4bf8-113">PARAMETERS</span></span>

### <span data-ttu-id="c4bf8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c4bf8-114">-AsJob</span></span>
<span data-ttu-id="c4bf8-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c4bf8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c4bf8-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="c4bf8-116">-ColumnName</span></span>
<span data-ttu-id="c4bf8-117">Nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="c4bf8-117">Name of column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4bf8-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c4bf8-118">-DatabaseName</span></span>
<span data-ttu-id="c4bf8-119">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="c4bf8-119">The name of the Azure SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4bf8-120">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="c4bf8-120">-DatabaseObject</span></span>
<span data-ttu-id="c4bf8-121">Oggetto database SQL.</span><span class="sxs-lookup"><span data-stu-id="c4bf8-121">The SQL database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4bf8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4bf8-122">-DefaultProfile</span></span>
<span data-ttu-id="c4bf8-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c4bf8-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4bf8-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4bf8-124">-InputObject</span></span>
<span data-ttu-id="c4bf8-125">Oggetto che rappresenta una classificazione di sensitivity del database SQL.</span><span class="sxs-lookup"><span data-stu-id="c4bf8-125">An object representing a SQL Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel
Parameter Sets: InputObjectParameterSet
Aliases: ClassificationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4bf8-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4bf8-126">-PassThru</span></span>
<span data-ttu-id="c4bf8-127">Specifica se restituire il modello di classificazione della sensibilità alla fine dell'esecuzione dei cmdlet</span><span class="sxs-lookup"><span data-stu-id="c4bf8-127">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="c4bf8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4bf8-128">-ResourceGroupName</span></span>
<span data-ttu-id="c4bf8-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c4bf8-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4bf8-130">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="c4bf8-130">-SchemaName</span></span>
<span data-ttu-id="c4bf8-131">Nome dello schema.</span><span class="sxs-lookup"><span data-stu-id="c4bf8-131">Name of schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4bf8-132">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="c4bf8-132">-ServerName</span></span>
<span data-ttu-id="c4bf8-133">Nome di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c4bf8-133">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4bf8-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="c4bf8-134">-TableName</span></span>
<span data-ttu-id="c4bf8-135">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="c4bf8-135">Name of table.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4bf8-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c4bf8-136">-Confirm</span></span>
<span data-ttu-id="c4bf8-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4bf8-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4bf8-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4bf8-138">-WhatIf</span></span>
<span data-ttu-id="c4bf8-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4bf8-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c4bf8-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4bf8-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4bf8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4bf8-141">CommonParameters</span></span>
<span data-ttu-id="c4bf8-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4bf8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4bf8-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c4bf8-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4bf8-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c4bf8-144">INPUTS</span></span>

### <span data-ttu-id="c4bf8-145">Microsoft. Azure. Commands. SQL. DataClassification. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="c4bf8-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="c4bf8-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4bf8-146">OUTPUTS</span></span>

### <span data-ttu-id="c4bf8-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c4bf8-147">System.Boolean</span></span>

## <span data-ttu-id="c4bf8-148">Note</span><span class="sxs-lookup"><span data-stu-id="c4bf8-148">NOTES</span></span>

## <span data-ttu-id="c4bf8-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4bf8-149">RELATED LINKS</span></span>

[<span data-ttu-id="c4bf8-150">Altre informazioni sull'individuazione e la classificazione dei dati di database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="c4bf8-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)