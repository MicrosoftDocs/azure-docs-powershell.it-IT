---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 600B621A-1311-4A05-9807-7B0E49D5A63C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/get-azurermschedulerjobcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: da1133895d062e3f49fae0bf6571c3bfeb72992c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687457"
---
# <span data-ttu-id="58e9e-101">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="58e9e-101">Get-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="58e9e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="58e9e-102">SYNOPSIS</span></span>
<span data-ttu-id="58e9e-103">Ottiene le raccolte processi.</span><span class="sxs-lookup"><span data-stu-id="58e9e-103">Gets job collections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58e9e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58e9e-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobCollection [-ResourceGroupName <String>] [-JobCollectionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58e9e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58e9e-105">DESCRIPTION</span></span>
<span data-ttu-id="58e9e-106">Il cmdlet **Get-AzureRmSchedulerJobCollection** ottiene le raccolte processi in Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="58e9e-106">The **Get-AzureRmSchedulerJobCollection** cmdlet gets job collections in Azure Scheduler.</span></span>

## <span data-ttu-id="58e9e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58e9e-107">EXAMPLES</span></span>

## <span data-ttu-id="58e9e-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="58e9e-108">PARAMETERS</span></span>

### <span data-ttu-id="58e9e-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58e9e-109">-DefaultProfile</span></span>
<span data-ttu-id="58e9e-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="58e9e-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58e9e-111">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="58e9e-111">-JobCollectionName</span></span>
<span data-ttu-id="58e9e-112">Specifica il nome di una raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="58e9e-112">Specifies the name of a job collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58e9e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58e9e-113">-ResourceGroupName</span></span>
<span data-ttu-id="58e9e-114">Specifica il gruppo di risorse da cui questo cmdlet ottiene le raccolte processi.</span><span class="sxs-lookup"><span data-stu-id="58e9e-114">Specifies resource group from which this cmdlet gets job collections.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58e9e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58e9e-115">CommonParameters</span></span>
<span data-ttu-id="58e9e-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58e9e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58e9e-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58e9e-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58e9e-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="58e9e-118">INPUTS</span></span>

### <span data-ttu-id="58e9e-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="58e9e-119">None</span></span>
<span data-ttu-id="58e9e-120">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="58e9e-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="58e9e-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58e9e-121">OUTPUTS</span></span>

### <span data-ttu-id="58e9e-122">System. Object</span><span class="sxs-lookup"><span data-stu-id="58e9e-122">System.Object</span></span>

## <span data-ttu-id="58e9e-123">Note</span><span class="sxs-lookup"><span data-stu-id="58e9e-123">NOTES</span></span>

## <span data-ttu-id="58e9e-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58e9e-124">RELATED LINKS</span></span>

[<span data-ttu-id="58e9e-125">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="58e9e-125">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="58e9e-126">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="58e9e-126">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="58e9e-127">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="58e9e-127">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="58e9e-128">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="58e9e-128">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="58e9e-129">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="58e9e-129">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


