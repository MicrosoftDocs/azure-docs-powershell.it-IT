---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 3d406bf0dffb0ee250e1494fc05727d0a4c983ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520915"
---
# <span data-ttu-id="76551-101">Remove-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="76551-101">Remove-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="76551-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="76551-102">SYNOPSIS</span></span>
<span data-ttu-id="76551-103">{{Fill in Sinossi}}</span><span class="sxs-lookup"><span data-stu-id="76551-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76551-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="76551-104">SYNTAX</span></span>

```
Remove-AzureRmServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76551-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76551-105">DESCRIPTION</span></span>
<span data-ttu-id="76551-106">Il cmdlet **Remove-AzureRmServiceEndpointPolicy** rimuove un criterio endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="76551-106">The **Remove-AzureRmServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="76551-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="76551-107">EXAMPLES</span></span>

### <span data-ttu-id="76551-108">Esempio 1: rimuove un criterio endpoint di servizio tramite Name</span><span class="sxs-lookup"><span data-stu-id="76551-108">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzureRmServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="76551-109">Questo comando rimuove un criterio endpoint servizio con nome PolicyDef1</span><span class="sxs-lookup"><span data-stu-id="76551-109">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="76551-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="76551-110">PARAMETERS</span></span>

### <span data-ttu-id="76551-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76551-111">-DefaultProfile</span></span>
<span data-ttu-id="76551-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="76551-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76551-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="76551-113">-Name</span></span>
<span data-ttu-id="76551-114">Nome della definizione dell'endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="76551-114">The name of the service endpoint definition</span></span>

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

### <span data-ttu-id="76551-115">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="76551-115">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="76551-116">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="76551-116">The ServiceEndpointPolicy</span></span>

```yaml
Type: PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76551-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76551-117">CommonParameters</span></span>
<span data-ttu-id="76551-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76551-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="76551-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76551-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76551-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="76551-120">INPUTS</span></span>

### <span data-ttu-id="76551-121">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="76551-121">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="76551-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="76551-122">OUTPUTS</span></span>

### <span data-ttu-id="76551-123">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="76551-123">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="76551-124">Note</span><span class="sxs-lookup"><span data-stu-id="76551-124">NOTES</span></span>

## <span data-ttu-id="76551-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="76551-125">RELATED LINKS</span></span>
