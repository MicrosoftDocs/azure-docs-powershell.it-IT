---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsJob.md
ms.openlocfilehash: 2b15c1a3b4b69b1a1db3eb25dd953cf62644c8a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93856717"
---
# <span data-ttu-id="725ea-101">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="725ea-101">Remove-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="725ea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="725ea-102">SYNOPSIS</span></span>
<span data-ttu-id="725ea-103">Rimuove un processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="725ea-103">Removes a Stream Analytics job.</span></span>

## <span data-ttu-id="725ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="725ea-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="725ea-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="725ea-105">DESCRIPTION</span></span>
<span data-ttu-id="725ea-106">Il cmdlet **Remove-AzStreamAnalyticsJob** Elimina in modo asincrono un processo specifico di analisi del flusso in Azure.</span><span class="sxs-lookup"><span data-stu-id="725ea-106">The **Remove-AzStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="725ea-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="725ea-107">EXAMPLES</span></span>

### <span data-ttu-id="725ea-108">ESEMPIO 1: rimuovere un processo</span><span class="sxs-lookup"><span data-stu-id="725ea-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="725ea-109">Questo comando rimuove il job StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="725ea-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="725ea-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="725ea-110">PARAMETERS</span></span>

### <span data-ttu-id="725ea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="725ea-111">-DefaultProfile</span></span>
<span data-ttu-id="725ea-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="725ea-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="725ea-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="725ea-113">-Name</span></span>
<span data-ttu-id="725ea-114">Specifica il nome del processo di analisi di Azure Stream da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="725ea-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="725ea-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="725ea-115">-ResourceGroupName</span></span>
<span data-ttu-id="725ea-116">Specifica il nome del gruppo di risorse a cui appartiene il processo di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="725ea-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="725ea-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="725ea-117">-Confirm</span></span>
<span data-ttu-id="725ea-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="725ea-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="725ea-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="725ea-119">-WhatIf</span></span>
<span data-ttu-id="725ea-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="725ea-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="725ea-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="725ea-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="725ea-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="725ea-122">CommonParameters</span></span>
<span data-ttu-id="725ea-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="725ea-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="725ea-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="725ea-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="725ea-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="725ea-125">INPUTS</span></span>

### <span data-ttu-id="725ea-126">System. String</span><span class="sxs-lookup"><span data-stu-id="725ea-126">System.String</span></span>

## <span data-ttu-id="725ea-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="725ea-127">OUTPUTS</span></span>

### <span data-ttu-id="725ea-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="725ea-128">System.Boolean</span></span>

## <span data-ttu-id="725ea-129">Note</span><span class="sxs-lookup"><span data-stu-id="725ea-129">NOTES</span></span>

## <span data-ttu-id="725ea-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="725ea-130">RELATED LINKS</span></span>

[<span data-ttu-id="725ea-131">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="725ea-131">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="725ea-132">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="725ea-132">New-AzStreamAnalyticsJob</span></span>](./New-AzStreamAnalyticsJob.md)

[<span data-ttu-id="725ea-133">Start-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="725ea-133">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="725ea-134">Stop-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="725ea-134">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


