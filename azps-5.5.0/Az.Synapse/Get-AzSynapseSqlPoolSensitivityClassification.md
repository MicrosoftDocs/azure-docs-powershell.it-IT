---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: 6affe94fdbfa7a698ad7d666d1847365fc8e25ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197366"
---
# <span data-ttu-id="ebca4-101">Get-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="ebca4-101">Get-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="ebca4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebca4-102">SYNOPSIS</span></span>
<span data-ttu-id="ebca4-103">Recupera i tipi di informazioni correnti e le etichette di riservatezza delle colonne nel pool SQL dati.</span><span class="sxs-lookup"><span data-stu-id="ebca4-103">Gets the current information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="ebca4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ebca4-104">SYNTAX</span></span>

### <span data-ttu-id="ebca4-105">SqlPoolObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ebca4-105">SqlPoolObjectParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebca4-106">SqlPoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebca4-106">SqlPoolParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebca4-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebca4-107">ColumnParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ebca4-108">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebca4-108">SqlPoolObjectColumnParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ebca4-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ebca4-109">DESCRIPTION</span></span>
<span data-ttu-id="ebca4-110">Il Get-AzSynapseSqlPoolSensitivityClassification cmdlet restituisce i tipi di informazioni correnti e le etichette di riservatezza delle colonne nel pool di SQL Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="ebca4-110">The Get-AzSynapseSqlPoolSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure Synapse SQL pool.</span></span>

## <span data-ttu-id="ebca4-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ebca4-111">EXAMPLES</span></span>

### <span data-ttu-id="ebca4-112">Esempio 1: Ottenere i tipi di informazioni correnti e le etichette di riservatezza di un pool di SQL Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="ebca4-112">Example 1: Get current information types and sensitivity labels of an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
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

### <span data-ttu-id="ebca4-113">Esempio 2: Ottenere i tipi di informazioni correnti e le etichette di riservatezza di un pool di SQL Azure Synapse con Piping.</span><span class="sxs-lookup"><span data-stu-id="ebca4-113">Example 2: Get current information types and sensitivity labels of an Azure Synapse SQL pool with Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Get-AzSynapseSqlPoolSensitivityClassification

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
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

### <span data-ttu-id="ebca4-114">Esempio 3: Ottenere il tipo di informazioni corrente e l'etichetta di riservatezza di una colonna specifica di un pool di SQL Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="ebca4-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="ebca4-115">Esempio 4: Ottenere il tipo di informazioni corrente e l'etichetta di riservatezza di una colonna specifica di un pool di SQL Azure Synapse usando Piping.</span><span class="sxs-lookup"><span data-stu-id="ebca4-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolSensitivityClassification -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

## <span data-ttu-id="ebca4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ebca4-116">PARAMETERS</span></span>

### <span data-ttu-id="ebca4-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ebca4-117">-AsJob</span></span>
<span data-ttu-id="ebca4-118">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ebca4-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ebca4-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="ebca4-119">-ColumnName</span></span>
<span data-ttu-id="ebca4-120">Nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="ebca4-120">Name of column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebca4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebca4-121">-DefaultProfile</span></span>
<span data-ttu-id="ebca4-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ebca4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebca4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebca4-123">-ResourceGroupName</span></span>
<span data-ttu-id="ebca4-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ebca4-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebca4-125">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="ebca4-125">-SchemaName</span></span>
<span data-ttu-id="ebca4-126">Nome dello schema.</span><span class="sxs-lookup"><span data-stu-id="ebca4-126">Name of schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebca4-127">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="ebca4-127">-SqlPoolName</span></span>
<span data-ttu-id="ebca4-128">Nome del pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="ebca4-128">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebca4-129">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="ebca4-129">-SqlPoolObject</span></span>
<span data-ttu-id="ebca4-130">SQL di input del pool, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="ebca4-130">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SqlPoolObjectParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebca4-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="ebca4-131">-TableName</span></span>
<span data-ttu-id="ebca4-132">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="ebca4-132">Name of table.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebca4-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ebca4-133">-WorkspaceName</span></span>
<span data-ttu-id="ebca4-134">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="ebca4-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ebca4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebca4-135">CommonParameters</span></span>
<span data-ttu-id="ebca4-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebca4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebca4-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ebca4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebca4-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="ebca4-138">INPUTS</span></span>

### <span data-ttu-id="ebca4-139">System.String</span><span class="sxs-lookup"><span data-stu-id="ebca4-139">System.String</span></span>

### <span data-ttu-id="ebca4-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="ebca4-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="ebca4-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ebca4-141">OUTPUTS</span></span>

### <span data-ttu-id="ebca4-142">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="ebca4-142">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

## <span data-ttu-id="ebca4-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="ebca4-143">NOTES</span></span>

## <span data-ttu-id="ebca4-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ebca4-144">RELATED LINKS</span></span>
