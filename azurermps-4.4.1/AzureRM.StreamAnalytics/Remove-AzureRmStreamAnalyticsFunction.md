---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 75B0776E-32D5-4EE4-B35C-73E13185A4F1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: 10687094bcbbc6cc9a52e648d830d46eac089c4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520736"
---
# <span data-ttu-id="bb689-101">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="bb689-101">Remove-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="bb689-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bb689-102">SYNOPSIS</span></span>
<span data-ttu-id="bb689-103">Elimina una funzione da un processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="bb689-103">Deletes a function from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb689-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb689-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsFunction [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb689-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb689-105">DESCRIPTION</span></span>
<span data-ttu-id="bb689-106">Il cmdlet **Remove-AzureRmStreamAnalyticsFunction** Elimina una funzione in modo asincrono da un processo di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="bb689-106">The **Remove-AzureRmStreamAnalyticsFunction** cmdlet deletes a function asynchronously from an Azure Stream Analytics job.</span></span>

## <span data-ttu-id="bb689-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb689-107">EXAMPLES</span></span>

### <span data-ttu-id="bb689-108">Esempio 1: rimuovere una funzione di analisi del flusso</span><span class="sxs-lookup"><span data-stu-id="bb689-108">Example 1: Remove a Stream Analytics function</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -Name "ScoreTweet"
```

<span data-ttu-id="bb689-109">Questo comando rimuove la funzione denominata ScoreTweet dal processo denominato StreamJob22.</span><span class="sxs-lookup"><span data-stu-id="bb689-109">This command removes the function named ScoreTweet from the job named StreamJob22.</span></span>

## <span data-ttu-id="bb689-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bb689-110">PARAMETERS</span></span>

### <span data-ttu-id="bb689-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="bb689-111">-JobName</span></span>
<span data-ttu-id="bb689-112">Specifica il nome del processo di analisi del flusso a cui appartiene una funzione.</span><span class="sxs-lookup"><span data-stu-id="bb689-112">Specifies the name of the Stream Analytics job to which a function belongs.</span></span>
<span data-ttu-id="bb689-113">Questo cmdlet consente di rimuovere una funzione dal processo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="bb689-113">This cmdlet removes a function from the job that this parameter specifies.</span></span>

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

### <span data-ttu-id="bb689-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="bb689-114">-Name</span></span>
<span data-ttu-id="bb689-115">Specifica il nome della funzione di analisi del flusso rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb689-115">Specifies the name of the Stream Analytics function that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bb689-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb689-116">-ResourceGroupName</span></span>
<span data-ttu-id="bb689-117">Specifica il nome del gruppo di risorse a cui appartiene una funzione di analisi dello stream.</span><span class="sxs-lookup"><span data-stu-id="bb689-117">Specifies the name of the resource group to which a Stream Analytics function belongs.</span></span>
<span data-ttu-id="bb689-118">Questo cmdlet elimina una funzione nel gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="bb689-118">This cmdlet deletes a function in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="bb689-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bb689-119">-Confirm</span></span>
<span data-ttu-id="bb689-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb689-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb689-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb689-121">-WhatIf</span></span>
<span data-ttu-id="bb689-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb689-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb689-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb689-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb689-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb689-124">-DefaultProfile</span></span>
<span data-ttu-id="bb689-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bb689-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb689-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb689-126">CommonParameters</span></span>
<span data-ttu-id="bb689-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb689-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb689-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb689-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb689-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bb689-129">INPUTS</span></span>

## <span data-ttu-id="bb689-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb689-130">OUTPUTS</span></span>

### <span data-ttu-id="bb689-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="bb689-131">System.Object</span></span>

## <span data-ttu-id="bb689-132">Note</span><span class="sxs-lookup"><span data-stu-id="bb689-132">NOTES</span></span>

## <span data-ttu-id="bb689-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb689-133">RELATED LINKS</span></span>

[<span data-ttu-id="bb689-134">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="bb689-134">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="bb689-135">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="bb689-135">New-AzureRmStreamAnalyticsFunction</span></span>](./New-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="bb689-136">Test-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="bb689-136">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


