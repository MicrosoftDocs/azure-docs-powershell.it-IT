---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortLinkConfig.md
ms.openlocfilehash: a8326afbeb6d71d54ec861eb3ec65868e7e230bb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956990"
---
# <span data-ttu-id="341de-101">Get-AzExpressRoutePortLinkConfig</span><span class="sxs-lookup"><span data-stu-id="341de-101">Get-AzExpressRoutePortLinkConfig</span></span>

## <span data-ttu-id="341de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="341de-102">SYNOPSIS</span></span>
<span data-ttu-id="341de-103">Ottiene una configurazione del collegamento ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="341de-103">Gets an ExpressRoutePort link configuration.</span></span>

## <span data-ttu-id="341de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="341de-104">SYNTAX</span></span>

### <span data-ttu-id="341de-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="341de-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="341de-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="341de-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePortLinkConfig -ResourceId <String> -ExpressRoutePort <PSExpressRoutePort>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="341de-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="341de-107">DESCRIPTION</span></span>
<span data-ttu-id="341de-108">Il cmdlet **Get-AzExpressRoutePortLinkConfig** recupera la configurazione di un collegamento di expressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="341de-108">The **Get-AzExpressRoutePortLinkConfig** cmdlet retrieves the configuration of a link of an ExpressRoutePort.</span></span>

## <span data-ttu-id="341de-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="341de-109">EXAMPLES</span></span>

### <span data-ttu-id="341de-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="341de-110">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

<span data-ttu-id="341de-111">Recupera la configurazione Link1 di ExpressRoutePort $erport</span><span class="sxs-lookup"><span data-stu-id="341de-111">Gets the Link1 configuration of ExpressRoutePort $erport</span></span>

### <span data-ttu-id="341de-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="341de-112">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

<span data-ttu-id="341de-113">Ottiene la configurazione del collegamento con resourceId $id in ExpressRoutePort $erport</span><span class="sxs-lookup"><span data-stu-id="341de-113">Gets the configuration of link with ResourceId $id in ExpressRoutePort $erport</span></span>

## <span data-ttu-id="341de-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="341de-114">PARAMETERS</span></span>

### <span data-ttu-id="341de-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="341de-115">-DefaultProfile</span></span>
<span data-ttu-id="341de-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="341de-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="341de-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="341de-117">-ExpressRoutePort</span></span>
<span data-ttu-id="341de-118">Riferimento della risorsa ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="341de-118">The reference of the ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="341de-119">-Name</span><span class="sxs-lookup"><span data-stu-id="341de-119">-Name</span></span>
<span data-ttu-id="341de-120">Nome del collegamento.</span><span class="sxs-lookup"><span data-stu-id="341de-120">Name of the link.</span></span>

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

### <span data-ttu-id="341de-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="341de-121">-ResourceId</span></span>
<span data-ttu-id="341de-122">ResourceId del collegamento.</span><span class="sxs-lookup"><span data-stu-id="341de-122">ResourceId of the link.</span></span>

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

### <span data-ttu-id="341de-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="341de-123">CommonParameters</span></span>
<span data-ttu-id="341de-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="341de-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="341de-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="341de-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="341de-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="341de-126">INPUTS</span></span>

### <span data-ttu-id="341de-127">System.String</span><span class="sxs-lookup"><span data-stu-id="341de-127">System.String</span></span>

### <span data-ttu-id="341de-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="341de-128">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="341de-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="341de-129">OUTPUTS</span></span>

### <span data-ttu-id="341de-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span><span class="sxs-lookup"><span data-stu-id="341de-130">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span></span>

## <span data-ttu-id="341de-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="341de-131">NOTES</span></span>

## <span data-ttu-id="341de-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="341de-132">RELATED LINKS</span></span>
