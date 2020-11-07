---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: ecd5a8eafc70a88b4ebda17a83f2b40139f5463f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686377"
---
# <span data-ttu-id="4b3aa-101">Set-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4b3aa-101">Set-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="4b3aa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4b3aa-102">SYNOPSIS</span></span>
<span data-ttu-id="4b3aa-103">{{Fill in Sinossi}}</span><span class="sxs-lookup"><span data-stu-id="4b3aa-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b3aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4b3aa-104">SYNTAX</span></span>

```
Set-AzureRmServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b3aa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b3aa-105">DESCRIPTION</span></span>
<span data-ttu-id="4b3aa-106">Il cmdlet **set-AzureRmServiceEndpointPolicy** crea un criterio endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="4b3aa-106">The **Set-AzureRmServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="4b3aa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4b3aa-107">EXAMPLES</span></span>

### <span data-ttu-id="4b3aa-108">Esempio 1: imposta un criterio endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="4b3aa-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzureRmServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="4b3aa-109">Questo comando aggiorna un criterio endpoint del servizio denominato Policy1 definito dall'oggetto $serviceEndpointPolicy appartengono alla ResourceGroup "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="4b3aa-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="4b3aa-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4b3aa-110">PARAMETERS</span></span>

### <span data-ttu-id="4b3aa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b3aa-111">-DefaultProfile</span></span>
<span data-ttu-id="4b3aa-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4b3aa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b3aa-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4b3aa-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="4b3aa-114">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4b3aa-114">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="4b3aa-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b3aa-115">CommonParameters</span></span>
<span data-ttu-id="4b3aa-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b3aa-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4b3aa-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b3aa-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b3aa-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4b3aa-118">INPUTS</span></span>

### <span data-ttu-id="4b3aa-119">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4b3aa-119">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="4b3aa-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4b3aa-120">OUTPUTS</span></span>

### <span data-ttu-id="4b3aa-121">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4b3aa-121">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="4b3aa-122">Note</span><span class="sxs-lookup"><span data-stu-id="4b3aa-122">NOTES</span></span>

## <span data-ttu-id="4b3aa-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4b3aa-123">RELATED LINKS</span></span>
