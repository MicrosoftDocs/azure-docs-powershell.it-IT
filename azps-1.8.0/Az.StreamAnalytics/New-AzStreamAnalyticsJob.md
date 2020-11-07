---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F281B351-F7C7-47D1-9745-FFE4BAA840FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
ms.openlocfilehash: b50141c37c55d55f8fd8e823f09fefad49a55543
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676406"
---
# <span data-ttu-id="d2b87-101">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d2b87-101">New-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="d2b87-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d2b87-102">SYNOPSIS</span></span>
<span data-ttu-id="d2b87-103">Crea o aggiorna un processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="d2b87-103">Creates or updates a Stream Analytics job.</span></span>

## <span data-ttu-id="d2b87-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d2b87-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsJob [[-Name] <String>] [-File] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2b87-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2b87-105">DESCRIPTION</span></span>
<span data-ttu-id="d2b87-106">Il cmdlet **New-AzStreamAnalyticsJob** crea un nuovo processo di analisi del flusso in Azure o aggiorna la definizione di un processo specificato esistente.</span><span class="sxs-lookup"><span data-stu-id="d2b87-106">The **New-AzStreamAnalyticsJob** cmdlet creates a new Stream Analytics job in Azure or updates the definition of an existing specified job.</span></span>
<span data-ttu-id="d2b87-107">Il nome del processo può essere specificato in. File JSON o nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="d2b87-107">The name of the job can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="d2b87-108">Se entrambi sono specificati, la riga di comando nome deve corrispondere al nome nel file.</span><span class="sxs-lookup"><span data-stu-id="d2b87-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="d2b87-109">Se si specifica un nome di processo già esistente e non si specifica il parametro *Force* , il cmdlet chiederà se sostituire o meno il processo esistente.</span><span class="sxs-lookup"><span data-stu-id="d2b87-109">If you specify a job name that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing job.</span></span>
<span data-ttu-id="d2b87-110">Se specifichi il parametro *Force* e specifichi un nome lavoro esistente, la definizione del processo verrà sostituita senza conferma.</span><span class="sxs-lookup"><span data-stu-id="d2b87-110">If you specify the *Force* parameter and specify an existing job name, the job definition will be replaced without confirmation.</span></span>

## <span data-ttu-id="d2b87-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d2b87-111">EXAMPLES</span></span>

### <span data-ttu-id="d2b87-112">ESEMPIO 1: creare un processo</span><span class="sxs-lookup"><span data-stu-id="d2b87-112">EXAMPLE 1: Create a job</span></span>
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json"
```

<span data-ttu-id="d2b87-113">Questo comando crea un processo dalla definizione in JobDefinition.jsattivata.</span><span class="sxs-lookup"><span data-stu-id="d2b87-113">This command creates a job from the definition in JobDefinition.json.</span></span>
<span data-ttu-id="d2b87-114">Se un processo esistente con il nome specificato nel file di definizione del processo è già definito, il cmdlet chiederà se sostituirlo o meno.</span><span class="sxs-lookup"><span data-stu-id="d2b87-114">If an existing job with the specified name in the job definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="d2b87-115">ESEMPIO 2: sostituire una definizione di processo</span><span class="sxs-lookup"><span data-stu-id="d2b87-115">EXAMPLE 2: Replace a job definition</span></span>
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json" -Name "StreamingJob" -Force
```

<span data-ttu-id="d2b87-116">Questo comando sostituisce la definizione del processo per StreamingJob senza conferma.</span><span class="sxs-lookup"><span data-stu-id="d2b87-116">This command replaces the job definition for StreamingJob without confirmation.</span></span>

## <span data-ttu-id="d2b87-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d2b87-117">PARAMETERS</span></span>

### <span data-ttu-id="d2b87-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2b87-118">-DefaultProfile</span></span>
<span data-ttu-id="d2b87-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d2b87-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2b87-120">-File</span><span class="sxs-lookup"><span data-stu-id="d2b87-120">-File</span></span>
<span data-ttu-id="d2b87-121">Specifica il percorso di un file JSON che contiene la rappresentazione JSON del processo di analisi di Azure Stream da creare.</span><span class="sxs-lookup"><span data-stu-id="d2b87-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics job to create.</span></span>

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

### <span data-ttu-id="d2b87-122">-Force</span><span class="sxs-lookup"><span data-stu-id="d2b87-122">-Force</span></span>
<span data-ttu-id="d2b87-123">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d2b87-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d2b87-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="d2b87-124">-Name</span></span>
<span data-ttu-id="d2b87-125">Specifica il nome del processo di analisi di Azure Stream da creare.</span><span class="sxs-lookup"><span data-stu-id="d2b87-125">Specifies the name of the Azure Stream Analytics job to create.</span></span>

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

### <span data-ttu-id="d2b87-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2b87-126">-ResourceGroupName</span></span>
<span data-ttu-id="d2b87-127">Specifica il nome del gruppo di risorse a cui deve appartenere il processo di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="d2b87-127">Specifies the name of the resource group to which the Azure Stream Analytics job should belong.</span></span>

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

### <span data-ttu-id="d2b87-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d2b87-128">-Confirm</span></span>
<span data-ttu-id="d2b87-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2b87-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2b87-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2b87-130">-WhatIf</span></span>
<span data-ttu-id="d2b87-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2b87-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2b87-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2b87-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2b87-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2b87-133">CommonParameters</span></span>
<span data-ttu-id="d2b87-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2b87-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2b87-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2b87-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2b87-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d2b87-136">INPUTS</span></span>

### <span data-ttu-id="d2b87-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d2b87-137">System.String</span></span>

## <span data-ttu-id="d2b87-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d2b87-138">OUTPUTS</span></span>

### <span data-ttu-id="d2b87-139">Microsoft. Azure. Commands. StreamAnalytics. Models. PSJob</span><span class="sxs-lookup"><span data-stu-id="d2b87-139">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="d2b87-140">Note</span><span class="sxs-lookup"><span data-stu-id="d2b87-140">NOTES</span></span>

## <span data-ttu-id="d2b87-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d2b87-141">RELATED LINKS</span></span>

[<span data-ttu-id="d2b87-142">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d2b87-142">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="d2b87-143">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d2b87-143">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="d2b87-144">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d2b87-144">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="d2b87-145">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d2b87-145">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)

[<span data-ttu-id="d2b87-146">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d2b87-146">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)

