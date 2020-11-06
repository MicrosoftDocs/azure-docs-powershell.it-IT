---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteportlinkconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortLinkConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortLinkConfig.md
ms.openlocfilehash: c758131685787ec8627f6e0cd3760e2ee42107c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521341"
---
# <span data-ttu-id="04e2c-101">Get-AzureRmExpressRoutePortLinkConfig</span><span class="sxs-lookup"><span data-stu-id="04e2c-101">Get-AzureRmExpressRoutePortLinkConfig</span></span>

## <span data-ttu-id="04e2c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="04e2c-102">SYNOPSIS</span></span>
<span data-ttu-id="04e2c-103">Ottiene una configurazione del collegamento ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="04e2c-103">Gets an ExpressRoutePort link configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04e2c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="04e2c-104">SYNTAX</span></span>

### <span data-ttu-id="04e2c-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="04e2c-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="04e2c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="04e2c-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort <PSExpressRoutePort> -ResourceId <String> 
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04e2c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04e2c-107">DESCRIPTION</span></span>
<span data-ttu-id="04e2c-108">Il cmdlet **Get-AzureRmExpressRoutePortLinkConfig** recupera la configurazione di un collegamento di un ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="04e2c-108">The **Get-AzureRmExpressRoutePortLinkConfig** cmdlet retrieves the configuration of a link of an ExpressRoutePort.</span></span>

## <span data-ttu-id="04e2c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="04e2c-109">EXAMPLES</span></span>

### <span data-ttu-id="04e2c-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="04e2c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort $erport -Name Link1
```

<span data-ttu-id="04e2c-111">Ottiene la configurazione Link1 di ExpressRoutePort $erport</span><span class="sxs-lookup"><span data-stu-id="04e2c-111">Gets the Link1 configuration of ExpressRoutePort $erport</span></span>

### <span data-ttu-id="04e2c-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="04e2c-112">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePortLinkConfig -ExpressRoutePort $erport -ResourceId $id
```

<span data-ttu-id="04e2c-113">Ottiene la configurazione del collegamento con ResourceId $id in ExpressRoutePort $erport</span><span class="sxs-lookup"><span data-stu-id="04e2c-113">Gets the configuration of link with ResourceId $id in ExpressRoutePort $erport</span></span>

## <span data-ttu-id="04e2c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="04e2c-114">PARAMETERS</span></span>

### <span data-ttu-id="04e2c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04e2c-115">-DefaultProfile</span></span>
<span data-ttu-id="04e2c-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="04e2c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04e2c-117">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="04e2c-117">-ExpressRoutePort</span></span>
<span data-ttu-id="04e2c-118">Il riferimento della risorsa ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="04e2c-118">The reference of the ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="04e2c-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="04e2c-119">-Name</span></span>
<span data-ttu-id="04e2c-120">Nome del collegamento.</span><span class="sxs-lookup"><span data-stu-id="04e2c-120">Name of the link.</span></span>

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

### <span data-ttu-id="04e2c-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04e2c-121">-ResourceId</span></span>
<span data-ttu-id="04e2c-122">ResourceId del collegamento.</span><span class="sxs-lookup"><span data-stu-id="04e2c-122">ResourceId of the link.</span></span>

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

### <span data-ttu-id="04e2c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04e2c-123">CommonParameters</span></span>
<span data-ttu-id="04e2c-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04e2c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04e2c-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04e2c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04e2c-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="04e2c-126">INPUTS</span></span>

### <span data-ttu-id="04e2c-127">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="04e2c-127">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="04e2c-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="04e2c-128">OUTPUTS</span></span>

### <span data-ttu-id="04e2c-129">Microsoft. Azure. Commands. Network. Models. PSExpressRouteLink</span><span class="sxs-lookup"><span data-stu-id="04e2c-129">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink</span></span>

## <span data-ttu-id="04e2c-130">Note</span><span class="sxs-lookup"><span data-stu-id="04e2c-130">NOTES</span></span>

## <span data-ttu-id="04e2c-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="04e2c-131">RELATED LINKS</span></span>
