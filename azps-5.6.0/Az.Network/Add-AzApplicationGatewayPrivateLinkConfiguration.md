---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 0bc3d62ad690ab8bed961045ce46448af8700bd8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982606"
---
# <span data-ttu-id="0e20b-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e20b-101">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="0e20b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e20b-102">SYNOPSIS</span></span>
<span data-ttu-id="0e20b-103">Aggiunge una configurazione di collegamento privato a un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="0e20b-103">Adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="0e20b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0e20b-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0e20b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0e20b-105">DESCRIPTION</span></span>
<span data-ttu-id="0e20b-106">Il cmdlet **Add-AzApplicationGatewayPrivateLinkConfiguration** aggiunge una configurazione di collegamento privato a un gateway di applicazione.</span><span class="sxs-lookup"><span data-stu-id="0e20b-106">The **Add-AzApplicationGatewayPrivateLinkConfiguration** cmdlet adds a private link configuration to an application gateway.</span></span>

## <span data-ttu-id="0e20b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0e20b-107">EXAMPLES</span></span>

### <span data-ttu-id="0e20b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0e20b-108">Example 1</span></span>
```powershell
PS C:\> $PrivateLinkIpConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "ipConfig01" -Subnet $subnet -Primary
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $PrivateLinkIpConfiguration
```

<span data-ttu-id="0e20b-109">Il primo comando crea una configurazione privataLinkIpConfiguration e la archivia nella $PrivateLinkIpConfiguration variabile.</span><span class="sxs-lookup"><span data-stu-id="0e20b-109">The first command creates a privateLinkIpConfiguration and stores it in the $PrivateLinkIpConfiguration variable.</span></span>
<span data-ttu-id="0e20b-110">Il secondo comando recupera il gateway applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="0e20b-110">The second command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="0e20b-111">Il terzo comando aggiunge la configurazione del collegamento privato denominata privateLinkConfig01 per il gateway in $AppGw</span><span class="sxs-lookup"><span data-stu-id="0e20b-111">The third command adds the private link configuration named privateLinkConfig01, for the gateway in $AppGw</span></span>

## <span data-ttu-id="0e20b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e20b-112">PARAMETERS</span></span>

### <span data-ttu-id="0e20b-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0e20b-113">-ApplicationGateway</span></span>
<span data-ttu-id="0e20b-114">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0e20b-114">The applicationGateway</span></span>

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

### <span data-ttu-id="0e20b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e20b-115">-DefaultProfile</span></span>
<span data-ttu-id="0e20b-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0e20b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e20b-117">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e20b-117">-IpConfiguration</span></span>
<span data-ttu-id="0e20b-118">Elenco di ipConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e20b-118">The list of ipConfiguration</span></span>

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

### <span data-ttu-id="0e20b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0e20b-119">-Name</span></span>
<span data-ttu-id="0e20b-120">Nome della configurazione privateLink</span><span class="sxs-lookup"><span data-stu-id="0e20b-120">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="0e20b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e20b-121">CommonParameters</span></span>
<span data-ttu-id="0e20b-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e20b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e20b-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0e20b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e20b-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="0e20b-124">INPUTS</span></span>

### <span data-ttu-id="0e20b-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0e20b-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="0e20b-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="0e20b-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="0e20b-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0e20b-127">OUTPUTS</span></span>

### <span data-ttu-id="0e20b-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0e20b-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0e20b-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="0e20b-129">NOTES</span></span>

## <span data-ttu-id="0e20b-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0e20b-130">RELATED LINKS</span></span>

[<span data-ttu-id="0e20b-131">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e20b-131">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="0e20b-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e20b-132">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="0e20b-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e20b-133">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="0e20b-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e20b-134">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)