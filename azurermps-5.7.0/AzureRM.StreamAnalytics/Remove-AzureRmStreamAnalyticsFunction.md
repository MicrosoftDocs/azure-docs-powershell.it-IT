---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: d76b1139955490189aeb9c2269cc4e9ede8197be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517808"
---
# <span data-ttu-id="efd1b-101">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="efd1b-101">Remove-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="efd1b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="efd1b-102">SYNOPSIS</span></span>
<span data-ttu-id="efd1b-103">Elimina una funzione da un processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="efd1b-103">Deletes a function from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efd1b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="efd1b-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efd1b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="efd1b-105">DESCRIPTION</span></span>
<span data-ttu-id="efd1b-106">Il cmdlet **Remove-AzureRmStreamAnalyticsFunction** Elimina una funzione in modo asincrono da un processo di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="efd1b-106">The **Remove-AzureRmStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="efd1b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="efd1b-107">EXAMPLES</span></span>

### <span data-ttu-id="efd1b-108">Esempio 1: rimuovere una funzione di analisi del flusso</span><span class="sxs-lookup"><span data-stu-id="efd1b-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="efd1b-109">Questo comando rimuove la funzione denominata ScoreTweet dal processo denominato StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="efd1b-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="efd1b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="efd1b-110">PARAMETERS</span></span>

### <span data-ttu-id="efd1b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efd1b-111">-DefaultProfile</span></span>
<span data-ttu-id="efd1b-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="efd1b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efd1b-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="efd1b-113">-JobName</span></span>
<span data-ttu-id="efd1b-114">Specifica il nome del processo di analisi del flusso a cui appartiene una funzione.</span><span class="sxs-lookup"><span data-stu-id="efd1b-114">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="efd1b-115">Questo cmdlet consente di rimuovere una funzione dal processo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="efd1b-115">This cmdlet removes a function from the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="efd1b-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="efd1b-116">-Name</span></span>
<span data-ttu-id="efd1b-117">Specifica il nome della funzione di analisi del flusso rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efd1b-117">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efd1b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efd1b-118">-ResourceGroupName</span></span>
<span data-ttu-id="efd1b-119">Specifica il nome del gruppo di risorse a cui appartiene una funzione di analisi dello stream.</span><span class="sxs-lookup"><span data-stu-id="efd1b-119">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="efd1b-120">Questo cmdlet elimina una funzione nel gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="efd1b-120">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="efd1b-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="efd1b-121">-Confirm</span></span>
<span data-ttu-id="efd1b-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efd1b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efd1b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efd1b-123">-WhatIf</span></span>
<span data-ttu-id="efd1b-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="efd1b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efd1b-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="efd1b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efd1b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efd1b-126">CommonParameters</span></span>
<span data-ttu-id="efd1b-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efd1b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efd1b-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efd1b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efd1b-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="efd1b-129">INPUTS</span></span>

### <span data-ttu-id="efd1b-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="efd1b-130">None</span></span>
<span data-ttu-id="efd1b-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="efd1b-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="efd1b-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="efd1b-132">OUTPUTS</span></span>

### <span data-ttu-id="efd1b-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="efd1b-133">System.Object</span></span>

## <span data-ttu-id="efd1b-134">Note</span><span class="sxs-lookup"><span data-stu-id="efd1b-134">NOTES</span></span>

## <span data-ttu-id="efd1b-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="efd1b-135">RELATED LINKS</span></span>

[<span data-ttu-id="efd1b-136">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="efd1b-136">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="efd1b-137">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="efd1b-137">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="efd1b-138">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="efd1b-138">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


