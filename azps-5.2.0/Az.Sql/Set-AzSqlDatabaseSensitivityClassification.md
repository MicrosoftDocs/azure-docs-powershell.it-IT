---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: 4409825b758d34e656b18a198aefd0da32824fcd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354715"
---
# <span data-ttu-id="39982-101">Set-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="39982-101">Set-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="39982-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="39982-102">SYNOPSIS</span></span>
<span data-ttu-id="39982-103">Imposta i tipi di informazioni e le etichette di sensitività delle colonne nel database.</span><span class="sxs-lookup"><span data-stu-id="39982-103">Sets the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="39982-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39982-104">SYNTAX</span></span>

### <span data-ttu-id="39982-105">ClassificationObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="39982-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseSensitivityClassification -ClassificationObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39982-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="39982-106">ColumnParameterSet</span></span>
```
Set-AzSqlDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39982-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="39982-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39982-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="39982-108">DESCRIPTION</span></span>
<span data-ttu-id="39982-109">Il cmdlet Set-AzSqlDatabaseSensitivityClassification imposta i tipi di informazioni e le etichette di sensitività delle colonne nel database.</span><span class="sxs-lookup"><span data-stu-id="39982-109">The Set-AzSqlDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="39982-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39982-110">EXAMPLES</span></span>

### <span data-ttu-id="39982-111">Esempio 1: impostare il tipo di informazioni e l'etichetta di sensitività di una colonna in un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="39982-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL database.</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="39982-112">Esempio 2: impostare i tipi di informazioni consigliate e le etichette di sensitività delle colonne in un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="39982-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Set-AzSqlDatabaseSensitivityClassification
```

### <span data-ttu-id="39982-113">Esempio 3: impostare il tipo di informazioni e l'etichetta di sensitività di una colonna in un database SQL di Azure usando piping.</span><span class="sxs-lookup"><span data-stu-id="39982-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Set-AzSqlDatabaseSensitivityClassification  -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="39982-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="39982-114">PARAMETERS</span></span>

### <span data-ttu-id="39982-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39982-115">-AsJob</span></span>
<span data-ttu-id="39982-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="39982-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="39982-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="39982-117">-ClassificationObject</span></span>
<span data-ttu-id="39982-118">Oggetto che rappresenta una classificazione di sensitivity del database SQL.</span><span class="sxs-lookup"><span data-stu-id="39982-118">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="39982-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="39982-119">-ColumnName</span></span>
<span data-ttu-id="39982-120">Nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="39982-120">Name of column.</span></span>

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

### <span data-ttu-id="39982-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="39982-121">-DatabaseName</span></span>
<span data-ttu-id="39982-122">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="39982-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="39982-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="39982-123">-DatabaseObject</span></span>
<span data-ttu-id="39982-124">Oggetto database SQL.</span><span class="sxs-lookup"><span data-stu-id="39982-124">The SQL database object.</span></span>

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

### <span data-ttu-id="39982-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39982-125">-DefaultProfile</span></span>
<span data-ttu-id="39982-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="39982-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39982-127">-InformationType</span><span class="sxs-lookup"><span data-stu-id="39982-127">-InformationType</span></span>
<span data-ttu-id="39982-128">Nome che descrive il tipo di informazioni dei dati archiviati nella colonna.</span><span class="sxs-lookup"><span data-stu-id="39982-128">A name that describes the information type of the data stored in the column.</span></span>

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

### <span data-ttu-id="39982-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39982-129">-PassThru</span></span>
<span data-ttu-id="39982-130">Specifica se restituire il modello di classificazione della sensibilità alla fine dell'esecuzione dei cmdlet</span><span class="sxs-lookup"><span data-stu-id="39982-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="39982-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39982-131">-ResourceGroupName</span></span>
<span data-ttu-id="39982-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="39982-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="39982-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="39982-133">-SchemaName</span></span>
<span data-ttu-id="39982-134">Nome dello schema.</span><span class="sxs-lookup"><span data-stu-id="39982-134">Name of schema.</span></span>

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

### <span data-ttu-id="39982-135">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="39982-135">-SensitivityLabel</span></span>
<span data-ttu-id="39982-136">Nome che descrive la sensibilità dei dati archiviati nella colonna.</span><span class="sxs-lookup"><span data-stu-id="39982-136">A name that describes the sensitivity of the data stored in the column.</span></span>

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

### <span data-ttu-id="39982-137">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="39982-137">-ServerName</span></span>
<span data-ttu-id="39982-138">Nome di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="39982-138">SQL server name.</span></span>

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

### <span data-ttu-id="39982-139">-TableName</span><span class="sxs-lookup"><span data-stu-id="39982-139">-TableName</span></span>
<span data-ttu-id="39982-140">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="39982-140">Name of table.</span></span>

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

### <span data-ttu-id="39982-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="39982-141">-Confirm</span></span>
<span data-ttu-id="39982-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39982-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39982-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39982-143">-WhatIf</span></span>
<span data-ttu-id="39982-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39982-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39982-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39982-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39982-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39982-146">CommonParameters</span></span>
<span data-ttu-id="39982-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39982-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39982-148">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39982-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39982-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="39982-149">INPUTS</span></span>

### <span data-ttu-id="39982-150">Microsoft. Azure. Commands. SQL. DataClassification. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="39982-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="39982-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39982-151">OUTPUTS</span></span>

### <span data-ttu-id="39982-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="39982-152">System.Boolean</span></span>

## <span data-ttu-id="39982-153">Note</span><span class="sxs-lookup"><span data-stu-id="39982-153">NOTES</span></span>

## <span data-ttu-id="39982-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39982-154">RELATED LINKS</span></span>

[<span data-ttu-id="39982-155">Altre informazioni sull'individuazione e la classificazione dei dati di database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="39982-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
