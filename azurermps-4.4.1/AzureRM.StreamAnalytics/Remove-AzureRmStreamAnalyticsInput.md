---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 1449F64F-A8F9-4E8E-B62B-17DEF3A0FB30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsInput.md
ms.openlocfilehash: f801a7c8dd83927e8aceebdc98138aa6ad39d31c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520735"
---
# <span data-ttu-id="6d62f-101">Remove-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="6d62f-101">Remove-AzureRmStreamAnalyticsInput</span></span>

## <span data-ttu-id="6d62f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6d62f-102">SYNOPSIS</span></span>
<span data-ttu-id="6d62f-103">Elimina un input da un processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="6d62f-103">Deletes an input from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d62f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6d62f-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsInput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d62f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d62f-105">DESCRIPTION</span></span>
<span data-ttu-id="6d62f-106">Il cmdlet **Remove-AzureRmStreamAnalyticsInput** Elimina in modo asincrono un input da un processo di analisi del flusso in Azure.</span><span class="sxs-lookup"><span data-stu-id="6d62f-106">The **Remove-AzureRmStreamAnalyticsInput** cmdlet asynchronously deletes an input from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="6d62f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6d62f-107">EXAMPLES</span></span>

### <span data-ttu-id="6d62f-108">ESEMPIO 1: rimuovere un flusso di input da un processo</span><span class="sxs-lookup"><span data-stu-id="6d62f-108">EXAMPLE 1: Remove an input stream from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "EventStream"
```

<span data-ttu-id="6d62f-109">Questo comando rimuove l'input EventStream da StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="6d62f-109">This command removes the input EventStream from StreamingJob.</span></span>

## <span data-ttu-id="6d62f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6d62f-110">PARAMETERS</span></span>

### <span data-ttu-id="6d62f-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="6d62f-111">-JobName</span></span>
<span data-ttu-id="6d62f-112">Specifica il nome del processo di analisi di Azure stream a cui appartiene l'input di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="6d62f-112">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="6d62f-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="6d62f-113">-Name</span></span>
<span data-ttu-id="6d62f-114">Specifica il nome dell'input di analisi di Azure Stream da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6d62f-114">Specifies the name of the Azure Stream Analytics input to remove.</span></span>

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

### <span data-ttu-id="6d62f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d62f-115">-ResourceGroupName</span></span>
<span data-ttu-id="6d62f-116">Specifica il nome del gruppo di risorse a cui appartiene l'input di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="6d62f-116">Specifies the name of the resource group to which the Azure Stream Analytics input belongs.</span></span>

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

### <span data-ttu-id="6d62f-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6d62f-117">-Confirm</span></span>
<span data-ttu-id="6d62f-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d62f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d62f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d62f-119">-WhatIf</span></span>
<span data-ttu-id="6d62f-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d62f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d62f-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d62f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d62f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d62f-122">-DefaultProfile</span></span>
<span data-ttu-id="6d62f-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6d62f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d62f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d62f-124">CommonParameters</span></span>
<span data-ttu-id="6d62f-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d62f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d62f-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d62f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d62f-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6d62f-127">INPUTS</span></span>

## <span data-ttu-id="6d62f-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6d62f-128">OUTPUTS</span></span>

### <span data-ttu-id="6d62f-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="6d62f-129">System.Object</span></span>

## <span data-ttu-id="6d62f-130">Note</span><span class="sxs-lookup"><span data-stu-id="6d62f-130">NOTES</span></span>

## <span data-ttu-id="6d62f-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6d62f-131">RELATED LINKS</span></span>

[<span data-ttu-id="6d62f-132">New-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="6d62f-132">New-AzureRmStreamAnalyticsInput</span></span>](./New-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="6d62f-133">Get-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="6d62f-133">Get-AzureRmStreamAnalyticsInput</span></span>](./Get-AzureRmStreamAnalyticsInput.md)

[<span data-ttu-id="6d62f-134">Test-AzureRmStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="6d62f-134">Test-AzureRmStreamAnalyticsInput</span></span>](./Test-AzureRmStreamAnalyticsInput.md)


