---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancer.md
ms.openlocfilehash: 764d26c2b0b95b74277fc74dab03fe55d12261f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519564"
---
# <span data-ttu-id="8b200-101">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8b200-101">Get-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="8b200-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8b200-102">SYNOPSIS</span></span>
<span data-ttu-id="8b200-103">Ottiene un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="8b200-103">Gets a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b200-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8b200-104">SYNTAX</span></span>

### <span data-ttu-id="8b200-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="8b200-105">NoExpand</span></span>
```
Get-AzureRmLoadBalancer [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b200-106">Espandere</span><span class="sxs-lookup"><span data-stu-id="8b200-106">Expand</span></span>
```
Get-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b200-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b200-107">DESCRIPTION</span></span>
<span data-ttu-id="8b200-108">Il cmdlet **Get-AzureRmLoadBalancer** ottiene uno o più gruppi di bilanciamento del carico di Azure contenuti in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8b200-108">The **Get-AzureRmLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="8b200-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8b200-109">EXAMPLES</span></span>

### <span data-ttu-id="8b200-110">Esempio 1: ottenere un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="8b200-110">Example 1: Get a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="8b200-111">Questo comando ottiene il bilanciamento del carico denominato MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="8b200-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="8b200-112">Prima di poter eseguire questo cmdlet deve esistere un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="8b200-112">A load balancer must exist before you can run this cmdlet.</span></span>

## <span data-ttu-id="8b200-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8b200-113">PARAMETERS</span></span>

### <span data-ttu-id="8b200-114">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="8b200-114">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b200-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="8b200-115">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b200-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b200-116">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b200-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b200-117">-DefaultProfile</span></span>
<span data-ttu-id="8b200-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8b200-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b200-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b200-119">CommonParameters</span></span>
<span data-ttu-id="8b200-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b200-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b200-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b200-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b200-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8b200-122">INPUTS</span></span>

## <span data-ttu-id="8b200-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8b200-123">OUTPUTS</span></span>

### <span data-ttu-id="8b200-124">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8b200-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="8b200-125">Note</span><span class="sxs-lookup"><span data-stu-id="8b200-125">NOTES</span></span>

## <span data-ttu-id="8b200-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8b200-126">RELATED LINKS</span></span>

[<span data-ttu-id="8b200-127">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8b200-127">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="8b200-128">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8b200-128">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

[<span data-ttu-id="8b200-129">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="8b200-129">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


