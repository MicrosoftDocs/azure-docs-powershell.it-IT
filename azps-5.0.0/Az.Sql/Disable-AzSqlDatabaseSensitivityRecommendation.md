---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/disable-azsqldatabasesensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Disable-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: f9a8ab299571e4e04f3061773d19b920f52d22a8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193639"
---
# <span data-ttu-id="ef058-101">Disable-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="ef058-101">Disable-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="ef058-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ef058-102">SYNOPSIS</span></span>
<span data-ttu-id="ef058-103">Disabilita (respinge) i consigli di sensitività sulle colonne del database.</span><span class="sxs-lookup"><span data-stu-id="ef058-103">Disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="ef058-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ef058-104">SYNTAX</span></span>

### <span data-ttu-id="ef058-105">InputObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ef058-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -InputObject <SqlDatabaseSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef058-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef058-106">ColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef058-107">DatabaseObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef058-107">DatabaseObjectColumnParameterSet</span></span>
```
Disable-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef058-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef058-108">DESCRIPTION</span></span>
<span data-ttu-id="ef058-109">Il cmdlet Disable-AzSqlDatabaseSensitivityRecommendation Disabilita le raccomandazioni di sensitivity per le colonne del database.</span><span class="sxs-lookup"><span data-stu-id="ef058-109">The Disable-AzSqlDatabaseSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the database.</span></span>

## <span data-ttu-id="ef058-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ef058-110">EXAMPLES</span></span>

### <span data-ttu-id="ef058-111">Esempio 1: disabilitare i consigli di sensitività per una determinata colonna in un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="ef058-111">Example 1: Disable sensitivity recommendations on a given column in an Azure SQL Database.</span></span>
```powershell
PS C:\> Disable-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="ef058-112">Esempio 2: disabilitare i consigli di sensitività per le colonne che hanno suggerimenti per la sensibilità in un database SQL di Azure tramite piping.</span><span class="sxs-lookup"><span data-stu-id="ef058-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation
```

### <span data-ttu-id="ef058-113">Esempio 3: disabilitare i consigli di sensitività per una determinata colonna in un database SQL di Azure tramite piping.</span><span class="sxs-lookup"><span data-stu-id="ef058-113">Example 3: Disable sensitivity recommendations on a given column in an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Disable-AzSqlDatabaseSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="ef058-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ef058-114">PARAMETERS</span></span>

### <span data-ttu-id="ef058-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef058-115">-AsJob</span></span>
<span data-ttu-id="ef058-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ef058-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ef058-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="ef058-117">-ColumnName</span></span>
<span data-ttu-id="ef058-118">Nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="ef058-118">Name of column.</span></span>

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

### <span data-ttu-id="ef058-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ef058-119">-DatabaseName</span></span>
<span data-ttu-id="ef058-120">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="ef058-120">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="ef058-121">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="ef058-121">-DatabaseObject</span></span>
<span data-ttu-id="ef058-122">Oggetto database SQL.</span><span class="sxs-lookup"><span data-stu-id="ef058-122">The SQL database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef058-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef058-123">-DefaultProfile</span></span>
<span data-ttu-id="ef058-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ef058-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef058-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef058-125">-InputObject</span></span>
<span data-ttu-id="ef058-126">Oggetto che rappresenta una classificazione di sensitivity del database SQL.</span><span class="sxs-lookup"><span data-stu-id="ef058-126">An object representing a SQL Database Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel
Parameter Sets: InputObjectParameterSet
Aliases: ClassificationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef058-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef058-127">-PassThru</span></span>
<span data-ttu-id="ef058-128">Specifica se restituire il modello di classificazione della sensibilità alla fine dell'esecuzione dei cmdlet</span><span class="sxs-lookup"><span data-stu-id="ef058-128">Specifies whether to output the sensitivity classification model at end of cmdlet execution</span></span>

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

### <span data-ttu-id="ef058-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef058-129">-ResourceGroupName</span></span>
<span data-ttu-id="ef058-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ef058-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="ef058-131">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="ef058-131">-SchemaName</span></span>
<span data-ttu-id="ef058-132">Nome dello schema.</span><span class="sxs-lookup"><span data-stu-id="ef058-132">Name of schema.</span></span>

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

### <span data-ttu-id="ef058-133">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="ef058-133">-ServerName</span></span>
<span data-ttu-id="ef058-134">Nome di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ef058-134">SQL server name.</span></span>

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

### <span data-ttu-id="ef058-135">-TableName</span><span class="sxs-lookup"><span data-stu-id="ef058-135">-TableName</span></span>
<span data-ttu-id="ef058-136">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="ef058-136">Name of table.</span></span>

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

### <span data-ttu-id="ef058-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ef058-137">-Confirm</span></span>
<span data-ttu-id="ef058-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef058-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef058-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef058-139">-WhatIf</span></span>
<span data-ttu-id="ef058-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ef058-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef058-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ef058-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef058-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef058-142">CommonParameters</span></span>
<span data-ttu-id="ef058-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef058-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef058-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef058-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef058-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ef058-145">INPUTS</span></span>

### <span data-ttu-id="ef058-146">Microsoft. Azure. Commands. SQL. DataClassification. Model. SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="ef058-146">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="ef058-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ef058-147">OUTPUTS</span></span>

### <span data-ttu-id="ef058-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ef058-148">System.Boolean</span></span>

## <span data-ttu-id="ef058-149">Note</span><span class="sxs-lookup"><span data-stu-id="ef058-149">NOTES</span></span>

## <span data-ttu-id="ef058-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ef058-150">RELATED LINKS</span></span>

[<span data-ttu-id="ef058-151">Altre informazioni sull'individuazione e la classificazione dei dati di database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="ef058-151">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)