---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
ms.openlocfilehash: 5dc2b6a9650cdf4110858edf1b061f69adac48f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686380"
---
# <span data-ttu-id="f47ae-101">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f47ae-101">Set-AzureRmRouteFilter</span></span>

## <span data-ttu-id="f47ae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f47ae-102">SYNOPSIS</span></span>
<span data-ttu-id="f47ae-103">{{Fill in Sinossi}}</span><span class="sxs-lookup"><span data-stu-id="f47ae-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f47ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f47ae-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f47ae-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f47ae-105">DESCRIPTION</span></span>
<span data-ttu-id="f47ae-106">{{Fill nella descrizione}}</span><span class="sxs-lookup"><span data-stu-id="f47ae-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="f47ae-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f47ae-107">EXAMPLES</span></span>

### <span data-ttu-id="f47ae-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f47ae-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="f47ae-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="f47ae-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="f47ae-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f47ae-110">PARAMETERS</span></span>

### <span data-ttu-id="f47ae-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f47ae-111">-AsJob</span></span>
<span data-ttu-id="f47ae-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f47ae-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f47ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f47ae-113">-DefaultProfile</span></span>
<span data-ttu-id="f47ae-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f47ae-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f47ae-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f47ae-115">-Force</span></span>
<span data-ttu-id="f47ae-116">Non chiedere conferma se si vuole usare una risorsa per un sovrarito</span><span class="sxs-lookup"><span data-stu-id="f47ae-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="f47ae-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="f47ae-117">-RouteFilter</span></span>
<span data-ttu-id="f47ae-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="f47ae-118">The RouteFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f47ae-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f47ae-119">-Confirm</span></span>
<span data-ttu-id="f47ae-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f47ae-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f47ae-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f47ae-121">-WhatIf</span></span>
<span data-ttu-id="f47ae-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f47ae-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f47ae-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f47ae-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f47ae-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f47ae-124">CommonParameters</span></span>
<span data-ttu-id="f47ae-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f47ae-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f47ae-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f47ae-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f47ae-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f47ae-127">INPUTS</span></span>

### <span data-ttu-id="f47ae-128">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f47ae-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>
<span data-ttu-id="f47ae-129">Parametri: RouteFilter (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f47ae-129">Parameters: RouteFilter (ByValue)</span></span>

## <span data-ttu-id="f47ae-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f47ae-130">OUTPUTS</span></span>

### <span data-ttu-id="f47ae-131">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="f47ae-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="f47ae-132">Note</span><span class="sxs-lookup"><span data-stu-id="f47ae-132">NOTES</span></span>

## <span data-ttu-id="f47ae-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f47ae-133">RELATED LINKS</span></span>
