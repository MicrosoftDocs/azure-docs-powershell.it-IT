---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasesensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityClassification.md
ms.openlocfilehash: beada19e6b5ba7792c3fda6ca07ce987bd15fe2a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191127"
---
# <span data-ttu-id="73b37-101">Get-AzSqlDatabaseSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="73b37-101">Get-AzSqlDatabaseSensitivityClassification</span></span>

## <span data-ttu-id="73b37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73b37-102">SYNOPSIS</span></span>
<span data-ttu-id="73b37-103">Recupera i tipi di informazioni correnti e le etichette di riservatezza delle colonne nel database.</span><span class="sxs-lookup"><span data-stu-id="73b37-103">Gets the current information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="73b37-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="73b37-104">SYNTAX</span></span>

### <span data-ttu-id="73b37-105">DatabaseObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="73b37-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73b37-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="73b37-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73b37-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="73b37-107">ColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73b37-108">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="73b37-108">DatabaseObjectColumnParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityClassification -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="73b37-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="73b37-109">DESCRIPTION</span></span>
<span data-ttu-id="73b37-110">Il Get-AzSqlDatabaseSensitivityClassification cmdlet di riservatezza restituisce i tipi di informazioni correnti e le etichette di riservatezza delle colonne nel database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="73b37-110">The Get-AzSqlDatabaseSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure SQL database.</span></span>

## <span data-ttu-id="73b37-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="73b37-111">EXAMPLES</span></span>

### <span data-ttu-id="73b37-112">Esempio 1: Ottenere i tipi di informazioni correnti e le etichette di riservatezza di un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="73b37-112">Example 1: Get current information types and sensitivity labels of an Azure SQL Database.</span></span>
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

### <span data-ttu-id="73b37-113">Esempio 2: Ottenere i tipi di informazioni correnti e le etichette di riservatezza di un database SQL Azure con Piping.</span><span class="sxs-lookup"><span data-stu-id="73b37-113">Example 2: Get current information types and sensitivity labels of an Azure SQL Database with Piping.</span></span>
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

### <span data-ttu-id="73b37-114">Esempio 3: Ottenere il tipo di informazioni corrente e l'etichetta di riservatezza di una colonna specifica di un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="73b37-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure SQL Database.</span></span>
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

### <span data-ttu-id="73b37-115">Esempio 4: Ottenere il tipo di informazioni corrente e l'etichetta di riservatezza di una colonna specifica di un database SQL Azure usando Piping.</span><span class="sxs-lookup"><span data-stu-id="73b37-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure SQL Database using Piping.</span></span>
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

## <span data-ttu-id="73b37-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73b37-116">PARAMETERS</span></span>

### <span data-ttu-id="73b37-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73b37-117">-AsJob</span></span>
<span data-ttu-id="73b37-118">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="73b37-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="73b37-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="73b37-119">-ColumnName</span></span>
<span data-ttu-id="73b37-120">Nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="73b37-120">Name of column.</span></span>

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

### <span data-ttu-id="73b37-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="73b37-121">-DatabaseName</span></span>
<span data-ttu-id="73b37-122">Il nome del database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="73b37-122">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="73b37-123">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="73b37-123">-DatabaseObject</span></span>
<span data-ttu-id="73b37-124">Oggetto SQL di database.</span><span class="sxs-lookup"><span data-stu-id="73b37-124">The SQL database object.</span></span>

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

### <span data-ttu-id="73b37-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73b37-125">-DefaultProfile</span></span>
<span data-ttu-id="73b37-126">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="73b37-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73b37-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73b37-127">-ResourceGroupName</span></span>
<span data-ttu-id="73b37-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="73b37-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="73b37-129">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="73b37-129">-SchemaName</span></span>
<span data-ttu-id="73b37-130">Nome dello schema.</span><span class="sxs-lookup"><span data-stu-id="73b37-130">Name of schema.</span></span>

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

### <span data-ttu-id="73b37-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="73b37-131">-ServerName</span></span>
<span data-ttu-id="73b37-132">SQL del server.</span><span class="sxs-lookup"><span data-stu-id="73b37-132">SQL server name.</span></span>

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

### <span data-ttu-id="73b37-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="73b37-133">-TableName</span></span>
<span data-ttu-id="73b37-134">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="73b37-134">Name of table.</span></span>

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

### <span data-ttu-id="73b37-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73b37-135">CommonParameters</span></span>
<span data-ttu-id="73b37-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73b37-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73b37-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="73b37-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73b37-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="73b37-138">INPUTS</span></span>

### <span data-ttu-id="73b37-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="73b37-139">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="73b37-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="73b37-140">OUTPUTS</span></span>

### <span data-ttu-id="73b37-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="73b37-141">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="73b37-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="73b37-142">NOTES</span></span>

## <span data-ttu-id="73b37-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="73b37-143">RELATED LINKS</span></span>

[<span data-ttu-id="73b37-144">Altre informazioni sull'individuazione e la classificazione SQL dati del database di Azure</span><span class="sxs-lookup"><span data-stu-id="73b37-144">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
