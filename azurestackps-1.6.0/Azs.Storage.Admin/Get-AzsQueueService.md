---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 62c174a3aec5034b230954922f6aab5078fe4bac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490970"
---
# <span data-ttu-id="c2375-101">Get-AzsQueueService</span><span class="sxs-lookup"><span data-stu-id="c2375-101">Get-AzsQueueService</span></span>

## <span data-ttu-id="c2375-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c2375-102">SYNOPSIS</span></span>
<span data-ttu-id="c2375-103">Restituisce il servizio code.</span><span class="sxs-lookup"><span data-stu-id="c2375-103">Returns the queue service.</span></span>

## <span data-ttu-id="c2375-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2375-104">SYNTAX</span></span>

```
Get-AzsQueueService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="c2375-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2375-105">DESCRIPTION</span></span>
<span data-ttu-id="c2375-106">Restituisce il servizio code.</span><span class="sxs-lookup"><span data-stu-id="c2375-106">Returns the queue service.</span></span>

## <span data-ttu-id="c2375-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2375-107">EXAMPLES</span></span>

### <span data-ttu-id="c2375-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c2375-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsQueueService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="c2375-109">Ottenere il servizio code.</span><span class="sxs-lookup"><span data-stu-id="c2375-109">Get the queue service.</span></span>

## <span data-ttu-id="c2375-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c2375-110">PARAMETERS</span></span>

### <span data-ttu-id="c2375-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="c2375-111">-FarmName</span></span>
<span data-ttu-id="c2375-112">ID farm.</span><span class="sxs-lookup"><span data-stu-id="c2375-112">Farm Id.</span></span>

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

### <span data-ttu-id="c2375-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2375-113">-ResourceGroupName</span></span>
<span data-ttu-id="c2375-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c2375-114">Resource group name.</span></span>

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

### <span data-ttu-id="c2375-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2375-115">CommonParameters</span></span>
<span data-ttu-id="c2375-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2375-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2375-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2375-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2375-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c2375-118">INPUTS</span></span>

## <span data-ttu-id="c2375-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2375-119">OUTPUTS</span></span>

### <span data-ttu-id="c2375-120">Microsoft. AzureStack. Management. storage. admin. Models. QueueService</span><span class="sxs-lookup"><span data-stu-id="c2375-120">Microsoft.AzureStack.Management.Storage.Admin.Models.QueueService</span></span>

## <span data-ttu-id="c2375-121">Note</span><span class="sxs-lookup"><span data-stu-id="c2375-121">NOTES</span></span>

## <span data-ttu-id="c2375-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2375-122">RELATED LINKS</span></span>
