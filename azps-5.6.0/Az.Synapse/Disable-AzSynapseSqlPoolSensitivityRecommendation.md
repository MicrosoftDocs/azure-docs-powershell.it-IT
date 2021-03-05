---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/disable-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: a9085433bb888fa8e37405881a20a55a4f08b96d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961102"
---
# <span data-ttu-id="fb8db-101">Disable-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="fb8db-101">Disable-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="fb8db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb8db-102">SYNOPSIS</span></span>
<span data-ttu-id="fb8db-103">Disabilita (ignora) i suggerimenti di riservatezza per le colonne nel SQL pool.</span><span class="sxs-lookup"><span data-stu-id="fb8db-103">Disables (dismisses) sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="fb8db-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fb8db-104">SYNTAX</span></span>

### <span data-ttu-id="fb8db-105">InputObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fb8db-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation -InputObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb8db-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb8db-106">ColumnParameterSet</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb8db-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb8db-107">SqlPoolObjectColumnParameterSet</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb8db-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fb8db-108">DESCRIPTION</span></span>
<span data-ttu-id="fb8db-109">Il cmdlet Disable-AzSynapseSqlPoolSensitivityRecommendation disabilita (elimina) i suggerimenti di riservatezza per le colonne nel pool SQL.</span><span class="sxs-lookup"><span data-stu-id="fb8db-109">The Disable-AzSynapseSqlPoolSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="fb8db-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fb8db-110">EXAMPLES</span></span>

### <span data-ttu-id="fb8db-111">Esempio 1: Disabilitare i suggerimenti di riservatezza per una determinata colonna in un pool di SQL Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="fb8db-111">Example 1: Disable sensitivity recommendations on a given column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Disable-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="fb8db-112">Esempio 2: Disabilitare i suggerimenti di riservatezza per le colonne che hanno suggerimenti di riservatezza in un pool di SQL Azure Synapse con Piping.</span><span class="sxs-lookup"><span data-stu-id="fb8db-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Disable-AzSynapseSqlPoolSensitivityRecommendation
```

### <span data-ttu-id="fb8db-113">Esempio 3: Disabilitare i suggerimenti di riservatezza per una determinata colonna in un pool SQL Azure Synapse con Piping.</span><span class="sxs-lookup"><span data-stu-id="fb8db-113">Example 3: Disable sensitivity recommendations on a given column in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Disable-AzSynapseSqlPoolSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="fb8db-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb8db-114">PARAMETERS</span></span>

### <span data-ttu-id="fb8db-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb8db-115">-AsJob</span></span>
<span data-ttu-id="fb8db-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="fb8db-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb8db-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="fb8db-117">-ColumnName</span></span>
<span data-ttu-id="fb8db-118">Nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="fb8db-118">Name of column.</span></span>

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

### <span data-ttu-id="fb8db-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb8db-119">-DefaultProfile</span></span>
<span data-ttu-id="fb8db-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fb8db-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb8db-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb8db-121">-InputObject</span></span>
<span data-ttu-id="fb8db-122">Oggetto che rappresenta una classificazione SQL riservatezza del pool.</span><span class="sxs-lookup"><span data-stu-id="fb8db-122">An object representing a SQL Pool Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel
Parameter Sets: InputObjectParameterSet
Aliases: ClassificationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb8db-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb8db-123">-PassThru</span></span>
<span data-ttu-id="fb8db-124">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="fb8db-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="fb8db-125">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="fb8db-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="fb8db-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb8db-126">-ResourceGroupName</span></span>
<span data-ttu-id="fb8db-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fb8db-127">Resource group name.</span></span>

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

### <span data-ttu-id="fb8db-128">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="fb8db-128">-SchemaName</span></span>
<span data-ttu-id="fb8db-129">Nome dello schema.</span><span class="sxs-lookup"><span data-stu-id="fb8db-129">Name of schema.</span></span>

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

### <span data-ttu-id="fb8db-130">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="fb8db-130">-SqlPoolName</span></span>
<span data-ttu-id="fb8db-131">Nome del pool SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="fb8db-131">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="fb8db-132">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="fb8db-132">-SqlPoolObject</span></span>
<span data-ttu-id="fb8db-133">SQL di input del pool, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="fb8db-133">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="fb8db-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="fb8db-134">-TableName</span></span>
<span data-ttu-id="fb8db-135">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="fb8db-135">Name of table.</span></span>

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

### <span data-ttu-id="fb8db-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fb8db-136">-WorkspaceName</span></span>
<span data-ttu-id="fb8db-137">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="fb8db-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="fb8db-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb8db-138">-Confirm</span></span>
<span data-ttu-id="fb8db-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb8db-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb8db-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb8db-140">-WhatIf</span></span>
<span data-ttu-id="fb8db-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb8db-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb8db-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fb8db-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb8db-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb8db-143">CommonParameters</span></span>
<span data-ttu-id="fb8db-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb8db-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb8db-145">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fb8db-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb8db-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="fb8db-146">INPUTS</span></span>

### <span data-ttu-id="fb8db-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="fb8db-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="fb8db-148">System.String</span><span class="sxs-lookup"><span data-stu-id="fb8db-148">System.String</span></span>

### <span data-ttu-id="fb8db-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="fb8db-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="fb8db-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fb8db-150">OUTPUTS</span></span>

### <span data-ttu-id="fb8db-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fb8db-151">System.Boolean</span></span>

## <span data-ttu-id="fb8db-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="fb8db-152">NOTES</span></span>

## <span data-ttu-id="fb8db-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fb8db-153">RELATED LINKS</span></span>
