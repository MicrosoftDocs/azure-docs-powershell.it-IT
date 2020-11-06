---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: b6c703b1c3373e4e0f1347d9bb2a9819ac1e5de6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516359"
---
# <span data-ttu-id="9997c-101">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9997c-101">Remove-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="9997c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9997c-102">SYNOPSIS</span></span>
<span data-ttu-id="9997c-103">Rimuove un processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="9997c-103">Removes a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9997c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9997c-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9997c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9997c-105">DESCRIPTION</span></span>
<span data-ttu-id="9997c-106">Il cmdlet **Remove-AzureRmStreamAnalyticsJob** Elimina in modo asincrono un processo specifico di analisi del flusso in Azure.</span><span class="sxs-lookup"><span data-stu-id="9997c-106">The **Remove-AzureRmStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="9997c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9997c-107">EXAMPLES</span></span>

### <span data-ttu-id="9997c-108">ESEMPIO 1: rimuovere un processo</span><span class="sxs-lookup"><span data-stu-id="9997c-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="9997c-109">Questo comando rimuove il job StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="9997c-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="9997c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9997c-110">PARAMETERS</span></span>

### <span data-ttu-id="9997c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9997c-111">-DefaultProfile</span></span>
<span data-ttu-id="9997c-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9997c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9997c-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="9997c-113">-Name</span></span>
<span data-ttu-id="9997c-114">Specifica il nome del processo di analisi di Azure Stream da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="9997c-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="9997c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9997c-115">-ResourceGroupName</span></span>
<span data-ttu-id="9997c-116">Specifica il nome del gruppo di risorse a cui appartiene il processo di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="9997c-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="9997c-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9997c-117">-Confirm</span></span>
<span data-ttu-id="9997c-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9997c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9997c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9997c-119">-WhatIf</span></span>
<span data-ttu-id="9997c-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9997c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9997c-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9997c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9997c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9997c-122">CommonParameters</span></span>
<span data-ttu-id="9997c-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9997c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9997c-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9997c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9997c-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9997c-125">INPUTS</span></span>

### <span data-ttu-id="9997c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="9997c-126">System.String</span></span>

## <span data-ttu-id="9997c-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9997c-127">OUTPUTS</span></span>

### <span data-ttu-id="9997c-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9997c-128">System.Boolean</span></span>

## <span data-ttu-id="9997c-129">Note</span><span class="sxs-lookup"><span data-stu-id="9997c-129">NOTES</span></span>

## <span data-ttu-id="9997c-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9997c-130">RELATED LINKS</span></span>

[<span data-ttu-id="9997c-131">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9997c-131">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="9997c-132">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9997c-132">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="9997c-133">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9997c-133">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="9997c-134">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="9997c-134">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


