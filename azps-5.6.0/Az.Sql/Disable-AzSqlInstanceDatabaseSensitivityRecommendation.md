---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/disable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: 95c5829c3d715b1510c1a58e8baf5e7809f9cd8a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014877"
---
# <span data-ttu-id="22bb8-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="22bb8-101">Disable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="22bb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22bb8-102">SYNOPSIS</span></span>
<span data-ttu-id="22bb8-103">Disabilita (ignora) i suggerimenti di riservatezza per le colonne nel database SQL istanza gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="22bb8-103">Disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="22bb8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22bb8-104">SYNTAX</span></span>

### <span data-ttu-id="22bb8-105">InputObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="22bb8-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22bb8-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="22bb8-106">ColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22bb8-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="22bb8-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22bb8-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="22bb8-108">DESCRIPTION</span></span>
<span data-ttu-id="22bb8-109">Il cmdlet Disable-AzSqlInstanceDatabaseSensitivityRecommendation disabilita (elimina) i suggerimenti di riservatezza per le colonne nel database SQL istanza gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="22bb8-109">The Disable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="22bb8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22bb8-110">EXAMPLES</span></span>

### <span data-ttu-id="22bb8-111">Esempio 1: Disabilitare i suggerimenti di riservatezza per una determinata colonna in un database SQL istanza gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="22bb8-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Disable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="22bb8-112">Esempio 2: Disabilitare i suggerimenti di riservatezza per le colonne che hanno suggerimenti di riservatezza in un database di istanze gestite di Azure SQL con Piping.</span><span class="sxs-lookup"><span data-stu-id="22bb8-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation
```

### <span data-ttu-id="22bb8-113">Esempio 3: Disabilitare i suggerimenti di riservatezza per una determinata colonna in un database di istanze gestite di Azure SQL con Piping.</span><span class="sxs-lookup"><span data-stu-id="22bb8-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Disable-AzSqlInstanceDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="22bb8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22bb8-114">PARAMETERS</span></span>

### <span data-ttu-id="22bb8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22bb8-115">-AsJob</span></span>
<span data-ttu-id="22bb8-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="22bb8-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22bb8-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="22bb8-117">-ColumnName</span></span>
<span data-ttu-id="22bb8-118">Nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="22bb8-118">Name of column.</span></span>

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

### <span data-ttu-id="22bb8-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="22bb8-119">-DatabaseName</span></span>
<span data-ttu-id="22bb8-120">Il nome del database dell'SQL gestito di Azure.</span><span class="sxs-lookup"><span data-stu-id="22bb8-120">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="22bb8-121">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="22bb8-121">-DatabaseObject</span></span>
<span data-ttu-id="22bb8-122">L'oggetto SQL di istanza gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="22bb8-122">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="22bb8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22bb8-123">-DefaultProfile</span></span>
<span data-ttu-id="22bb8-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="22bb8-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22bb8-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22bb8-125">-InputObject</span></span>
<span data-ttu-id="22bb8-126">Oggetto che rappresenta una classificazione di riservatezza SQL di riservatezza del database dell'istanza gestita.</span><span class="sxs-lookup"><span data-stu-id="22bb8-126">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="22bb8-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="22bb8-127">-InstanceName</span></span>
<span data-ttu-id="22bb8-128">Nome dell SQL istanza gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="22bb8-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="22bb8-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22bb8-129">-PassThru</span></span>
<span data-ttu-id="22bb8-130">Specifica se l'output del modello di classificazione di riservatezza alla fine dell'esecuzione del cmdlet</span><span class="sxs-lookup"><span data-stu-id="22bb8-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="22bb8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22bb8-131">-ResourceGroupName</span></span>
<span data-ttu-id="22bb8-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="22bb8-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="22bb8-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="22bb8-133">-SchemaName</span></span>
<span data-ttu-id="22bb8-134">Nome dello schema.</span><span class="sxs-lookup"><span data-stu-id="22bb8-134">Name of schema.</span></span>

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

### <span data-ttu-id="22bb8-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="22bb8-135">-TableName</span></span>
<span data-ttu-id="22bb8-136">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="22bb8-136">Name of table.</span></span>

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

### <span data-ttu-id="22bb8-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22bb8-137">-Confirm</span></span>
<span data-ttu-id="22bb8-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22bb8-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22bb8-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22bb8-139">-WhatIf</span></span>
<span data-ttu-id="22bb8-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22bb8-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="22bb8-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22bb8-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22bb8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22bb8-142">CommonParameters</span></span>
<span data-ttu-id="22bb8-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22bb8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22bb8-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="22bb8-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22bb8-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="22bb8-145">INPUTS</span></span>

### <span data-ttu-id="22bb8-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="22bb8-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="22bb8-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22bb8-147">OUTPUTS</span></span>

### <span data-ttu-id="22bb8-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="22bb8-148">System.Boolean</span></span>

## <span data-ttu-id="22bb8-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="22bb8-149">NOTES</span></span>

## <span data-ttu-id="22bb8-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22bb8-150">RELATED LINKS</span></span>

[<span data-ttu-id="22bb8-151">Altre informazioni sull'individuazione e la classificazione SQL dati del database di Azure</span><span class="sxs-lookup"><span data-stu-id="22bb8-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/azure/sql-database/sql-database-data-discovery-and-classification)