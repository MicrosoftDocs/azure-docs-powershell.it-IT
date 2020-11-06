---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F6D8710D-1D42-493C-B7F1-EDA35FCCDC23
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjobhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobHistory.md
ms.openlocfilehash: 5bf5745270db8cea076ccac9cff2d4e9b7a4bc06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520845"
---
# <span data-ttu-id="0976c-101">Get-AzureRmSchedulerJobHistory</span><span class="sxs-lookup"><span data-stu-id="0976c-101">Get-AzureRmSchedulerJobHistory</span></span>

## <span data-ttu-id="0976c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0976c-102">SYNOPSIS</span></span>
<span data-ttu-id="0976c-103">Ottiene la cronologia processi.</span><span class="sxs-lookup"><span data-stu-id="0976c-103">Gets job history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0976c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0976c-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobHistory -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 [-JobExecutionStatus <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0976c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0976c-105">DESCRIPTION</span></span>
<span data-ttu-id="0976c-106">Il cmdlet **Get-AzureRmSchedulerJobHistory** ottiene la cronologia per un processo di pianificazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="0976c-106">The **Get-AzureRmSchedulerJobHistory** cmdlet gets history for an Azure Scheduler job.</span></span>

## <span data-ttu-id="0976c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0976c-107">EXAMPLES</span></span>

## <span data-ttu-id="0976c-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0976c-108">PARAMETERS</span></span>

### <span data-ttu-id="0976c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0976c-109">-DefaultProfile</span></span>
<span data-ttu-id="0976c-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0976c-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0976c-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="0976c-111">-JobCollectionName</span></span>
<span data-ttu-id="0976c-112">Specifica il nome di una raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="0976c-112">Specifies the name of a job collection.</span></span>

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

### <span data-ttu-id="0976c-113">-JobExecutionStatus</span><span class="sxs-lookup"><span data-stu-id="0976c-113">-JobExecutionStatus</span></span>
<span data-ttu-id="0976c-114">Specifica lo stato di un processo.</span><span class="sxs-lookup"><span data-stu-id="0976c-114">Specifies the status of a job.</span></span>
<span data-ttu-id="0976c-115">Questo cmdlet consente di ottenere la cronologia corrispondente allo stato specificato.</span><span class="sxs-lookup"><span data-stu-id="0976c-115">This cmdlet gets history that matches the status that you specify.</span></span>
<span data-ttu-id="0976c-116">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0976c-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0976c-117">Completato</span><span class="sxs-lookup"><span data-stu-id="0976c-117">Completed</span></span> 
- <span data-ttu-id="0976c-118">Fallito</span><span class="sxs-lookup"><span data-stu-id="0976c-118">Failed</span></span> 
- <span data-ttu-id="0976c-119">Posticipato</span><span class="sxs-lookup"><span data-stu-id="0976c-119">Postponed</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Completed, Failed, Postponed

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0976c-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="0976c-120">-JobName</span></span>
<span data-ttu-id="0976c-121">Specifica il nome di un processo per cui questo cmdlet ottiene la cronologia.</span><span class="sxs-lookup"><span data-stu-id="0976c-121">Specifies the name of a job for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="0976c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0976c-122">-ResourceGroupName</span></span>
<span data-ttu-id="0976c-123">Specifica il gruppo di risorse a cui appartiene il processo.</span><span class="sxs-lookup"><span data-stu-id="0976c-123">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="0976c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0976c-124">CommonParameters</span></span>
<span data-ttu-id="0976c-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0976c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0976c-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0976c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0976c-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0976c-127">INPUTS</span></span>

### <span data-ttu-id="0976c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0976c-128">System.String</span></span>

## <span data-ttu-id="0976c-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0976c-129">OUTPUTS</span></span>

### <span data-ttu-id="0976c-130">Microsoft. Azure. Commands. Scheduler. Models. PSJobHistory</span><span class="sxs-lookup"><span data-stu-id="0976c-130">Microsoft.Azure.Commands.Scheduler.Models.PSJobHistory</span></span>

## <span data-ttu-id="0976c-131">Note</span><span class="sxs-lookup"><span data-stu-id="0976c-131">NOTES</span></span>

## <span data-ttu-id="0976c-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0976c-132">RELATED LINKS</span></span>

[<span data-ttu-id="0976c-133">Get-AzureRmSchedulerJob</span><span class="sxs-lookup"><span data-stu-id="0976c-133">Get-AzureRmSchedulerJob</span></span>](./Get-AzureRmSchedulerJob.md)


