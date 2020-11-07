---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutefilter
schema: 2.0.0
ms.openlocfilehash: 895819175f9fe4215d926d57c55307bbb4c75ab3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866832"
---
# <span data-ttu-id="7fd91-101">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7fd91-101">Set-AzureRmRouteFilter</span></span>

## <span data-ttu-id="7fd91-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7fd91-102">SYNOPSIS</span></span>
<span data-ttu-id="7fd91-103">{{Fill in Sinossi}}</span><span class="sxs-lookup"><span data-stu-id="7fd91-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fd91-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7fd91-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fd91-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7fd91-105">DESCRIPTION</span></span>
<span data-ttu-id="7fd91-106">{{Fill nella descrizione}}</span><span class="sxs-lookup"><span data-stu-id="7fd91-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="7fd91-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7fd91-107">EXAMPLES</span></span>

### <span data-ttu-id="7fd91-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7fd91-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="7fd91-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="7fd91-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="7fd91-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7fd91-110">PARAMETERS</span></span>

### <span data-ttu-id="7fd91-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7fd91-111">-AsJob</span></span>
<span data-ttu-id="7fd91-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7fd91-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd91-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fd91-113">-DefaultProfile</span></span>
<span data-ttu-id="7fd91-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7fd91-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fd91-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7fd91-115">-Force</span></span>
<span data-ttu-id="7fd91-116">Non chiedere conferma se si vuole usare una risorsa per un sovrarito</span><span class="sxs-lookup"><span data-stu-id="7fd91-116">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd91-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="7fd91-117">-RouteFilter</span></span>
<span data-ttu-id="7fd91-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="7fd91-118">The RouteFilter</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fd91-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7fd91-119">-Confirm</span></span>
<span data-ttu-id="7fd91-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7fd91-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd91-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fd91-121">-WhatIf</span></span>
<span data-ttu-id="7fd91-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7fd91-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7fd91-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7fd91-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd91-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fd91-124">CommonParameters</span></span>
<span data-ttu-id="7fd91-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fd91-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fd91-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fd91-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fd91-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7fd91-127">INPUTS</span></span>

### <span data-ttu-id="7fd91-128">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7fd91-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="7fd91-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7fd91-129">OUTPUTS</span></span>

### <span data-ttu-id="7fd91-130">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="7fd91-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="7fd91-131">Note</span><span class="sxs-lookup"><span data-stu-id="7fd91-131">NOTES</span></span>

## <span data-ttu-id="7fd91-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7fd91-132">RELATED LINKS</span></span>

