---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlInstanceDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: d5923be20fd893aefee4e9a5789c2f6f57f20fbe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676923"
---
# <span data-ttu-id="9a190-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="9a190-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="9a190-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9a190-102">SYNOPSIS</span></span>
<span data-ttu-id="9a190-103">Ottiene i tipi di informazioni e le etichette di sensitività consigliati delle colonne nel database di istanze gestite di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="9a190-103">Gets the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="9a190-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9a190-104">SYNTAX</span></span>

### <span data-ttu-id="9a190-105">DatabaseObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9a190-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a190-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a190-106">DatabaseParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a190-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a190-107">DESCRIPTION</span></span>
<span data-ttu-id="9a190-108">Il cmdlet Get-AzSqlInstanceDatabaseSensitivityRecommendation restituisce i tipi di informazioni e le etichette di sensitività consigliati delle colonne nel database di istanze gestite di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="9a190-108">The Get-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="9a190-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9a190-109">EXAMPLES</span></span>

### <span data-ttu-id="9a190-110">Esempio 1: ottenere i tipi di informazioni e le etichette di sensitività consigliati di un database di istanze gestite di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="9a190-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database

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

### <span data-ttu-id="9a190-111">Esempio 2: ottenere tipi di informazioni e etichette di sensitività consigliate di un database di istanze gestite di Azure SQL tramite piping.</span><span class="sxs-lookup"><span data-stu-id="9a190-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL managed instance database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityRecommendation

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

## <span data-ttu-id="9a190-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9a190-112">PARAMETERS</span></span>

### <span data-ttu-id="9a190-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a190-113">-AsJob</span></span>
<span data-ttu-id="9a190-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9a190-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a190-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9a190-115">-DatabaseName</span></span>
<span data-ttu-id="9a190-116">Nome del database di istanze gestite di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="9a190-116">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="9a190-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="9a190-117">-DatabaseObject</span></span>
<span data-ttu-id="9a190-118">Oggetto di database dell'istanza gestita di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="9a190-118">The Azure SQL managed instance database object.</span></span>

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

### <span data-ttu-id="9a190-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a190-119">-DefaultProfile</span></span>
<span data-ttu-id="9a190-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9a190-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a190-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="9a190-121">-InstanceName</span></span>
<span data-ttu-id="9a190-122">Nome dell'istanza gestita di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="9a190-122">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="9a190-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a190-123">-ResourceGroupName</span></span>
<span data-ttu-id="9a190-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9a190-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="9a190-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a190-125">CommonParameters</span></span>
<span data-ttu-id="9a190-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a190-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a190-127">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a190-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a190-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9a190-128">INPUTS</span></span>

### <span data-ttu-id="9a190-129">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="9a190-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="9a190-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9a190-130">OUTPUTS</span></span>

### <span data-ttu-id="9a190-131">Microsoft. Azure. Commands. SQL. DataClassification. Model. ManagedDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="9a190-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="9a190-132">Note</span><span class="sxs-lookup"><span data-stu-id="9a190-132">NOTES</span></span>

## <span data-ttu-id="9a190-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9a190-133">RELATED LINKS</span></span>

[<span data-ttu-id="9a190-134">Altre informazioni sull'individuazione e la classificazione dei dati di database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="9a190-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
