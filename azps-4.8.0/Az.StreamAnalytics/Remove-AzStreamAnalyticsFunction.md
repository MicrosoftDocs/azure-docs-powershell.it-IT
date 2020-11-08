---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsFunction.md
ms.openlocfilehash: d481cf5ba28a87e098691d4b3fa5c179670d881d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191738"
---
# <span data-ttu-id="00a58-101">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="00a58-101">Remove-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="00a58-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="00a58-102">SYNOPSIS</span></span>
<span data-ttu-id="00a58-103">Elimina una funzione da un processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="00a58-103">Deletes a function from a Stream Analytics job.</span></span>

## <span data-ttu-id="00a58-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="00a58-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00a58-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00a58-105">DESCRIPTION</span></span>
<span data-ttu-id="00a58-106">Il cmdlet **Remove-AzStreamAnalyticsFunction** Elimina una funzione in modo asincrono da un processo di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="00a58-106">The **Remove-AzStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="00a58-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="00a58-107">EXAMPLES</span></span>

### <span data-ttu-id="00a58-108">Esempio 1: rimuovere una funzione di analisi del flusso</span><span class="sxs-lookup"><span data-stu-id="00a58-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="00a58-109">Questo comando rimuove la funzione denominata ScoreTweet dal processo denominato StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="00a58-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="00a58-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="00a58-110">PARAMETERS</span></span>

### <span data-ttu-id="00a58-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00a58-111">-DefaultProfile</span></span>
<span data-ttu-id="00a58-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="00a58-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00a58-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="00a58-113">-JobName</span></span>
<span data-ttu-id="00a58-114">Specifica il nome del processo di analisi del flusso a cui appartiene una funzione.</span><span class="sxs-lookup"><span data-stu-id="00a58-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="00a58-115">Questo cmdlet consente di rimuovere una funzione dal processo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="00a58-115">This cmdlet removes a function from the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="00a58-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="00a58-116">-Name</span></span>
<span data-ttu-id="00a58-117">Specifica il nome della funzione di analisi del flusso rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00a58-117">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

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

### <span data-ttu-id="00a58-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00a58-118">-ResourceGroupName</span></span>
<span data-ttu-id="00a58-119">Specifica il nome del gruppo di risorse a cui appartiene una funzione di analisi dello stream.</span><span class="sxs-lookup"><span data-stu-id="00a58-119">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="00a58-120">Questo cmdlet elimina una funzione nel gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="00a58-120">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="00a58-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="00a58-121">-Confirm</span></span>
<span data-ttu-id="00a58-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00a58-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00a58-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00a58-123">-WhatIf</span></span>
<span data-ttu-id="00a58-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="00a58-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00a58-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="00a58-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00a58-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00a58-126">CommonParameters</span></span>
<span data-ttu-id="00a58-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00a58-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00a58-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00a58-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00a58-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="00a58-129">INPUTS</span></span>

### <span data-ttu-id="00a58-130">System. String</span><span class="sxs-lookup"><span data-stu-id="00a58-130">System.String</span></span>

## <span data-ttu-id="00a58-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="00a58-131">OUTPUTS</span></span>

### <span data-ttu-id="00a58-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="00a58-132">System.Boolean</span></span>

## <span data-ttu-id="00a58-133">Note</span><span class="sxs-lookup"><span data-stu-id="00a58-133">NOTES</span></span>

## <span data-ttu-id="00a58-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="00a58-134">RELATED LINKS</span></span>

[<span data-ttu-id="00a58-135">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="00a58-135">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="00a58-136">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="00a58-136">New-AzStreamAnalyticsFunction</span></span>](./New-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="00a58-137">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="00a58-137">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


