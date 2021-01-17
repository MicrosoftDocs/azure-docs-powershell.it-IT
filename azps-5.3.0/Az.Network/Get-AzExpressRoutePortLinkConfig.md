---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
ms.openlocfilehash: 197d18f5d7585f6ae7e865b1c2b0449d032b4238
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380169"
---
# <span data-ttu-id="b9061-101">Get-AzExpressRoutePortLinkConfig</span><span class="sxs-lookup"><span data-stu-id="b9061-101">Get-AzExpressRoutePortLinkConfig</span></span>

## <span data-ttu-id="b9061-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b9061-102">SYNOPSIS</span></span>
<span data-ttu-id="b9061-103">Ottiene una configurazione del collegamento ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="b9061-103">Gets an ExpressRoutePort link configuration.</span></span>

## <span data-ttu-id="b9061-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9061-104">SYNTAX</span></span>

### <span data-ttu-id="b9061-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b9061-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9061-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9061-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePortLinkConfig -ResourceId <String> -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9061-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9061-107">DESCRIPTION</span></span>
<span data-ttu-id="b9061-108">Il cmdlet **Get-AzExpressRoutePortLinkConfig** recupera la configurazione di un collegamento di un ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="b9061-108">The **Get-AzExpressRoutePortLinkConfig** cmdlet retrieves the configuration of a link of an ExpressRoutePort.</span></span>

## <span data-ttu-id="b9061-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9061-109">EXAMPLES</span></span>

### <span data-ttu-id="b9061-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b9061-110">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

<span data-ttu-id="b9061-111">Ottiene la configurazione Link1 di ExpressRoutePort $erport</span><span class="sxs-lookup"><span data-stu-id="b9061-111">Gets the Link1 configuration of ExpressRoutePort $erport</span></span>

### <span data-ttu-id="b9061-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b9061-112">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

<span data-ttu-id="b9061-113">Ottiene la configurazione del collegamento con ResourceId $id in ExpressRoutePort $erport</span><span class="sxs-lookup"><span data-stu-id="b9061-113">Gets the configuration of link with ResourceId $id in ExpressRoutePort $erport</span></span>

## <span data-ttu-id="b9061-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b9061-114">PARAMETERS</span></span>

### <span data-ttu-id="b9061-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9061-115">-DefaultProfile</span></span>
<span data-ttu-id="b9061-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b9061-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9061-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b9061-117">-ExpressRoutePort</span></span>
<span data-ttu-id="b9061-118">Il riferimento della risorsa ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="b9061-118">The reference of the ExpressRoutePort resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9061-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9061-119">-Name</span></span>
<span data-ttu-id="b9061-120">Nome del collegamento.</span><span class="sxs-lookup"><span data-stu-id="b9061-120">Name of the link.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9061-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9061-121">-ResourceId</span></span>
<span data-ttu-id="b9061-122">ResourceId del collegamento.</span><span class="sxs-lookup"><span data-stu-id="b9061-122">ResourceId of the link.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9061-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9061-123">CommonParameters</span></span>
<span data-ttu-id="b9061-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9061-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9061-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9061-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9061-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b9061-126">INPUTS</span></span>

### <span data-ttu-id="b9061-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b9061-127">System.String</span></span>

### <span data-ttu-id="b9061-128">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="b9061-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="b9061-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9061-129">OUTPUTS</span></span>

### <span data-ttu-id="b9061-130">Microsoft. Azure. Commands. Network. Models. PSExpressRouteLink</span><span class="sxs-lookup"><span data-stu-id="b9061-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span></span>

## <span data-ttu-id="b9061-131">Note</span><span class="sxs-lookup"><span data-stu-id="b9061-131">NOTES</span></span>

## <span data-ttu-id="b9061-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9061-132">RELATED LINKS</span></span>
