---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: beada19e6b5ba7792c3fda6ca07ce987bd15fe2a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372018"
---
# <span data-ttu-id="78b6f-101">Get-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="78b6f-101">Get-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="78b6f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="78b6f-102">SYNOPSIS</span></span>
<span data-ttu-id="78b6f-103">Ottiene i tipi di informazioni correnti e le etichette di sensitività delle colonne nel database.</span><span class="sxs-lookup"><span data-stu-id="78b6f-103">Gets the current information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="78b6f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="78b6f-104">SYNTAX</span></span>

### <span data-ttu-id="78b6f-105">DatabaseObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="78b6f-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78b6f-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="78b6f-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78b6f-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="78b6f-107">ColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="78b6f-108">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="78b6f-108">DatabaseObjectColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="78b6f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78b6f-109">DESCRIPTION</span></span>
<span data-ttu-id="78b6f-110">Il cmdlet Get-AzSqlDatabaseSensitivityClassification restituisce i tipi di informazioni correnti e le etichette di sensitività delle colonne nel database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="78b6f-110">The Get-AzSqlDatabaseSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure SQL database.</span></span>

## <span data-ttu-id="78b6f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="78b6f-111">EXAMPLES</span></span>

### <span data-ttu-id="78b6f-112">Esempio 1: ottenere i tipi di informazioni correnti e le etichette di sensitività di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="78b6f-112">Example 1: Get current information types and sensitivity labels of an Azure SQL Database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="78b6f-113">Esempio 2: ottenere i tipi di informazioni correnti e le etichette di sensitività di un database SQL di Azure con piping.</span><span class="sxs-lookup"><span data-stu-id="78b6f-113">Example 2: Get current information types and sensitivity labels of an Azure SQL Database with Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityClassification

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="78b6f-114">Esempio 3: ottenere il tipo di informazioni corrente e l'etichetta di sensitività di una specifica colonna di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="78b6f-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure SQL Database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityClassification -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="78b6f-115">Esempio 4: ottenere il tipo di informazioni corrente e l'etichetta di sensitività di una specifica colonna di un database SQL di Azure tramite piping.</span><span class="sxs-lookup"><span data-stu-id="78b6f-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure SQL Database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityClassification -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

## <span data-ttu-id="78b6f-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="78b6f-116">PARAMETERS</span></span>

### <span data-ttu-id="78b6f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78b6f-117">-AsJob</span></span>
<span data-ttu-id="78b6f-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="78b6f-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="78b6f-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="78b6f-119">-ColumnName</span></span>
<span data-ttu-id="78b6f-120">Nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="78b6f-120">Name of column.</span></span>

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

### <span data-ttu-id="78b6f-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="78b6f-121">-DatabaseName</span></span>
<span data-ttu-id="78b6f-122">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="78b6f-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="78b6f-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="78b6f-123">-DatabaseObject</span></span>
<span data-ttu-id="78b6f-124">Oggetto database SQL.</span><span class="sxs-lookup"><span data-stu-id="78b6f-124">The SQL database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet, DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78b6f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78b6f-125">-DefaultProfile</span></span>
<span data-ttu-id="78b6f-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="78b6f-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78b6f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78b6f-127">-ResourceGroupName</span></span>
<span data-ttu-id="78b6f-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="78b6f-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="78b6f-129">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="78b6f-129">-SchemaName</span></span>
<span data-ttu-id="78b6f-130">Nome dello schema.</span><span class="sxs-lookup"><span data-stu-id="78b6f-130">Name of schema.</span></span>

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

### <span data-ttu-id="78b6f-131">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="78b6f-131">-ServerName</span></span>
<span data-ttu-id="78b6f-132">Nome di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="78b6f-132">SQL server name.</span></span>

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

### <span data-ttu-id="78b6f-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="78b6f-133">-TableName</span></span>
<span data-ttu-id="78b6f-134">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="78b6f-134">Name of table.</span></span>

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

### <span data-ttu-id="78b6f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78b6f-135">CommonParameters</span></span>
<span data-ttu-id="78b6f-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78b6f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78b6f-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78b6f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78b6f-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="78b6f-138">INPUTS</span></span>

### <span data-ttu-id="78b6f-139">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="78b6f-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="78b6f-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="78b6f-140">OUTPUTS</span></span>

### <span data-ttu-id="78b6f-141">Microsoft. Azure. Commands. SQL. DataClassification. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="78b6f-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="78b6f-142">Note</span><span class="sxs-lookup"><span data-stu-id="78b6f-142">NOTES</span></span>

## <span data-ttu-id="78b6f-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="78b6f-143">RELATED LINKS</span></span>

[<span data-ttu-id="78b6f-144">Altre informazioni sull'individuazione e la classificazione dei dati di database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="78b6f-144">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
