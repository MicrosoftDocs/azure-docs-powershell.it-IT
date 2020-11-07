---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: c476f19f8c2ab8af334f92e75b67aeee151793fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676724"
---
# <span data-ttu-id="65bb4-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="65bb4-101">Set-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="65bb4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="65bb4-102">SYNOPSIS</span></span>
<span data-ttu-id="65bb4-103">Imposta i tipi di informazioni e le etichette di sensitività delle colonne nel database di istanze gestite di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="65bb4-103">Sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="65bb4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="65bb4-104">SYNTAX</span></span>

### <span data-ttu-id="65bb4-105">ClassificationObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="65bb4-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification
 -ClassificationObject <ManagedDatabaseSensitivityClassificationModel> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65bb4-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="65bb4-106">ColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-InstanceName] <String> [-DatabaseName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65bb4-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="65bb4-107">DatabaseObjectColumnParameterSet</span></span>
```
Set-AzSqlInstanceDatabaseSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -DatabaseObject <AzureSqlManagedDatabaseModel> -SchemaName <String> -TableName <String> -ColumnName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65bb4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="65bb4-108">DESCRIPTION</span></span>
<span data-ttu-id="65bb4-109">Il cmdlet Set-AzSqlInstanceDatabaseSensitivityClassification imposta i tipi di informazioni e le etichette di sensitività delle colonne nel database di istanze gestite di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="65bb4-109">The Set-AzSqlInstanceDatabaseSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="65bb4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="65bb4-110">EXAMPLES</span></span>

### <span data-ttu-id="65bb4-111">Esempio 1: impostare il tipo di informazioni e l'etichetta di sensitività di una colonna in un database di istanze gestite di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="65bb4-111">Example 1: Set information type and sensitivity label of a column in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="65bb4-112">Esempio 2: impostare i tipi di informazioni consigliate e le etichette di sensitività delle colonne in un database di istanze gestite di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="65bb4-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification
```

### <span data-ttu-id="65bb4-113">Esempio 3: impostare il tipo di informazioni e l'etichetta di sensitività di una colonna in un database di istanza gestito di Azure SQL tramite piping.</span><span class="sxs-lookup"><span data-stu-id="65bb4-113">Example 3: Set information type and sensitivity label of a column in an Azure SQL managed instance database, using piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database | Set-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="65bb4-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="65bb4-114">PARAMETERS</span></span>

### <span data-ttu-id="65bb4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65bb4-115">-AsJob</span></span>
<span data-ttu-id="65bb4-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="65bb4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65bb4-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="65bb4-117">-ClassificationObject</span></span>
<span data-ttu-id="65bb4-118">Oggetto che rappresenta una classificazione di sensitività del database dell'istanza di SQL Managed.</span><span class="sxs-lookup"><span data-stu-id="65bb4-118">An object representing a SQL Managed Instance Database Sensitivity Classification.</span></span>

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

### <span data-ttu-id="65bb4-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="65bb4-119">-ColumnName</span></span>
<span data-ttu-id="65bb4-120">Nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="65bb4-120">Name of column.</span></span>

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

### <span data-ttu-id="65bb4-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="65bb4-121">-DatabaseName</span></span>
<span data-ttu-id="65bb4-122">Nome del database di istanze gestite di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="65bb4-122">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="65bb4-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="65bb4-123">-DatabaseObject</span></span>
<span data-ttu-id="65bb4-124">Oggetto di database dell'istanza gestita di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="65bb4-124">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="65bb4-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65bb4-125">-DefaultProfile</span></span>
<span data-ttu-id="65bb4-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="65bb4-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65bb4-127">-InformationType</span><span class="sxs-lookup"><span data-stu-id="65bb4-127">-InformationType</span></span>
<span data-ttu-id="65bb4-128">Nome che descrive il tipo di informazioni dei dati archiviati nella colonna.</span><span class="sxs-lookup"><span data-stu-id="65bb4-128">A name that describes the information type of the data stored in the column.</span></span>

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

### <span data-ttu-id="65bb4-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="65bb4-129">-InstanceName</span></span>
<span data-ttu-id="65bb4-130">Nome dell'istanza gestita di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="65bb4-130">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="65bb4-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="65bb4-131">-PassThru</span></span>
<span data-ttu-id="65bb4-132">Specifica se restituire il modello di classificazione della sensibilità alla fine dell'esecuzione dei cmdlet</span><span class="sxs-lookup"><span data-stu-id="65bb4-132">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="65bb4-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65bb4-133">-ResourceGroupName</span></span>
<span data-ttu-id="65bb4-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="65bb4-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="65bb4-135">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="65bb4-135">-SchemaName</span></span>
<span data-ttu-id="65bb4-136">Nome dello schema.</span><span class="sxs-lookup"><span data-stu-id="65bb4-136">Name of schema.</span></span>

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

### <span data-ttu-id="65bb4-137">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="65bb4-137">-SensitivityLabel</span></span>
<span data-ttu-id="65bb4-138">Nome che descrive la sensibilità dei dati archiviati nella colonna.</span><span class="sxs-lookup"><span data-stu-id="65bb4-138">A name that describes the sensitivity of the data stored in the column.</span></span>

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

### <span data-ttu-id="65bb4-139">-TableName</span><span class="sxs-lookup"><span data-stu-id="65bb4-139">-TableName</span></span>
<span data-ttu-id="65bb4-140">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="65bb4-140">Name of table.</span></span>

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

### <span data-ttu-id="65bb4-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="65bb4-141">-Confirm</span></span>
<span data-ttu-id="65bb4-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65bb4-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65bb4-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65bb4-143">-WhatIf</span></span>
<span data-ttu-id="65bb4-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="65bb4-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="65bb4-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="65bb4-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65bb4-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65bb4-146">CommonParameters</span></span>
<span data-ttu-id="65bb4-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65bb4-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65bb4-148">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65bb4-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65bb4-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="65bb4-149">INPUTS</span></span>

### <span data-ttu-id="65bb4-150">Microsoft. Azure. Commands. SQL. DataClassification. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="65bb4-150">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="65bb4-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="65bb4-151">OUTPUTS</span></span>

### <span data-ttu-id="65bb4-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="65bb4-152">System.Boolean</span></span>

## <span data-ttu-id="65bb4-153">Note</span><span class="sxs-lookup"><span data-stu-id="65bb4-153">NOTES</span></span>

## <span data-ttu-id="65bb4-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="65bb4-154">RELATED LINKS</span></span>

[<span data-ttu-id="65bb4-155">Altre informazioni sull'individuazione e la classificazione dei dati di database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="65bb4-155">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
