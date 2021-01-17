---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/enable-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: 52abddf2db18a6e70a1b876629feff0761bed014
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474570"
---
# <span data-ttu-id="12ae3-101">Enable-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="12ae3-101">Enable-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="12ae3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="12ae3-102">SYNOPSIS</span></span>
<span data-ttu-id="12ae3-103">Abilita suggerimenti per la sensitività sulle colonne (le raccomandazioni sono abilitate per impostazione predefinita in tutte le colonne) nel pool SQL.</span><span class="sxs-lookup"><span data-stu-id="12ae3-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the SQL pool.</span></span>

## <span data-ttu-id="12ae3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12ae3-104">SYNTAX</span></span>

### <span data-ttu-id="12ae3-105">InputObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="12ae3-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation -InputObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12ae3-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="12ae3-106">ColumnParameterSet</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12ae3-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="12ae3-107">SqlPoolObjectColumnParameterSet</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12ae3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12ae3-108">DESCRIPTION</span></span>
<span data-ttu-id="12ae3-109">Il cmdlet Enable-AzSynapseSqlPoolSensitivityRecommendation consente di abilitare i consigli di sensitività per le colonne nel pool SQL.</span><span class="sxs-lookup"><span data-stu-id="12ae3-109">The Enable-AzSynapseSqlPoolSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="12ae3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12ae3-110">EXAMPLES</span></span>

### <span data-ttu-id="12ae3-111">Esempio 1: abilitare i consigli di sensitività per una determinata colonna in un pool di SQL sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="12ae3-111">Example 1: Enable sensitivity recommendations on a given column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="12ae3-112">Esempio 2: abilitare i consigli di sensitività in un pool di SQL sinapsi di colonna Azure con piping.</span><span class="sxs-lookup"><span data-stu-id="12ae3-112">Example 2: Enable sensitivity recommendations on a given column Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Enable-AzSynapseSqlPoolSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="12ae3-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="12ae3-113">PARAMETERS</span></span>

### <span data-ttu-id="12ae3-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12ae3-114">-AsJob</span></span>
<span data-ttu-id="12ae3-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="12ae3-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="12ae3-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="12ae3-116">-ColumnName</span></span>
<span data-ttu-id="12ae3-117">Nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="12ae3-117">Name of column.</span></span>

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

### <span data-ttu-id="12ae3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12ae3-118">-DefaultProfile</span></span>
<span data-ttu-id="12ae3-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="12ae3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12ae3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12ae3-120">-InputObject</span></span>
<span data-ttu-id="12ae3-121">Oggetto che rappresenta una classificazione di sensitivity del pool SQL.</span><span class="sxs-lookup"><span data-stu-id="12ae3-121">An object representing a SQL Pool Sensitivity Classification.</span></span>

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

### <span data-ttu-id="12ae3-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12ae3-122">-PassThru</span></span>
<span data-ttu-id="12ae3-123">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="12ae3-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="12ae3-124">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="12ae3-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="12ae3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12ae3-125">-ResourceGroupName</span></span>
<span data-ttu-id="12ae3-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="12ae3-126">Resource group name.</span></span>

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

### <span data-ttu-id="12ae3-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="12ae3-127">-SchemaName</span></span>
<span data-ttu-id="12ae3-128">Nome dello schema.</span><span class="sxs-lookup"><span data-stu-id="12ae3-128">Name of schema.</span></span>

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

### <span data-ttu-id="12ae3-129">-Sqlpoolname</span><span class="sxs-lookup"><span data-stu-id="12ae3-129">-SqlPoolName</span></span>
<span data-ttu-id="12ae3-130">Nome del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="12ae3-130">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="12ae3-131">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="12ae3-131">-SqlPoolObject</span></span>
<span data-ttu-id="12ae3-132">Oggetto di input del pool SQL, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="12ae3-132">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="12ae3-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="12ae3-133">-TableName</span></span>
<span data-ttu-id="12ae3-134">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="12ae3-134">Name of table.</span></span>

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

### <span data-ttu-id="12ae3-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="12ae3-135">-WorkspaceName</span></span>
<span data-ttu-id="12ae3-136">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="12ae3-136">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="12ae3-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="12ae3-137">-Confirm</span></span>
<span data-ttu-id="12ae3-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12ae3-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12ae3-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12ae3-139">-WhatIf</span></span>
<span data-ttu-id="12ae3-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12ae3-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12ae3-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12ae3-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12ae3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12ae3-142">CommonParameters</span></span>
<span data-ttu-id="12ae3-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12ae3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12ae3-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12ae3-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12ae3-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="12ae3-145">INPUTS</span></span>

### <span data-ttu-id="12ae3-146">Microsoft. Azure. Commands. sinapsi. Models. DataClassification. SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="12ae3-146">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="12ae3-147">System. String</span><span class="sxs-lookup"><span data-stu-id="12ae3-147">System.String</span></span>

### <span data-ttu-id="12ae3-148">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="12ae3-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="12ae3-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12ae3-149">OUTPUTS</span></span>

### <span data-ttu-id="12ae3-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="12ae3-150">System.Boolean</span></span>

## <span data-ttu-id="12ae3-151">Note</span><span class="sxs-lookup"><span data-stu-id="12ae3-151">NOTES</span></span>

## <span data-ttu-id="12ae3-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12ae3-152">RELATED LINKS</span></span>
