---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
ms.openlocfilehash: 1091a8433cd226982d3f2addf7e02b2414020fe4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520681"
---
# <span data-ttu-id="ced80-101">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ced80-101">Set-AzureRmRouteFilter</span></span>

## <span data-ttu-id="ced80-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ced80-102">SYNOPSIS</span></span>
<span data-ttu-id="ced80-103">{{Fill in Sinossi}}</span><span class="sxs-lookup"><span data-stu-id="ced80-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ced80-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ced80-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ced80-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ced80-105">DESCRIPTION</span></span>
<span data-ttu-id="ced80-106">{{Fill nella descrizione}}</span><span class="sxs-lookup"><span data-stu-id="ced80-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="ced80-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ced80-107">EXAMPLES</span></span>

### <span data-ttu-id="ced80-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ced80-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="ced80-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="ced80-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="ced80-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ced80-110">PARAMETERS</span></span>

### <span data-ttu-id="ced80-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ced80-111">-AsJob</span></span>
<span data-ttu-id="ced80-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ced80-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ced80-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ced80-113">-DefaultProfile</span></span>
<span data-ttu-id="ced80-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ced80-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ced80-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ced80-115">-Force</span></span>
<span data-ttu-id="ced80-116">Non chiedere conferma se si vuole usare una risorsa per un sovrarito</span><span class="sxs-lookup"><span data-stu-id="ced80-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="ced80-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="ced80-117">-RouteFilter</span></span>
<span data-ttu-id="ced80-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="ced80-118">The RouteFilter</span></span>

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

### <span data-ttu-id="ced80-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ced80-119">-Confirm</span></span>
<span data-ttu-id="ced80-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ced80-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ced80-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ced80-121">-WhatIf</span></span>
<span data-ttu-id="ced80-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ced80-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ced80-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ced80-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ced80-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ced80-124">CommonParameters</span></span>
<span data-ttu-id="ced80-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ced80-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ced80-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ced80-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ced80-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ced80-127">INPUTS</span></span>

### <span data-ttu-id="ced80-128">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ced80-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="ced80-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ced80-129">OUTPUTS</span></span>

### <span data-ttu-id="ced80-130">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ced80-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="ced80-131">Note</span><span class="sxs-lookup"><span data-stu-id="ced80-131">NOTES</span></span>

## <span data-ttu-id="ced80-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ced80-132">RELATED LINKS</span></span>
