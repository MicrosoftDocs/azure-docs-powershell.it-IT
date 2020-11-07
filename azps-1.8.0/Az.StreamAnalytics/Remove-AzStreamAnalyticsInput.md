---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/remove-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/Remove-AzStreamAnalyticsInput.md
ms.openlocfilehash: fe6c78c0a4d1f4fa3ae9f7f917bdcffa49431575
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676401"
---
# <span data-ttu-id="385de-101">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="385de-101">Remove-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="385de-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="385de-102">SYNOPSIS</span></span>
<span data-ttu-id="385de-103">Elimina un input da un processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="385de-103">Deletes an input from a Stream Analytics job.</span></span>

## <span data-ttu-id="385de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="385de-104">SYNTAX</span></span>

```
Remove-AzStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="385de-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="385de-105">DESCRIPTION</span></span>
<span data-ttu-id="385de-106">Il cmdlet **Remove-AzStreamAnalyticsInput** Elimina in modo asincrono un input da un processo di analisi del flusso in Azure.</span><span class="sxs-lookup"><span data-stu-id="385de-106">The **Remove-AzStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="385de-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="385de-107">EXAMPLES</span></span>

### <span data-ttu-id="385de-108">ESEMPIO 1: rimuovere un flusso di input da un processo</span><span class="sxs-lookup"><span data-stu-id="385de-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="385de-109">Questo comando rimuove l'input EventStream da StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="385de-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="385de-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="385de-110">PARAMETERS</span></span>

### <span data-ttu-id="385de-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="385de-111">-DefaultProfile</span></span>
<span data-ttu-id="385de-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="385de-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="385de-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="385de-113">-JobName</span></span>
<span data-ttu-id="385de-114">Specifica il nome del processo di analisi di Azure stream a cui appartiene l'input di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="385de-114">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="385de-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="385de-115">-Name</span></span>
<span data-ttu-id="385de-116">Specifica il nome dell'input di analisi di Azure Stream da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="385de-116">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="385de-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="385de-117">-ResourceGroupName</span></span>
<span data-ttu-id="385de-118">Specifica il nome del gruppo di risorse a cui appartiene l'input di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="385de-118">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="385de-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="385de-119">-Confirm</span></span>
<span data-ttu-id="385de-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="385de-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="385de-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="385de-121">-WhatIf</span></span>
<span data-ttu-id="385de-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="385de-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="385de-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="385de-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="385de-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="385de-124">CommonParameters</span></span>
<span data-ttu-id="385de-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="385de-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="385de-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="385de-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="385de-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="385de-127">INPUTS</span></span>

### <span data-ttu-id="385de-128">System. String</span><span class="sxs-lookup"><span data-stu-id="385de-128">System.String</span></span>

## <span data-ttu-id="385de-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="385de-129">OUTPUTS</span></span>

### <span data-ttu-id="385de-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="385de-130">System.Boolean</span></span>

## <span data-ttu-id="385de-131">Note</span><span class="sxs-lookup"><span data-stu-id="385de-131">NOTES</span></span>

## <span data-ttu-id="385de-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="385de-132">RELATED LINKS</span></span>

[<span data-ttu-id="385de-133">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="385de-133">New-AzStreamAnalyticsInput</span></span>](./New-AzStreamAnalyticsInput.md)

[<span data-ttu-id="385de-134">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="385de-134">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="385de-135">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="385de-135">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


