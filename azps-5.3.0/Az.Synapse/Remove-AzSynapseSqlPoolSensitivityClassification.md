---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: a278b316a62639c6c33d4f05491e314a2b9a1e85
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383347"
---
# <span data-ttu-id="4ccfa-101">Remove-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="4ccfa-101">Remove-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="4ccfa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4ccfa-102">SYNOPSIS</span></span>
<span data-ttu-id="4ccfa-103">Rimuove i tipi di informazioni e le etichette di sensitività delle colonne nel pool SQL.</span><span class="sxs-lookup"><span data-stu-id="4ccfa-103">Removes the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="4ccfa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ccfa-104">SYNTAX</span></span>

### <span data-ttu-id="4ccfa-105">ClassificationObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4ccfa-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification -ClassificationObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ccfa-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ccfa-106">ColumnParameterSet</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ccfa-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ccfa-107">SqlPoolObjectColumnParameterSet</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ccfa-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ccfa-108">DESCRIPTION</span></span>
<span data-ttu-id="4ccfa-109">Il cmdlet Remove-AzSynapseSqlPoolSensitivityClassification consente di rimuovere i tipi di informazioni e le etichette di sensitività delle colonne nel pool SQL.</span><span class="sxs-lookup"><span data-stu-id="4ccfa-109">The Remove-AzSynapseSqlPoolSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="4ccfa-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ccfa-110">EXAMPLES</span></span>

### <span data-ttu-id="4ccfa-111">Esempio 1: rimuovere il tipo di informazioni e l'etichetta di sensitività di una colonna in un pool di SQL sinapsi di Azure.</span><span class="sxs-lookup"><span data-stu-id="4ccfa-111">Example 1: Remove information type and sensitivity label of a column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="4ccfa-112">Esempio 2: rimuovere i tipi di informazioni correnti e le etichette di sensitività delle colonne in un pool di SQL sinapsi di Azure tramite piping.</span><span class="sxs-lookup"><span data-stu-id="4ccfa-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Remove-AzSynapseSqlPoolSensitivityClassification
```

### <span data-ttu-id="4ccfa-113">Esempio 3: rimuovere il tipo di informazioni e l'etichetta di sensitività di una colonna in un pool di SQL sinapsi di Azure tramite piping.</span><span class="sxs-lookup"><span data-stu-id="4ccfa-113">Example 3: Remove information type and sensitivity label of a column in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Remove-AzSynapseSqlPoolSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="4ccfa-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4ccfa-114">PARAMETERS</span></span>

### <span data-ttu-id="4ccfa-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ccfa-115">-AsJob</span></span>
<span data-ttu-id="4ccfa-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4ccfa-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4ccfa-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="4ccfa-117">-ClassificationObject</span></span>
<span data-ttu-id="4ccfa-118">Oggetto che rappresenta una classificazione di sensitivity del pool SQL.</span><span class="sxs-lookup"><span data-stu-id="4ccfa-118">An object representing a SQL Pool Sensitivity Classification.</span></span>

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

### <span data-ttu-id="4ccfa-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="4ccfa-119">-ColumnName</span></span>
<span data-ttu-id="4ccfa-120">Nome della colonna.</span><span class="sxs-lookup"><span data-stu-id="4ccfa-120">Name of column.</span></span>

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

### <span data-ttu-id="4ccfa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ccfa-121">-DefaultProfile</span></span>
<span data-ttu-id="4ccfa-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4ccfa-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ccfa-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ccfa-123">-PassThru</span></span>
<span data-ttu-id="4ccfa-124">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="4ccfa-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="4ccfa-125">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="4ccfa-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="4ccfa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ccfa-126">-ResourceGroupName</span></span>
<span data-ttu-id="4ccfa-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4ccfa-127">Resource group name.</span></span>

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

### <span data-ttu-id="4ccfa-128">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="4ccfa-128">-SchemaName</span></span>
<span data-ttu-id="4ccfa-129">Nome dello schema.</span><span class="sxs-lookup"><span data-stu-id="4ccfa-129">Name of schema.</span></span>

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

### <span data-ttu-id="4ccfa-130">-Sqlpoolname</span><span class="sxs-lookup"><span data-stu-id="4ccfa-130">-SqlPoolName</span></span>
<span data-ttu-id="4ccfa-131">Nome del pool di sinapsi SQL.</span><span class="sxs-lookup"><span data-stu-id="4ccfa-131">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="4ccfa-132">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="4ccfa-132">-SqlPoolObject</span></span>
<span data-ttu-id="4ccfa-133">Oggetto di input del pool SQL, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="4ccfa-133">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4ccfa-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="4ccfa-134">-TableName</span></span>
<span data-ttu-id="4ccfa-135">Nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="4ccfa-135">Name of table.</span></span>

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

### <span data-ttu-id="4ccfa-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4ccfa-136">-WorkspaceName</span></span>
<span data-ttu-id="4ccfa-137">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="4ccfa-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4ccfa-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4ccfa-138">-Confirm</span></span>
<span data-ttu-id="4ccfa-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ccfa-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ccfa-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ccfa-140">-WhatIf</span></span>
<span data-ttu-id="4ccfa-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ccfa-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ccfa-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ccfa-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ccfa-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ccfa-143">CommonParameters</span></span>
<span data-ttu-id="4ccfa-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ccfa-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ccfa-145">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ccfa-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ccfa-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4ccfa-146">INPUTS</span></span>

### <span data-ttu-id="4ccfa-147">Microsoft. Azure. Commands. sinapsi. Models. DataClassification. SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="4ccfa-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="4ccfa-148">System. String</span><span class="sxs-lookup"><span data-stu-id="4ccfa-148">System.String</span></span>

### <span data-ttu-id="4ccfa-149">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="4ccfa-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="4ccfa-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ccfa-150">OUTPUTS</span></span>

### <span data-ttu-id="4ccfa-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4ccfa-151">System.Boolean</span></span>

## <span data-ttu-id="4ccfa-152">Note</span><span class="sxs-lookup"><span data-stu-id="4ccfa-152">NOTES</span></span>

## <span data-ttu-id="4ccfa-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ccfa-153">RELATED LINKS</span></span>
