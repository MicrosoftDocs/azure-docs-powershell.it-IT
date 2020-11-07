---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 43B2A4FD-DA74-403A-89D0-40FE9A3E5A7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 1669d30081ab0ec99579228efbf26d8c76207865
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676404"
---
# <span data-ttu-id="d2f81-101">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="d2f81-101">New-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="d2f81-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d2f81-102">SYNOPSIS</span></span>
<span data-ttu-id="d2f81-103">Crea o aggiorna gli output per un processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="d2f81-103">Creates or updates outputs for a Stream Analytics job.</span></span>

## <span data-ttu-id="d2f81-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d2f81-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d2f81-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d2f81-105">DESCRIPTION</span></span>
<span data-ttu-id="d2f81-106">Il cmdlet **New-AzStreamAnalyticsOutput** crea un output all'interno di un processo di analisi del flusso o aggiorna un output esistente.</span><span class="sxs-lookup"><span data-stu-id="d2f81-106">The **New-AzStreamAnalyticsOutput** cmdlet creates an output within a Stream Analytics job or updates an existing output.</span></span>
<span data-ttu-id="d2f81-107">Il nome dell'output può essere specificato in. File JSON o nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="d2f81-107">The name of the output can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="d2f81-108">Se entrambi sono specificati, la riga di comando nome deve corrispondere al nome nel file.</span><span class="sxs-lookup"><span data-stu-id="d2f81-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="d2f81-109">Se specifichi un output già esistente e non specifichi il parametro *Force* , il cmdlet chiederà se sostituire o meno l'output esistente.</span><span class="sxs-lookup"><span data-stu-id="d2f81-109">If you specify an output that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing output.</span></span>
<span data-ttu-id="d2f81-110">Se specifichi il parametro *Force* e specifichi un nome di output esistente, l'output verrà sostituito senza conferma.</span><span class="sxs-lookup"><span data-stu-id="d2f81-110">If you specify the *Force* parameter and specify an existing output name, the output will be replaced without confirmation.</span></span>

## <span data-ttu-id="d2f81-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d2f81-111">EXAMPLES</span></span>

### <span data-ttu-id="d2f81-112">ESEMPIO 1: aggiungere un output a un processo</span><span class="sxs-lookup"><span data-stu-id="d2f81-112">EXAMPLE 1: Add an output to a job</span></span>
```
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="d2f81-113">Questo comando crea un nuovo output denominato output nel processo denominato StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="d2f81-113">This command creates a new output called Output in the job called StreamingJob.</span></span>
<span data-ttu-id="d2f81-114">Se un output esistente con questo nome è già definito, il cmdlet chiederà se sostituirlo o meno.</span><span class="sxs-lookup"><span data-stu-id="d2f81-114">If an existing output with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="d2f81-115">ESEMPIO 2: sostituire una definizione di output del processo</span><span class="sxs-lookup"><span data-stu-id="d2f81-115">EXAMPLE 2: Replace a job output definition</span></span>
```
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output" -Force
```

<span data-ttu-id="d2f81-116">Questo comando sostituisce la definizione per l'output nel processo denominato StreamingJob senza conferma.</span><span class="sxs-lookup"><span data-stu-id="d2f81-116">This command replaces the definition for Output in the job called StreamingJob without confirmation.</span></span>

## <span data-ttu-id="d2f81-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d2f81-117">PARAMETERS</span></span>

### <span data-ttu-id="d2f81-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2f81-118">-DefaultProfile</span></span>
<span data-ttu-id="d2f81-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d2f81-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2f81-120">-File</span><span class="sxs-lookup"><span data-stu-id="d2f81-120">-File</span></span>
<span data-ttu-id="d2f81-121">Specifica il percorso di un file JSON che contiene la rappresentazione JSON dell'output di analisi di Azure Stream da creare.</span><span class="sxs-lookup"><span data-stu-id="d2f81-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="d2f81-122">-Force</span><span class="sxs-lookup"><span data-stu-id="d2f81-122">-Force</span></span>
<span data-ttu-id="d2f81-123">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d2f81-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d2f81-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="d2f81-124">-JobName</span></span>
<span data-ttu-id="d2f81-125">Specifica il nome del processo di analisi di Azure Stream in cui creare l'output di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="d2f81-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="d2f81-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="d2f81-126">-Name</span></span>
<span data-ttu-id="d2f81-127">Specifica il nome dell'output di analisi di Azure Stream da creare.</span><span class="sxs-lookup"><span data-stu-id="d2f81-127">Specifies the name of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="d2f81-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2f81-128">-ResourceGroupName</span></span>
<span data-ttu-id="d2f81-129">Specifica il nome del gruppo di risorse in cui creare l'output di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="d2f81-129">Specifies the name of the resource group under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="d2f81-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d2f81-130">-Confirm</span></span>
<span data-ttu-id="d2f81-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2f81-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2f81-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2f81-132">-WhatIf</span></span>
<span data-ttu-id="d2f81-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2f81-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2f81-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d2f81-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2f81-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2f81-135">CommonParameters</span></span>
<span data-ttu-id="d2f81-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2f81-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2f81-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2f81-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2f81-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d2f81-138">INPUTS</span></span>

### <span data-ttu-id="d2f81-139">System. String</span><span class="sxs-lookup"><span data-stu-id="d2f81-139">System.String</span></span>

## <span data-ttu-id="d2f81-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d2f81-140">OUTPUTS</span></span>

### <span data-ttu-id="d2f81-141">Microsoft. Azure. Commands. StreamAnalytics. Models. PSOutput</span><span class="sxs-lookup"><span data-stu-id="d2f81-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="d2f81-142">Note</span><span class="sxs-lookup"><span data-stu-id="d2f81-142">NOTES</span></span>

## <span data-ttu-id="d2f81-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d2f81-143">RELATED LINKS</span></span>

[<span data-ttu-id="d2f81-144">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="d2f81-144">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="d2f81-145">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="d2f81-145">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="d2f81-146">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="d2f81-146">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


