---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: EE41BE86-37D4-4A2B-9007-D019CD62BA9D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 9904699d95429e029f330e5c3ca3e5957eb4c35e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685645"
---
# <span data-ttu-id="35f08-101">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="35f08-101">Remove-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="35f08-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="35f08-102">SYNOPSIS</span></span>
<span data-ttu-id="35f08-103">Elimina un output da un processo di analisi del flusso.</span><span class="sxs-lookup"><span data-stu-id="35f08-103">Deletes an output from a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35f08-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35f08-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsOutput [-JobName] <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35f08-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35f08-105">DESCRIPTION</span></span>
<span data-ttu-id="35f08-106">Il cmdlet **Remove-AzureRmStreamAnalyticsOutput** Elimina in modo asincrono un output da un processo di analisi del flusso in Azure.</span><span class="sxs-lookup"><span data-stu-id="35f08-106">The **Remove-AzureRmStreamAnalyticsOutput** cmdlet asynchronously deletes an output from a Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="35f08-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35f08-107">EXAMPLES</span></span>

### <span data-ttu-id="35f08-108">ESEMPIO 1: rimuovere un output da un processo</span><span class="sxs-lookup"><span data-stu-id="35f08-108">EXAMPLE 1: Remove an output from a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="35f08-109">Questo comando rimuove l'output di output in Job StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="35f08-109">This command removes the output Output in the job StreamingJob.</span></span>

## <span data-ttu-id="35f08-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="35f08-110">PARAMETERS</span></span>

### <span data-ttu-id="35f08-111">-JobName</span><span class="sxs-lookup"><span data-stu-id="35f08-111">-JobName</span></span>
<span data-ttu-id="35f08-112">Specifica il nome del processo di analisi di Azure stream a cui appartiene l'output di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="35f08-112">Specifies the name of the Azure Stream Analytics job to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="35f08-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="35f08-113">-Name</span></span>
<span data-ttu-id="35f08-114">Specifica il nome dell'output di analisi di Azure Stream da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="35f08-114">Specifies the name of the Azure Stream Analytics output to remove.</span></span>

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

### <span data-ttu-id="35f08-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35f08-115">-ResourceGroupName</span></span>
<span data-ttu-id="35f08-116">Specifica il nome del gruppo di risorse a cui appartiene l'output di analisi di Azure Stream.</span><span class="sxs-lookup"><span data-stu-id="35f08-116">Specifies the name of the resource group to which the Azure Stream Analytics output belongs.</span></span>

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

### <span data-ttu-id="35f08-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="35f08-117">-Confirm</span></span>
<span data-ttu-id="35f08-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35f08-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35f08-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35f08-119">-WhatIf</span></span>
<span data-ttu-id="35f08-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35f08-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35f08-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35f08-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35f08-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35f08-122">-DefaultProfile</span></span>
<span data-ttu-id="35f08-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="35f08-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35f08-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35f08-124">CommonParameters</span></span>
<span data-ttu-id="35f08-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35f08-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35f08-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35f08-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35f08-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="35f08-127">INPUTS</span></span>

## <span data-ttu-id="35f08-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35f08-128">OUTPUTS</span></span>

### <span data-ttu-id="35f08-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="35f08-129">System.Object</span></span>

## <span data-ttu-id="35f08-130">Note</span><span class="sxs-lookup"><span data-stu-id="35f08-130">NOTES</span></span>

## <span data-ttu-id="35f08-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35f08-131">RELATED LINKS</span></span>

[<span data-ttu-id="35f08-132">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="35f08-132">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="35f08-133">New-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="35f08-133">New-AzureRmStreamAnalyticsOutput</span></span>](./New-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="35f08-134">Test-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="35f08-134">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


