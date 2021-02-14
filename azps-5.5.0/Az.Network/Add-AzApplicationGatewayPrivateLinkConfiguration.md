---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 2083dd00c5163a67492ff9973fdf7399d67d7cb6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189983"
---
# <span data-ttu-id="c05c1-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="c05c1-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="c05c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c05c1-102">SYNOPSIS</span></span>
<span data-ttu-id="c05c1-103">Aggiunge una configurazione di collegamento privato a un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="c05c1-103">Adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="c05c1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c05c1-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c05c1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c05c1-105">DESCRIPTION</span></span>
<span data-ttu-id="c05c1-106">Il cmdlet **Add-AzApplicationGatewayPrivateLinkConfiguration** aggiunge una configurazione di collegamento privato a un gateway di applicazione.</span><span class="sxs-lookup"><span data-stu-id="c05c1-106">The **Add-AzApplicationGatewayPrivateLinkConfiguration** cmdlet adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="c05c1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c05c1-107">EXAMPLES</span></span>

### <span data-ttu-id="c05c1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c05c1-108">Example 1</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $PrivateLinkIpConfiguration
```

<span data-ttu-id="c05c1-109">Il primo comando crea una configurazione privataLinkIpConfiguration e la archivia nella $PrivateLinkIpConfiguration variabile.</span><span class="sxs-lookup"><span data-stu-id="c05c1-109">The first command creates a privateLinkIpConfiguration and stores it in the $PrivateLinkIpConfiguration variable.</span></span>
<span data-ttu-id="c05c1-110">Il secondo comando recupera il gateway applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw locale.</span><span class="sxs-lookup"><span data-stu-id="c05c1-110">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c05c1-111">Il terzo comando aggiunge la configurazione del collegamento privato denominata privateLinkConfig01 per il gateway in $AppGw</span><span class="sxs-lookup"><span data-stu-id="c05c1-111">The third command adds the private link configuration named privateLinkConfig01, for the gateway in $AppGw</span></span>

## <span data-ttu-id="c05c1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c05c1-112">PARAMETERS</span></span>

### <span data-ttu-id="c05c1-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c05c1-113">-ApplicationGateway</span></span>
<span data-ttu-id="c05c1-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c05c1-114">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c05c1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c05c1-115">-DefaultProfile</span></span>
<span data-ttu-id="c05c1-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c05c1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c05c1-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="c05c1-117">-IpConfiguration</span></span>
<span data-ttu-id="c05c1-118">Elenco di ipConfiguration</span><span class="sxs-lookup"><span data-stu-id="c05c1-118">The list of ipConfiguration</span></span>

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c05c1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c05c1-119">-Name</span></span>
<span data-ttu-id="c05c1-120">Nome della configurazione privateLink</span><span class="sxs-lookup"><span data-stu-id="c05c1-120">The name of the privateLink configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c05c1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c05c1-121">CommonParameters</span></span>
<span data-ttu-id="c05c1-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c05c1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c05c1-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c05c1-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c05c1-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="c05c1-124">INPUTS</span></span>

### <span data-ttu-id="c05c1-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c05c1-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="c05c1-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="c05c1-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="c05c1-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c05c1-127">OUTPUTS</span></span>

### <span data-ttu-id="c05c1-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c05c1-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c05c1-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="c05c1-129">NOTES</span></span>

## <span data-ttu-id="c05c1-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c05c1-130">RELATED LINKS</span></span>

[<span data-ttu-id="c05c1-131">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="c05c1-131">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="c05c1-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="c05c1-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="c05c1-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="c05c1-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="c05c1-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="c05c1-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)