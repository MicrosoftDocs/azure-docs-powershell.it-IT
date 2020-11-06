---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 600B621A-1311-4A05-9807-7B0E49D5A63C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Get-AzureRmSchedulerJobCollection.md
ms.openlocfilehash: a75eafd57ff7351aa1858114da1cdc7f44b9875c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521530"
---
# <span data-ttu-id="2142c-101">Get-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="2142c-101">Get-AzureRmSchedulerJobCollection</span></span>

## <span data-ttu-id="2142c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2142c-102">SYNOPSIS</span></span>
<span data-ttu-id="2142c-103">Ottiene le raccolte processi.</span><span class="sxs-lookup"><span data-stu-id="2142c-103">Gets job collections.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2142c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2142c-104">SYNTAX</span></span>

```
Get-AzureRmSchedulerJobCollection [-ResourceGroupName <String>] [-JobCollectionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2142c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2142c-105">DESCRIPTION</span></span>
<span data-ttu-id="2142c-106">Il cmdlet **Get-AzureRmSchedulerJobCollection** ottiene le raccolte processi in Azure Scheduler.</span><span class="sxs-lookup"><span data-stu-id="2142c-106">The **Get-AzureRmSchedulerJobCollection** cmdlet gets job collections in Azure Scheduler.</span></span>

## <span data-ttu-id="2142c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2142c-107">EXAMPLES</span></span>

## <span data-ttu-id="2142c-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2142c-108">PARAMETERS</span></span>

### <span data-ttu-id="2142c-109">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="2142c-109">-JobCollectionName</span></span>
<span data-ttu-id="2142c-110">Specifica il nome di una raccolta processi.</span><span class="sxs-lookup"><span data-stu-id="2142c-110">Specifies the name of a job collection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2142c-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2142c-111">-ResourceGroupName</span></span>
<span data-ttu-id="2142c-112">Specifica il gruppo di risorse da cui questo cmdlet ottiene le raccolte processi.</span><span class="sxs-lookup"><span data-stu-id="2142c-112">Specifies resource group from which this cmdlet gets job collections.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2142c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2142c-113">-DefaultProfile</span></span>
<span data-ttu-id="2142c-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2142c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2142c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2142c-115">CommonParameters</span></span>
<span data-ttu-id="2142c-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2142c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2142c-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2142c-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2142c-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2142c-118">INPUTS</span></span>

## <span data-ttu-id="2142c-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2142c-119">OUTPUTS</span></span>

### <span data-ttu-id="2142c-120">System. Object</span><span class="sxs-lookup"><span data-stu-id="2142c-120">System.Object</span></span>

## <span data-ttu-id="2142c-121">Note</span><span class="sxs-lookup"><span data-stu-id="2142c-121">NOTES</span></span>

## <span data-ttu-id="2142c-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2142c-122">RELATED LINKS</span></span>

[<span data-ttu-id="2142c-123">Disable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="2142c-123">Disable-AzureRmSchedulerJobCollection</span></span>](./Disable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="2142c-124">Enable-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="2142c-124">Enable-AzureRmSchedulerJobCollection</span></span>](./Enable-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="2142c-125">New-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="2142c-125">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="2142c-126">Remove-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="2142c-126">Remove-AzureRmSchedulerJobCollection</span></span>](./Remove-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="2142c-127">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="2142c-127">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)


