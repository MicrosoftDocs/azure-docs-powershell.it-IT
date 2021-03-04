---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: e01404958156967c6881655ab42eb965152ebaaf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953742"
---
# <span data-ttu-id="20060-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="20060-101">Set-AzApplicationGatewayPrivateLinkConfiguration</span></span>

## <span data-ttu-id="20060-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20060-102">SYNOPSIS</span></span>
<span data-ttu-id="20060-103">Modifica una configurazione PrivateLink per un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="20060-103">Modifies an PrivateLink Configuration for an application gateway.</span></span>

## <span data-ttu-id="20060-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="20060-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20060-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="20060-105">DESCRIPTION</span></span>
<span data-ttu-id="20060-106">Il cmdlet **Set-AzApplicationGatewayPrivateLinkConfiguration** modifica una configurazione privateLink per un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="20060-106">The **Set-AzApplicationGatewayPrivateLinkConfiguration** cmdlet modifies an privateLink configuration for an Azure application gateway.</span></span>

## <span data-ttu-id="20060-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="20060-107">EXAMPLES</span></span>

### <span data-ttu-id="20060-108">Esempio 1: Impostare una configurazione PrivateLink</span><span class="sxs-lookup"><span data-stu-id="20060-108">Example 1: Set a PrivateLink Configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayPrivateLinkConfiguration -ApplicationGateway $AppGw -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration01
```

<span data-ttu-id="20060-109">Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="20060-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="20060-110">Il secondo comando imposta la configurazione privateLink con il nome privateLinkConfig01 in modo da usare la configurazione IP archiviata in $privateLinkIpConfiguration 01</span><span class="sxs-lookup"><span data-stu-id="20060-110">The second command sets the privateLink configuration with name privateLinkConfig01 to use the ip configuration stored in $privateLinkIpConfiguration01</span></span>

## <span data-ttu-id="20060-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20060-111">PARAMETERS</span></span>

### <span data-ttu-id="20060-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="20060-112">-ApplicationGateway</span></span>
<span data-ttu-id="20060-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="20060-113">The applicationGateway</span></span>

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

### <span data-ttu-id="20060-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20060-114">-DefaultProfile</span></span>
<span data-ttu-id="20060-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="20060-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20060-116">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="20060-116">-IpConfiguration</span></span>
<span data-ttu-id="20060-117">Elenco di ipConfiguration</span><span class="sxs-lookup"><span data-stu-id="20060-117">The list of ipConfiguration</span></span>

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

### <span data-ttu-id="20060-118">-Name</span><span class="sxs-lookup"><span data-stu-id="20060-118">-Name</span></span>
<span data-ttu-id="20060-119">Nome della configurazione privateLink</span><span class="sxs-lookup"><span data-stu-id="20060-119">The name of the privateLink configuration</span></span>

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

### <span data-ttu-id="20060-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20060-120">-Confirm</span></span>
<span data-ttu-id="20060-121">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20060-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20060-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20060-122">-WhatIf</span></span>
<span data-ttu-id="20060-123">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="20060-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20060-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="20060-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20060-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20060-125">CommonParameters</span></span>
<span data-ttu-id="20060-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20060-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20060-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="20060-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20060-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="20060-128">INPUTS</span></span>

### <span data-ttu-id="20060-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="20060-129">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

### <span data-ttu-id="20060-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="20060-130">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]</span></span>

## <span data-ttu-id="20060-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="20060-131">OUTPUTS</span></span>

### <span data-ttu-id="20060-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="20060-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="20060-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="20060-133">NOTES</span></span>

## <span data-ttu-id="20060-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="20060-134">RELATED LINKS</span></span>

[<span data-ttu-id="20060-135">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="20060-135">New-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./New-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="20060-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="20060-136">Add-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="20060-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="20060-137">Get-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[<span data-ttu-id="20060-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="20060-138">Remove-AzApplicationGatewayPrivateLinkConfiguration</span></span>](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)