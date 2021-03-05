---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F281B351-F7C7-47D1-9745-FFE4BAA840FD
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/new-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
ms.openlocfilehash: 8a9da4d68456b612cbd1bd4db3997cc67e724975
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961198"
---
# <span data-ttu-id="1d7d5-101">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="1d7d5-101">New-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="1d7d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d7d5-102">SYNOPSIS</span></span>
<span data-ttu-id="1d7d5-103">Crea o aggiorna un processo di Analisi di flusso.</span><span class="sxs-lookup"><span data-stu-id="1d7d5-103">Creates or updates a Stream Analytics job.</span></span>

## <span data-ttu-id="1d7d5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1d7d5-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsJob [[-Name] <String>] [-File] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d7d5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1d7d5-105">DESCRIPTION</span></span>
<span data-ttu-id="1d7d5-106">Il cmdlet **New-AzStreamAnalyticsJob** crea un nuovo processo di Analisi di flusso in Azure o aggiorna la definizione di un processo specificato esistente.</span><span class="sxs-lookup"><span data-stu-id="1d7d5-106">The **New-AzStreamAnalyticsJob** cmdlet creates a new Stream Analytics job in Azure or updates the definition of an existing specified job.</span></span>
<span data-ttu-id="1d7d5-107">Il nome del processo può essere specificato nel campo . JSON o nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="1d7d5-107">The name of the job can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="1d7d5-108">Se vengono specificati entrambi, il nome nella riga di comando deve corrispondere al nome del file.</span><span class="sxs-lookup"><span data-stu-id="1d7d5-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="1d7d5-109">Se si specifica un nome di processo già esistente e non si specifica il parametro *Force,* il cmdlet chiederà se sostituire o meno il processo esistente.</span><span class="sxs-lookup"><span data-stu-id="1d7d5-109">If you specify a job name that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing job.</span></span>
<span data-ttu-id="1d7d5-110">Se si specifica il *parametro Force* e si specifica un nome di processo esistente, la definizione del processo verrà sostituita senza conferma.</span><span class="sxs-lookup"><span data-stu-id="1d7d5-110">If you specify the *Force* parameter and specify an existing job name, the job definition will be replaced without confirmation.</span></span>

## <span data-ttu-id="1d7d5-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1d7d5-111">EXAMPLES</span></span>

### <span data-ttu-id="1d7d5-112">ESEMPIO 1: Creare un processo</span><span class="sxs-lookup"><span data-stu-id="1d7d5-112">EXAMPLE 1: Create a job</span></span>
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json"
```

<span data-ttu-id="1d7d5-113">Questo comando crea un processo dalla definizione in JobDefinition.jsavanti.</span><span class="sxs-lookup"><span data-stu-id="1d7d5-113">This command creates a job from the definition in JobDefinition.json.</span></span>
<span data-ttu-id="1d7d5-114">Se è già definito un processo esistente con il nome specificato nel file di definizione del processo, il cmdlet chiederà se sostituirlo o meno.</span><span class="sxs-lookup"><span data-stu-id="1d7d5-114">If an existing job with the specified name in the job definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="1d7d5-115">ESEMPIO 2: Sostituire una definizione di processo</span><span class="sxs-lookup"><span data-stu-id="1d7d5-115">EXAMPLE 2: Replace a job definition</span></span>
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json" -Name "StreamingJob" -Force
```

<span data-ttu-id="1d7d5-116">Questo comando sostituisce la definizione di processo per StreamingJob senza conferma.</span><span class="sxs-lookup"><span data-stu-id="1d7d5-116">This command replaces the job definition for StreamingJob without confirmation.</span></span>

## <span data-ttu-id="1d7d5-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d7d5-117">PARAMETERS</span></span>

### <span data-ttu-id="1d7d5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d7d5-118">-DefaultProfile</span></span>
<span data-ttu-id="1d7d5-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1d7d5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d7d5-120">-File</span><span class="sxs-lookup"><span data-stu-id="1d7d5-120">-File</span></span>
<span data-ttu-id="1d7d5-121">Specifica il percorso di un file JSON che contiene la rappresentazione JSON del processo di Analisi di flusso di Azure da creare.</span><span class="sxs-lookup"><span data-stu-id="1d7d5-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics job to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d7d5-122">-Force</span><span class="sxs-lookup"><span data-stu-id="1d7d5-122">-Force</span></span>
<span data-ttu-id="1d7d5-123">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="1d7d5-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1d7d5-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1d7d5-124">-Name</span></span>
<span data-ttu-id="1d7d5-125">Specifica il nome del processo di Analisi di flusso di Azure da creare.</span><span class="sxs-lookup"><span data-stu-id="1d7d5-125">Specifies the name of the Azure Stream Analytics job to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d7d5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d7d5-126">-ResourceGroupName</span></span>
<span data-ttu-id="1d7d5-127">Specifica il nome del gruppo di risorse a cui deve appartenere il processo di Analisi di flusso di Azure.</span><span class="sxs-lookup"><span data-stu-id="1d7d5-127">Specifies the name of the resource group to which the Azure Stream Analytics job should belong.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d7d5-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d7d5-128">-Confirm</span></span>
<span data-ttu-id="1d7d5-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d7d5-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d7d5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d7d5-130">-WhatIf</span></span>
<span data-ttu-id="1d7d5-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d7d5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d7d5-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d7d5-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d7d5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d7d5-133">CommonParameters</span></span>
<span data-ttu-id="1d7d5-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d7d5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d7d5-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d7d5-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d7d5-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="1d7d5-136">INPUTS</span></span>

### <span data-ttu-id="1d7d5-137">System.String</span><span class="sxs-lookup"><span data-stu-id="1d7d5-137">System.String</span></span>

## <span data-ttu-id="1d7d5-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1d7d5-138">OUTPUTS</span></span>

### <span data-ttu-id="1d7d5-139">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span><span class="sxs-lookup"><span data-stu-id="1d7d5-139">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="1d7d5-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="1d7d5-140">NOTES</span></span>

## <span data-ttu-id="1d7d5-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1d7d5-141">RELATED LINKS</span></span>

[<span data-ttu-id="1d7d5-142">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="1d7d5-142">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="1d7d5-143">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="1d7d5-143">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="1d7d5-144">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="1d7d5-144">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="1d7d5-145">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="1d7d5-145">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)

[<span data-ttu-id="1d7d5-146">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="1d7d5-146">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


