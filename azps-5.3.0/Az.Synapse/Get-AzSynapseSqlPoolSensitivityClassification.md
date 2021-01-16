---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: 6affe94fdbfa7a698ad7d666d1847365fc8e25ac
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383837"
---
# <span data-ttu-id="c3e80-101">Get-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="c3e80-101">Get-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="c3e80-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c3e80-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e80-103">Ottiene i tipi di informazioni correnti e le etichette di sensitività delle colonne nel pool SQL.</span><span class="sxs-lookup"><span data-stu-id="c3e80-103">Gets the current information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="c3e80-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3e80-104">SYNTAX</span></span>

### <span data-ttu-id="c3e80-105">SqlPoolObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c3e80-105">SqlPoolObjectParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3e80-106">SqlPoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3e80-106">SqlPoolParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3e80-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3e80-107">ColumnParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3e80-108">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3e80-108">SqlPoolObjectColumnParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c3e80-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3e80-109">DESCRIPTION</span></span>
<span data-ttu-id="c3e80-110">Il cmdlet Get-AzSynapseSqlPoolSensitivityClassification restituisce i tipi di informazioni correnti e le etichette di sensitività delle colonne nel pool di SQL sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="c3e80-110">The Get-AzSynapseSqlPoolSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure Synapse SQL pool.</span></span>

## <span data-ttu-id="c3e80-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3e80-111">EXAMPLES</span></span>

### <span data-ttu-id="c3e80-112">Esempio 1: ottenere i tipi di informazioni correnti e le etichette di sensibilità di un pool di SQL sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="c3e80-112">Example 1: Get current information types and sensitivity labels of an Azure Synapse SQL pool.</span></span>
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

### <span data-ttu-id="c3e80-113">Esempio 2: ottenere i tipi di informazioni correnti e le etichette di sensibilità di un pool di SQL sinapsi di Azure con piping.</span><span class="sxs-lookup"><span data-stu-id="c3e80-113">Example 2: Get current information types and sensitivity labels of an Azure Synapse SQL pool with Piping.</span></span>
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

### <span data-ttu-id="c3e80-114">Esempio 3: ottenere il tipo di informazioni corrente e l'etichetta di sensitività di una specifica colonna di un pool di SQL sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="c3e80-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure Synapse SQL pool.</span></span>
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

### <span data-ttu-id="c3e80-115">Esempio 4: ottenere il tipo di informazioni corrente e l'etichetta di sensitività di una specifica colonna di un pool di SQL sinapsi di Azure tramite piping.</span><span class="sxs-lookup"><span data-stu-id="c3e80-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure Synapse SQL pool using Piping.</span></span>
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

## <span data-ttu-id="c3e80-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c3e80-116">PARAMETERS</span></span>

### <span data-ttu-id="c3e80-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3e80-117">-AsJob</span></span>
<span data-ttu-id="c3e80-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c3e80-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c3e80-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="c3e80-119">-ColumnName</span></span>
<span data-ttu-id="c3e80-120">Nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="c3e80-120">Name of column.</span></span>

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

### <span data-ttu-id="c3e80-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3e80-121">-DefaultProfile</span></span>
<span data-ttu-id="c3e80-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c3e80-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3e80-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3e80-123">-ResourceGroupName</span></span>
<span data-ttu-id="c3e80-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c3e80-124">Resource group name.</span></span>

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

### <span data-ttu-id="c3e80-125">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="c3e80-125">-SchemaName</span></span>
<span data-ttu-id="c3e80-126">Nome dello schema.</span><span class="sxs-lookup"><span data-stu-id="c3e80-126">Name of schema.</span></span>

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

### <span data-ttu-id="c3e80-127">-Sqlpoolname</span><span class="sxs-lookup"><span data-stu-id="c3e80-127">-SqlPoolName</span></span>
<span data-ttu-id="c3e80-128">Nome del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="c3e80-128">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="c3e80-129">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="c3e80-129">-SqlPoolObject</span></span>
<span data-ttu-id="c3e80-130">Oggetto di input del pool SQL, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="c3e80-130">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c3e80-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="c3e80-131">-TableName</span></span>
<span data-ttu-id="c3e80-132">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="c3e80-132">Name of table.</span></span>

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

### <span data-ttu-id="c3e80-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c3e80-133">-WorkspaceName</span></span>
<span data-ttu-id="c3e80-134">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="c3e80-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c3e80-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e80-135">CommonParameters</span></span>
<span data-ttu-id="c3e80-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3e80-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e80-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3e80-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e80-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c3e80-138">INPUTS</span></span>

### <span data-ttu-id="c3e80-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c3e80-139">System.String</span></span>

### <span data-ttu-id="c3e80-140">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="c3e80-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="c3e80-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3e80-141">OUTPUTS</span></span>

### <span data-ttu-id="c3e80-142">Microsoft. Azure. Commands. sinapsi. Models. DataClassification. SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="c3e80-142">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

## <span data-ttu-id="c3e80-143">Note</span><span class="sxs-lookup"><span data-stu-id="c3e80-143">NOTES</span></span>

## <span data-ttu-id="c3e80-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3e80-144">RELATED LINKS</span></span>
