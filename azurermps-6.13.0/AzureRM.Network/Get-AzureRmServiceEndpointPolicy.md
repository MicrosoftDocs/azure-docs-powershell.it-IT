---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: 989b6aa91c0dabec1b72425f214c4097df374041
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511707"
---
# <span data-ttu-id="5d9eb-101">Get-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5d9eb-101">Get-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="5d9eb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5d9eb-102">SYNOPSIS</span></span>
<span data-ttu-id="5d9eb-103">{{Fill in Sinossi}}</span><span class="sxs-lookup"><span data-stu-id="5d9eb-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d9eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5d9eb-104">SYNTAX</span></span>

```
Get-AzureRmServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d9eb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5d9eb-105">DESCRIPTION</span></span>
<span data-ttu-id="5d9eb-106">Il cmdlet **Get-AzureRmServiceEndpointPolicy** ottiene un criterio endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="5d9eb-106">The **Get-AzureRmServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="5d9eb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5d9eb-107">EXAMPLES</span></span>

### <span data-ttu-id="5d9eb-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5d9eb-108">Example 1</span></span>
```
$policy = Get-AzureRmServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5d9eb-109">Questo comando ottiene il criterio endpoint del servizio denominato ServiceEndpointPolicy1 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $policy.</span><span class="sxs-lookup"><span data-stu-id="5d9eb-109">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="5d9eb-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5d9eb-110">Example 2</span></span>
```
$policyList = Get-AzureRmServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5d9eb-111">Questo comando consente di ottenere un elenco di tutti i criteri endpoint del servizio nel gruppo di risorse denominato ResourceGroup01 e di archiviarlo nella variabile $policyList.</span><span class="sxs-lookup"><span data-stu-id="5d9eb-111">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

## <span data-ttu-id="5d9eb-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5d9eb-112">PARAMETERS</span></span>

### <span data-ttu-id="5d9eb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d9eb-113">-DefaultProfile</span></span>
<span data-ttu-id="5d9eb-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5d9eb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d9eb-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="5d9eb-115">-Name</span></span>
<span data-ttu-id="5d9eb-116">Nome del criterio endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="5d9eb-116">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d9eb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d9eb-117">-ResourceGroupName</span></span>
<span data-ttu-id="5d9eb-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5d9eb-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d9eb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d9eb-119">CommonParameters</span></span>
<span data-ttu-id="5d9eb-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d9eb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5d9eb-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d9eb-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d9eb-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5d9eb-122">INPUTS</span></span>

### <span data-ttu-id="5d9eb-123">System. String</span><span class="sxs-lookup"><span data-stu-id="5d9eb-123">System.String</span></span>


## <span data-ttu-id="5d9eb-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5d9eb-124">OUTPUTS</span></span>

### <span data-ttu-id="5d9eb-125">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5d9eb-125">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="5d9eb-126">Note</span><span class="sxs-lookup"><span data-stu-id="5d9eb-126">NOTES</span></span>

## <span data-ttu-id="5d9eb-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5d9eb-127">RELATED LINKS</span></span>
