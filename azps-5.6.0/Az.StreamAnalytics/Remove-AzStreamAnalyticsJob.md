---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/remove-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
ms.openlocfilehash: 183aa9dd5cc7da6e0d86c1fa1018bcfe405c0f7e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973758"
---
# <span data-ttu-id="ba777-101">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ba777-101">Remove-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="ba777-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba777-102">SYNOPSIS</span></span>
<span data-ttu-id="ba777-103">Rimuove un processo di Analisi di flusso.</span><span class="sxs-lookup"><span data-stu-id="ba777-103">Removes a Stream Analytics job.</span></span>

## <span data-ttu-id="ba777-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba777-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba777-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ba777-105">DESCRIPTION</span></span>
<span data-ttu-id="ba777-106">Il cmdlet **Remove-AzStreamAnalyticsJob** elimina in modo asincrono uno specifico processo di Analisi di flusso in Azure.</span><span class="sxs-lookup"><span data-stu-id="ba777-106">The **Remove-AzStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="ba777-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba777-107">EXAMPLES</span></span>

### <span data-ttu-id="ba777-108">ESEMPIO 1: Rimuovere un processo</span><span class="sxs-lookup"><span data-stu-id="ba777-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="ba777-109">Questo comando rimuove il processo StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="ba777-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="ba777-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba777-110">PARAMETERS</span></span>

### <span data-ttu-id="ba777-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba777-111">-DefaultProfile</span></span>
<span data-ttu-id="ba777-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ba777-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba777-113">-Name</span><span class="sxs-lookup"><span data-stu-id="ba777-113">-Name</span></span>
<span data-ttu-id="ba777-114">Specifica il nome del processo di Analisi di flusso di Azure da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ba777-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="ba777-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba777-115">-ResourceGroupName</span></span>
<span data-ttu-id="ba777-116">Specifica il nome del gruppo di risorse a cui appartiene il processo di Analisi di flusso di Azure.</span><span class="sxs-lookup"><span data-stu-id="ba777-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="ba777-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ba777-117">-Confirm</span></span>
<span data-ttu-id="ba777-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba777-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba777-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba777-119">-WhatIf</span></span>
<span data-ttu-id="ba777-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ba777-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba777-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ba777-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba777-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba777-122">CommonParameters</span></span>
<span data-ttu-id="ba777-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba777-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba777-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba777-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba777-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="ba777-125">INPUTS</span></span>

### <span data-ttu-id="ba777-126">System.String</span><span class="sxs-lookup"><span data-stu-id="ba777-126">System.String</span></span>

## <span data-ttu-id="ba777-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba777-127">OUTPUTS</span></span>

### <span data-ttu-id="ba777-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ba777-128">System.Boolean</span></span>

## <span data-ttu-id="ba777-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="ba777-129">NOTES</span></span>

## <span data-ttu-id="ba777-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba777-130">RELATED LINKS</span></span>

[<span data-ttu-id="ba777-131">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ba777-131">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="ba777-132">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ba777-132">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="ba777-133">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ba777-133">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="ba777-134">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="ba777-134">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


