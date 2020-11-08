---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: c594a9bf247355201bc08e438af1d9dff8cd3f7d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021439"
---
# <span data-ttu-id="a6565-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="a6565-101">Remove-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="a6565-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a6565-102">SYNOPSIS</span></span>
<span data-ttu-id="a6565-103">Rimuove i tipi di informazioni e le etichette di sensitività delle colonne nel database di istanze gestite di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a6565-103">Removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="a6565-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6565-104">SYNTAX</span></span>

### <span data-ttu-id="a6565-105">ClassificationObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a6565-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6565-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6565-106">ColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6565-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6565-107">DatabaseObjectColumnParameterSet</span></span>
```
Remove-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6565-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6565-108">DESCRIPTION</span></span>
<span data-ttu-id="a6565-109">Il cmdlet Remove-AzSqlInstanceDatabaseSensitivityClassification rimuove i tipi di informazioni e le etichette di sensitività delle colonne nel database di istanze gestite di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a6565-109">The Remove-AzSqlInstanceDatabaseSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="a6565-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6565-110">EXAMPLES</span></span>

### <span data-ttu-id="a6565-111">Esempio 1: rimuovere il tipo di informazioni e l'etichetta di sensitività di una colonna in un database di istanze gestite di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a6565-111">Example 1: Remove information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="a6565-112">Esempio 2: rimuovere i tipi di informazioni correnti e le etichette di sensitività delle colonne in un database di istanze gestite di Azure SQL con piping.</span><span class="sxs-lookup"><span data-stu-id="a6565-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Remove-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="a6565-113">Esempio 3: rimuovere il tipo di informazioni e l'etichetta di sensitività di una colonna in un database di istanze gestite di Azure SQL con piping.</span><span class="sxs-lookup"><span data-stu-id="a6565-113">Example 3: Remove information type and sensitivity label of a column in an Azure SQL managed instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Remove-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="a6565-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a6565-114">PARAMETERS</span></span>

### <span data-ttu-id="a6565-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6565-115">-AsJob</span></span>
<span data-ttu-id="a6565-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a6565-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a6565-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="a6565-117">-ClassificationObject</span></span>
<span data-ttu-id="a6565-118">Oggetto che rappresenta una classificazione di sensitività del database dell'istanza di SQL Managed.</span><span class="sxs-lookup"><span data-stu-id="a6565-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="a6565-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="a6565-119">-ColumnName</span></span>
<span data-ttu-id="a6565-120">Nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="a6565-120">Name of column.</span></span>

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

### <span data-ttu-id="a6565-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a6565-121">-DatabaseName</span></span>
<span data-ttu-id="a6565-122">Nome del database di istanze gestite di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a6565-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="a6565-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="a6565-123">-DatabaseObject</span></span>
<span data-ttu-id="a6565-124">Oggetto di database dell'istanza gestita di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a6565-124">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="a6565-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6565-125">-DefaultProfile</span></span>
<span data-ttu-id="a6565-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a6565-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6565-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="a6565-127">-InstanceName</span></span>
<span data-ttu-id="a6565-128">Nome dell'istanza gestita di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a6565-128">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="a6565-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6565-129">-PassThru</span></span>
<span data-ttu-id="a6565-130">Specifica se restituire il modello di classificazione della sensibilità alla fine dell'esecuzione dei cmdlet</span><span class="sxs-lookup"><span data-stu-id="a6565-130">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="a6565-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6565-131">-ResourceGroupName</span></span>
<span data-ttu-id="a6565-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a6565-132">The name of the resource group.</span></span>

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

### <span data-ttu-id="a6565-133">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="a6565-133">-SchemaName</span></span>
<span data-ttu-id="a6565-134">Nome dello schema.</span><span class="sxs-lookup"><span data-stu-id="a6565-134">Name of schema.</span></span>

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

### <span data-ttu-id="a6565-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="a6565-135">-TableName</span></span>
<span data-ttu-id="a6565-136">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="a6565-136">Name of table.</span></span>

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

### <span data-ttu-id="a6565-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a6565-137">-Confirm</span></span>
<span data-ttu-id="a6565-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6565-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6565-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6565-139">-WhatIf</span></span>
<span data-ttu-id="a6565-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6565-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a6565-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6565-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6565-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6565-142">CommonParameters</span></span>
<span data-ttu-id="a6565-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6565-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6565-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6565-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6565-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a6565-145">INPUTS</span></span>

### <span data-ttu-id="a6565-146">Microsoft. Azure. Commands. SQL. DataClassification. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="a6565-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="a6565-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6565-147">OUTPUTS</span></span>

### <span data-ttu-id="a6565-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a6565-148">System.Boolean</span></span>

## <span data-ttu-id="a6565-149">Note</span><span class="sxs-lookup"><span data-stu-id="a6565-149">NOTES</span></span>

## <span data-ttu-id="a6565-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6565-150">RELATED LINKS</span></span>

[<span data-ttu-id="a6565-151">Altre informazioni sull'individuazione e la classificazione dei dati di database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="a6565-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
