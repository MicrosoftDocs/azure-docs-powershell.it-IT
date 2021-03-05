---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 88e08a15c864386d2e073f83f437d0db537f2ae7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003021"
---
# <span data-ttu-id="26606-101">Set-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="26606-101">Set-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="26606-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26606-102">SYNOPSIS</span></span>
<span data-ttu-id="26606-103">Imposta i tipi di informazioni e le etichette di riservatezza delle colonne nel database.</span><span class="sxs-lookup"><span data-stu-id="26606-103">Sets the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="26606-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26606-104">SYNTAX</span></span>

### <span data-ttu-id="26606-105">ClassificationObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="26606-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseSensitivityClassification -ClassificationObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26606-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="26606-106">ColumnParameterSet</span></span>
```
Set-AzSqlDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26606-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="26606-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26606-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="26606-108">DESCRIPTION</span></span>
<span data-ttu-id="26606-109">Il Set-AzSqlDatabaseSensitivityClassification cmdlet imposta i tipi di informazioni e le etichette di riservatezza delle colonne nel database.</span><span class="sxs-lookup"><span data-stu-id="26606-109">The Set-AzSqlDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="26606-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26606-110">EXAMPLES</span></span>

### <span data-ttu-id="26606-111">Esempio 1: impostare il tipo di informazioni e l'etichetta di riservatezza di una colonna in un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="26606-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL database.</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="26606-112">Esempio 2: Impostare i tipi di informazioni consigliati e le etichette di riservatezza delle colonne in un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="26606-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Set-AzSqlDatabaseSensitivityClassification
```

### <span data-ttu-id="26606-113">Esempio 3: Impostare il tipo di informazioni e l'etichetta di riservatezza di una colonna in un database SQL Azure, usando le funzionalità di piping.</span><span class="sxs-lookup"><span data-stu-id="26606-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Set-AzSqlDatabaseSensitivityClassification  -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="26606-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26606-114">PARAMETERS</span></span>

### <span data-ttu-id="26606-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26606-115">-AsJob</span></span>
<span data-ttu-id="26606-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="26606-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26606-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="26606-117">-ClassificationObject</span></span>
<span data-ttu-id="26606-118">Oggetto che rappresenta una classificazione SQL riservatezza del database.</span><span class="sxs-lookup"><span data-stu-id="26606-118">An object representing a SQL Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel
Parameter Sets: ClassificationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26606-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="26606-119">-ColumnName</span></span>
<span data-ttu-id="26606-120">Nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="26606-120">Name of column.</span></span>

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

### <span data-ttu-id="26606-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="26606-121">-DatabaseName</span></span>
<span data-ttu-id="26606-122">Il nome del database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="26606-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="26606-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="26606-123">-DatabaseObject</span></span>
<span data-ttu-id="26606-124">Oggetto SQL di database.</span><span class="sxs-lookup"><span data-stu-id="26606-124">The SQL database object.</span></span>

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

### <span data-ttu-id="26606-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26606-125">-DefaultProfile</span></span>
<span data-ttu-id="26606-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="26606-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26606-127">-InformationType</span><span class="sxs-lookup"><span data-stu-id="26606-127">-InformationType</span></span>
<span data-ttu-id="26606-128">Nome che descrive il tipo di informazioni dei dati archiviati nella colonna.</span><span class="sxs-lookup"><span data-stu-id="26606-128">A name that describes the information type of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26606-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26606-129">-PassThru</span></span>
<span data-ttu-id="26606-130">Specifica se eseguire l'output del modello di classificazione di riservatezza al termine dell'esecuzione del cmdlet</span><span class="sxs-lookup"><span data-stu-id="26606-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="26606-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26606-131">-ResourceGroupName</span></span>
<span data-ttu-id="26606-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="26606-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="26606-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="26606-133">-SchemaName</span></span>
<span data-ttu-id="26606-134">Nome dello schema.</span><span class="sxs-lookup"><span data-stu-id="26606-134">Name of schema.</span></span>

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

### <span data-ttu-id="26606-135">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="26606-135">-SensitivityLabel</span></span>
<span data-ttu-id="26606-136">Nome che descrive la riservatezza dei dati archiviati nella colonna.</span><span class="sxs-lookup"><span data-stu-id="26606-136">A name that describes the sensitivity of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26606-137">-ServerName</span><span class="sxs-lookup"><span data-stu-id="26606-137">-ServerName</span></span>
<span data-ttu-id="26606-138">SQL del server.</span><span class="sxs-lookup"><span data-stu-id="26606-138">SQL server name.</span></span>

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

### <span data-ttu-id="26606-139">-TableName</span><span class="sxs-lookup"><span data-stu-id="26606-139">-TableName</span></span>
<span data-ttu-id="26606-140">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="26606-140">Name of table.</span></span>

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

### <span data-ttu-id="26606-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26606-141">-Confirm</span></span>
<span data-ttu-id="26606-142">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26606-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26606-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26606-143">-WhatIf</span></span>
<span data-ttu-id="26606-144">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26606-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26606-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26606-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26606-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26606-146">CommonParameters</span></span>
<span data-ttu-id="26606-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26606-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26606-148">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="26606-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26606-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="26606-149">INPUTS</span></span>

### <span data-ttu-id="26606-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="26606-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="26606-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26606-151">OUTPUTS</span></span>

### <span data-ttu-id="26606-152">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="26606-152">System.Boolean</span></span>

## <span data-ttu-id="26606-153">NOTE</span><span class="sxs-lookup"><span data-stu-id="26606-153">NOTES</span></span>

## <span data-ttu-id="26606-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26606-154">RELATED LINKS</span></span>

[<span data-ttu-id="26606-155">Altre informazioni sull'individuazione e la classificazione SQL dati del database di Azure</span><span class="sxs-lookup"><span data-stu-id="26606-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)
