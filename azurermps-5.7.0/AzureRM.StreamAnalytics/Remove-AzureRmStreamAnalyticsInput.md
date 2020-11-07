---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 9e228c2520402f1b8395c6ca4d90909905f6cb0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685597"
---
# <span data-ttu-id="68d4a-101">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="68d4a-101">Remove-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="68d4a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="68d4a-102">SYNOPSIS</span></span>
<span data-ttu-id="68d4a-103">Elimina un input da un processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="68d4a-103">Deletes an input from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68d4a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68d4a-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68d4a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68d4a-105">DESCRIPTION</span></span>
<span data-ttu-id="68d4a-106">Il cmdlet **Remove-AzureRmStreamAnalyticsInput** Elimina in modo asincrono un input da un processo di analisi del flusso in Azure.</span><span class="sxs-lookup"><span data-stu-id="68d4a-106">The **Remove-AzureRmStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="68d4a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68d4a-107">EXAMPLES</span></span>

### <span data-ttu-id="68d4a-108">ESEMPIO 1: rimuovere un flusso di input da un processo</span><span class="sxs-lookup"><span data-stu-id="68d4a-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="68d4a-109">Questo comando rimuove l'input EventStream da StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="68d4a-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="68d4a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="68d4a-110">PARAMETERS</span></span>

### <span data-ttu-id="68d4a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68d4a-111">-DefaultProfile</span></span>
<span data-ttu-id="68d4a-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="68d4a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68d4a-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="68d4a-113">-JobName</span></span>
<span data-ttu-id="68d4a-114">Specifica il nome del processo di analisi di Azure stream a cui appartiene l'input di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="68d4a-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="68d4a-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="68d4a-115">-Name</span></span>
<span data-ttu-id="68d4a-116">Specifica il nome dell'input di analisi di Azure Stream da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="68d4a-116">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="68d4a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68d4a-117">-ResourceGroupName</span></span>
<span data-ttu-id="68d4a-118">Specifica il nome del gruppo di risorse a cui appartiene l'input di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="68d4a-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="68d4a-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="68d4a-119">-Confirm</span></span>
<span data-ttu-id="68d4a-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68d4a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68d4a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68d4a-121">-WhatIf</span></span>
<span data-ttu-id="68d4a-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="68d4a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68d4a-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="68d4a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68d4a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68d4a-124">CommonParameters</span></span>
<span data-ttu-id="68d4a-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68d4a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68d4a-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68d4a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68d4a-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="68d4a-127">INPUTS</span></span>

### <span data-ttu-id="68d4a-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="68d4a-128">None</span></span>
<span data-ttu-id="68d4a-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="68d4a-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="68d4a-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68d4a-130">OUTPUTS</span></span>

### <span data-ttu-id="68d4a-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="68d4a-131">System.Object</span></span>

## <span data-ttu-id="68d4a-132">Note</span><span class="sxs-lookup"><span data-stu-id="68d4a-132">NOTES</span></span>

## <span data-ttu-id="68d4a-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68d4a-133">RELATED LINKS</span></span>

[<span data-ttu-id="68d4a-134">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="68d4a-134">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="68d4a-135">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="68d4a-135">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="68d4a-136">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="68d4a-136">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


