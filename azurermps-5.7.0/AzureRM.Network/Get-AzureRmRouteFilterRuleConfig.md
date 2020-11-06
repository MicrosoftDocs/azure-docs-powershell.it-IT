---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: d5acd58d9b36e3a581ec025b06e256652a9c4eba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511104"
---
# <span data-ttu-id="28264-101">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="28264-101">Get-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="28264-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="28264-102">SYNOPSIS</span></span>
<span data-ttu-id="28264-103">{{Fill in Sinossi}}</span><span class="sxs-lookup"><span data-stu-id="28264-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28264-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28264-104">SYNTAX</span></span>

```
Get-AzureRmRouteFilterRuleConfig [-Name <String>] -RouteFilter <PSRouteFilter>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28264-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28264-105">DESCRIPTION</span></span>
<span data-ttu-id="28264-106">{{Fill nella descrizione}}</span><span class="sxs-lookup"><span data-stu-id="28264-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="28264-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28264-107">EXAMPLES</span></span>

### <span data-ttu-id="28264-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="28264-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="28264-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="28264-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="28264-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="28264-110">PARAMETERS</span></span>

### <span data-ttu-id="28264-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28264-111">-DefaultProfile</span></span>
<span data-ttu-id="28264-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="28264-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28264-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="28264-113">-Name</span></span>
<span data-ttu-id="28264-114">Nome della regola di filtro route</span><span class="sxs-lookup"><span data-stu-id="28264-114">The name of the route filter rule</span></span>

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

### <span data-ttu-id="28264-115">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="28264-115">-RouteFilter</span></span>
<span data-ttu-id="28264-116">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="28264-116">The RouteFilter</span></span>

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

### <span data-ttu-id="28264-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28264-117">CommonParameters</span></span>
<span data-ttu-id="28264-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28264-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28264-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28264-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28264-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="28264-120">INPUTS</span></span>

### <span data-ttu-id="28264-121">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="28264-121">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="28264-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28264-122">OUTPUTS</span></span>

### <span data-ttu-id="28264-123">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="28264-123">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="28264-124">Note</span><span class="sxs-lookup"><span data-stu-id="28264-124">NOTES</span></span>

## <span data-ttu-id="28264-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28264-125">RELATED LINKS</span></span>

