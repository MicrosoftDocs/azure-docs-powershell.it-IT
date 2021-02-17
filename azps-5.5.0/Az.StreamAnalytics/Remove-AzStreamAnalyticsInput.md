---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
ms.openlocfilehash: d3c5e578e6921297d7d5edc467e10b9a2b4e9e53
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182943"
---
# <span data-ttu-id="5ea9b-101">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="5ea9b-101">Remove-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="5ea9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ea9b-102">SYNOPSIS</span></span>
<span data-ttu-id="5ea9b-103">Elimina un input da un processo di Analisi di flusso.</span><span class="sxs-lookup"><span data-stu-id="5ea9b-103">Deletes an input from a Stream Analytics job.</span></span>

## <span data-ttu-id="5ea9b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ea9b-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ea9b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5ea9b-105">DESCRIPTION</span></span>
<span data-ttu-id="5ea9b-106">Il cmdlet **Remove-AzStreamAnalyticsInput** elimina in modo asincrono un input da un processo di Analisi di flusso in Azure.</span><span class="sxs-lookup"><span data-stu-id="5ea9b-106">The **Remove-AzStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="5ea9b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ea9b-107">EXAMPLES</span></span>

### <span data-ttu-id="5ea9b-108">ESEMPIO 1: Rimuovere un flusso di input da un processo</span><span class="sxs-lookup"><span data-stu-id="5ea9b-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="5ea9b-109">Questo comando rimuove l'input EventStream da StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="5ea9b-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="5ea9b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ea9b-110">PARAMETERS</span></span>

### <span data-ttu-id="5ea9b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ea9b-111">-DefaultProfile</span></span>
<span data-ttu-id="5ea9b-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5ea9b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ea9b-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="5ea9b-113">-JobName</span></span>
<span data-ttu-id="5ea9b-114">Specifica il nome del processo di Analisi di flusso di Azure a cui appartiene l'input di Analisi di flusso di Azure.</span><span class="sxs-lookup"><span data-stu-id="5ea9b-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="5ea9b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5ea9b-115">-Name</span></span>
<span data-ttu-id="5ea9b-116">Specifica il nome dell'input di Azure Stream Analytics da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="5ea9b-116">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="5ea9b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ea9b-117">-ResourceGroupName</span></span>
<span data-ttu-id="5ea9b-118">Specifica il nome del gruppo di risorse a cui appartiene l'input di Analisi di flusso di Azure.</span><span class="sxs-lookup"><span data-stu-id="5ea9b-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="5ea9b-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ea9b-119">-Confirm</span></span>
<span data-ttu-id="5ea9b-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ea9b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ea9b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ea9b-121">-WhatIf</span></span>
<span data-ttu-id="5ea9b-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5ea9b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ea9b-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5ea9b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ea9b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ea9b-124">CommonParameters</span></span>
<span data-ttu-id="5ea9b-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ea9b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ea9b-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ea9b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ea9b-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="5ea9b-127">INPUTS</span></span>

### <span data-ttu-id="5ea9b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="5ea9b-128">System.String</span></span>

## <span data-ttu-id="5ea9b-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ea9b-129">OUTPUTS</span></span>

### <span data-ttu-id="5ea9b-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5ea9b-130">System.Boolean</span></span>

## <span data-ttu-id="5ea9b-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="5ea9b-131">NOTES</span></span>

## <span data-ttu-id="5ea9b-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ea9b-132">RELATED LINKS</span></span>

[<span data-ttu-id="5ea9b-133">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="5ea9b-133">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="5ea9b-134">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="5ea9b-134">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="5ea9b-135">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="5ea9b-135">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


