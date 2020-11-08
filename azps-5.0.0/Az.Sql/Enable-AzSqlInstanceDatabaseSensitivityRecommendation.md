---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/enable-azsqlinstancedatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Enable-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: e21bf168093d2589321d6952ca45af7e9f8c0cbe
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200172"
---
# <span data-ttu-id="79cd1-101">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="79cd1-101">Enable-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="79cd1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="79cd1-102">SYNOPSIS</span></span>
<span data-ttu-id="79cd1-103">Abilita i consigli di sensitività per le colonne (le raccomandazioni sono abilitate per impostazione predefinita in tutte le colonne) nel database di istanze gestite di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="79cd1-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="79cd1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79cd1-104">SYNTAX</span></span>

### <span data-ttu-id="79cd1-105">InputObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="79cd1-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation
 -InputObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79cd1-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="79cd1-106">ColumnParameterSet</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79cd1-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="79cd1-107">DatabaseObjectColumnParameterSet</span></span>
```
Enable-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79cd1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79cd1-108">DESCRIPTION</span></span>
<span data-ttu-id="79cd1-109">Il cmdlet Enable-AzSqlInstanceDatabaseSensitivityRecommendation consente di abilitare i consigli di sensitività sulle colonne nel database di istanze gestite di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="79cd1-109">The Enable-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="79cd1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79cd1-110">EXAMPLES</span></span>

### <span data-ttu-id="79cd1-111">Esempio 1: abilitare i consigli di sensitività per una determinata colonna in un database di istanze gestite di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="79cd1-111">Example 1: Enable sensitivity recommendations on a given column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Enable-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="79cd1-112">Esempio 2: abilitare i consigli di sensitività per una determinata colonna in un database di istanze gestite di Azure SQL con piping.</span><span class="sxs-lookup"><span data-stu-id="79cd1-112">Example 2: Enable sensitivity recommendations on a given column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="79cd1-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="79cd1-113">PARAMETERS</span></span>

### <span data-ttu-id="79cd1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79cd1-114">-AsJob</span></span>
<span data-ttu-id="79cd1-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="79cd1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="79cd1-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="79cd1-116">-ColumnName</span></span>
<span data-ttu-id="79cd1-117">Nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="79cd1-117">Name of column.</span></span>

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

### <span data-ttu-id="79cd1-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="79cd1-118">-DatabaseName</span></span>
<span data-ttu-id="79cd1-119">Nome del database di istanze gestite di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="79cd1-119">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="79cd1-120">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="79cd1-120">-DatabaseObject</span></span>
<span data-ttu-id="79cd1-121">Oggetto di database dell'istanza gestita di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="79cd1-121">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="79cd1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79cd1-122">-DefaultProfile</span></span>
<span data-ttu-id="79cd1-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="79cd1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79cd1-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79cd1-124">-InputObject</span></span>
<span data-ttu-id="79cd1-125">Oggetto che rappresenta una classificazione di sensitività del database dell'istanza di SQL Managed.</span><span class="sxs-lookup"><span data-stu-id="79cd1-125">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="79cd1-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="79cd1-126">-InstanceName</span></span>
<span data-ttu-id="79cd1-127">Nome dell'istanza gestita di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="79cd1-127">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="79cd1-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79cd1-128">-PassThru</span></span>
<span data-ttu-id="79cd1-129">Specifica se restituire il modello di classificazione della sensibilità alla fine dell'esecuzione dei cmdlet</span><span class="sxs-lookup"><span data-stu-id="79cd1-129">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="79cd1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79cd1-130">-ResourceGroupName</span></span>
<span data-ttu-id="79cd1-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="79cd1-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="79cd1-132">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="79cd1-132">-SchemaName</span></span>
<span data-ttu-id="79cd1-133">Nome dello schema.</span><span class="sxs-lookup"><span data-stu-id="79cd1-133">Name of schema.</span></span>

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

### <span data-ttu-id="79cd1-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="79cd1-134">-TableName</span></span>
<span data-ttu-id="79cd1-135">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="79cd1-135">Name of table.</span></span>

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

### <span data-ttu-id="79cd1-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="79cd1-136">-Confirm</span></span>
<span data-ttu-id="79cd1-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79cd1-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79cd1-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79cd1-138">-WhatIf</span></span>
<span data-ttu-id="79cd1-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79cd1-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79cd1-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79cd1-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79cd1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79cd1-141">CommonParameters</span></span>
<span data-ttu-id="79cd1-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79cd1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79cd1-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79cd1-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79cd1-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="79cd1-144">INPUTS</span></span>

### <span data-ttu-id="79cd1-145">Microsoft. Azure. Commands. SQL. DataClassification. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="79cd1-145">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="79cd1-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79cd1-146">OUTPUTS</span></span>

### <span data-ttu-id="79cd1-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="79cd1-147">System.Boolean</span></span>

## <span data-ttu-id="79cd1-148">Note</span><span class="sxs-lookup"><span data-stu-id="79cd1-148">NOTES</span></span>

## <span data-ttu-id="79cd1-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79cd1-149">RELATED LINKS</span></span>

[<span data-ttu-id="79cd1-150">Altre informazioni sull'individuazione e la classificazione dei dati di database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="79cd1-150">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)