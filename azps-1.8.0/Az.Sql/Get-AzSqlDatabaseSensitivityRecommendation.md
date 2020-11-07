---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: ba8229bcddf27a2a14d50efc2cbd32e6e47015c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676971"
---
# <span data-ttu-id="066f1-101">Get-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="066f1-101">Get-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="066f1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="066f1-102">SYNOPSIS</span></span>
<span data-ttu-id="066f1-103">Ottiene i tipi di informazioni e le etichette di sensitività consigliati delle colonne nel database.</span><span class="sxs-lookup"><span data-stu-id="066f1-103">Gets the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="066f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="066f1-104">SYNTAX</span></span>

### <span data-ttu-id="066f1-105">DatabaseObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="066f1-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="066f1-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="066f1-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="066f1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="066f1-107">DESCRIPTION</span></span>
<span data-ttu-id="066f1-108">Il cmdlet Get-AzSqlDatabaseSensitivityRecommendation restituisce i tipi di informazioni e le etichette di sensitività consigliati delle colonne nel database.</span><span class="sxs-lookup"><span data-stu-id="066f1-108">The Get-AzSqlDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="066f1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="066f1-109">EXAMPLES</span></span>

### <span data-ttu-id="066f1-110">Esempio 1: ottenere i tipi di informazioni e le etichette di sensitività consigliati di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="066f1-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database

ResourceGroupName : resourceGroup
ServerName        : server
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

### <span data-ttu-id="066f1-111">Esempio 2: ottenere i tipi di informazioni e le etichette di sensitività consigliati di un database SQL di Azure tramite piping.</span><span class="sxs-lookup"><span data-stu-id="066f1-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityRecommendation

ResourceGroupName : resourceGroup
ServerName        : server
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

## <span data-ttu-id="066f1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="066f1-112">PARAMETERS</span></span>

### <span data-ttu-id="066f1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="066f1-113">-AsJob</span></span>
<span data-ttu-id="066f1-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="066f1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="066f1-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="066f1-115">-DatabaseName</span></span>
<span data-ttu-id="066f1-116">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="066f1-116">The name of the Azure SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="066f1-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="066f1-117">-DatabaseObject</span></span>
<span data-ttu-id="066f1-118">Oggetto database SQL.</span><span class="sxs-lookup"><span data-stu-id="066f1-118">The SQL database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="066f1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="066f1-119">-DefaultProfile</span></span>
<span data-ttu-id="066f1-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="066f1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="066f1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="066f1-121">-ResourceGroupName</span></span>
<span data-ttu-id="066f1-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="066f1-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="066f1-123">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="066f1-123">-ServerName</span></span>
<span data-ttu-id="066f1-124">Nome di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="066f1-124">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="066f1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="066f1-125">CommonParameters</span></span>
<span data-ttu-id="066f1-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="066f1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="066f1-127">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="066f1-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="066f1-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="066f1-128">INPUTS</span></span>

### <span data-ttu-id="066f1-129">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="066f1-129">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="066f1-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="066f1-130">OUTPUTS</span></span>

### <span data-ttu-id="066f1-131">Microsoft. Azure. Commands. SQL. DataClassification. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="066f1-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="066f1-132">Note</span><span class="sxs-lookup"><span data-stu-id="066f1-132">NOTES</span></span>

## <span data-ttu-id="066f1-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="066f1-133">RELATED LINKS</span></span>

[<span data-ttu-id="066f1-134">Altre informazioni sull'individuazione e la classificazione dei dati di database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="066f1-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)