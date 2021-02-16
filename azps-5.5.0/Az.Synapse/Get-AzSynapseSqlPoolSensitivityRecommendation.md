---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: 89b9b5df2f8233254d4c1cb430a80f0a8a91c13b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195607"
---
# <span data-ttu-id="e5d32-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="e5d32-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="e5d32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5d32-102">SYNOPSIS</span></span>
<span data-ttu-id="e5d32-103">Recupera i tipi di informazioni consigliati e le etichette di riservatezza delle colonne nel SQL pool.</span><span class="sxs-lookup"><span data-stu-id="e5d32-103">Gets the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="e5d32-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5d32-104">SYNTAX</span></span>

### <span data-ttu-id="e5d32-105">SqlPoolObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e5d32-105">SqlPoolObjectParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5d32-106">SqlPoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5d32-106">SqlPoolParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5d32-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e5d32-107">DESCRIPTION</span></span>
<span data-ttu-id="e5d32-108">Il Get-AzSynapseSqlPoolSensitivityRecommendation cmdlet restituisce i tipi di informazioni consigliate e le etichette di riservatezza delle colonne nel pool SQL dati.</span><span class="sxs-lookup"><span data-stu-id="e5d32-108">The Get-AzSynapseSqlPoolSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="e5d32-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5d32-109">EXAMPLES</span></span>

### <span data-ttu-id="e5d32-110">Esempio 1: Ottenere i tipi di informazioni consigliati e le etichette di riservatezza di un pool di SQL Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="e5d32-110">Example 1: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool

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

### <span data-ttu-id="e5d32-111">Esempio 2: ottenere i tipi di informazioni consigliati e le etichette di riservatezza di un pool di SQL Azure Synapse con Piping.</span><span class="sxs-lookup"><span data-stu-id="e5d32-111">Example 2: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolSensitivityRecommendation

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

## <span data-ttu-id="e5d32-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5d32-112">PARAMETERS</span></span>

### <span data-ttu-id="e5d32-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5d32-113">-AsJob</span></span>
<span data-ttu-id="e5d32-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e5d32-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e5d32-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5d32-115">-DefaultProfile</span></span>
<span data-ttu-id="e5d32-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e5d32-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5d32-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5d32-117">-ResourceGroupName</span></span>
<span data-ttu-id="e5d32-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e5d32-118">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5d32-119">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="e5d32-119">-SqlPoolName</span></span>
<span data-ttu-id="e5d32-120">Nome del pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="e5d32-120">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5d32-121">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="e5d32-121">-SqlPoolObject</span></span>
<span data-ttu-id="e5d32-122">SQL di input del pool, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="e5d32-122">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SqlPoolObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5d32-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e5d32-123">-WorkspaceName</span></span>
<span data-ttu-id="e5d32-124">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="e5d32-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5d32-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5d32-125">CommonParameters</span></span>
<span data-ttu-id="e5d32-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5d32-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5d32-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e5d32-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5d32-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="e5d32-128">INPUTS</span></span>

### <span data-ttu-id="e5d32-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e5d32-129">System.String</span></span>

### <span data-ttu-id="e5d32-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="e5d32-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="e5d32-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5d32-131">OUTPUTS</span></span>

### <span data-ttu-id="e5d32-132">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="e5d32-132">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

## <span data-ttu-id="e5d32-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="e5d32-133">NOTES</span></span>

## <span data-ttu-id="e5d32-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5d32-134">RELATED LINKS</span></span>
