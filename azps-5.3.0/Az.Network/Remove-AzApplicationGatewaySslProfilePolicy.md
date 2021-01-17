---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaysslprofilepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfilePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewaySslProfilePolicy.md
ms.openlocfilehash: 541293160a1cf9e3d32de5d378c24d1ee4b2705b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475900"
---
# <span data-ttu-id="e532c-101">Remove-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="e532c-101">Remove-AzApplicationGatewaySslProfilePolicy</span></span>

## <span data-ttu-id="e532c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e532c-102">SYNOPSIS</span></span>
<span data-ttu-id="e532c-103">Rimuove un criterio SSL da un profilo SSL di Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e532c-103">Removes an SSL policy from an Azure application gateway SSL profile.</span></span>

## <span data-ttu-id="e532c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e532c-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewaySslProfilePolicy -SslProfile <PSApplicationGatewaySslProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e532c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e532c-105">DESCRIPTION</span></span>
<span data-ttu-id="e532c-106">Il cmdlet Remove-AzApplicationGatewaySslProfilePolicy rimuove un criterio SSL da un profilo SSL di Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e532c-106">The Remove-AzApplicationGatewaySslProfilePolicy cmdlet removes an SSL policy from an Azure application gateway SSL profile.</span></span>

## <span data-ttu-id="e532c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e532c-107">EXAMPLES</span></span>

### <span data-ttu-id="e532c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e532c-108">Example 1</span></span>
```powershell
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $profile  = Get-AzApplicationGatewaySslProfile -Name "Profile01" -ApplicationGateway $AppGw
PS C:\> $profile = Remove-AzApplicationGatewaySslProfilePolicy -SslProfile $profile
```

<span data-ttu-id="e532c-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e532c-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span> <span data-ttu-id="e532c-110">Il secondo comando ottiene il profilo SSL denominato Profile01 per $AppGw e lo archivia nella variabile $profile.</span><span class="sxs-lookup"><span data-stu-id="e532c-110">The second command gets the SSL profile named Profile01 for $AppGw and stores it in the $profile variable.</span></span> <span data-ttu-id="e532c-111">L'ultimo comando rimuove i criteri SSL del profilo SSL archiviati in $profile.</span><span class="sxs-lookup"><span data-stu-id="e532c-111">The last command removes the ssl policy of the ssl profile stored in $profile.</span></span>

## <span data-ttu-id="e532c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e532c-112">PARAMETERS</span></span>

### <span data-ttu-id="e532c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e532c-113">-DefaultProfile</span></span>
<span data-ttu-id="e532c-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e532c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e532c-115">-SslProfile</span><span class="sxs-lookup"><span data-stu-id="e532c-115">-SslProfile</span></span>
<span data-ttu-id="e532c-116">Profilo SSL di applicationGateway</span><span class="sxs-lookup"><span data-stu-id="e532c-116">The applicationGateway SSL profile</span></span>

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

### <span data-ttu-id="e532c-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e532c-117">-Confirm</span></span>
<span data-ttu-id="e532c-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e532c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e532c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e532c-119">-WhatIf</span></span>
<span data-ttu-id="e532c-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e532c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e532c-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e532c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e532c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e532c-122">CommonParameters</span></span>
<span data-ttu-id="e532c-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e532c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e532c-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e532c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e532c-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e532c-125">INPUTS</span></span>

### <span data-ttu-id="e532c-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="e532c-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="e532c-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e532c-127">OUTPUTS</span></span>

### <span data-ttu-id="e532c-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslProfile</span><span class="sxs-lookup"><span data-stu-id="e532c-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslProfile</span></span>

## <span data-ttu-id="e532c-129">Note</span><span class="sxs-lookup"><span data-stu-id="e532c-129">NOTES</span></span>

## <span data-ttu-id="e532c-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e532c-130">RELATED LINKS</span></span>

[<span data-ttu-id="e532c-131">New-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="e532c-131">New-AzApplicationGatewaySslProfilePolicy</span></span>](./New-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="e532c-132">Add-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="e532c-132">Add-AzApplicationGatewaySslProfilePolicy</span></span>](./Add-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="e532c-133">Get-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="e532c-133">Get-AzApplicationGatewaySslProfilePolicy</span></span>](./Get-AzApplicationGatewaySslProfilePolicy.md)

[<span data-ttu-id="e532c-134">Set-AzApplicationGatewaySslProfilePolicy</span><span class="sxs-lookup"><span data-stu-id="e532c-134">Set-AzApplicationGatewaySslProfilePolicy</span></span>](./Set-AzApplicationGatewaySslProfilePolicy.md)