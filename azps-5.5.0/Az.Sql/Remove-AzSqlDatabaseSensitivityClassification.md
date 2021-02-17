---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 15da7969c5e47376e04bb78a02ff611c9326b947
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176839"
---
# <span data-ttu-id="62b0f-101">Remove-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="62b0f-101">Remove-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="62b0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62b0f-102">SYNOPSIS</span></span>
<span data-ttu-id="62b0f-103">Rimuove i tipi di informazioni e le etichette di riservatezza delle colonne nel database.</span><span class="sxs-lookup"><span data-stu-id="62b0f-103">Removes the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="62b0f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62b0f-104">SYNTAX</span></span>

### <span data-ttu-id="62b0f-105">ClassificationObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="62b0f-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification -ClassificationObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62b0f-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="62b0f-106">ColumnParameterSet</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62b0f-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="62b0f-107">DatabaseObjectColumnParameterSet</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62b0f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="62b0f-108">DESCRIPTION</span></span>
<span data-ttu-id="62b0f-109">Il Remove-AzSqlDatabaseSensitivityClassification rimuovere i tipi di informazioni e le etichette di riservatezza delle colonne nel database.</span><span class="sxs-lookup"><span data-stu-id="62b0f-109">The Remove-AzSqlDatabaseSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="62b0f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62b0f-110">EXAMPLES</span></span>

### <span data-ttu-id="62b0f-111">Esempio 1: Rimuovere il tipo di informazioni e l'etichetta di riservatezza di una colonna in un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="62b0f-111">Example 1: Remove information type and sensitivity label of a column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="62b0f-112">Esempio 2: Rimuovere i tipi di informazioni correnti e le etichette di riservatezza delle colonne in un database SQL Azure tramite Piping.</span><span class="sxs-lookup"><span data-stu-id="62b0f-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Remove-AzSqlDatabaseSensitivityClassification
```

### <span data-ttu-id="62b0f-113">Esempio 3: Rimuovere il tipo di informazioni e l'etichetta di riservatezza di una colonna in un database SQL Azure con Piping.</span><span class="sxs-lookup"><span data-stu-id="62b0f-113">Example 3: Remove information type and sensitivity label of a column in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Remove-AzSqlDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="62b0f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62b0f-114">PARAMETERS</span></span>

### <span data-ttu-id="62b0f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62b0f-115">-AsJob</span></span>
<span data-ttu-id="62b0f-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="62b0f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="62b0f-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="62b0f-117">-ClassificationObject</span></span>
<span data-ttu-id="62b0f-118">Oggetto che rappresenta una classificazione di riservatezza SQL di riservatezza del database.</span><span class="sxs-lookup"><span data-stu-id="62b0f-118">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="62b0f-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="62b0f-119">-ColumnName</span></span>
<span data-ttu-id="62b0f-120">Nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="62b0f-120">Name of column.</span></span>

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

### <span data-ttu-id="62b0f-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="62b0f-121">-DatabaseName</span></span>
<span data-ttu-id="62b0f-122">Il nome del database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="62b0f-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="62b0f-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="62b0f-123">-DatabaseObject</span></span>
<span data-ttu-id="62b0f-124">Oggetto SQL di database.</span><span class="sxs-lookup"><span data-stu-id="62b0f-124">The SQL database object.</span></span>

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

### <span data-ttu-id="62b0f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62b0f-125">-DefaultProfile</span></span>
<span data-ttu-id="62b0f-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="62b0f-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62b0f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62b0f-127">-PassThru</span></span>
<span data-ttu-id="62b0f-128">Specifica se l'output del modello di classificazione di riservatezza alla fine dell'esecuzione del cmdlet</span><span class="sxs-lookup"><span data-stu-id="62b0f-128">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="62b0f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62b0f-129">-ResourceGroupName</span></span>
<span data-ttu-id="62b0f-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="62b0f-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="62b0f-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="62b0f-131">-SchemaName</span></span>
<span data-ttu-id="62b0f-132">Nome dello schema.</span><span class="sxs-lookup"><span data-stu-id="62b0f-132">Name of schema.</span></span>

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

### <span data-ttu-id="62b0f-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="62b0f-133">-ServerName</span></span>
<span data-ttu-id="62b0f-134">SQL del server.</span><span class="sxs-lookup"><span data-stu-id="62b0f-134">SQL server name.</span></span>

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

### <span data-ttu-id="62b0f-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="62b0f-135">-TableName</span></span>
<span data-ttu-id="62b0f-136">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="62b0f-136">Name of table.</span></span>

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

### <span data-ttu-id="62b0f-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62b0f-137">-Confirm</span></span>
<span data-ttu-id="62b0f-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62b0f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62b0f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62b0f-139">-WhatIf</span></span>
<span data-ttu-id="62b0f-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62b0f-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62b0f-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62b0f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62b0f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62b0f-142">CommonParameters</span></span>
<span data-ttu-id="62b0f-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62b0f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62b0f-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="62b0f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62b0f-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="62b0f-145">INPUTS</span></span>

### <span data-ttu-id="62b0f-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="62b0f-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="62b0f-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62b0f-147">OUTPUTS</span></span>

### <span data-ttu-id="62b0f-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="62b0f-148">System.Boolean</span></span>

## <span data-ttu-id="62b0f-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="62b0f-149">NOTES</span></span>

## <span data-ttu-id="62b0f-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62b0f-150">RELATED LINKS</span></span>

[<span data-ttu-id="62b0f-151">Altre informazioni sull'individuazione e la classificazione SQL dati del database di Azure</span><span class="sxs-lookup"><span data-stu-id="62b0f-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
