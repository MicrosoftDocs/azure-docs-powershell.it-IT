---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysslprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySslProfile.md
ms.openlocfilehash: 1763dfab6815efd625ff43ee248664a3f7b36cb9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372119"
---
# <span data-ttu-id="6a14f-101">Set-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="6a14f-101">Set-AzApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="6a14f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a14f-102">SYNOPSIS</span></span>
<span data-ttu-id="6a14f-103">Aggiorna il profilo SSL per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6a14f-103">Updates ssl profile for an application gateway.</span></span>

## <span data-ttu-id="6a14f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a14f-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySslProfile -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SslPolicy <PSApplicationGatewaySslPolicy>]
 [-ClientAuthConfiguration <PSApplicationGatewayClientAuthConfiguration>]
 [-TrustedClientCertificates <PSApplicationGatewayTrustedClientCertificate[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a14f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a14f-105">DESCRIPTION</span></span>
<span data-ttu-id="6a14f-106">Il cmdlet **set-AzApplicationGatewaySslProfile** aggiorna il profilo SSL per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="6a14f-106">The **Set-AzApplicationGatewaySslProfile** cmdlet updates the ssl profile for an Azure application gateway.</span></span>

## <span data-ttu-id="6a14f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a14f-107">EXAMPLES</span></span>

### <span data-ttu-id="6a14f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6a14f-108">Example 1</span></span>
```powershell
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySslProfile -ApplicationGateway $AppGw -Name "Profile01" -ClientAuthConfiguration $newclientconfig
```

<span data-ttu-id="6a14f-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="6a14f-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="6a14f-110">Il secondo comando Aggiorna il profilo SSL del gateway dell'applicazione nella variabile $AppGw per aggiornare la configurazione di autenticazione del client al nuovo valore archiviato in $newclientconfig.</span><span class="sxs-lookup"><span data-stu-id="6a14f-110">The second command updates the ssl profile of the application gateway in the $AppGw variable to update the client auth configuration to the new value stored in $newclientconfig.</span></span>

## <span data-ttu-id="6a14f-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a14f-111">PARAMETERS</span></span>

### <span data-ttu-id="6a14f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6a14f-112">-ApplicationGateway</span></span>
<span data-ttu-id="6a14f-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6a14f-113">The applicationGateway</span></span>

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

### <span data-ttu-id="6a14f-114">-ClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a14f-114">-ClientAuthConfiguration</span></span>
<span data-ttu-id="6a14f-115">Impostazioni di configurazione dell'autenticazione client</span><span class="sxs-lookup"><span data-stu-id="6a14f-115">Client authentication configuration settings</span></span>

```yaml
Type: PSApplicationGatewayClientAuthConfiguration
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a14f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a14f-116">-DefaultProfile</span></span>
<span data-ttu-id="6a14f-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a14f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a14f-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a14f-118">-Name</span></span>
<span data-ttu-id="6a14f-119">Nome del profilo SSL</span><span class="sxs-lookup"><span data-stu-id="6a14f-119">The name of the SSL profile</span></span>

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

### <span data-ttu-id="6a14f-120">-SslPolicy</span><span class="sxs-lookup"><span data-stu-id="6a14f-120">-SslPolicy</span></span>
<span data-ttu-id="6a14f-121">Criteri SSL</span><span class="sxs-lookup"><span data-stu-id="6a14f-121">SSL policy</span></span>

```yaml
Type: PSApplicationGatewaySslPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a14f-122">-TrustedClientCertificates</span><span class="sxs-lookup"><span data-stu-id="6a14f-122">-TrustedClientCertificates</span></span>
<span data-ttu-id="6a14f-123">Catene di certificati CA client attendibili</span><span class="sxs-lookup"><span data-stu-id="6a14f-123">The trusted client CA certificate chains</span></span>

```yaml
Type: PSApplicationGatewayTrustedClientCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a14f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a14f-124">CommonParameters</span></span>
<span data-ttu-id="6a14f-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a14f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a14f-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a14f-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a14f-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a14f-127">INPUTS</span></span>

### <span data-ttu-id="6a14f-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6a14f-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6a14f-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a14f-129">OUTPUTS</span></span>

### <span data-ttu-id="6a14f-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6a14f-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6a14f-131">Note</span><span class="sxs-lookup"><span data-stu-id="6a14f-131">NOTES</span></span>

## <span data-ttu-id="6a14f-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a14f-132">RELATED LINKS</span></span>

[<span data-ttu-id="6a14f-133">Add-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="6a14f-133">Add-AzApplicationGatewaySslProfile</span></span>](./Add-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="6a14f-134">New-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="6a14f-134">New-AzApplicationGatewaySslProfile</span></span>](./New-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="6a14f-135">Get-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="6a14f-135">Get-AzApplicationGatewaySslProfile</span></span>](./Get-AzApplicationGatewaySslProfile.md)

[<span data-ttu-id="6a14f-136">Remove-AzApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="6a14f-136">Remove-AzApplicationGatewaySslProfile</span></span>](./Remove-AzApplicationGatewaySslProfile.md)