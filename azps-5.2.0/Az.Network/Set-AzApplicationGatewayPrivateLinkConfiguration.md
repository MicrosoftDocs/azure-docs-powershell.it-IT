---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: 78af871cf476ee80c57e22e2469b48bb4d4337a1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369809"
---
# <span data-ttu-id="2ce9f-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ce9f-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="2ce9f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2ce9f-102">SYNOPSIS</span></span>
<span data-ttu-id="2ce9f-103">Modifica una configurazione PrivateLink per un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2ce9f-103">Modifies an PrivateLink Configuration for an application gateway.</span></span>

## <span data-ttu-id="2ce9f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ce9f-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ce9f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ce9f-105">DESCRIPTION</span></span>
<span data-ttu-id="2ce9f-106">Il cmdlet **set-AzApplicationGatewayPrivateLinkConfiguration** modifica una configurazione privateLink per un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="2ce9f-106">The **Set-AzApplicationGatewayPrivateLinkConfiguration** cmdlet modifies an privateLink configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="2ce9f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ce9f-107">EXAMPLES</span></span>

### <span data-ttu-id="2ce9f-108">Esempio 1: impostare una configurazione di PrivateLink</span><span class="sxs-lookup"><span data-stu-id="2ce9f-108">Example 1: Set a PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration01
```

<span data-ttu-id="2ce9f-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="2ce9f-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="2ce9f-110">Il secondo comando imposta la configurazione di privateLink con il nome privateLinkConfig01 per usare la configurazione IP archiviata in $privateLinkIpConfiguration 01</span><span class="sxs-lookup"><span data-stu-id="2ce9f-110">The second command sets the privateLink configuration with name privateLinkConfig01 to use the ip configuration stored in $privateLinkIpConfiguration01</span></span>

## <span data-ttu-id="2ce9f-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2ce9f-111">PARAMETERS</span></span>

### <span data-ttu-id="2ce9f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2ce9f-112">-ApplicationGateway</span></span>
<span data-ttu-id="2ce9f-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2ce9f-113">The applicationGateway</span></span>

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

### <span data-ttu-id="2ce9f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ce9f-114">-DefaultProfile</span></span>
<span data-ttu-id="2ce9f-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2ce9f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ce9f-116">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ce9f-116">-IpConfiguration</span></span>
<span data-ttu-id="2ce9f-117">Elenco di ipConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ce9f-117">The list of ipConfiguration</span></span>

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

### <span data-ttu-id="2ce9f-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="2ce9f-118">-Name</span></span>
<span data-ttu-id="2ce9f-119">Nome della configurazione di privateLink</span><span class="sxs-lookup"><span data-stu-id="2ce9f-119">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="2ce9f-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2ce9f-120">-Confirm</span></span>
<span data-ttu-id="2ce9f-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ce9f-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ce9f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ce9f-122">-WhatIf</span></span>
<span data-ttu-id="2ce9f-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ce9f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ce9f-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ce9f-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ce9f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ce9f-125">CommonParameters</span></span>
<span data-ttu-id="2ce9f-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ce9f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ce9f-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ce9f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ce9f-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2ce9f-128">INPUTS</span></span>

### <span data-ttu-id="2ce9f-129">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2ce9f-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="2ce9f-130">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayPrivateLinkIpConfiguration []</span><span class="sxs-lookup"><span data-stu-id="2ce9f-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="2ce9f-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ce9f-131">OUTPUTS</span></span>

### <span data-ttu-id="2ce9f-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2ce9f-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2ce9f-133">Note</span><span class="sxs-lookup"><span data-stu-id="2ce9f-133">NOTES</span></span>

## <span data-ttu-id="2ce9f-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ce9f-134">RELATED LINKS</span></span>

[<span data-ttu-id="2ce9f-135">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ce9f-135">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="2ce9f-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ce9f-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="2ce9f-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ce9f-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="2ce9f-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ce9f-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)