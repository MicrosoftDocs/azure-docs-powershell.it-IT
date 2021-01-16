---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: bb47d791f23df044e5a4677835f85b6f107f2822
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383193"
---
# <span data-ttu-id="608f3-101">Set-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="608f3-101">Set-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="608f3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="608f3-102">SYNOPSIS</span></span>
<span data-ttu-id="608f3-103">Imposta i tipi di informazioni e le etichette di sensitività delle colonne nel pool SQL.</span><span class="sxs-lookup"><span data-stu-id="608f3-103">Sets the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="608f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="608f3-104">SYNTAX</span></span>

### <span data-ttu-id="608f3-105">ClassificationObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="608f3-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification -ClassificationObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="608f3-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="608f3-106">ColumnParameterSet</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-WorkspaceName] <String> [-SqlPoolName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="608f3-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="608f3-107">SqlPoolObjectColumnParameterSet</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="608f3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="608f3-108">DESCRIPTION</span></span>
<span data-ttu-id="608f3-109">Il cmdlet Set-AzSynapseSqlPoolSensitivityClassification imposta i tipi di informazioni e le etichette di sensitività delle colonne nel pool SQL.</span><span class="sxs-lookup"><span data-stu-id="608f3-109">The Set-AzSynapseSqlPoolSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="608f3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="608f3-110">EXAMPLES</span></span>

### <span data-ttu-id="608f3-111">Esempio 1: impostare il tipo di informazioni e l'etichetta di sensitività di una colonna in un pool di SQL sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="608f3-111">Example 1: Set information type and sensitivity label of a column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="608f3-112">Esempio 2: impostare i tipi di informazioni consigliati e le etichette di sensitività delle colonne in un pool di SQL sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="608f3-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolSensitivityClassification
```

### <span data-ttu-id="608f3-113">Esempio 3: impostare il tipo di informazioni e l'etichetta di sensitività di una colonna in un pool di SQL sinapsi di Azure, usando piping.</span><span class="sxs-lookup"><span data-stu-id="608f3-113">Example 3: Set information type and sensitivity label of a column in an Azure Synapse SQL pool, using piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolSensitivityClassification  -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="608f3-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="608f3-114">PARAMETERS</span></span>

### <span data-ttu-id="608f3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="608f3-115">-AsJob</span></span>
<span data-ttu-id="608f3-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="608f3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="608f3-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="608f3-117">-ClassificationObject</span></span>
<span data-ttu-id="608f3-118">Oggetto che rappresenta una classificazione di sensitivity del pool SQL.</span><span class="sxs-lookup"><span data-stu-id="608f3-118">An object representing a SQL Pool Sensitivity Classification.</span></span>

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

### <span data-ttu-id="608f3-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="608f3-119">-ColumnName</span></span>
<span data-ttu-id="608f3-120">Nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="608f3-120">Name of column.</span></span>

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

### <span data-ttu-id="608f3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="608f3-121">-DefaultProfile</span></span>
<span data-ttu-id="608f3-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="608f3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="608f3-123">-InformationType</span><span class="sxs-lookup"><span data-stu-id="608f3-123">-InformationType</span></span>
<span data-ttu-id="608f3-124">Nome che descrive il tipo di informazioni dei dati archiviati nella colonna.</span><span class="sxs-lookup"><span data-stu-id="608f3-124">A name that describes the information type of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="608f3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="608f3-125">-PassThru</span></span>
<span data-ttu-id="608f3-126">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="608f3-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="608f3-127">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="608f3-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="608f3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="608f3-128">-ResourceGroupName</span></span>
<span data-ttu-id="608f3-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="608f3-129">Resource group name.</span></span>

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

### <span data-ttu-id="608f3-130">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="608f3-130">-SchemaName</span></span>
<span data-ttu-id="608f3-131">Nome dello schema.</span><span class="sxs-lookup"><span data-stu-id="608f3-131">Name of schema.</span></span>

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

### <span data-ttu-id="608f3-132">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="608f3-132">-SensitivityLabel</span></span>
<span data-ttu-id="608f3-133">Nome che descrive la sensibilità dei dati archiviati nella colonna.</span><span class="sxs-lookup"><span data-stu-id="608f3-133">A name that describes the sensitivity of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="608f3-134">-Sqlpoolname</span><span class="sxs-lookup"><span data-stu-id="608f3-134">-SqlPoolName</span></span>
<span data-ttu-id="608f3-135">Nome del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="608f3-135">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="608f3-136">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="608f3-136">-SqlPoolObject</span></span>
<span data-ttu-id="608f3-137">Oggetto di input del pool SQL, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="608f3-137">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="608f3-138">-TableName</span><span class="sxs-lookup"><span data-stu-id="608f3-138">-TableName</span></span>
<span data-ttu-id="608f3-139">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="608f3-139">Name of table.</span></span>

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

### <span data-ttu-id="608f3-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="608f3-140">-WorkspaceName</span></span>
<span data-ttu-id="608f3-141">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="608f3-141">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="608f3-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="608f3-142">-Confirm</span></span>
<span data-ttu-id="608f3-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="608f3-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="608f3-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="608f3-144">-WhatIf</span></span>
<span data-ttu-id="608f3-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="608f3-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="608f3-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="608f3-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="608f3-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="608f3-147">CommonParameters</span></span>
<span data-ttu-id="608f3-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="608f3-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="608f3-149">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="608f3-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="608f3-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="608f3-150">INPUTS</span></span>

### <span data-ttu-id="608f3-151">System. String</span><span class="sxs-lookup"><span data-stu-id="608f3-151">System.String</span></span>

### <span data-ttu-id="608f3-152">Microsoft. Azure. Commands. sinapsi. Models. DataClassification. SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="608f3-152">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="608f3-153">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="608f3-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="608f3-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="608f3-154">OUTPUTS</span></span>

### <span data-ttu-id="608f3-155">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="608f3-155">System.Boolean</span></span>

## <span data-ttu-id="608f3-156">Note</span><span class="sxs-lookup"><span data-stu-id="608f3-156">NOTES</span></span>

## <span data-ttu-id="608f3-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="608f3-157">RELATED LINKS</span></span>
