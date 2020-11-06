---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 64ebe431333914a907c515744501f4624a7977ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512131"
---
# <span data-ttu-id="27e04-101">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="27e04-101">Remove-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="27e04-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="27e04-102">SYNOPSIS</span></span>
<span data-ttu-id="27e04-103">Rimuove un processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="27e04-103">Removes a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27e04-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27e04-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27e04-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27e04-105">DESCRIPTION</span></span>
<span data-ttu-id="27e04-106">Il cmdlet **Remove-AzureRmStreamAnalyticsJob** Elimina in modo asincrono un processo specifico di analisi del flusso in Azure.</span><span class="sxs-lookup"><span data-stu-id="27e04-106">The **Remove-AzureRmStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="27e04-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27e04-107">EXAMPLES</span></span>

### <span data-ttu-id="27e04-108">ESEMPIO 1: rimuovere un processo</span><span class="sxs-lookup"><span data-stu-id="27e04-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="27e04-109">Questo comando rimuove il job StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="27e04-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="27e04-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="27e04-110">PARAMETERS</span></span>

### <span data-ttu-id="27e04-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27e04-111">-DefaultProfile</span></span>
<span data-ttu-id="27e04-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="27e04-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27e04-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="27e04-113">-Name</span></span>
<span data-ttu-id="27e04-114">Specifica il nome del processo di analisi di Azure Stream da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="27e04-114">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="27e04-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27e04-115">-ResourceGroupName</span></span>
<span data-ttu-id="27e04-116">Specifica il nome del gruppo di risorse a cui appartiene il processo di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="27e04-116">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="27e04-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="27e04-117">-Confirm</span></span>
<span data-ttu-id="27e04-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27e04-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27e04-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27e04-119">-WhatIf</span></span>
<span data-ttu-id="27e04-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27e04-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27e04-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27e04-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27e04-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27e04-122">CommonParameters</span></span>
<span data-ttu-id="27e04-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27e04-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27e04-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27e04-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27e04-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="27e04-125">INPUTS</span></span>

### <span data-ttu-id="27e04-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="27e04-126">None</span></span>
<span data-ttu-id="27e04-127">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="27e04-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="27e04-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27e04-128">OUTPUTS</span></span>

### <span data-ttu-id="27e04-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="27e04-129">System.Object</span></span>

## <span data-ttu-id="27e04-130">Note</span><span class="sxs-lookup"><span data-stu-id="27e04-130">NOTES</span></span>

## <span data-ttu-id="27e04-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27e04-131">RELATED LINKS</span></span>

[<span data-ttu-id="27e04-132">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="27e04-132">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="27e04-133">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="27e04-133">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="27e04-134">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="27e04-134">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="27e04-135">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="27e04-135">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


