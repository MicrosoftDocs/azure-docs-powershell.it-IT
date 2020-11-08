---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/start-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Start-AzSynapseSparkSession.md
ms.openlocfilehash: b066807d812fc9a74b36b2826cc978589d39ea49
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190440"
---
# <span data-ttu-id="80629-101">Start-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="80629-101">Start-AzSynapseSparkSession</span></span>

## <span data-ttu-id="80629-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="80629-102">SYNOPSIS</span></span>
<span data-ttu-id="80629-103">Avvia una sessione di Spark analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="80629-103">Starts a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="80629-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="80629-104">SYNTAX</span></span>

### <span data-ttu-id="80629-105">CreateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="80629-105">CreateByNameParameterSet (Default)</span></span>
```
Start-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> [-Language <String>] -Name <String>
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80629-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="80629-106">CreateByParentObjectParameterSet</span></span>
```
Start-AzSynapseSparkSession -SparkPoolObject <PSSynapseSparkPool> [-Language <String>] -Name <String>
 [-ReferenceFile <String[]>] -ExecutorCount <Int32> -ExecutorSize <String> [-Configuration <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80629-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80629-107">DESCRIPTION</span></span>
<span data-ttu-id="80629-108">Il cmdlet **Start-AzSynapseSparkSession** avvia una sessione di Spark analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="80629-108">The **Start-AzSynapseSparkSession** cmdlet starts a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="80629-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="80629-109">EXAMPLES</span></span>

### <span data-ttu-id="80629-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="80629-110">Example 1</span></span>
```powershell
PS C:\> Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
```

<span data-ttu-id="80629-111">Questo comando avvia una sessione di Spark di analisi di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="80629-111">This command starts an Azure Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="80629-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="80629-112">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Start-AzSynapseSparkSession -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
```

<span data-ttu-id="80629-113">Questo comando avvia una sessione di Spark di analisi di Azure sinapsi tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="80629-113">This command starts an Azure Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="80629-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="80629-114">PARAMETERS</span></span>

### <span data-ttu-id="80629-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80629-115">-AsJob</span></span>
<span data-ttu-id="80629-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="80629-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="80629-117">-Configurazione</span><span class="sxs-lookup"><span data-stu-id="80629-117">-Configuration</span></span>
<span data-ttu-id="80629-118">Proprietà di configurazione Spark.</span><span class="sxs-lookup"><span data-stu-id="80629-118">Spark configuration properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80629-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80629-119">-DefaultProfile</span></span>
<span data-ttu-id="80629-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="80629-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80629-121">-ExecutorCount</span><span class="sxs-lookup"><span data-stu-id="80629-121">-ExecutorCount</span></span>
<span data-ttu-id="80629-122">Numero di esecutori da allocare nel pool di scintille specificato per il processo.</span><span class="sxs-lookup"><span data-stu-id="80629-122">Number of executors to be allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80629-123">-ExecutorSize</span><span class="sxs-lookup"><span data-stu-id="80629-123">-ExecutorSize</span></span>
<span data-ttu-id="80629-124">Numero di core e memoria da usare per gli esecutori assegnati nel pool di scintille specificato per il processo.</span><span class="sxs-lookup"><span data-stu-id="80629-124">Number of core and memory to be used for executors allocated in the specified Spark pool for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Small, Medium, Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80629-125">-Lingua</span><span class="sxs-lookup"><span data-stu-id="80629-125">-Language</span></span>
<span data-ttu-id="80629-126">Lingua del codice di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="80629-126">Language of the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80629-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="80629-127">-Name</span></span>
<span data-ttu-id="80629-128">Nome della sessione di Spark.</span><span class="sxs-lookup"><span data-stu-id="80629-128">Name of Spark session.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80629-129">-ReferenceFile</span><span class="sxs-lookup"><span data-stu-id="80629-129">-ReferenceFile</span></span>
<span data-ttu-id="80629-130">File aggiuntivi usati per riferimento nel file di definizione principale.</span><span class="sxs-lookup"><span data-stu-id="80629-130">Additional files used for reference in the main definition file.</span></span> <span data-ttu-id="80629-131">Elenco URI di archiviazione delimitato da virgole.</span><span class="sxs-lookup"><span data-stu-id="80629-131">Comma-separated storage URI list.</span></span> <span data-ttu-id="80629-132">ad esempio abfss://filesystem@account.dfs.core.windows.net/file1.txt , ", abfss://filesystem@account.dfs.core.windows.net/result/ "</span><span class="sxs-lookup"><span data-stu-id="80629-132">e.g. "abfss://filesystem@account.dfs.core.windows.net/file1.txt,abfss://filesystem@account.dfs.core.windows.net/result/"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80629-133">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="80629-133">-SparkPoolName</span></span>
<span data-ttu-id="80629-134">Nome del pool di scintille sinapsi.</span><span class="sxs-lookup"><span data-stu-id="80629-134">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80629-135">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="80629-135">-SparkPoolObject</span></span>
<span data-ttu-id="80629-136">Oggetto di input del pool di Spark, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="80629-136">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80629-137">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="80629-137">-WorkspaceName</span></span>
<span data-ttu-id="80629-138">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="80629-138">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80629-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="80629-139">-Confirm</span></span>
<span data-ttu-id="80629-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80629-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80629-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80629-141">-WhatIf</span></span>
<span data-ttu-id="80629-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80629-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="80629-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80629-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80629-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80629-144">CommonParameters</span></span>
<span data-ttu-id="80629-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80629-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80629-146">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80629-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80629-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="80629-147">INPUTS</span></span>

### <span data-ttu-id="80629-148">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="80629-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

## <span data-ttu-id="80629-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="80629-149">OUTPUTS</span></span>

### <span data-ttu-id="80629-150">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="80629-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="80629-151">Note</span><span class="sxs-lookup"><span data-stu-id="80629-151">NOTES</span></span>

## <span data-ttu-id="80629-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="80629-152">RELATED LINKS</span></span>
