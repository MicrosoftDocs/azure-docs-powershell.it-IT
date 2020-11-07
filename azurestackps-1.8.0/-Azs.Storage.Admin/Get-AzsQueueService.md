---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 62c174a3aec5034b230954922f6aab5078fe4bac
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93859430"
---
# <span data-ttu-id="36b88-101">Get-AzsQueueService</span><span class="sxs-lookup"><span data-stu-id="36b88-101">Get-AzsQueueService</span></span>

## <span data-ttu-id="36b88-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="36b88-102">SYNOPSIS</span></span>
<span data-ttu-id="36b88-103">Restituisce il servizio code.</span><span class="sxs-lookup"><span data-stu-id="36b88-103">Returns the queue service.</span></span>

## <span data-ttu-id="36b88-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36b88-104">SYNTAX</span></span>

```
Get-AzsQueueService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="36b88-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36b88-105">DESCRIPTION</span></span>
<span data-ttu-id="36b88-106">Restituisce il servizio code.</span><span class="sxs-lookup"><span data-stu-id="36b88-106">Returns the queue service.</span></span>

## <span data-ttu-id="36b88-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36b88-107">EXAMPLES</span></span>

### <span data-ttu-id="36b88-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="36b88-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsQueueService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="36b88-109">Ottenere il servizio code.</span><span class="sxs-lookup"><span data-stu-id="36b88-109">Get the queue service.</span></span>

## <span data-ttu-id="36b88-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="36b88-110">PARAMETERS</span></span>

### <span data-ttu-id="36b88-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="36b88-111">-FarmName</span></span>
<span data-ttu-id="36b88-112">ID farm.</span><span class="sxs-lookup"><span data-stu-id="36b88-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b88-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36b88-113">-ResourceGroupName</span></span>
<span data-ttu-id="36b88-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="36b88-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b88-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36b88-115">CommonParameters</span></span>
<span data-ttu-id="36b88-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36b88-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36b88-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36b88-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36b88-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="36b88-118">INPUTS</span></span>

## <span data-ttu-id="36b88-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36b88-119">OUTPUTS</span></span>

### <span data-ttu-id="36b88-120">Microsoft. AzureStack. Management. storage. admin. Models. QueueService</span><span class="sxs-lookup"><span data-stu-id="36b88-120">Microsoft.AzureStack.Management.Storage.Admin.Models.QueueService</span></span>

## <span data-ttu-id="36b88-121">Note</span><span class="sxs-lookup"><span data-stu-id="36b88-121">NOTES</span></span>

## <span data-ttu-id="36b88-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36b88-122">RELATED LINKS</span></span>

