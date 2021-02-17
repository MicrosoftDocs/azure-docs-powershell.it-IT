---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 72118b8edd5f9816e14a5cfd19abbd5cabaca3dd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196198"
---
# <span data-ttu-id="19207-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="19207-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="19207-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19207-102">SYNOPSIS</span></span>
<span data-ttu-id="19207-103">Disabilita (ignora) i suggerimenti di riservatezza per le colonne nel database SQL istanza gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="19207-103">Disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="19207-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="19207-104">SYNTAX</span></span>

### <span data-ttu-id="19207-105">InputObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="19207-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19207-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="19207-106">ColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19207-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="19207-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19207-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="19207-108">DESCRIPTION</span></span>
<span data-ttu-id="19207-109">Il cmdlet Disable-AzSqlInstanceDatabaseSensitivityRecommendation disabilita (elimina) i suggerimenti di riservatezza per le colonne nel database SQL istanza gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="19207-109">The Disable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="19207-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="19207-110">EXAMPLES</span></span>

### <span data-ttu-id="19207-111">Esempio 1: Disabilitare i suggerimenti di riservatezza per una determinata colonna in un database SQL istanza gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="19207-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Disable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="19207-112">Esempio 2: Disabilitare i suggerimenti di riservatezza per le colonne che hanno suggerimenti di riservatezza in un database di istanze gestite di Azure SQL con Piping.</span><span class="sxs-lookup"><span data-stu-id="19207-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation
```

### <span data-ttu-id="19207-113">Esempio 3: Disabilitare i suggerimenti di riservatezza per una determinata colonna in un database di istanze gestite di Azure SQL con Piping.</span><span class="sxs-lookup"><span data-stu-id="19207-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="19207-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19207-114">PARAMETERS</span></span>

### <span data-ttu-id="19207-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19207-115">-AsJob</span></span>
<span data-ttu-id="19207-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="19207-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="19207-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="19207-117">-ColumnName</span></span>
<span data-ttu-id="19207-118">Nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="19207-118">Name of column.</span></span>

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

### <span data-ttu-id="19207-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="19207-119">-DatabaseName</span></span>
<span data-ttu-id="19207-120">Il nome del database dell'SQL gestito di Azure.</span><span class="sxs-lookup"><span data-stu-id="19207-120">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="19207-121">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="19207-121">-DatabaseObject</span></span>
<span data-ttu-id="19207-122">L'oggetto SQL di istanza gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="19207-122">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="19207-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19207-123">-DefaultProfile</span></span>
<span data-ttu-id="19207-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="19207-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19207-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19207-125">-InputObject</span></span>
<span data-ttu-id="19207-126">Oggetto che rappresenta una classificazione di riservatezza SQL di riservatezza del database dell'istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="19207-126">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="19207-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="19207-127">-InstanceName</span></span>
<span data-ttu-id="19207-128">Nome SQL'istanza gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="19207-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="19207-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19207-129">-PassThru</span></span>
<span data-ttu-id="19207-130">Specifica se l'output del modello di classificazione di riservatezza alla fine dell'esecuzione del cmdlet</span><span class="sxs-lookup"><span data-stu-id="19207-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="19207-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19207-131">-ResourceGroupName</span></span>
<span data-ttu-id="19207-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="19207-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="19207-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="19207-133">-SchemaName</span></span>
<span data-ttu-id="19207-134">Nome dello schema.</span><span class="sxs-lookup"><span data-stu-id="19207-134">Name of schema.</span></span>

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

### <span data-ttu-id="19207-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="19207-135">-TableName</span></span>
<span data-ttu-id="19207-136">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="19207-136">Name of table.</span></span>

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

### <span data-ttu-id="19207-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19207-137">-Confirm</span></span>
<span data-ttu-id="19207-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19207-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19207-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19207-139">-WhatIf</span></span>
<span data-ttu-id="19207-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19207-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19207-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19207-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19207-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19207-142">CommonParameters</span></span>
<span data-ttu-id="19207-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19207-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19207-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="19207-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19207-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="19207-145">INPUTS</span></span>

### <span data-ttu-id="19207-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="19207-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="19207-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="19207-147">OUTPUTS</span></span>

### <span data-ttu-id="19207-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="19207-148">System.Boolean</span></span>

## <span data-ttu-id="19207-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="19207-149">NOTES</span></span>

## <span data-ttu-id="19207-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="19207-150">RELATED LINKS</span></span>

[<span data-ttu-id="19207-151">Altre informazioni sull'individuazione e la classificazione SQL dati del database di Azure</span><span class="sxs-lookup"><span data-stu-id="19207-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)