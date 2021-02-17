---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
ms.openlocfilehash: d481cf5ba28a87e098691d4b3fa5c179670d881d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182951"
---
# <span data-ttu-id="21d12-101">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="21d12-101">Remove-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="21d12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21d12-102">SYNOPSIS</span></span>
<span data-ttu-id="21d12-103">Elimina una funzione da un processo di Analisi di flusso.</span><span class="sxs-lookup"><span data-stu-id="21d12-103">Deletes a function from a Stream Analytics job.</span></span>

## <span data-ttu-id="21d12-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="21d12-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21d12-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="21d12-105">DESCRIPTION</span></span>
<span data-ttu-id="21d12-106">Il cmdlet **Remove-AzStreamAnalyticsFunction** elimina una funzione in modo asincrono da un processo di Analisi di flusso di Azure.</span><span class="sxs-lookup"><span data-stu-id="21d12-106">The **Remove-AzStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="21d12-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="21d12-107">EXAMPLES</span></span>

### <span data-ttu-id="21d12-108">Esempio 1: Rimuovere una funzione di Analisi di flusso</span><span class="sxs-lookup"><span data-stu-id="21d12-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="21d12-109">Questo comando rimuove la funzione denominata ScoreTweet dal processo denominato StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="21d12-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="21d12-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21d12-110">PARAMETERS</span></span>

### <span data-ttu-id="21d12-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21d12-111">-DefaultProfile</span></span>
<span data-ttu-id="21d12-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="21d12-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21d12-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="21d12-113">-JobName</span></span>
<span data-ttu-id="21d12-114">Specifica il nome del processo di Analisi di flusso a cui appartiene una funzione.</span><span class="sxs-lookup"><span data-stu-id="21d12-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="21d12-115">Questo cmdlet rimuove una funzione dal processo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="21d12-115">This cmdlet removes a function from the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="21d12-116">-Name</span><span class="sxs-lookup"><span data-stu-id="21d12-116">-Name</span></span>
<span data-ttu-id="21d12-117">Specifica il nome della funzione Analisi di flusso rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21d12-117">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21d12-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21d12-118">-ResourceGroupName</span></span>
<span data-ttu-id="21d12-119">Specifica il nome del gruppo di risorse a cui appartiene una funzione di Analisi di flusso.</span><span class="sxs-lookup"><span data-stu-id="21d12-119">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="21d12-120">Questo cmdlet elimina una funzione nel gruppo di risorse specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="21d12-120">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="21d12-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21d12-121">-Confirm</span></span>
<span data-ttu-id="21d12-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21d12-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21d12-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21d12-123">-WhatIf</span></span>
<span data-ttu-id="21d12-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21d12-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21d12-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21d12-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21d12-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21d12-126">CommonParameters</span></span>
<span data-ttu-id="21d12-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21d12-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21d12-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21d12-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21d12-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="21d12-129">INPUTS</span></span>

### <span data-ttu-id="21d12-130">System.String</span><span class="sxs-lookup"><span data-stu-id="21d12-130">System.String</span></span>

## <span data-ttu-id="21d12-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="21d12-131">OUTPUTS</span></span>

### <span data-ttu-id="21d12-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="21d12-132">System.Boolean</span></span>

## <span data-ttu-id="21d12-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="21d12-133">NOTES</span></span>

## <span data-ttu-id="21d12-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="21d12-134">RELATED LINKS</span></span>

[<span data-ttu-id="21d12-135">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="21d12-135">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="21d12-136">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="21d12-136">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="21d12-137">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="21d12-137">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


