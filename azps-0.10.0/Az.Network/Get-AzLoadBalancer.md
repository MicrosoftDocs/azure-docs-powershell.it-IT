---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancer.md
ms.openlocfilehash: f5f0ce9768226c79210db3a38c5c09303e94a852
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860794"
---
# <span data-ttu-id="1b317-101">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1b317-101">Get-AzLoadBalancer</span></span>

## <span data-ttu-id="1b317-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1b317-102">SYNOPSIS</span></span>
<span data-ttu-id="1b317-103">Ottiene un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="1b317-103">Gets a load balancer.</span></span>

## <span data-ttu-id="1b317-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1b317-104">SYNTAX</span></span>

### <span data-ttu-id="1b317-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="1b317-105">NoExpand</span></span>
```
Get-AzLoadBalancer [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b317-106">Espandere</span><span class="sxs-lookup"><span data-stu-id="1b317-106">Expand</span></span>
```
Get-AzLoadBalancer -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b317-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b317-107">DESCRIPTION</span></span>
<span data-ttu-id="1b317-108">Il cmdlet **Get-AzLoadBalancer** ottiene uno o più gruppi di bilanciamento del carico di Azure contenuti in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1b317-108">The **Get-AzLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="1b317-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1b317-109">EXAMPLES</span></span>

### <span data-ttu-id="1b317-110">Esempio 1: ottenere un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="1b317-110">Example 1: Get a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="1b317-111">Questo comando ottiene il bilanciamento del carico denominato MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="1b317-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="1b317-112">Prima di poter eseguire questo cmdlet deve esistere un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="1b317-112">A load balancer must exist before you can run this cmdlet.</span></span>

## <span data-ttu-id="1b317-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1b317-113">PARAMETERS</span></span>

### <span data-ttu-id="1b317-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b317-114">-DefaultProfile</span></span>
<span data-ttu-id="1b317-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1b317-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b317-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="1b317-116">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b317-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="1b317-117">-Name</span></span>
```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b317-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b317-118">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b317-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b317-119">CommonParameters</span></span>
<span data-ttu-id="1b317-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b317-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b317-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b317-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b317-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1b317-122">INPUTS</span></span>

## <span data-ttu-id="1b317-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1b317-123">OUTPUTS</span></span>

### <span data-ttu-id="1b317-124">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1b317-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="1b317-125">Note</span><span class="sxs-lookup"><span data-stu-id="1b317-125">NOTES</span></span>

## <span data-ttu-id="1b317-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1b317-126">RELATED LINKS</span></span>

[<span data-ttu-id="1b317-127">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1b317-127">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="1b317-128">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1b317-128">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="1b317-129">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1b317-129">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


