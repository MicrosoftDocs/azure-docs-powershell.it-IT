---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 79EB2AD9-BFE1-49BE-870F-7DFC99D6FE17
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 38d0c63dba4ac5cdc6b64ea3013f24a19bc048fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676410"
---
# <span data-ttu-id="2c982-101">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="2c982-101">New-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="2c982-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2c982-102">SYNOPSIS</span></span>
<span data-ttu-id="2c982-103">Crea o sostituisce una funzione in un processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="2c982-103">Creates or replaces a function in a Stream Analytics job.</span></span>

## <span data-ttu-id="2c982-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2c982-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c982-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c982-105">DESCRIPTION</span></span>
<span data-ttu-id="2c982-106">Il cmdlet **New-AzStreamAnalyticsFunction** crea una funzione in un processo di analisi di Azure Stream o sostituisce una funzione esistente.</span><span class="sxs-lookup"><span data-stu-id="2c982-106">The **New-AzStreamAnalyticsFunction** cmdlet creates a function in an Azure Stream Analytics job or replaces an existing function.</span></span>
<span data-ttu-id="2c982-107">Definire la funzione in un file JSON (JavaScript Object Notation).</span><span class="sxs-lookup"><span data-stu-id="2c982-107">Define the function in a JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="2c982-108">Puoi specificare il nome della funzione usando il parametro *Name* o nel file JSON.</span><span class="sxs-lookup"><span data-stu-id="2c982-108">You can specify the name of the function by using the *Name* parameter or in the .json file.</span></span>
<span data-ttu-id="2c982-109">Se specifichi il nome in entrambi i modi, i nomi devono corrispondere.</span><span class="sxs-lookup"><span data-stu-id="2c982-109">If you specify the name in both ways, the names must match.</span></span>
<span data-ttu-id="2c982-110">Per sostituire una funzione esistente, specificare il nome della funzione esistente.</span><span class="sxs-lookup"><span data-stu-id="2c982-110">To replace an existing function, specify the name of the existing function.</span></span>

## <span data-ttu-id="2c982-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2c982-111">EXAMPLES</span></span>

### <span data-ttu-id="2c982-112">Esempio 1: creare una funzione di analisi del flusso</span><span class="sxs-lookup"><span data-stu-id="2c982-112">Example 1: Create a Stream Analytics function</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob07" -File "C:\Function07.json"
```

<span data-ttu-id="2c982-113">Questo comando crea una funzione dal file Function07.jsattivata.</span><span class="sxs-lookup"><span data-stu-id="2c982-113">This command creates a function from the file Function07.json.</span></span>
<span data-ttu-id="2c982-114">Il nome della funzione viene archiviato nel file con estensione JSON.</span><span class="sxs-lookup"><span data-stu-id="2c982-114">The name of the function is stored in the .json file.</span></span>

### <span data-ttu-id="2c982-115">Esempio 2: creare una funzione di analisi dello stream denominata ScoreTweet</span><span class="sxs-lookup"><span data-stu-id="2c982-115">Example 2: Create a Stream Analytics function named ScoreTweet</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet"
```

<span data-ttu-id="2c982-116">Questo comando crea una funzione nel processo denominato ScoreTweet.</span><span class="sxs-lookup"><span data-stu-id="2c982-116">This command creates a function on the job named ScoreTweet.</span></span>

### <span data-ttu-id="2c982-117">Esempio 3: sostituire una funzione di analisi del flusso</span><span class="sxs-lookup"><span data-stu-id="2c982-117">Example 3: Replace a Stream Analytics function</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet" -Force
```

<span data-ttu-id="2c982-118">Questo comando sostituisce la definizione della funzione esistente denominata ScoreTweet con la definizione in Function22.jsattivata.</span><span class="sxs-lookup"><span data-stu-id="2c982-118">This command replaces the definition of the existing function named ScoreTweet with the definition in Function22.json.</span></span>

## <span data-ttu-id="2c982-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2c982-119">PARAMETERS</span></span>

### <span data-ttu-id="2c982-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c982-120">-DefaultProfile</span></span>
<span data-ttu-id="2c982-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2c982-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c982-122">-File</span><span class="sxs-lookup"><span data-stu-id="2c982-122">-File</span></span>
<span data-ttu-id="2c982-123">Specifica il percorso di un file con estensione JSON che contiene la rappresentazione JSON della funzione analisi flusso.</span><span class="sxs-lookup"><span data-stu-id="2c982-123">Specifies the path of a .json file that contains the JSON representation of the Stream Analytics function.</span></span>

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

### <span data-ttu-id="2c982-124">-Force</span><span class="sxs-lookup"><span data-stu-id="2c982-124">-Force</span></span>
<span data-ttu-id="2c982-125">Indica che questo cmdlet sostituisce una funzione di analisi dello stream esistente senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="2c982-125">Indicates that this cmdlet replaces an existing Stream Analytics function without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="2c982-126">-JobName</span><span class="sxs-lookup"><span data-stu-id="2c982-126">-JobName</span></span>
<span data-ttu-id="2c982-127">Specifica il nome del processo di analisi del flusso in cui questo cmdlet crea una funzione di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="2c982-127">Specifies the name of the Stream Analytics job under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="2c982-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="2c982-128">-Name</span></span>
<span data-ttu-id="2c982-129">Specifica il nome della funzione analisi flusso creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c982-129">Specifies the name of the Stream Analytics function that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2c982-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c982-130">-ResourceGroupName</span></span>
<span data-ttu-id="2c982-131">Specifica il nome del gruppo di risorse in cui questo cmdlet crea una funzione di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="2c982-131">Specifies the name of the resource group under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="2c982-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2c982-132">-Confirm</span></span>
<span data-ttu-id="2c982-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c982-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c982-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c982-134">-WhatIf</span></span>
<span data-ttu-id="2c982-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2c982-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c982-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2c982-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c982-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c982-137">CommonParameters</span></span>
<span data-ttu-id="2c982-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c982-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c982-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c982-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c982-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2c982-140">INPUTS</span></span>

### <span data-ttu-id="2c982-141">System. String</span><span class="sxs-lookup"><span data-stu-id="2c982-141">System.String</span></span>

## <span data-ttu-id="2c982-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2c982-142">OUTPUTS</span></span>

### <span data-ttu-id="2c982-143">Microsoft. Azure. Commands. StreamAnalytics. Models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="2c982-143">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="2c982-144">Note</span><span class="sxs-lookup"><span data-stu-id="2c982-144">NOTES</span></span>

## <span data-ttu-id="2c982-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2c982-145">RELATED LINKS</span></span>

[<span data-ttu-id="2c982-146">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="2c982-146">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="2c982-147">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="2c982-147">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="2c982-148">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="2c982-148">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)

