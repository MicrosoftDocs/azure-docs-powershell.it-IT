---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: e21bf168093d2589321d6952ca45af7e9f8c0cbe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207907"
---
# <span data-ttu-id="41d6e-101">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="41d6e-101">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="41d6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41d6e-102">SYNOPSIS</span></span>
<span data-ttu-id="41d6e-103">Abilita i suggerimenti di riservatezza per le colonne (i suggerimenti sono abilitati per impostazione predefinita in tutte le colonne) nel database SQL istanza gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="41d6e-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="41d6e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="41d6e-104">SYNTAX</span></span>

### <span data-ttu-id="41d6e-105">InputObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="41d6e-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41d6e-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="41d6e-106">ColumnParameterSet</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41d6e-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="41d6e-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41d6e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="41d6e-108">DESCRIPTION</span></span>
<span data-ttu-id="41d6e-109">Il cmdlet Enable-AzSqlInstanceDatabaseSensitivityRecommendation abilita i suggerimenti di riservatezza per le colonne nel database SQL istanza gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="41d6e-109">The Enable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="41d6e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="41d6e-110">EXAMPLES</span></span>

### <span data-ttu-id="41d6e-111">Esempio 1: Abilitare i suggerimenti di riservatezza per una determinata colonna in un database SQL istanza gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="41d6e-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Enable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="41d6e-112">Esempio 2: Abilitare i suggerimenti di riservatezza per una determinata colonna in un database di istanze gestite di Azure SQL con Piping.</span><span class="sxs-lookup"><span data-stu-id="41d6e-112">Example 2: Enable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="41d6e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41d6e-113">PARAMETERS</span></span>

### <span data-ttu-id="41d6e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41d6e-114">-AsJob</span></span>
<span data-ttu-id="41d6e-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="41d6e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41d6e-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="41d6e-116">-ColumnName</span></span>
<span data-ttu-id="41d6e-117">Nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="41d6e-117">Name of column.</span></span>

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

### <span data-ttu-id="41d6e-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="41d6e-118">-DatabaseName</span></span>
<span data-ttu-id="41d6e-119">Il nome del database dell'SQL gestito di Azure.</span><span class="sxs-lookup"><span data-stu-id="41d6e-119">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="41d6e-120">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="41d6e-120">-DatabaseObject</span></span>
<span data-ttu-id="41d6e-121">L'oggetto SQL di istanza gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="41d6e-121">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="41d6e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41d6e-122">-DefaultProfile</span></span>
<span data-ttu-id="41d6e-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="41d6e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41d6e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41d6e-124">-InputObject</span></span>
<span data-ttu-id="41d6e-125">Oggetto che rappresenta una classificazione di riservatezza SQL di riservatezza del database dell'istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="41d6e-125">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel
Parameter Sets: InputObjectParameterSet
Aliases: ClassificationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41d6e-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="41d6e-126">-InstanceName</span></span>
<span data-ttu-id="41d6e-127">Nome SQL'istanza gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="41d6e-127">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="41d6e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41d6e-128">-PassThru</span></span>
<span data-ttu-id="41d6e-129">Specifica se l'output del modello di classificazione di riservatezza alla fine dell'esecuzione del cmdlet</span><span class="sxs-lookup"><span data-stu-id="41d6e-129">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="41d6e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41d6e-130">-ResourceGroupName</span></span>
<span data-ttu-id="41d6e-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="41d6e-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="41d6e-132">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="41d6e-132">-SchemaName</span></span>
<span data-ttu-id="41d6e-133">Nome dello schema.</span><span class="sxs-lookup"><span data-stu-id="41d6e-133">Name of schema.</span></span>

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

### <span data-ttu-id="41d6e-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="41d6e-134">-TableName</span></span>
<span data-ttu-id="41d6e-135">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="41d6e-135">Name of table.</span></span>

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

### <span data-ttu-id="41d6e-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41d6e-136">-Confirm</span></span>
<span data-ttu-id="41d6e-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41d6e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41d6e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41d6e-138">-WhatIf</span></span>
<span data-ttu-id="41d6e-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="41d6e-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41d6e-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="41d6e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41d6e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41d6e-141">CommonParameters</span></span>
<span data-ttu-id="41d6e-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41d6e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41d6e-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="41d6e-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41d6e-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="41d6e-144">INPUTS</span></span>

### <span data-ttu-id="41d6e-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="41d6e-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="41d6e-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="41d6e-146">OUTPUTS</span></span>

### <span data-ttu-id="41d6e-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="41d6e-147">System.Boolean</span></span>

## <span data-ttu-id="41d6e-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="41d6e-148">NOTES</span></span>

## <span data-ttu-id="41d6e-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="41d6e-149">RELATED LINKS</span></span>

[<span data-ttu-id="41d6e-150">Altre informazioni sull'individuazione e la classificazione SQL dati del database di Azure</span><span class="sxs-lookup"><span data-stu-id="41d6e-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)