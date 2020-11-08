---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 43B2A4FD-DA74-403A-89D0-40FE9A3E5A7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
ms.openlocfilehash: b0e32d58d416fce869995595c3e2a2ff69e8f349
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199635"
---
# <span data-ttu-id="9c17d-101">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="9c17d-101">New-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="9c17d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9c17d-102">SYNOPSIS</span></span>
<span data-ttu-id="9c17d-103">Crea o aggiorna gli output per un processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="9c17d-103">Creates or updates outputs for a Stream Analytics job.</span></span>

## <span data-ttu-id="9c17d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c17d-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9c17d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9c17d-105">DESCRIPTION</span></span>
<span data-ttu-id="9c17d-106">Il cmdlet **New-AzStreamAnalyticsOutput** crea un output all'interno di un processo di analisi del flusso o aggiorna un output esistente.</span><span class="sxs-lookup"><span data-stu-id="9c17d-106">The **New-AzStreamAnalyticsOutput** cmdlet creates an output within a Stream Analytics job or updates an existing output.</span></span>
<span data-ttu-id="9c17d-107">Il nome dell'output può essere specificato in. File JSON o nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="9c17d-107">The name of the output can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="9c17d-108">Se entrambi sono specificati, la riga di comando nome deve corrispondere al nome nel file.</span><span class="sxs-lookup"><span data-stu-id="9c17d-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="9c17d-109">Se specifichi un output già esistente e non specifichi il parametro *Force* , il cmdlet chiederà se sostituire o meno l'output esistente.</span><span class="sxs-lookup"><span data-stu-id="9c17d-109">If you specify an output that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing output.</span></span>
<span data-ttu-id="9c17d-110">Se specifichi il parametro *Force* e specifichi un nome di output esistente, l'output verrà sostituito senza conferma.</span><span class="sxs-lookup"><span data-stu-id="9c17d-110">If you specify the *Force* parameter and specify an existing output name, the output will be replaced without confirmation.</span></span>

## <span data-ttu-id="9c17d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c17d-111">EXAMPLES</span></span>

### <span data-ttu-id="9c17d-112">Esempio 1: aggiungere un output a un processo</span><span class="sxs-lookup"><span data-stu-id="9c17d-112">Example 1: Add an output to a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="9c17d-113">Questo comando crea un nuovo output denominato output nel processo denominato StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="9c17d-113">This command creates a new output called Output in the job called StreamingJob.</span></span>
<span data-ttu-id="9c17d-114">Se un output esistente con questo nome è già definito, il cmdlet chiederà se sostituirlo o meno.</span><span class="sxs-lookup"><span data-stu-id="9c17d-114">If an existing output with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="9c17d-115">Esempio 2: sostituire una definizione di output del processo</span><span class="sxs-lookup"><span data-stu-id="9c17d-115">Example 2: Replace a job output definition</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output" -Force
```

<span data-ttu-id="9c17d-116">Questo comando sostituisce la definizione per l'output nel processo denominato StreamingJob senza conferma.</span><span class="sxs-lookup"><span data-stu-id="9c17d-116">This command replaces the definition for Output in the job called StreamingJob without confirmation.</span></span>

## <span data-ttu-id="9c17d-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9c17d-117">PARAMETERS</span></span>

### <span data-ttu-id="9c17d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c17d-118">-DefaultProfile</span></span>
<span data-ttu-id="9c17d-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9c17d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c17d-120">-File</span><span class="sxs-lookup"><span data-stu-id="9c17d-120">-File</span></span>
<span data-ttu-id="9c17d-121">Specifica il percorso di un file JSON che contiene la rappresentazione JSON dell'output di analisi di Azure Stream da creare.</span><span class="sxs-lookup"><span data-stu-id="9c17d-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics output to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c17d-122">-Force</span><span class="sxs-lookup"><span data-stu-id="9c17d-122">-Force</span></span>
<span data-ttu-id="9c17d-123">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9c17d-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9c17d-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="9c17d-124">-JobName</span></span>
<span data-ttu-id="9c17d-125">Specifica il nome del processo di analisi di Azure Stream in cui creare l'output di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="9c17d-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics output.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c17d-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c17d-126">-Name</span></span>
<span data-ttu-id="9c17d-127">Specifica il nome dell'output di analisi di Azure Stream da creare.</span><span class="sxs-lookup"><span data-stu-id="9c17d-127">Specifies the name of the Azure Stream Analytics output to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c17d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c17d-128">-ResourceGroupName</span></span>
<span data-ttu-id="9c17d-129">Specifica il nome del gruppo di risorse in cui creare l'output di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="9c17d-129">Specifies the name of the resource group under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="9c17d-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9c17d-130">-Confirm</span></span>
<span data-ttu-id="9c17d-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c17d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c17d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c17d-132">-WhatIf</span></span>
<span data-ttu-id="9c17d-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c17d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c17d-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c17d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c17d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c17d-135">CommonParameters</span></span>
<span data-ttu-id="9c17d-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c17d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c17d-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c17d-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c17d-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9c17d-138">INPUTS</span></span>

### <span data-ttu-id="9c17d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9c17d-139">System.String</span></span>

## <span data-ttu-id="9c17d-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c17d-140">OUTPUTS</span></span>

### <span data-ttu-id="9c17d-141">Microsoft. Azure. Commands. StreamAnalytics. Models. PSOutput</span><span class="sxs-lookup"><span data-stu-id="9c17d-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="9c17d-142">Note</span><span class="sxs-lookup"><span data-stu-id="9c17d-142">NOTES</span></span>

## <span data-ttu-id="9c17d-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c17d-143">RELATED LINKS</span></span>

[<span data-ttu-id="9c17d-144">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="9c17d-144">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="9c17d-145">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="9c17d-145">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="9c17d-146">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="9c17d-146">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


