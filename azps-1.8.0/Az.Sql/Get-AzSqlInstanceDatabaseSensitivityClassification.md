---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityClassification.md
ms.openlocfilehash: 89190f171ec9634e13eaa56499f6eca87e75ccf5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676929"
---
# <span data-ttu-id="e57c9-101">Get-AzSqlInstanceDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="e57c9-101">Get-AzSqlInstanceDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="e57c9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e57c9-102">SYNOPSIS</span></span>
<span data-ttu-id="e57c9-103">Ottiene i tipi di informazioni correnti e le etichette di sensitività delle colonne nel database di istanze gestite di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e57c9-103">Gets the current information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="e57c9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e57c9-104">SYNTAX</span></span>

### <span data-ttu-id="e57c9-105">DatabaseObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e57c9-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e57c9-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="e57c9-106">DatabaseParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e57c9-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="e57c9-107">ColumnParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e57c9-108">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="e57c9-108">DatabaseObjectColumnParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityClassification -DatabaseObject <AzureSqlManagedDatabaseModel>
 -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e57c9-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e57c9-109">DESCRIPTION</span></span>
<span data-ttu-id="e57c9-110">Il cmdlet Get-AzSqlInstanceDatabaseSensitivityClassification restituisce i tipi di informazioni correnti e le etichette di sensitività delle colonne nel database di istanze gestite di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e57c9-110">The Get-AzSqlInstanceDatabaseSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="e57c9-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e57c9-111">EXAMPLES</span></span>

### <span data-ttu-id="e57c9-112">Esempio 1: ottenere i tipi di informazioni correnti e le etichette di sensibilità di un database di istanze gestite di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e57c9-112">Example 1: Get current information types and sensitivity labels of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema1,
                        TableName: table1,
                        ColumnName: column1,
                        SensitivityLabel: label1,
                        InformationType: informationType1,
                    }, {
                        SchemaName: schema2,
                        TableName: table2,
                        ColumnName: column2,
                        SensitivityLabel: label2,
                    }, {
                        SchemaName: schema3,
                        TableName: table3,
                        ColumnName: column3,
                        SensitivityLabel: label3,
                    }}
```

### <span data-ttu-id="e57c9-113">Esempio 2: ottenere i tipi di informazioni correnti e le etichette di sensitività di un database di istanze gestite di Azure SQL con piping.</span><span class="sxs-lookup"><span data-stu-id="e57c9-113">Example 2: Get current information types and sensitivity labels of an Azure SQL managed Instance database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityClassification

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema1,
                        TableName: table1,
                        ColumnName: column1,
                        SensitivityLabel: label1,
                        InformationType: informationType1,
                    }, {
                        SchemaName: schema2,
                        TableName: table2,
                        ColumnName: column2,
                        SensitivityLabel: label2,
                    }, {
                        SchemaName: schema3,
                        TableName: table3,
                        ColumnName: column3,
                        SensitivityLabel: label3,
                    }}
```

### <span data-ttu-id="e57c9-114">Esempio 3: ottenere il tipo di informazioni corrente e l'etichetta di sensitività di una specifica colonna di un database di istanze gestite di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e57c9-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityClassification -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database -SchemaName schema -TableName table -ColumnName column

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema,
                        TableName: table,
                        ColumnName: column,
                        SensitivityLabel: label,
                        InformationType: informationType,
                    }}
```

### <span data-ttu-id="e57c9-115">Esempio 4: ottenere il tipo di informazioni corrente e l'etichetta di sensitività di una specifica colonna di un database di istanze gestite di Azure SQL tramite piping.</span><span class="sxs-lookup"><span data-stu-id="e57c9-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure SQL managed instance database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityClassification -SchemaName schema -TableName table -ColumnName column

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema,
                        TableName: table,
                        ColumnName: column,
                        SensitivityLabel: label,
                        InformationType: informationType,
                    }}
```

## <span data-ttu-id="e57c9-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e57c9-116">PARAMETERS</span></span>

### <span data-ttu-id="e57c9-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e57c9-117">-AsJob</span></span>
<span data-ttu-id="e57c9-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e57c9-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e57c9-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="e57c9-119">-ColumnName</span></span>
<span data-ttu-id="e57c9-120">Nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="e57c9-120">Name of column.</span></span>

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

### <span data-ttu-id="e57c9-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e57c9-121">-DatabaseName</span></span>
<span data-ttu-id="e57c9-122">Nome del database di istanze gestite di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e57c9-122">The name of the Azure SQL managed instance database.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e57c9-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="e57c9-123">-DatabaseObject</span></span>
<span data-ttu-id="e57c9-124">Oggetto di database dell'istanza gestita di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e57c9-124">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e57c9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e57c9-125">-DefaultProfile</span></span>
<span data-ttu-id="e57c9-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e57c9-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e57c9-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="e57c9-127">-InstanceName</span></span>
<span data-ttu-id="e57c9-128">Nome dell'istanza gestita di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e57c9-128">Azure SQL managed instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e57c9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e57c9-129">-ResourceGroupName</span></span>
<span data-ttu-id="e57c9-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e57c9-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e57c9-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="e57c9-131">-SchemaName</span></span>
<span data-ttu-id="e57c9-132">Nome dello schema.</span><span class="sxs-lookup"><span data-stu-id="e57c9-132">Name of schema.</span></span>

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

### <span data-ttu-id="e57c9-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="e57c9-133">-TableName</span></span>
<span data-ttu-id="e57c9-134">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="e57c9-134">Name of table.</span></span>

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

### <span data-ttu-id="e57c9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e57c9-135">CommonParameters</span></span>
<span data-ttu-id="e57c9-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e57c9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e57c9-137">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e57c9-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e57c9-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e57c9-138">INPUTS</span></span>

### <span data-ttu-id="e57c9-139">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e57c9-139">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="e57c9-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e57c9-140">OUTPUTS</span></span>

### <span data-ttu-id="e57c9-141">Microsoft. Azure. Commands. SQL. DataClassification. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="e57c9-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="e57c9-142">Note</span><span class="sxs-lookup"><span data-stu-id="e57c9-142">NOTES</span></span>

## <span data-ttu-id="e57c9-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e57c9-143">RELATED LINKS</span></span>

[<span data-ttu-id="e57c9-144">Altre informazioni sull'individuazione e la classificazione dei dati di database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="e57c9-144">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
