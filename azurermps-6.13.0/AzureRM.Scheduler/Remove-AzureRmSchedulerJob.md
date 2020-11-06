---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 774699A8-8916-4F2A-973E-97E5E487D42E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/remove-azurermschedulerjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Remove-AzureRmSchedulerJob.md
ms.openlocfilehash: 6a15f51290efec856494737881693c3d1fae0620
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511471"
---
# <span data-ttu-id="1dfa5-101">Remove-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="1dfa5-101">Remove-AzureRmSchedulerJob</span></span>

## <span data-ttu-id="1dfa5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1dfa5-102">SYNOPSIS</span></span>
<span data-ttu-id="1dfa5-103">Rimuove un processo di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="1dfa5-103">Removes a Scheduler job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1dfa5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1dfa5-104">SYNTAX</span></span>

```
Remove-AzureRmSchedulerJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dfa5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1dfa5-105">DESCRIPTION</span></span>
<span data-ttu-id="1dfa5-106">Il cmdlet **Remove-AzureRmSchedulerJob** rimuove un processo di pianificazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1dfa5-106">The **Remove-AzureRmSchedulerJob** cmdlet removes an Azure Scheduler job.</span></span>

## <span data-ttu-id="1dfa5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1dfa5-107">EXAMPLES</span></span>

## <span data-ttu-id="1dfa5-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1dfa5-108">PARAMETERS</span></span>

### <span data-ttu-id="1dfa5-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dfa5-109">-DefaultProfile</span></span>
<span data-ttu-id="1dfa5-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1dfa5-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dfa5-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="1dfa5-111">-JobCollectionName</span></span>
<span data-ttu-id="1dfa5-112">Specifica il nome di una raccolta processi contenente il processo da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="1dfa5-112">Specifies the name of a job collection that contains the job to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dfa5-113">-JobName</span><span class="sxs-lookup"><span data-stu-id="1dfa5-113">-JobName</span></span>
<span data-ttu-id="1dfa5-114">Specifica il nome di un processo da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="1dfa5-114">Specifies the name of a job to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dfa5-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1dfa5-115">-PassThru</span></span>
<span data-ttu-id="1dfa5-116">Indica che questo cmdlet restituisce il valore Success per Success.</span><span class="sxs-lookup"><span data-stu-id="1dfa5-116">Indicates that this cmdlet returns a value of Success on success.</span></span>
<span data-ttu-id="1dfa5-117">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="1dfa5-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dfa5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dfa5-118">-ResourceGroupName</span></span>
<span data-ttu-id="1dfa5-119">Specifica il gruppo di risorse del processo da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="1dfa5-119">Specifies the resource group of the job to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dfa5-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1dfa5-120">-Confirm</span></span>
<span data-ttu-id="1dfa5-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dfa5-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dfa5-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dfa5-122">-WhatIf</span></span>
<span data-ttu-id="1dfa5-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1dfa5-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dfa5-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1dfa5-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dfa5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dfa5-125">CommonParameters</span></span>
<span data-ttu-id="1dfa5-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dfa5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dfa5-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dfa5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dfa5-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1dfa5-128">INPUTS</span></span>

### <span data-ttu-id="1dfa5-129">System. String</span><span class="sxs-lookup"><span data-stu-id="1dfa5-129">System.String</span></span>

## <span data-ttu-id="1dfa5-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1dfa5-130">OUTPUTS</span></span>

### <span data-ttu-id="1dfa5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1dfa5-131">System.String</span></span>

## <span data-ttu-id="1dfa5-132">Note</span><span class="sxs-lookup"><span data-stu-id="1dfa5-132">NOTES</span></span>

## <span data-ttu-id="1dfa5-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1dfa5-133">RELATED LINKS</span></span>

[<span data-ttu-id="1dfa5-134">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="1dfa5-134">Get-AzureRmSchedulerJob</span></span>](./Get-AzureRmSchedulerJob.md)


