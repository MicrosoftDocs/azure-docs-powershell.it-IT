---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 9512d2d2a51e70b2a0b5e7aa2e8240a8aeb1be1a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488914"
---
# <span data-ttu-id="8de48-101">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="8de48-101">Set-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="8de48-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8de48-102">SYNOPSIS</span></span>
<span data-ttu-id="8de48-103">Modifica la configurazione auth client di un oggetto profilo SSL.</span><span class="sxs-lookup"><span data-stu-id="8de48-103">Modifies the client auth configuration of a ssl profile object.</span></span>

## <span data-ttu-id="8de48-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8de48-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayClientAuthConfiguration -SslProfile <PSApplicationGatewaySslProfile>
 [-VerifyClientCertIssuerDN] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8de48-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8de48-105">DESCRIPTION</span></span>
<span data-ttu-id="8de48-106">Il cmdlet **set-AzApplicationGatewayClientAuthConfiguration** modifica la configurazione auth client di un oggetto profilo SSL.</span><span class="sxs-lookup"><span data-stu-id="8de48-106">The **Set-AzApplicationGatewayClientAuthConfiguration** cmdlet modifies the client auth configuration of a ssl profile object.</span></span>

## <span data-ttu-id="8de48-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8de48-107">EXAMPLES</span></span>

### <span data-ttu-id="8de48-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8de48-108">Example 1</span></span>
```powershell
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "SslProfile01" -ApplicationGateway $AppGw
PS C:\> Set-AzApplicationGatewayClientAuthConfiguration -SslProfile $profile -VerifyClientCertIssuerDN
```

<span data-ttu-id="8de48-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="8de48-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="8de48-110">Il secondo comando ottiene il profilo SSL denominato SslProfile01 per $AppGw e archivia le impostazioni nella variabile $profile.</span><span class="sxs-lookup"><span data-stu-id="8de48-110">The second command gets the ssl profile named SslProfile01 for $AppGw and stores the settings in the $profile variable.</span></span> <span data-ttu-id="8de48-111">L'ultimo comando modifica la configurazione auth client dell'oggetto profilo SSL archiviato in $profile.</span><span class="sxs-lookup"><span data-stu-id="8de48-111">The last command modifies the client auth configuration of the ssl profile object stored in $profile.</span></span>

## <span data-ttu-id="8de48-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8de48-112">PARAMETERS</span></span>

### <span data-ttu-id="8de48-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8de48-113">-DefaultProfile</span></span>
<span data-ttu-id="8de48-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8de48-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8de48-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="8de48-115">-SslProfile</span></span>
<span data-ttu-id="8de48-116">Profilo SSL</span><span class="sxs-lookup"><span data-stu-id="8de48-116">The ssl profile</span></span>

```yaml
Type: PSApplicationGatewaySslProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8de48-117">-VerifyClientCertIssuerDN</span><span class="sxs-lookup"><span data-stu-id="8de48-117">-VerifyClientCertIssuerDN</span></span>
<span data-ttu-id="8de48-118">Verificare il nome dell'autorità di certificazione del certificato client.</span><span class="sxs-lookup"><span data-stu-id="8de48-118">Verify client certificate issuer name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8de48-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8de48-119">CommonParameters</span></span>
<span data-ttu-id="8de48-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8de48-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8de48-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8de48-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8de48-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8de48-122">INPUTS</span></span>

### <span data-ttu-id="8de48-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="8de48-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="8de48-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8de48-124">OUTPUTS</span></span>

### <span data-ttu-id="8de48-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="8de48-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="8de48-126">Note</span><span class="sxs-lookup"><span data-stu-id="8de48-126">NOTES</span></span>

## <span data-ttu-id="8de48-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8de48-127">RELATED LINKS</span></span>

[<span data-ttu-id="8de48-128">Add-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="8de48-128">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="8de48-129">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="8de48-129">New-AzApplicationGatewayClientAuthConfiguration</span></span>](./New-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="8de48-130">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="8de48-130">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="8de48-131">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="8de48-131">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)