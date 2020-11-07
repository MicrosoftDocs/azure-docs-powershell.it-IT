---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8756DA1-7BB9-4CD5-9D81-E11FF7A26125
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLocalNetworkGateway.md
ms.openlocfilehash: 88c17626da87608a1086331289cb99f8e7668e5a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860761"
---
# <span data-ttu-id="f7a3d-101">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f7a3d-101">Get-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="f7a3d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f7a3d-102">SYNOPSIS</span></span>
<span data-ttu-id="f7a3d-103">Ottiene un gateway di rete locale</span><span class="sxs-lookup"><span data-stu-id="f7a3d-103">Gets a Local Network Gateway</span></span>

## <span data-ttu-id="f7a3d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f7a3d-104">SYNTAX</span></span>

```
Get-AzLocalNetworkGateway [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7a3d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7a3d-105">DESCRIPTION</span></span>
<span data-ttu-id="f7a3d-106">Il gateway di rete locale è l'oggetto che rappresenta il dispositivo VPN in locale.</span><span class="sxs-lookup"><span data-stu-id="f7a3d-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="f7a3d-107">Il cmdlet **Get-AzLocalNetworkGateway** restituisce l'oggetto che rappresenta il Gateway on-Prem in base al nome e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f7a3d-107">The **Get-AzLocalNetworkGateway** cmdlet returns the object representing your on-prem gateway based on Name and Resource Group Name.</span></span>

## <span data-ttu-id="f7a3d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f7a3d-108">EXAMPLES</span></span>

### <span data-ttu-id="f7a3d-109">1: ottenere un gateway di rete locale</span><span class="sxs-lookup"><span data-stu-id="f7a3d-109">1: Get a Local Network Gateway</span></span>
```
Get-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
```

<span data-ttu-id="f7a3d-110">Restituisce l'oggetto del gateway di rete locale con il nome "myLocalGW" nel gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="f7a3d-110">Returns the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG"</span></span>

## <span data-ttu-id="f7a3d-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f7a3d-111">PARAMETERS</span></span>

### <span data-ttu-id="f7a3d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7a3d-112">-DefaultProfile</span></span>
<span data-ttu-id="f7a3d-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f7a3d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7a3d-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="f7a3d-114">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7a3d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7a3d-115">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7a3d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7a3d-116">CommonParameters</span></span>
<span data-ttu-id="f7a3d-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7a3d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7a3d-118">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7a3d-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7a3d-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f7a3d-119">INPUTS</span></span>

## <span data-ttu-id="f7a3d-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f7a3d-120">OUTPUTS</span></span>

### <span data-ttu-id="f7a3d-121">Microsoft. Azure. Commands. Network. Models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f7a3d-121">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="f7a3d-122">Note</span><span class="sxs-lookup"><span data-stu-id="f7a3d-122">NOTES</span></span>

## <span data-ttu-id="f7a3d-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f7a3d-123">RELATED LINKS</span></span>

