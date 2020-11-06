---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 9ba839bbfc6740d9d62c9a036d233a8b5a1ce0e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520732"
---
# <span data-ttu-id="6866a-101">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6866a-101">Remove-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="6866a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6866a-102">SYNOPSIS</span></span>
<span data-ttu-id="6866a-103">Rimuove un processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="6866a-103">Removes a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6866a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6866a-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6866a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6866a-105">DESCRIPTION</span></span>
<span data-ttu-id="6866a-106">Il cmdlet **Remove-AzureRmStreamAnalyticsJob** Elimina in modo asincrono un processo specifico di analisi del flusso in Azure.</span><span class="sxs-lookup"><span data-stu-id="6866a-106">The **Remove-AzureRmStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="6866a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6866a-107">EXAMPLES</span></span>

### <span data-ttu-id="6866a-108">ESEMPIO 1: rimuovere un processo</span><span class="sxs-lookup"><span data-stu-id="6866a-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="6866a-109">Questo comando rimuove il job StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="6866a-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="6866a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6866a-110">PARAMETERS</span></span>

### <span data-ttu-id="6866a-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="6866a-111">-Name</span></span>
<span data-ttu-id="6866a-112">Specifica il nome del processo di analisi di Azure Stream da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6866a-112">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="6866a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6866a-113">-ResourceGroupName</span></span>
<span data-ttu-id="6866a-114">Specifica il nome del gruppo di risorse a cui appartiene il processo di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="6866a-114">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="6866a-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6866a-115">-Confirm</span></span>
<span data-ttu-id="6866a-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6866a-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6866a-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6866a-117">-WhatIf</span></span>
<span data-ttu-id="6866a-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6866a-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6866a-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6866a-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6866a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6866a-120">-DefaultProfile</span></span>
<span data-ttu-id="6866a-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6866a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6866a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6866a-122">CommonParameters</span></span>
<span data-ttu-id="6866a-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6866a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6866a-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6866a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6866a-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6866a-125">INPUTS</span></span>

## <span data-ttu-id="6866a-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6866a-126">OUTPUTS</span></span>

### <span data-ttu-id="6866a-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="6866a-127">System.Object</span></span>

## <span data-ttu-id="6866a-128">Note</span><span class="sxs-lookup"><span data-stu-id="6866a-128">NOTES</span></span>

## <span data-ttu-id="6866a-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6866a-129">RELATED LINKS</span></span>

[<span data-ttu-id="6866a-130">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6866a-130">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="6866a-131">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6866a-131">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="6866a-132">Start-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6866a-132">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="6866a-133">Stop-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="6866a-133">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


