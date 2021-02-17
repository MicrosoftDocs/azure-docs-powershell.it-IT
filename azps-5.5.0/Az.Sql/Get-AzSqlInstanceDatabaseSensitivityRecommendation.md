---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlInstanceDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: cf9250080e0d8e079257a4996b7d263bd96a2093
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196167"
---
# <span data-ttu-id="b1f78-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="b1f78-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="b1f78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1f78-102">SYNOPSIS</span></span>
<span data-ttu-id="b1f78-103">Recupera i tipi di informazioni consigliati e le etichette di riservatezza delle colonne nel database SQL istanza gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="b1f78-103">Gets the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="b1f78-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1f78-104">SYNTAX</span></span>

### <span data-ttu-id="b1f78-105">DatabaseObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b1f78-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1f78-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1f78-106">DatabaseParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1f78-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b1f78-107">DESCRIPTION</span></span>
<span data-ttu-id="b1f78-108">Il Get-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet restituisce i tipi di informazioni consigliate e le etichette di riservatezza delle colonne nel database SQL di istanze gestite di Azure.</span><span class="sxs-lookup"><span data-stu-id="b1f78-108">The Get-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="b1f78-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1f78-109">EXAMPLES</span></span>

### <span data-ttu-id="b1f78-110">Esempio 1: Ottenere i tipi di informazioni consigliati e le etichette di riservatezza di un database SQL istanza gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="b1f78-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

### <span data-ttu-id="b1f78-111">Esempio 2: ottenere i tipi di informazioni consigliati e le etichette di riservatezza di un database di SQL gestito di Azure con Piping.</span><span class="sxs-lookup"><span data-stu-id="b1f78-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL managed instance database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityRecommendation

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

## <span data-ttu-id="b1f78-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1f78-112">PARAMETERS</span></span>

### <span data-ttu-id="b1f78-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1f78-113">-AsJob</span></span>
<span data-ttu-id="b1f78-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b1f78-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1f78-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b1f78-115">-DatabaseName</span></span>
<span data-ttu-id="b1f78-116">Il nome del database dell'SQL gestito di Azure.</span><span class="sxs-lookup"><span data-stu-id="b1f78-116">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="b1f78-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="b1f78-117">-DatabaseObject</span></span>
<span data-ttu-id="b1f78-118">L'oggetto SQL di istanza gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="b1f78-118">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b1f78-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1f78-119">-DefaultProfile</span></span>
<span data-ttu-id="b1f78-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b1f78-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1f78-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="b1f78-121">-InstanceName</span></span>
<span data-ttu-id="b1f78-122">Nome SQL'istanza gestita di Azure.</span><span class="sxs-lookup"><span data-stu-id="b1f78-122">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="b1f78-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1f78-123">-ResourceGroupName</span></span>
<span data-ttu-id="b1f78-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b1f78-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="b1f78-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1f78-125">CommonParameters</span></span>
<span data-ttu-id="b1f78-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1f78-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1f78-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b1f78-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1f78-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="b1f78-128">INPUTS</span></span>

### <span data-ttu-id="b1f78-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="b1f78-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="b1f78-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1f78-130">OUTPUTS</span></span>

### <span data-ttu-id="b1f78-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="b1f78-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="b1f78-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="b1f78-132">NOTES</span></span>

## <span data-ttu-id="b1f78-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1f78-133">RELATED LINKS</span></span>

[<span data-ttu-id="b1f78-134">Altre informazioni sull'individuazione e la classificazione SQL dati del database di Azure</span><span class="sxs-lookup"><span data-stu-id="b1f78-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
