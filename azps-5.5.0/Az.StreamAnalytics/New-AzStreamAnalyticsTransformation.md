---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 8FF53426-D4AE-455E-A182-D7FBC7262FE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: 017c084e98d8983343ae1f8c19464cc254b26e2e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182959"
---
# <span data-ttu-id="b8051-101">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="b8051-101">New-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="b8051-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8051-102">SYNOPSIS</span></span>
<span data-ttu-id="b8051-103">Crea o aggiorna una trasformazione all'interno di un processo.</span><span class="sxs-lookup"><span data-stu-id="b8051-103">Creates or updates a transformation within a job.</span></span>

## <span data-ttu-id="b8051-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b8051-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsTransformation [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b8051-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b8051-105">DESCRIPTION</span></span>
<span data-ttu-id="b8051-106">Il cmdlet **New-AzStreamAnalytics Transformation** crea una trasformazione all'interno di un processo di Analisi di flusso o aggiorna la trasformazione esistente.</span><span class="sxs-lookup"><span data-stu-id="b8051-106">The **New-AzStreamAnalyticsTransformation** cmdlet creates a transformation within a Stream Analytics job or updates the existing transformation.</span></span>
<span data-ttu-id="b8051-107">Il nome della trasformazione può essere specificato nella proprietà . JSON o nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="b8051-107">The name of the transformation can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="b8051-108">Se vengono specificati entrambi, il nome nella riga di comando deve corrispondere al nome del file.</span><span class="sxs-lookup"><span data-stu-id="b8051-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="b8051-109">Se si specifica una trasformazione già esistente e non si specifica il parametro Force, il cmdlet chiederà se sostituire o meno la trasformazione esistente.</span><span class="sxs-lookup"><span data-stu-id="b8051-109">If you specify a transformation that already exists and do not specify the Force parameter, the cmdlet will ask whether or not to replace the existing transformation.</span></span>
<span data-ttu-id="b8051-110">Se si specifica il *parametro Force* e si specifica un nome di trasformazione esistente, la trasformazione verrà sostituita senza conferma.</span><span class="sxs-lookup"><span data-stu-id="b8051-110">If you specify the *Force* parameter and specify an existing transformation name, the transformation will be replaced without confirmation.</span></span>

## <span data-ttu-id="b8051-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b8051-111">EXAMPLES</span></span>

### <span data-ttu-id="b8051-112">Esempio 1: Creare o sostituire una trasformazione in un processo</span><span class="sxs-lookup"><span data-stu-id="b8051-112">Example 1: Create or replace a transformation in a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform"
```

<span data-ttu-id="b8051-113">Questo comando crea una trasformazione chiamata StreamingJobTransform nel processo denominato StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="b8051-113">This command creates a transformation called StreamingJobTransform in the job called StreamingJob.</span></span>
<span data-ttu-id="b8051-114">Se una trasformazione esistente è già definita con questo nome, il cmdlet chiederà se sostituirla o meno.</span><span class="sxs-lookup"><span data-stu-id="b8051-114">If an existing transformation is already defined with that name, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="b8051-115">Esempio 2: Sostituire una trasformazione in un processo</span><span class="sxs-lookup"><span data-stu-id="b8051-115">Example 2: Replace a transformation in a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform" -Force
```

<span data-ttu-id="b8051-116">Questo comando sostituisce la definizione di StreamingJobTransform nel processo StreamingJob senza conferma.</span><span class="sxs-lookup"><span data-stu-id="b8051-116">This command replaces the definition of StreamingJobTransform in the job StreamingJob without confirmation.</span></span>

## <span data-ttu-id="b8051-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8051-117">PARAMETERS</span></span>

### <span data-ttu-id="b8051-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8051-118">-DefaultProfile</span></span>
<span data-ttu-id="b8051-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b8051-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8051-120">-File</span><span class="sxs-lookup"><span data-stu-id="b8051-120">-File</span></span>
<span data-ttu-id="b8051-121">Specifica il percorso di un file JSON che contiene la rappresentazione JSON della trasformazione di Analisi di flusso di Azure da creare.</span><span class="sxs-lookup"><span data-stu-id="b8051-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="b8051-122">-Force</span><span class="sxs-lookup"><span data-stu-id="b8051-122">-Force</span></span>
<span data-ttu-id="b8051-123">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="b8051-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b8051-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="b8051-124">-JobName</span></span>
<span data-ttu-id="b8051-125">Specifica il nome del processo di Analisi di flusso di Azure in cui creare la trasformazione di Analisi di flusso di Azure.</span><span class="sxs-lookup"><span data-stu-id="b8051-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="b8051-126">-Name</span><span class="sxs-lookup"><span data-stu-id="b8051-126">-Name</span></span>
<span data-ttu-id="b8051-127">Specifica il nome della trasformazione di Analisi di flusso di Azure da creare.</span><span class="sxs-lookup"><span data-stu-id="b8051-127">Specifies the name of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="b8051-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8051-128">-ResourceGroupName</span></span>
<span data-ttu-id="b8051-129">Specifica il nome del gruppo di risorse in cui creare la trasformazione di Analisi di flusso di Azure.</span><span class="sxs-lookup"><span data-stu-id="b8051-129">Specifies the name of the resource group under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="b8051-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8051-130">-Confirm</span></span>
<span data-ttu-id="b8051-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8051-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8051-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8051-132">-WhatIf</span></span>
<span data-ttu-id="b8051-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b8051-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8051-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b8051-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8051-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8051-135">CommonParameters</span></span>
<span data-ttu-id="b8051-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8051-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8051-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8051-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8051-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="b8051-138">INPUTS</span></span>

### <span data-ttu-id="b8051-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b8051-139">System.String</span></span>

## <span data-ttu-id="b8051-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b8051-140">OUTPUTS</span></span>

### <span data-ttu-id="b8051-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PS Transformation</span><span class="sxs-lookup"><span data-stu-id="b8051-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="b8051-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="b8051-142">NOTES</span></span>

## <span data-ttu-id="b8051-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b8051-143">RELATED LINKS</span></span>

[<span data-ttu-id="b8051-144">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="b8051-144">Get-AzStreamAnalyticsTransformation</span></span>](./Get-AzStreamAnalyticsTransformation.md)


