---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: 369a9f0f9bb475d27512eb13047a5a4ffe334573
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967438"
---
# <span data-ttu-id="00ca6-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="00ca6-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="00ca6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00ca6-102">SYNOPSIS</span></span>
<span data-ttu-id="00ca6-103">Rimuove i tipi di informazioni e le etichette di riservatezza delle colonne nel database SQL istanza gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="00ca6-103">Removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="00ca6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="00ca6-104">SYNTAX</span></span>

### <span data-ttu-id="00ca6-105">ClassificationObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="00ca6-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00ca6-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="00ca6-106">ColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00ca6-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="00ca6-107">DatabaseObjectColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00ca6-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="00ca6-108">DESCRIPTION</span></span>
<span data-ttu-id="00ca6-109">Il Remove-AzSqlInstanceDatabaseSensitivityClassification cmdlet rimuove i tipi di informazioni e le etichette di riservatezza delle colonne nel database SQL istanza gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="00ca6-109">The Remove-AzSqlInstanceDatabaseSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="00ca6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="00ca6-110">EXAMPLES</span></span>

### <span data-ttu-id="00ca6-111">Esempio 1: Rimuovere il tipo di informazioni e l'etichetta di riservatezza di una colonna in un database SQL istanza gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="00ca6-111">Example 1: Remove information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="00ca6-112">Esempio 2: Rimuovere i tipi di informazioni correnti e le etichette di riservatezza delle colonne in un database SQL istanza gestita di Azure con Piping.</span><span class="sxs-lookup"><span data-stu-id="00ca6-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Remove-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="00ca6-113">Esempio 3: Rimuovere il tipo di informazioni e l'etichetta di riservatezza di una colonna in un database di istanze gestite di Azure SQL con Piping.</span><span class="sxs-lookup"><span data-stu-id="00ca6-113">Example 3: Remove information type and sensitivity label of a column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="00ca6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00ca6-114">PARAMETERS</span></span>

### <span data-ttu-id="00ca6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00ca6-115">-AsJob</span></span>
<span data-ttu-id="00ca6-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="00ca6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="00ca6-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="00ca6-117">-ClassificationObject</span></span>
<span data-ttu-id="00ca6-118">Oggetto che rappresenta una classificazione di riservatezza SQL di riservatezza del database dell'istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="00ca6-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel
Parameter Sets: ClassificationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00ca6-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="00ca6-119">-ColumnName</span></span>
<span data-ttu-id="00ca6-120">Nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="00ca6-120">Name of column.</span></span>

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

### <span data-ttu-id="00ca6-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="00ca6-121">-DatabaseName</span></span>
<span data-ttu-id="00ca6-122">Il nome del database dell'SQL gestito di Azure.</span><span class="sxs-lookup"><span data-stu-id="00ca6-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="00ca6-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="00ca6-123">-DatabaseObject</span></span>
<span data-ttu-id="00ca6-124">L'oggetto SQL di istanza gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="00ca6-124">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00ca6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00ca6-125">-DefaultProfile</span></span>
<span data-ttu-id="00ca6-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="00ca6-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00ca6-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="00ca6-127">-InstanceName</span></span>
<span data-ttu-id="00ca6-128">Nome SQL'istanza gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="00ca6-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="00ca6-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00ca6-129">-PassThru</span></span>
<span data-ttu-id="00ca6-130">Specifica se eseguire l'output del modello di classificazione di riservatezza al termine dell'esecuzione del cmdlet</span><span class="sxs-lookup"><span data-stu-id="00ca6-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="00ca6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00ca6-131">-ResourceGroupName</span></span>
<span data-ttu-id="00ca6-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="00ca6-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="00ca6-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="00ca6-133">-SchemaName</span></span>
<span data-ttu-id="00ca6-134">Nome dello schema.</span><span class="sxs-lookup"><span data-stu-id="00ca6-134">Name of schema.</span></span>

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

### <span data-ttu-id="00ca6-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="00ca6-135">-TableName</span></span>
<span data-ttu-id="00ca6-136">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="00ca6-136">Name of table.</span></span>

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

### <span data-ttu-id="00ca6-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00ca6-137">-Confirm</span></span>
<span data-ttu-id="00ca6-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00ca6-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00ca6-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00ca6-139">-WhatIf</span></span>
<span data-ttu-id="00ca6-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="00ca6-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="00ca6-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="00ca6-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00ca6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00ca6-142">CommonParameters</span></span>
<span data-ttu-id="00ca6-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00ca6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00ca6-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="00ca6-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00ca6-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="00ca6-145">INPUTS</span></span>

### <span data-ttu-id="00ca6-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="00ca6-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="00ca6-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="00ca6-147">OUTPUTS</span></span>

### <span data-ttu-id="00ca6-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="00ca6-148">System.Boolean</span></span>

## <span data-ttu-id="00ca6-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="00ca6-149">NOTES</span></span>

## <span data-ttu-id="00ca6-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="00ca6-150">RELATED LINKS</span></span>

[<span data-ttu-id="00ca6-151">Altre informazioni sull'individuazione e la classificazione SQL dati del database di Azure</span><span class="sxs-lookup"><span data-stu-id="00ca6-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)
