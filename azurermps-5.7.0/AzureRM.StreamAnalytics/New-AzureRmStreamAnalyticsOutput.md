---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 43B2A4FD-DA74-403A-89D0-40FE9A3E5A7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/new-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 7b18513a6a9e7ebbf82892500344d13f9cbc8185
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517819"
---
# <span data-ttu-id="d6799-101">New-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="d6799-101">New-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="d6799-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d6799-102">SYNOPSIS</span></span>
<span data-ttu-id="d6799-103">Crea o aggiorna gli output per un processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="d6799-103">Creates or updates outputs for a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6799-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d6799-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d6799-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6799-105">DESCRIPTION</span></span>
<span data-ttu-id="d6799-106">Il cmdlet **New-AzureRmStreamAnalyticsOutput** crea un output all'interno di un processo di analisi del flusso o aggiorna un output esistente.</span><span class="sxs-lookup"><span data-stu-id="d6799-106">The **New-AzureRmStreamAnalyticsOutput** cmdlet creates an output within a Stream Analytics job or updates an existing output.</span></span>
<span data-ttu-id="d6799-107">Il nome dell'output può essere specificato in. File JSON o nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="d6799-107">The name of the output can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="d6799-108">Se entrambi sono specificati, la riga di comando nome deve corrispondere al nome nel file.</span><span class="sxs-lookup"><span data-stu-id="d6799-108">If both are specified, the name on command line must match the name in the file.</span></span>

<span data-ttu-id="d6799-109">Se specifichi un output già esistente e non specifichi il parametro *Force* , il cmdlet chiederà se sostituire o meno l'output esistente.</span><span class="sxs-lookup"><span data-stu-id="d6799-109">If you specify an output that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing output.</span></span>

<span data-ttu-id="d6799-110">Se specifichi il parametro *Force* e specifichi un nome di output esistente, l'output verrà sostituito senza conferma.</span><span class="sxs-lookup"><span data-stu-id="d6799-110">If you specify the *Force* parameter and specify an existing output name, the output will be replaced without confirmation.</span></span>

## <span data-ttu-id="d6799-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d6799-111">EXAMPLES</span></span>

### <span data-ttu-id="d6799-112">ESEMPIO 1: aggiungere un output a un processo</span><span class="sxs-lookup"><span data-stu-id="d6799-112">EXAMPLE 1: Add an output to a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="d6799-113">Questo comando crea un nuovo output denominato output nel processo denominato StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="d6799-113">This command creates a new output called Output in the job called StreamingJob.</span></span>
<span data-ttu-id="d6799-114">Se un output esistente con questo nome è già definito, il cmdlet chiederà se sostituirlo o meno.</span><span class="sxs-lookup"><span data-stu-id="d6799-114">If an existing output with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="d6799-115">ESEMPIO 2: sostituire una definizione di output del processo</span><span class="sxs-lookup"><span data-stu-id="d6799-115">EXAMPLE 2: Replace a job output definition</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output" -Force
```

<span data-ttu-id="d6799-116">Questo comando sostituisce la definizione per l'output nel processo denominato StreamingJob senza conferma.</span><span class="sxs-lookup"><span data-stu-id="d6799-116">This command replaces the definition for Output in the job called StreamingJob without confirmation.</span></span>

## <span data-ttu-id="d6799-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d6799-117">PARAMETERS</span></span>

### <span data-ttu-id="d6799-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6799-118">-DefaultProfile</span></span>
<span data-ttu-id="d6799-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d6799-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6799-120">-File</span><span class="sxs-lookup"><span data-stu-id="d6799-120">-File</span></span>
<span data-ttu-id="d6799-121">Specifica il percorso di un file JSON che contiene la rappresentazione JSON dell'output di analisi di Azure Stream da creare.</span><span class="sxs-lookup"><span data-stu-id="d6799-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics output to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6799-122">-Force</span><span class="sxs-lookup"><span data-stu-id="d6799-122">-Force</span></span>
<span data-ttu-id="d6799-123">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d6799-123">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6799-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="d6799-124">-JobName</span></span>
<span data-ttu-id="d6799-125">Specifica il nome del processo di analisi di Azure Stream in cui creare l'output di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="d6799-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics output.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6799-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="d6799-126">-Name</span></span>
<span data-ttu-id="d6799-127">Specifica il nome dell'output di analisi di Azure Stream da creare.</span><span class="sxs-lookup"><span data-stu-id="d6799-127">Specifies the name of the Azure Stream Analytics output to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6799-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6799-128">-ResourceGroupName</span></span>
<span data-ttu-id="d6799-129">Specifica il nome del gruppo di risorse in cui creare l'output di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="d6799-129">Specifies the name of the resource group under which to create the Azure Stream Analytics output.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6799-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d6799-130">-Confirm</span></span>
<span data-ttu-id="d6799-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6799-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6799-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6799-132">-WhatIf</span></span>
<span data-ttu-id="d6799-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6799-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6799-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d6799-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6799-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6799-135">CommonParameters</span></span>
<span data-ttu-id="d6799-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6799-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6799-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6799-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6799-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d6799-138">INPUTS</span></span>

### <span data-ttu-id="d6799-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d6799-139">None</span></span>
<span data-ttu-id="d6799-140">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d6799-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d6799-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d6799-141">OUTPUTS</span></span>

### <span data-ttu-id="d6799-142">Microsoft. Azure. Commands. StreamAnalytics. Models. PSOutput</span><span class="sxs-lookup"><span data-stu-id="d6799-142">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="d6799-143">Note</span><span class="sxs-lookup"><span data-stu-id="d6799-143">NOTES</span></span>

## <span data-ttu-id="d6799-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d6799-144">RELATED LINKS</span></span>

[<span data-ttu-id="d6799-145">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="d6799-145">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="d6799-146">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="d6799-146">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="d6799-147">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="d6799-147">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


