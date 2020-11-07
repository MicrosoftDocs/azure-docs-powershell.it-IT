---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 23f7c8270f3d5c0073be9705e43086aae3a3e903
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864455"
---
# <span data-ttu-id="dd8c1-101">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="dd8c1-101">Remove-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="dd8c1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dd8c1-102">SYNOPSIS</span></span>
<span data-ttu-id="dd8c1-103">Elimina un output da un processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="dd8c1-103">Deletes an output from a Stream Analytics job.</span></span>

## <span data-ttu-id="dd8c1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd8c1-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd8c1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd8c1-105">DESCRIPTION</span></span>
<span data-ttu-id="dd8c1-106">Il cmdlet **Remove-AzStreamAnalyticsOutput** Elimina in modo asincrono un output da un processo di analisi del flusso in Azure.</span><span class="sxs-lookup"><span data-stu-id="dd8c1-106">The **Remove-AzStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="dd8c1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd8c1-107">EXAMPLES</span></span>

### <span data-ttu-id="dd8c1-108">ESEMPIO 1: rimuovere un output da un processo</span><span class="sxs-lookup"><span data-stu-id="dd8c1-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="dd8c1-109">Questo comando rimuove l'output di output in Job StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="dd8c1-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="dd8c1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dd8c1-110">PARAMETERS</span></span>

### <span data-ttu-id="dd8c1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd8c1-111">-DefaultProfile</span></span>
<span data-ttu-id="dd8c1-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dd8c1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd8c1-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="dd8c1-113">-JobName</span></span>
<span data-ttu-id="dd8c1-114">Specifica il nome del processo di analisi di Azure stream a cui appartiene l'output di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="dd8c1-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="dd8c1-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd8c1-115">-Name</span></span>
<span data-ttu-id="dd8c1-116">Specifica il nome dell'output di analisi di Azure Stream da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="dd8c1-116">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="dd8c1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd8c1-117">-ResourceGroupName</span></span>
<span data-ttu-id="dd8c1-118">Specifica il nome del gruppo di risorse a cui appartiene l'output di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="dd8c1-118">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="dd8c1-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dd8c1-119">-Confirm</span></span>
<span data-ttu-id="dd8c1-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd8c1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd8c1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd8c1-121">-WhatIf</span></span>
<span data-ttu-id="dd8c1-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd8c1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd8c1-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd8c1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd8c1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd8c1-124">CommonParameters</span></span>
<span data-ttu-id="dd8c1-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd8c1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd8c1-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd8c1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd8c1-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dd8c1-127">INPUTS</span></span>

### <span data-ttu-id="dd8c1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="dd8c1-128">System.String</span></span>

## <span data-ttu-id="dd8c1-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd8c1-129">OUTPUTS</span></span>

### <span data-ttu-id="dd8c1-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dd8c1-130">System.Boolean</span></span>

## <span data-ttu-id="dd8c1-131">Note</span><span class="sxs-lookup"><span data-stu-id="dd8c1-131">NOTES</span></span>

## <span data-ttu-id="dd8c1-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd8c1-132">RELATED LINKS</span></span>

[<span data-ttu-id="dd8c1-133">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="dd8c1-133">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="dd8c1-134">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="dd8c1-134">New-AzStreamAnalyticsOutput</span></span>](./New-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="dd8c1-135">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="dd8c1-135">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


