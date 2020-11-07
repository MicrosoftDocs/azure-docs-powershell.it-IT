---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: d60eff325b0240591fc3360276447861560860ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676810"
---
# <span data-ttu-id="1fbf3-101">Remove-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="1fbf3-101">Remove-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="1fbf3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1fbf3-102">SYNOPSIS</span></span>
<span data-ttu-id="1fbf3-103">Rimuove i tipi di informazioni e le etichette di sensitività delle colonne nel database.</span><span class="sxs-lookup"><span data-stu-id="1fbf3-103">Removes the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="1fbf3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1fbf3-104">SYNTAX</span></span>

### <span data-ttu-id="1fbf3-105">ClassificationObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1fbf3-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification -ClassificationObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fbf3-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fbf3-106">ColumnParameterSet</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fbf3-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fbf3-107">DatabaseObjectColumnParameterSet</span></span>
```
Remove-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fbf3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1fbf3-108">DESCRIPTION</span></span>
<span data-ttu-id="1fbf3-109">Il cmdlet Remove-AzSqlDatabaseSensitivityClassification consente di rimuovere i tipi di informazioni e le etichette di sensitività delle colonne nel database.</span><span class="sxs-lookup"><span data-stu-id="1fbf3-109">The Remove-AzSqlDatabaseSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="1fbf3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1fbf3-110">EXAMPLES</span></span>

### <span data-ttu-id="1fbf3-111">Esempio 1: rimuovere il tipo di informazioni e l'etichetta di sensitività di una colonna in un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="1fbf3-111">Example 1: Remove information type and sensitivity label of a column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Remove-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="1fbf3-112">Esempio 2: rimuovere i tipi di informazioni correnti e le etichette di sensitività delle colonne in un database SQL di Azure tramite piping.</span><span class="sxs-lookup"><span data-stu-id="1fbf3-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Remove-AzSqlDatabaseSensitivityClassification
```

### <span data-ttu-id="1fbf3-113">Esempio 3: rimuovere il tipo di informazioni e l'etichetta di sensitività di una colonna in un database SQL di Azure tramite piping.</span><span class="sxs-lookup"><span data-stu-id="1fbf3-113">Example 3: Remove information type and sensitivity label of a column in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Remove-AzSqlDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="1fbf3-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1fbf3-114">PARAMETERS</span></span>

### <span data-ttu-id="1fbf3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1fbf3-115">-AsJob</span></span>
<span data-ttu-id="1fbf3-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1fbf3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1fbf3-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="1fbf3-117">-ClassificationObject</span></span>
<span data-ttu-id="1fbf3-118">Oggetto che rappresenta una classificazione di sensitivity del database SQL.</span><span class="sxs-lookup"><span data-stu-id="1fbf3-118">An object representing a SQL Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="1fbf3-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="1fbf3-119">-ColumnName</span></span>
<span data-ttu-id="1fbf3-120">Nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="1fbf3-120">Name of column.</span></span>

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

### <span data-ttu-id="1fbf3-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1fbf3-121">-DatabaseName</span></span>
<span data-ttu-id="1fbf3-122">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="1fbf3-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="1fbf3-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="1fbf3-123">-DatabaseObject</span></span>
<span data-ttu-id="1fbf3-124">Oggetto database SQL.</span><span class="sxs-lookup"><span data-stu-id="1fbf3-124">The SQL database object.</span></span>

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

### <span data-ttu-id="1fbf3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fbf3-125">-DefaultProfile</span></span>
<span data-ttu-id="1fbf3-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1fbf3-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fbf3-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1fbf3-127">-PassThru</span></span>
<span data-ttu-id="1fbf3-128">Specifica se restituire il modello di classificazione della sensibilità alla fine dell'esecuzione dei cmdlet</span><span class="sxs-lookup"><span data-stu-id="1fbf3-128">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="1fbf3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fbf3-129">-ResourceGroupName</span></span>
<span data-ttu-id="1fbf3-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1fbf3-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="1fbf3-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="1fbf3-131">-SchemaName</span></span>
<span data-ttu-id="1fbf3-132">Nome dello schema.</span><span class="sxs-lookup"><span data-stu-id="1fbf3-132">Name of schema.</span></span>

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

### <span data-ttu-id="1fbf3-133">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="1fbf3-133">-ServerName</span></span>
<span data-ttu-id="1fbf3-134">Nome di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1fbf3-134">SQL server name.</span></span>

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

### <span data-ttu-id="1fbf3-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="1fbf3-135">-TableName</span></span>
<span data-ttu-id="1fbf3-136">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="1fbf3-136">Name of table.</span></span>

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

### <span data-ttu-id="1fbf3-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1fbf3-137">-Confirm</span></span>
<span data-ttu-id="1fbf3-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fbf3-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fbf3-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fbf3-139">-WhatIf</span></span>
<span data-ttu-id="1fbf3-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1fbf3-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1fbf3-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1fbf3-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fbf3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fbf3-142">CommonParameters</span></span>
<span data-ttu-id="1fbf3-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fbf3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fbf3-144">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1fbf3-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fbf3-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1fbf3-145">INPUTS</span></span>

### <span data-ttu-id="1fbf3-146">Microsoft. Azure. Commands. SQL. DataClassification. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="1fbf3-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="1fbf3-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1fbf3-147">OUTPUTS</span></span>

### <span data-ttu-id="1fbf3-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1fbf3-148">System.Boolean</span></span>

## <span data-ttu-id="1fbf3-149">Note</span><span class="sxs-lookup"><span data-stu-id="1fbf3-149">NOTES</span></span>

## <span data-ttu-id="1fbf3-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1fbf3-150">RELATED LINKS</span></span>

[<span data-ttu-id="1fbf3-151">Altre informazioni sull'individuazione e la classificazione dei dati di database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="1fbf3-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)