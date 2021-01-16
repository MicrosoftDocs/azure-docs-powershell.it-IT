---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: 89b9b5df2f8233254d4c1cb430a80f0a8a91c13b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383820"
---
# <span data-ttu-id="6f6a2-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="6f6a2-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="6f6a2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6f6a2-102">SYNOPSIS</span></span>
<span data-ttu-id="6f6a2-103">Ottiene i tipi di informazioni e le etichette di sensitività consigliati delle colonne nel pool SQL.</span><span class="sxs-lookup"><span data-stu-id="6f6a2-103">Gets the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="6f6a2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6f6a2-104">SYNTAX</span></span>

### <span data-ttu-id="6f6a2-105">SqlPoolObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6f6a2-105">SqlPoolObjectParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f6a2-106">SqlPoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="6f6a2-106">SqlPoolParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f6a2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6f6a2-107">DESCRIPTION</span></span>
<span data-ttu-id="6f6a2-108">Il cmdlet Get-AzSynapseSqlPoolSensitivityRecommendation restituisce i tipi di informazioni e le etichette di sensitività consigliati delle colonne nel pool SQL.</span><span class="sxs-lookup"><span data-stu-id="6f6a2-108">The Get-AzSynapseSqlPoolSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="6f6a2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6f6a2-109">EXAMPLES</span></span>

### <span data-ttu-id="6f6a2-110">Esempio 1: ottenere i tipi di informazioni e le etichette di sensitività consigliati di un pool di SQL sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="6f6a2-110">Example 1: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool.</span></span>
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

### <span data-ttu-id="6f6a2-111">Esempio 2: ottenere i tipi di informazioni e le etichette di sensitività consigliati di un pool di SQL sinapsi di Azure tramite piping.</span><span class="sxs-lookup"><span data-stu-id="6f6a2-111">Example 2: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool using Piping.</span></span>
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

## <span data-ttu-id="6f6a2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6f6a2-112">PARAMETERS</span></span>

### <span data-ttu-id="6f6a2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f6a2-113">-AsJob</span></span>
<span data-ttu-id="6f6a2-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6f6a2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6f6a2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f6a2-115">-DefaultProfile</span></span>
<span data-ttu-id="6f6a2-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6f6a2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f6a2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f6a2-117">-ResourceGroupName</span></span>
<span data-ttu-id="6f6a2-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6f6a2-118">Resource group name.</span></span>

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

### <span data-ttu-id="6f6a2-119">-Sqlpoolname</span><span class="sxs-lookup"><span data-stu-id="6f6a2-119">-SqlPoolName</span></span>
<span data-ttu-id="6f6a2-120">Nome del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="6f6a2-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="6f6a2-121">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="6f6a2-121">-SqlPoolObject</span></span>
<span data-ttu-id="6f6a2-122">Oggetto di input del pool SQL, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="6f6a2-122">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6f6a2-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6f6a2-123">-WorkspaceName</span></span>
<span data-ttu-id="6f6a2-124">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="6f6a2-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6f6a2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f6a2-125">CommonParameters</span></span>
<span data-ttu-id="6f6a2-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f6a2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f6a2-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f6a2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f6a2-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6f6a2-128">INPUTS</span></span>

### <span data-ttu-id="6f6a2-129">System. String</span><span class="sxs-lookup"><span data-stu-id="6f6a2-129">System.String</span></span>

### <span data-ttu-id="6f6a2-130">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="6f6a2-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="6f6a2-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6f6a2-131">OUTPUTS</span></span>

### <span data-ttu-id="6f6a2-132">Microsoft. Azure. Commands. sinapsi. Models. DataClassification. SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="6f6a2-132">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

## <span data-ttu-id="6f6a2-133">Note</span><span class="sxs-lookup"><span data-stu-id="6f6a2-133">NOTES</span></span>

## <span data-ttu-id="6f6a2-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6f6a2-134">RELATED LINKS</span></span>
