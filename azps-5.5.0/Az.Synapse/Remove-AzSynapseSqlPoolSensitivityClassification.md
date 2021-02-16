---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: a278b316a62639c6c33d4f05491e314a2b9a1e85
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182703"
---
# <span data-ttu-id="14df5-101">Remove-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="14df5-101">Remove-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="14df5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14df5-102">SYNOPSIS</span></span>
<span data-ttu-id="14df5-103">Rimuove i tipi di informazioni e le etichette di riservatezza delle colonne nel SQL pool.</span><span class="sxs-lookup"><span data-stu-id="14df5-103">Removes the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="14df5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14df5-104">SYNTAX</span></span>

### <span data-ttu-id="14df5-105">ClassificationObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="14df5-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification -ClassificationObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14df5-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="14df5-106">ColumnParameterSet</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14df5-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="14df5-107">SqlPoolObjectColumnParameterSet</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14df5-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="14df5-108">DESCRIPTION</span></span>
<span data-ttu-id="14df5-109">Il Remove-AzSynapseSqlPoolSensitivityClassification rimuovere i tipi di informazioni e le etichette di riservatezza delle colonne nel pool SQL informazioni.</span><span class="sxs-lookup"><span data-stu-id="14df5-109">The Remove-AzSynapseSqlPoolSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="14df5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14df5-110">EXAMPLES</span></span>

### <span data-ttu-id="14df5-111">Esempio 1: Rimuovere il tipo di informazioni e l'etichetta di riservatezza di una colonna in un pool di SQL Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="14df5-111">Example 1: Remove information type and sensitivity label of a column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="14df5-112">Esempio 2: Rimuovere i tipi di informazioni correnti e le etichette di riservatezza delle colonne in un pool SQL Azure Synapse con Piping.</span><span class="sxs-lookup"><span data-stu-id="14df5-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Remove-AzSynapseSqlPoolSensitivityClassification
```

### <span data-ttu-id="14df5-113">Esempio 3: Rimuovere il tipo di informazioni e l'etichetta di riservatezza di una colonna in un pool SQL Azure Synapse usando Piping.</span><span class="sxs-lookup"><span data-stu-id="14df5-113">Example 3: Remove information type and sensitivity label of a column in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Remove-AzSynapseSqlPoolSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="14df5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14df5-114">PARAMETERS</span></span>

### <span data-ttu-id="14df5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14df5-115">-AsJob</span></span>
<span data-ttu-id="14df5-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="14df5-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14df5-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="14df5-117">-ClassificationObject</span></span>
<span data-ttu-id="14df5-118">Oggetto che rappresenta una classificazione SQL riservatezza del pool.</span><span class="sxs-lookup"><span data-stu-id="14df5-118">An object representing a SQL Pool Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel
Parameter Sets: ClassificationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14df5-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="14df5-119">-ColumnName</span></span>
<span data-ttu-id="14df5-120">Nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="14df5-120">Name of column.</span></span>

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

### <span data-ttu-id="14df5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14df5-121">-DefaultProfile</span></span>
<span data-ttu-id="14df5-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="14df5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14df5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14df5-123">-PassThru</span></span>
<span data-ttu-id="14df5-124">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="14df5-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="14df5-125">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="14df5-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="14df5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14df5-126">-ResourceGroupName</span></span>
<span data-ttu-id="14df5-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="14df5-127">Resource group name.</span></span>

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

### <span data-ttu-id="14df5-128">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="14df5-128">-SchemaName</span></span>
<span data-ttu-id="14df5-129">Nome dello schema.</span><span class="sxs-lookup"><span data-stu-id="14df5-129">Name of schema.</span></span>

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

### <span data-ttu-id="14df5-130">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="14df5-130">-SqlPoolName</span></span>
<span data-ttu-id="14df5-131">Nome del pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="14df5-131">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="14df5-132">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="14df5-132">-SqlPoolObject</span></span>
<span data-ttu-id="14df5-133">SQL di input del pool, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="14df5-133">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14df5-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="14df5-134">-TableName</span></span>
<span data-ttu-id="14df5-135">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="14df5-135">Name of table.</span></span>

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

### <span data-ttu-id="14df5-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="14df5-136">-WorkspaceName</span></span>
<span data-ttu-id="14df5-137">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="14df5-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="14df5-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14df5-138">-Confirm</span></span>
<span data-ttu-id="14df5-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14df5-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14df5-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14df5-140">-WhatIf</span></span>
<span data-ttu-id="14df5-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14df5-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14df5-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14df5-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14df5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14df5-143">CommonParameters</span></span>
<span data-ttu-id="14df5-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14df5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14df5-145">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="14df5-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14df5-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="14df5-146">INPUTS</span></span>

### <span data-ttu-id="14df5-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="14df5-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="14df5-148">System.String</span><span class="sxs-lookup"><span data-stu-id="14df5-148">System.String</span></span>

### <span data-ttu-id="14df5-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="14df5-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="14df5-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14df5-150">OUTPUTS</span></span>

### <span data-ttu-id="14df5-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="14df5-151">System.Boolean</span></span>

## <span data-ttu-id="14df5-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="14df5-152">NOTES</span></span>

## <span data-ttu-id="14df5-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14df5-153">RELATED LINKS</span></span>
