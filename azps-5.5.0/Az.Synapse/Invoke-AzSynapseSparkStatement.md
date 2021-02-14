---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
ms.openlocfilehash: 64677ac73fecbaeaaaa327f21bc8e67e2a933d97
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188799"
---
# <span data-ttu-id="be9d2-101">Invoke-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="be9d2-101">Invoke-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="be9d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be9d2-102">SYNOPSIS</span></span>
<span data-ttu-id="be9d2-103">Richiama un'istruzione Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="be9d2-103">Invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="be9d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="be9d2-104">SYNTAX</span></span>

### <span data-ttu-id="be9d2-105">RunSparkStatementByCodePathParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="be9d2-105">RunSparkStatementByCodePathParameterSet (Default)</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be9d2-106">RunSparkStatementByCodeParameterSet</span><span class="sxs-lookup"><span data-stu-id="be9d2-106">RunSparkStatementByCodeParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be9d2-107">RunSparkStatementByCodeAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="be9d2-107">RunSparkStatementByCodeAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be9d2-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="be9d2-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="be9d2-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="be9d2-109">DESCRIPTION</span></span>
<span data-ttu-id="be9d2-110">Il cmdlet **Invoke-AzSynapseSparkStatement** richiama un'istruzione Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="be9d2-110">The **Invoke-AzSynapseSparkStatement** cmdlet invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="be9d2-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="be9d2-111">EXAMPLES</span></span>

### <span data-ttu-id="be9d2-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="be9d2-112">Example 1</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="be9d2-113">Questi comandi avviano una sessione spark, quindi richiamano un'istruzione Spark inline tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="be9d2-113">These commands start a Spark session then invoke an inline Spark statement through pipeline.</span></span>

### <span data-ttu-id="be9d2-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="be9d2-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSynapseSparkStatement -SessionId 324 -Language 'Spark' -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="be9d2-115">Questi comandi avviano una sessione spark, quindi richiamano un'istruzione Grafico spark in linea.</span><span class="sxs-lookup"><span data-stu-id="be9d2-115">These commands start a Spark session then invoke an inline Spark statement.</span></span>

### <span data-ttu-id="be9d2-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="be9d2-116">Example 3</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -FilePath C:\path\to\code.sc
```

<span data-ttu-id="be9d2-117">Questi comandi avviano una sessione Spark e richiamano le istruzioni Spark in un file.</span><span class="sxs-lookup"><span data-stu-id="be9d2-117">These commands start a Spark session then invoke Spark statements in a file.</span></span>

## <span data-ttu-id="be9d2-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be9d2-118">PARAMETERS</span></span>

### <span data-ttu-id="be9d2-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="be9d2-119">-AsJob</span></span>
<span data-ttu-id="be9d2-120">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="be9d2-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="be9d2-121">-Codice</span><span class="sxs-lookup"><span data-stu-id="be9d2-121">-Code</span></span>
<span data-ttu-id="be9d2-122">Codice di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="be9d2-122">The execution code.</span></span>

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

### <span data-ttu-id="be9d2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be9d2-123">-DefaultProfile</span></span>
<span data-ttu-id="be9d2-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="be9d2-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be9d2-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="be9d2-125">-FilePath</span></span>
<span data-ttu-id="be9d2-126">Specifica un percorso di file locale contenente il codice di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="be9d2-126">Specifies a local file path that contains the execution code.</span></span>

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

### <span data-ttu-id="be9d2-127">-Lingua</span><span class="sxs-lookup"><span data-stu-id="be9d2-127">-Language</span></span>
<span data-ttu-id="be9d2-128">Lingua del codice di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="be9d2-128">Language of the execution code.</span></span>

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

### <span data-ttu-id="be9d2-129">-Response</span><span class="sxs-lookup"><span data-stu-id="be9d2-129">-Response</span></span>
<span data-ttu-id="be9d2-130">Indica che deve essere restituita una risposta completa.</span><span class="sxs-lookup"><span data-stu-id="be9d2-130">Indicates full response should be return.</span></span>

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

### <span data-ttu-id="be9d2-131">-SessionId</span><span class="sxs-lookup"><span data-stu-id="be9d2-131">-SessionId</span></span>
<span data-ttu-id="be9d2-132">Identificatore della sessione spark.</span><span class="sxs-lookup"><span data-stu-id="be9d2-132">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="be9d2-133">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="be9d2-133">-SessionObject</span></span>
<span data-ttu-id="be9d2-134">Oggetto di input della sessione Spark, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="be9d2-134">Spark session input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="be9d2-135">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="be9d2-135">-SparkPoolName</span></span>
<span data-ttu-id="be9d2-136">Nome del pool Synapse Spark.</span><span class="sxs-lookup"><span data-stu-id="be9d2-136">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="be9d2-137">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="be9d2-137">-WorkspaceName</span></span>
<span data-ttu-id="be9d2-138">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="be9d2-138">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="be9d2-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be9d2-139">-Confirm</span></span>
<span data-ttu-id="be9d2-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be9d2-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be9d2-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be9d2-141">-WhatIf</span></span>
<span data-ttu-id="be9d2-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be9d2-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="be9d2-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be9d2-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be9d2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be9d2-144">CommonParameters</span></span>
<span data-ttu-id="be9d2-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be9d2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be9d2-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="be9d2-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be9d2-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="be9d2-147">INPUTS</span></span>

### <span data-ttu-id="be9d2-148">System.String</span><span class="sxs-lookup"><span data-stu-id="be9d2-148">System.String</span></span>

### <span data-ttu-id="be9d2-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="be9d2-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="be9d2-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="be9d2-150">OUTPUTS</span></span>

### <span data-ttu-id="be9d2-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseExtendedSparkStatement</span><span class="sxs-lookup"><span data-stu-id="be9d2-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseExtendedSparkStatement</span></span>

## <span data-ttu-id="be9d2-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="be9d2-152">NOTES</span></span>

## <span data-ttu-id="be9d2-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="be9d2-153">RELATED LINKS</span></span>
