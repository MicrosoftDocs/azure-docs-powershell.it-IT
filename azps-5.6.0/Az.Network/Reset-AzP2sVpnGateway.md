---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/powershell/module/az.network/reset-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzP2sVpnGateway.md
ms.openlocfilehash: c813f5d5921f0291174a77cf6cdc4b0a1f7ee6a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958158"
---
# <span data-ttu-id="00295-101">Reset-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="00295-101">Reset-AzP2sVpnGateway</span></span>

## <span data-ttu-id="00295-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00295-102">SYNOPSIS</span></span>
<span data-ttu-id="00295-103">Reimposta il gateway VPN P2S scalabile.</span><span class="sxs-lookup"><span data-stu-id="00295-103">Resets the scalable P2S VPN gateway.</span></span>

## <span data-ttu-id="00295-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="00295-104">SYNTAX</span></span>

```
Reset-AzP2sVpnGateway -P2SVpnGateway <PSP2SVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00295-105">ByP2SVpnGatewayName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="00295-105">ByP2SVpnGatewayName (Default)</span></span>
```
Reset-- -ResourceGroupName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00295-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="00295-106">ByP2SVpnGatewayObject</span></span>
```
Reset-- -InputObject <PSVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00295-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="00295-107">ByP2SVpnGatewayResourceId</span></span>
```
Reset-- -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00295-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="00295-108">DESCRIPTION</span></span>
<span data-ttu-id="00295-109">Reimposta P2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="00295-109">Resets the P2SVpnGateway</span></span>

## <span data-ttu-id="00295-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="00295-110">EXAMPLES</span></span>

### <span data-ttu-id="00295-111">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="00295-111">Example 1:</span></span>
```
$Gateway = Get-AzP2SVpnGateway -Name "ContosoVirtualGateway" -ResourceGroupName "RGName"
Reset-AzP2sVpnGateway -P2SVpnGateway $Gateway
```

## <span data-ttu-id="00295-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00295-112">PARAMETERS</span></span>

### <span data-ttu-id="00295-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00295-113">-AsJob</span></span>
<span data-ttu-id="00295-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="00295-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00295-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00295-115">-DefaultProfile</span></span>
<span data-ttu-id="00295-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="00295-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00295-117">-P2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="00295-117">-P2SVpnGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00295-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00295-118">CommonParameters</span></span>
<span data-ttu-id="00295-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00295-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00295-120">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00295-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00295-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="00295-121">INPUTS</span></span>

### <span data-ttu-id="00295-122">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="00295-122">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

### <span data-ttu-id="00295-123">System.String</span><span class="sxs-lookup"><span data-stu-id="00295-123">System.String</span></span>

## <span data-ttu-id="00295-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="00295-124">OUTPUTS</span></span>

### <span data-ttu-id="00295-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="00295-125">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="00295-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="00295-126">NOTES</span></span>

## <span data-ttu-id="00295-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="00295-127">RELATED LINKS</span></span>

[<span data-ttu-id="00295-128">Get-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="00295-128">Get-AzP2sVpnGateway</span></span>](./Get-AzP2sVpnGateway.md)

[<span data-ttu-id="00295-129">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="00295-129">New-AzP2sVpnGateway</span></span>](./New-AzP2sVpnGateway.md)

[<span data-ttu-id="00295-130">Remove-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="00295-130">Remove-AzP2sVpnGateway</span></span>](./Remove-AzP2sVpnGateway.md)

[<span data-ttu-id="00295-131">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="00295-131">Update-AzP2sVpnGateway</span></span>](./Update-AzP2sVpnGateway.md)
