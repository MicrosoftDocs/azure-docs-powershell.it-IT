---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/disable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 2f7d9421ada70946f18322828c138eca186df5c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011517"
---
# <span data-ttu-id="879b5-101">Disable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="879b5-101">Disable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="879b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="879b5-102">SYNOPSIS</span></span>
<span data-ttu-id="879b5-103">Disabilita (ignora) i suggerimenti di riservatezza per le colonne nel database.</span><span class="sxs-lookup"><span data-stu-id="879b5-103">Disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="879b5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="879b5-104">SYNTAX</span></span>

### <span data-ttu-id="879b5-105">InputObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="879b5-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="879b5-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="879b5-106">ColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="879b5-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="879b5-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="879b5-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="879b5-108">DESCRIPTION</span></span>
<span data-ttu-id="879b5-109">Il cmdlet Disable-AzSqlDatabaseSensitivityRecommendation disabilita (elimina) i suggerimenti di riservatezza per le colonne del database.</span><span class="sxs-lookup"><span data-stu-id="879b5-109">The Disable-AzSqlDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="879b5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="879b5-110">EXAMPLES</span></span>

### <span data-ttu-id="879b5-111">Esempio 1: Disabilitare i suggerimenti di riservatezza per una determinata colonna in un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="879b5-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Disable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="879b5-112">Esempio 2: Disabilitare i suggerimenti di riservatezza per le colonne che hanno suggerimenti di riservatezza in un database SQL Azure con Piping.</span><span class="sxs-lookup"><span data-stu-id="879b5-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation
```

### <span data-ttu-id="879b5-113">Esempio 3: Disabilitare i suggerimenti di riservatezza per una determinata colonna in un database SQL Azure tramite Piping.</span><span class="sxs-lookup"><span data-stu-id="879b5-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="879b5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="879b5-114">PARAMETERS</span></span>

### <span data-ttu-id="879b5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="879b5-115">-AsJob</span></span>
<span data-ttu-id="879b5-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="879b5-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="879b5-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="879b5-117">-ColumnName</span></span>
<span data-ttu-id="879b5-118">Nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="879b5-118">Name of column.</span></span>

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

### <span data-ttu-id="879b5-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="879b5-119">-DatabaseName</span></span>
<span data-ttu-id="879b5-120">Il nome del database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="879b5-120">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="879b5-121">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="879b5-121">-DatabaseObject</span></span>
<span data-ttu-id="879b5-122">Oggetto SQL di database.</span><span class="sxs-lookup"><span data-stu-id="879b5-122">The SQL database object.</span></span>

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

### <span data-ttu-id="879b5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="879b5-123">-DefaultProfile</span></span>
<span data-ttu-id="879b5-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="879b5-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="879b5-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="879b5-125">-InputObject</span></span>
<span data-ttu-id="879b5-126">Oggetto che rappresenta una classificazione SQL riservatezza del database.</span><span class="sxs-lookup"><span data-stu-id="879b5-126">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="879b5-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="879b5-127">-PassThru</span></span>
<span data-ttu-id="879b5-128">Specifica se eseguire l'output del modello di classificazione di riservatezza al termine dell'esecuzione del cmdlet</span><span class="sxs-lookup"><span data-stu-id="879b5-128">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="879b5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="879b5-129">-ResourceGroupName</span></span>
<span data-ttu-id="879b5-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="879b5-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="879b5-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="879b5-131">-SchemaName</span></span>
<span data-ttu-id="879b5-132">Nome dello schema.</span><span class="sxs-lookup"><span data-stu-id="879b5-132">Name of schema.</span></span>

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

### <span data-ttu-id="879b5-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="879b5-133">-ServerName</span></span>
<span data-ttu-id="879b5-134">SQL del server.</span><span class="sxs-lookup"><span data-stu-id="879b5-134">SQL server name.</span></span>

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

### <span data-ttu-id="879b5-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="879b5-135">-TableName</span></span>
<span data-ttu-id="879b5-136">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="879b5-136">Name of table.</span></span>

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

### <span data-ttu-id="879b5-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="879b5-137">-Confirm</span></span>
<span data-ttu-id="879b5-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="879b5-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="879b5-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="879b5-139">-WhatIf</span></span>
<span data-ttu-id="879b5-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="879b5-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="879b5-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="879b5-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="879b5-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="879b5-142">CommonParameters</span></span>
<span data-ttu-id="879b5-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="879b5-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="879b5-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="879b5-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="879b5-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="879b5-145">INPUTS</span></span>

### <span data-ttu-id="879b5-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="879b5-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="879b5-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="879b5-147">OUTPUTS</span></span>

### <span data-ttu-id="879b5-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="879b5-148">System.Boolean</span></span>

## <span data-ttu-id="879b5-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="879b5-149">NOTES</span></span>

## <span data-ttu-id="879b5-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="879b5-150">RELATED LINKS</span></span>

[<span data-ttu-id="879b5-151">Altre informazioni sull'individuazione e la classificazione SQL dati del database di Azure</span><span class="sxs-lookup"><span data-stu-id="879b5-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)