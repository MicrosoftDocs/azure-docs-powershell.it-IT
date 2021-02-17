---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 79EB2AD9-BFE1-49BE-870F-7DFC99D6FE17
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 71a6267b06ce47ee36f220033ec598af3680deeb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182991"
---
# <span data-ttu-id="6a884-101">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="6a884-101">New-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="6a884-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a884-102">SYNOPSIS</span></span>
<span data-ttu-id="6a884-103">Crea o sostituisce una funzione in un processo di Analisi di flusso.</span><span class="sxs-lookup"><span data-stu-id="6a884-103">Creates or replaces a function in a Stream Analytics job.</span></span>

## <span data-ttu-id="6a884-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a884-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6a884-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6a884-105">DESCRIPTION</span></span>
<span data-ttu-id="6a884-106">Il cmdlet **New-AzStreamAnalyticsFunction** crea una funzione in un processo di Analisi di flusso di Azure o sostituisce una funzione esistente.</span><span class="sxs-lookup"><span data-stu-id="6a884-106">The **New-AzStreamAnalyticsFunction** cmdlet creates a function in an Azure Stream Analytics job or replaces an existing function.</span></span>
<span data-ttu-id="6a884-107">Definire la funzione in un file JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="6a884-107">Define the function in a JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="6a884-108">È possibile specificare il nome della funzione usando il parametro *Name* o nel file JSON.</span><span class="sxs-lookup"><span data-stu-id="6a884-108">You can specify the name of the function by using the *Name* parameter or in the .json file.</span></span>
<span data-ttu-id="6a884-109">Se si specifica il nome in entrambi i modi, i nomi devono corrispondere.</span><span class="sxs-lookup"><span data-stu-id="6a884-109">If you specify the name in both ways, the names must match.</span></span>
<span data-ttu-id="6a884-110">Per sostituire una funzione esistente, specificare il nome della funzione esistente.</span><span class="sxs-lookup"><span data-stu-id="6a884-110">To replace an existing function, specify the name of the existing function.</span></span>

## <span data-ttu-id="6a884-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a884-111">EXAMPLES</span></span>

### <span data-ttu-id="6a884-112">Esempio 1: Creare una funzione di Analisi di flusso</span><span class="sxs-lookup"><span data-stu-id="6a884-112">Example 1: Create a Stream Analytics function</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob07" -File "C:\Function07.json"
```

<span data-ttu-id="6a884-113">Questo comando crea una funzione dalla cartella Function07.jsfile.</span><span class="sxs-lookup"><span data-stu-id="6a884-113">This command creates a function from the file Function07.json.</span></span>
<span data-ttu-id="6a884-114">Il nome della funzione viene archiviato nel file JSON.</span><span class="sxs-lookup"><span data-stu-id="6a884-114">The name of the function is stored in the .json file.</span></span>

### <span data-ttu-id="6a884-115">Esempio 2: Creare una funzione di Analisi di flusso denominata ScoreTweet</span><span class="sxs-lookup"><span data-stu-id="6a884-115">Example 2: Create a Stream Analytics function named ScoreTweet</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet"
```

<span data-ttu-id="6a884-116">Questo comando crea una funzione nel processo denominato ScoreTweet.</span><span class="sxs-lookup"><span data-stu-id="6a884-116">This command creates a function on the job named ScoreTweet.</span></span>

### <span data-ttu-id="6a884-117">Esempio 3: Sostituire una funzione di Analisi di flusso</span><span class="sxs-lookup"><span data-stu-id="6a884-117">Example 3: Replace a Stream Analytics function</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet" -Force
```

<span data-ttu-id="6a884-118">Questo comando sostituisce la definizione della funzione esistente denominata ScoreTweet con la definizione in Function22.jsavanti.</span><span class="sxs-lookup"><span data-stu-id="6a884-118">This command replaces the definition of the existing function named ScoreTweet with the definition in Function22.json.</span></span>

## <span data-ttu-id="6a884-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a884-119">PARAMETERS</span></span>

### <span data-ttu-id="6a884-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a884-120">-DefaultProfile</span></span>
<span data-ttu-id="6a884-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a884-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a884-122">-File</span><span class="sxs-lookup"><span data-stu-id="6a884-122">-File</span></span>
<span data-ttu-id="6a884-123">Specifica il percorso di un file JSON che contiene la rappresentazione JSON della funzione Analisi di flusso.</span><span class="sxs-lookup"><span data-stu-id="6a884-123">Specifies the path of a .json file that contains the JSON representation of the Stream Analytics function.</span></span>

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

### <span data-ttu-id="6a884-124">-Force</span><span class="sxs-lookup"><span data-stu-id="6a884-124">-Force</span></span>
<span data-ttu-id="6a884-125">Indica che questo cmdlet sostituisce una funzione di Analisi di flusso esistente senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="6a884-125">Indicates that this cmdlet replaces an existing Stream Analytics function without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="6a884-126">-JobName</span><span class="sxs-lookup"><span data-stu-id="6a884-126">-JobName</span></span>
<span data-ttu-id="6a884-127">Specifica il nome del processo di Analisi di flusso in cui questo cmdlet crea una funzione di Analisi di flusso.</span><span class="sxs-lookup"><span data-stu-id="6a884-127">Specifies the name of the Stream Analytics job under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="6a884-128">-Name</span><span class="sxs-lookup"><span data-stu-id="6a884-128">-Name</span></span>
<span data-ttu-id="6a884-129">Specifica il nome della funzione Analisi di flusso creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a884-129">Specifies the name of the Stream Analytics function that this cmdlet creates.</span></span>

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

### <span data-ttu-id="6a884-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a884-130">-ResourceGroupName</span></span>
<span data-ttu-id="6a884-131">Specifica il nome del gruppo di risorse in cui questo cmdlet crea una funzione di Analisi di flusso.</span><span class="sxs-lookup"><span data-stu-id="6a884-131">Specifies the name of the resource group under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="6a884-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a884-132">-Confirm</span></span>
<span data-ttu-id="6a884-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a884-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a884-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a884-134">-WhatIf</span></span>
<span data-ttu-id="6a884-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a884-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a884-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a884-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a884-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a884-137">CommonParameters</span></span>
<span data-ttu-id="6a884-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a884-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a884-139">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a884-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a884-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="6a884-140">INPUTS</span></span>

### <span data-ttu-id="6a884-141">System.String</span><span class="sxs-lookup"><span data-stu-id="6a884-141">System.String</span></span>

## <span data-ttu-id="6a884-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a884-142">OUTPUTS</span></span>

### <span data-ttu-id="6a884-143">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span><span class="sxs-lookup"><span data-stu-id="6a884-143">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="6a884-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="6a884-144">NOTES</span></span>

## <span data-ttu-id="6a884-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a884-145">RELATED LINKS</span></span>

[<span data-ttu-id="6a884-146">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="6a884-146">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="6a884-147">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="6a884-147">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="6a884-148">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="6a884-148">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


