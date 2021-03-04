---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/remove-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 950d761324f0750f2433b0b88edb5d37859945e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984014"
---
# <span data-ttu-id="06a39-101">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="06a39-101">Remove-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="06a39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06a39-102">SYNOPSIS</span></span>
<span data-ttu-id="06a39-103">Elimina un output da un processo di Analisi di flusso.</span><span class="sxs-lookup"><span data-stu-id="06a39-103">Deletes an output from a Stream Analytics job.</span></span>

## <span data-ttu-id="06a39-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06a39-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06a39-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="06a39-105">DESCRIPTION</span></span>
<span data-ttu-id="06a39-106">Il cmdlet **Remove-AzStreamAnalyticsOutput** elimina in modo asincrono un output da un processo di Analisi di flusso in Azure.</span><span class="sxs-lookup"><span data-stu-id="06a39-106">The **Remove-AzStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="06a39-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06a39-107">EXAMPLES</span></span>

### <span data-ttu-id="06a39-108">ESEMPIO 1: Rimuovere un output da un processo</span><span class="sxs-lookup"><span data-stu-id="06a39-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="06a39-109">Questo comando rimuove l'output di output nel processo StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="06a39-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="06a39-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06a39-110">PARAMETERS</span></span>

### <span data-ttu-id="06a39-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06a39-111">-DefaultProfile</span></span>
<span data-ttu-id="06a39-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="06a39-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06a39-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="06a39-113">-JobName</span></span>
<span data-ttu-id="06a39-114">Specifica il nome del processo di Analisi di flusso di Azure a cui appartiene l'output di Analisi di flusso di Azure.</span><span class="sxs-lookup"><span data-stu-id="06a39-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="06a39-115">-Name</span><span class="sxs-lookup"><span data-stu-id="06a39-115">-Name</span></span>
<span data-ttu-id="06a39-116">Specifica il nome dell'output di Analisi di flusso di Azure da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="06a39-116">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="06a39-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06a39-117">-ResourceGroupName</span></span>
<span data-ttu-id="06a39-118">Specifica il nome del gruppo di risorse a cui appartiene l'output di Analisi di flusso di Azure.</span><span class="sxs-lookup"><span data-stu-id="06a39-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="06a39-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06a39-119">-Confirm</span></span>
<span data-ttu-id="06a39-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06a39-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06a39-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06a39-121">-WhatIf</span></span>
<span data-ttu-id="06a39-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06a39-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06a39-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="06a39-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06a39-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06a39-124">CommonParameters</span></span>
<span data-ttu-id="06a39-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06a39-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06a39-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06a39-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06a39-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="06a39-127">INPUTS</span></span>

### <span data-ttu-id="06a39-128">System.String</span><span class="sxs-lookup"><span data-stu-id="06a39-128">System.String</span></span>

## <span data-ttu-id="06a39-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06a39-129">OUTPUTS</span></span>

### <span data-ttu-id="06a39-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="06a39-130">System.Boolean</span></span>

## <span data-ttu-id="06a39-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="06a39-131">NOTES</span></span>

## <span data-ttu-id="06a39-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06a39-132">RELATED LINKS</span></span>

[<span data-ttu-id="06a39-133">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="06a39-133">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="06a39-134">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="06a39-134">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="06a39-135">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="06a39-135">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


