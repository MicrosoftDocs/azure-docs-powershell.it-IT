---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 43B2A4FD-DA74-403A-89D0-40FE9A3E5A7E
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/new-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
ms.openlocfilehash: b4484d06802a8b17fc08b359b5dafb7e0a406ffa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007533"
---
# <span data-ttu-id="4085c-101">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="4085c-101">New-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="4085c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4085c-102">SYNOPSIS</span></span>
<span data-ttu-id="4085c-103">Crea o aggiorna gli output per un processo di Analisi di flusso.</span><span class="sxs-lookup"><span data-stu-id="4085c-103">Creates or updates outputs for a Stream Analytics job.</span></span>

## <span data-ttu-id="4085c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4085c-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4085c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4085c-105">DESCRIPTION</span></span>
<span data-ttu-id="4085c-106">Il cmdlet **New-AzStreamAnalyticsOutput crea** un output all'interno di un processo di Analisi di flusso o aggiorna un output esistente.</span><span class="sxs-lookup"><span data-stu-id="4085c-106">The **New-AzStreamAnalyticsOutput** cmdlet creates an output within a Stream Analytics job or updates an existing output.</span></span>
<span data-ttu-id="4085c-107">Il nome dell'output può essere specificato nella proprietà . JSON o nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="4085c-107">The name of the output can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="4085c-108">Se vengono specificati entrambi, il nome nella riga di comando deve corrispondere al nome del file.</span><span class="sxs-lookup"><span data-stu-id="4085c-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="4085c-109">Se si specifica un output già esistente e non si specifica il parametro *Force,* il cmdlet chiederà se sostituire o meno l'output esistente.</span><span class="sxs-lookup"><span data-stu-id="4085c-109">If you specify an output that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing output.</span></span>
<span data-ttu-id="4085c-110">Se si specifica il *parametro Force* e si specifica un nome di output esistente, l'output verrà sostituito senza conferma.</span><span class="sxs-lookup"><span data-stu-id="4085c-110">If you specify the *Force* parameter and specify an existing output name, the output will be replaced without confirmation.</span></span>

## <span data-ttu-id="4085c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4085c-111">EXAMPLES</span></span>

### <span data-ttu-id="4085c-112">Esempio 1: Aggiungere un output a un processo</span><span class="sxs-lookup"><span data-stu-id="4085c-112">Example 1: Add an output to a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="4085c-113">Questo comando crea un nuovo output denominato Output nel processo denominato StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="4085c-113">This command creates a new output called Output in the job called StreamingJob.</span></span>
<span data-ttu-id="4085c-114">Se è già definito un output esistente con questo nome, il cmdlet chiederà se sostituirlo o meno.</span><span class="sxs-lookup"><span data-stu-id="4085c-114">If an existing output with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="4085c-115">Esempio 2: Sostituire una definizione di output di processo</span><span class="sxs-lookup"><span data-stu-id="4085c-115">Example 2: Replace a job output definition</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output" -Force
```

<span data-ttu-id="4085c-116">Questo comando sostituisce la definizione per l'output nel processo chiamato StreamingJob senza conferma.</span><span class="sxs-lookup"><span data-stu-id="4085c-116">This command replaces the definition for Output in the job called StreamingJob without confirmation.</span></span>

## <span data-ttu-id="4085c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4085c-117">PARAMETERS</span></span>

### <span data-ttu-id="4085c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4085c-118">-DefaultProfile</span></span>
<span data-ttu-id="4085c-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4085c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4085c-120">-File</span><span class="sxs-lookup"><span data-stu-id="4085c-120">-File</span></span>
<span data-ttu-id="4085c-121">Specifica il percorso di un file JSON che contiene la rappresentazione JSON dell'output di Analisi di flusso di Azure da creare.</span><span class="sxs-lookup"><span data-stu-id="4085c-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="4085c-122">-Force</span><span class="sxs-lookup"><span data-stu-id="4085c-122">-Force</span></span>
<span data-ttu-id="4085c-123">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="4085c-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4085c-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="4085c-124">-JobName</span></span>
<span data-ttu-id="4085c-125">Specifica il nome del processo di Analisi di flusso di Azure in cui creare l'output di Analisi di flusso di Azure.</span><span class="sxs-lookup"><span data-stu-id="4085c-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="4085c-126">-Name</span><span class="sxs-lookup"><span data-stu-id="4085c-126">-Name</span></span>
<span data-ttu-id="4085c-127">Specifica il nome dell'output di Analisi di flusso di Azure da creare.</span><span class="sxs-lookup"><span data-stu-id="4085c-127">Specifies the name of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="4085c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4085c-128">-ResourceGroupName</span></span>
<span data-ttu-id="4085c-129">Specifica il nome del gruppo di risorse in cui creare l'output di Analisi di flusso di Azure.</span><span class="sxs-lookup"><span data-stu-id="4085c-129">Specifies the name of the resource group under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="4085c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4085c-130">-Confirm</span></span>
<span data-ttu-id="4085c-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4085c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4085c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4085c-132">-WhatIf</span></span>
<span data-ttu-id="4085c-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4085c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4085c-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4085c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4085c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4085c-135">CommonParameters</span></span>
<span data-ttu-id="4085c-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4085c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4085c-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4085c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4085c-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="4085c-138">INPUTS</span></span>

### <span data-ttu-id="4085c-139">System.String</span><span class="sxs-lookup"><span data-stu-id="4085c-139">System.String</span></span>

## <span data-ttu-id="4085c-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4085c-140">OUTPUTS</span></span>

### <span data-ttu-id="4085c-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span><span class="sxs-lookup"><span data-stu-id="4085c-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="4085c-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="4085c-142">NOTES</span></span>

## <span data-ttu-id="4085c-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4085c-143">RELATED LINKS</span></span>

[<span data-ttu-id="4085c-144">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="4085c-144">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="4085c-145">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="4085c-145">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="4085c-146">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="4085c-146">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


