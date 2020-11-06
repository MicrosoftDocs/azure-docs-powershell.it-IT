---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/remove-azurermstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: 8e80162d5efa6aa274617941df218812ae6901a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516363"
---
# <span data-ttu-id="5a4bb-101">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="5a4bb-101">Remove-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="5a4bb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5a4bb-102">SYNOPSIS</span></span>
<span data-ttu-id="5a4bb-103">Elimina un input da un processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="5a4bb-103">Deletes an input from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a4bb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5a4bb-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a4bb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5a4bb-105">DESCRIPTION</span></span>
<span data-ttu-id="5a4bb-106">Il cmdlet **Remove-AzureRmStreamAnalyticsInput** Elimina in modo asincrono un input da un processo di analisi del flusso in Azure.</span><span class="sxs-lookup"><span data-stu-id="5a4bb-106">The **Remove-AzureRmStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="5a4bb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5a4bb-107">EXAMPLES</span></span>

### <span data-ttu-id="5a4bb-108">ESEMPIO 1: rimuovere un flusso di input da un processo</span><span class="sxs-lookup"><span data-stu-id="5a4bb-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="5a4bb-109">Questo comando rimuove l'input EventStream da StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="5a4bb-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="5a4bb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5a4bb-110">PARAMETERS</span></span>

### <span data-ttu-id="5a4bb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a4bb-111">-DefaultProfile</span></span>
<span data-ttu-id="5a4bb-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5a4bb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a4bb-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="5a4bb-113">-JobName</span></span>
<span data-ttu-id="5a4bb-114">Specifica il nome del processo di analisi di Azure stream a cui appartiene l'input di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="5a4bb-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="5a4bb-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="5a4bb-115">-Name</span></span>
<span data-ttu-id="5a4bb-116">Specifica il nome dell'input di analisi di Azure Stream da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="5a4bb-116">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="5a4bb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a4bb-117">-ResourceGroupName</span></span>
<span data-ttu-id="5a4bb-118">Specifica il nome del gruppo di risorse a cui appartiene l'input di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="5a4bb-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="5a4bb-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5a4bb-119">-Confirm</span></span>
<span data-ttu-id="5a4bb-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a4bb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a4bb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a4bb-121">-WhatIf</span></span>
<span data-ttu-id="5a4bb-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5a4bb-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a4bb-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5a4bb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a4bb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a4bb-124">CommonParameters</span></span>
<span data-ttu-id="5a4bb-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a4bb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a4bb-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a4bb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a4bb-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5a4bb-127">INPUTS</span></span>

### <span data-ttu-id="5a4bb-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5a4bb-128">System.String</span></span>

## <span data-ttu-id="5a4bb-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5a4bb-129">OUTPUTS</span></span>

### <span data-ttu-id="5a4bb-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5a4bb-130">System.Boolean</span></span>

## <span data-ttu-id="5a4bb-131">Note</span><span class="sxs-lookup"><span data-stu-id="5a4bb-131">NOTES</span></span>

## <span data-ttu-id="5a4bb-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5a4bb-132">RELATED LINKS</span></span>

[<span data-ttu-id="5a4bb-133">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="5a4bb-133">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="5a4bb-134">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="5a4bb-134">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="5a4bb-135">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="5a4bb-135">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


