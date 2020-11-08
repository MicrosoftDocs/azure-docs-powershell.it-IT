---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
ms.openlocfilehash: 64677ac73fecbaeaaaa327f21bc8e67e2a933d97
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94030937"
---
# <span data-ttu-id="b7304-101">Invoke-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="b7304-101">Invoke-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="b7304-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b7304-102">SYNOPSIS</span></span>
<span data-ttu-id="b7304-103">Richiama un'istruzione Spark di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="b7304-103">Invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="b7304-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7304-104">SYNTAX</span></span>

### <span data-ttu-id="b7304-105">RunSparkStatementByCodePathParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b7304-105">RunSparkStatementByCodePathParameterSet (Default)</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7304-106">RunSparkStatementByCodeParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7304-106">RunSparkStatementByCodeParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7304-107">RunSparkStatementByCodeAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7304-107">RunSparkStatementByCodeAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7304-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7304-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b7304-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7304-109">DESCRIPTION</span></span>
<span data-ttu-id="b7304-110">Il cmdlet **Invoke-AzSynapseSparkStatement** richiama un'istruzione Spark di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="b7304-110">The **Invoke-AzSynapseSparkStatement** cmdlet invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="b7304-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7304-111">EXAMPLES</span></span>

### <span data-ttu-id="b7304-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b7304-112">Example 1</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="b7304-113">Questi comandi avviano una sessione di Spark e quindi richiamano un'istruzione Spark in linea tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="b7304-113">These commands start a Spark session then invoke an inline Spark statement through pipeline.</span></span>

### <span data-ttu-id="b7304-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b7304-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSynapseSparkStatement -SessionId 324 -Language 'Spark' -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="b7304-115">Questi comandi avviano una sessione di Spark e quindi richiamano un'istruzione Spark in linea.</span><span class="sxs-lookup"><span data-stu-id="b7304-115">These commands start a Spark session then invoke an inline Spark statement.</span></span>

### <span data-ttu-id="b7304-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="b7304-116">Example 3</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -FilePath C:\path\to\code.sc
```

<span data-ttu-id="b7304-117">Questi comandi avviano una sessione di Spark e quindi richiamano le istruzioni Spark in un file.</span><span class="sxs-lookup"><span data-stu-id="b7304-117">These commands start a Spark session then invoke Spark statements in a file.</span></span>

## <span data-ttu-id="b7304-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b7304-118">PARAMETERS</span></span>

### <span data-ttu-id="b7304-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7304-119">-AsJob</span></span>
<span data-ttu-id="b7304-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b7304-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b7304-121">-Codice</span><span class="sxs-lookup"><span data-stu-id="b7304-121">-Code</span></span>
<span data-ttu-id="b7304-122">Codice di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b7304-122">The execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodeParameterSet, RunSparkStatementByCodeAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7304-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7304-123">-DefaultProfile</span></span>
<span data-ttu-id="b7304-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b7304-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7304-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="b7304-125">-FilePath</span></span>
<span data-ttu-id="b7304-126">Specifica un percorso di file locale che contiene il codice di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b7304-126">Specifies a local file path that contains the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7304-127">-Lingua</span><span class="sxs-lookup"><span data-stu-id="b7304-127">-Language</span></span>
<span data-ttu-id="b7304-128">Lingua del codice di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="b7304-128">Language of the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7304-129">-Risposta</span><span class="sxs-lookup"><span data-stu-id="b7304-129">-Response</span></span>
<span data-ttu-id="b7304-130">Indica che la risposta completa deve essere restituita.</span><span class="sxs-lookup"><span data-stu-id="b7304-130">Indicates full response should be return.</span></span>

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

### <span data-ttu-id="b7304-131">-SessionId</span><span class="sxs-lookup"><span data-stu-id="b7304-131">-SessionId</span></span>
<span data-ttu-id="b7304-132">Identificatore della sessione di Spark.</span><span class="sxs-lookup"><span data-stu-id="b7304-132">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7304-133">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="b7304-133">-SessionObject</span></span>
<span data-ttu-id="b7304-134">Oggetto di input della sessione Spark, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="b7304-134">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7304-135">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="b7304-135">-SparkPoolName</span></span>
<span data-ttu-id="b7304-136">Nome del pool di scintille sinapsi.</span><span class="sxs-lookup"><span data-stu-id="b7304-136">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7304-137">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b7304-137">-WorkspaceName</span></span>
<span data-ttu-id="b7304-138">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="b7304-138">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7304-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b7304-139">-Confirm</span></span>
<span data-ttu-id="b7304-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7304-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7304-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7304-141">-WhatIf</span></span>
<span data-ttu-id="b7304-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7304-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b7304-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b7304-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7304-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7304-144">CommonParameters</span></span>
<span data-ttu-id="b7304-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7304-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7304-146">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7304-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7304-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b7304-147">INPUTS</span></span>

### <span data-ttu-id="b7304-148">System. String</span><span class="sxs-lookup"><span data-stu-id="b7304-148">System.String</span></span>

### <span data-ttu-id="b7304-149">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="b7304-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="b7304-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7304-150">OUTPUTS</span></span>

### <span data-ttu-id="b7304-151">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseExtendedSparkStatement</span><span class="sxs-lookup"><span data-stu-id="b7304-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseExtendedSparkStatement</span></span>

## <span data-ttu-id="b7304-152">Note</span><span class="sxs-lookup"><span data-stu-id="b7304-152">NOTES</span></span>

## <span data-ttu-id="b7304-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7304-153">RELATED LINKS</span></span>
