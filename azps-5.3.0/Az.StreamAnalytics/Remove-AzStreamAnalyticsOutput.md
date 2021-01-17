---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 23f7c8270f3d5c0073be9705e43086aae3a3e903
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384271"
---
# <span data-ttu-id="53546-101">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="53546-101">Remove-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="53546-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="53546-102">SYNOPSIS</span></span>
<span data-ttu-id="53546-103">Elimina un output da un processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="53546-103">Deletes an output from a Stream Analytics job.</span></span>

## <span data-ttu-id="53546-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="53546-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53546-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53546-105">DESCRIPTION</span></span>
<span data-ttu-id="53546-106">Il cmdlet **Remove-AzStreamAnalyticsOutput** Elimina in modo asincrono un output da un processo di analisi del flusso in Azure.</span><span class="sxs-lookup"><span data-stu-id="53546-106">The **Remove-AzStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="53546-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="53546-107">EXAMPLES</span></span>

### <span data-ttu-id="53546-108">ESEMPIO 1: rimuovere un output da un processo</span><span class="sxs-lookup"><span data-stu-id="53546-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="53546-109">Questo comando rimuove l'output di output in Job StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="53546-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="53546-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="53546-110">PARAMETERS</span></span>

### <span data-ttu-id="53546-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53546-111">-DefaultProfile</span></span>
<span data-ttu-id="53546-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="53546-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53546-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="53546-113">-JobName</span></span>
<span data-ttu-id="53546-114">Specifica il nome del processo di analisi di Azure stream a cui appartiene l'output di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="53546-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="53546-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="53546-115">-Name</span></span>
<span data-ttu-id="53546-116">Specifica il nome dell'output di analisi di Azure Stream da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="53546-116">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="53546-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53546-117">-ResourceGroupName</span></span>
<span data-ttu-id="53546-118">Specifica il nome del gruppo di risorse a cui appartiene l'output di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="53546-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="53546-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="53546-119">-Confirm</span></span>
<span data-ttu-id="53546-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53546-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53546-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53546-121">-WhatIf</span></span>
<span data-ttu-id="53546-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="53546-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53546-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="53546-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53546-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53546-124">CommonParameters</span></span>
<span data-ttu-id="53546-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53546-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53546-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53546-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53546-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="53546-127">INPUTS</span></span>

### <span data-ttu-id="53546-128">System. String</span><span class="sxs-lookup"><span data-stu-id="53546-128">System.String</span></span>

## <span data-ttu-id="53546-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="53546-129">OUTPUTS</span></span>

### <span data-ttu-id="53546-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="53546-130">System.Boolean</span></span>

## <span data-ttu-id="53546-131">Note</span><span class="sxs-lookup"><span data-stu-id="53546-131">NOTES</span></span>

## <span data-ttu-id="53546-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="53546-132">RELATED LINKS</span></span>

[<span data-ttu-id="53546-133">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="53546-133">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="53546-134">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="53546-134">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="53546-135">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="53546-135">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


