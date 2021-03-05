---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 443F6492-EFA7-4417-943A-3A8D47F8C83C
online version: https://docs.microsoft.com/powershell/module/az.network/reset-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVpnGateway.md
ms.openlocfilehash: 33abb4e724f5a442efd6791cbf6256100662ab65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979533"
---
# <span data-ttu-id="d98fa-101">Reset-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d98fa-101">Reset-AzVpnGateway</span></span>

## <span data-ttu-id="d98fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d98fa-102">SYNOPSIS</span></span>
<span data-ttu-id="d98fa-103">Reimposta il gateway VPN scalabile.</span><span class="sxs-lookup"><span data-stu-id="d98fa-103">Resets the scalable VPN gateway.</span></span>

## <span data-ttu-id="d98fa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d98fa-104">SYNTAX</span></span>

```
Reset-AzVpnGateway -VpnGateway <PSVpnGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d98fa-105">ByVpnGatewayName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d98fa-105">ByVpnGatewayName (Default)</span></span>
```
Reset-AzVpnGateway -ResourceGroupName <String> -Name <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d98fa-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="d98fa-106">ByVpnGatewayObject</span></span>
```
Reset-AzVpnGateway -InputObject <PSVpnGateway> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d98fa-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="d98fa-107">ByVpnGatewayResourceId</span></span>
```
Reset-AzVpnGateway -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d98fa-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d98fa-108">DESCRIPTION</span></span>
<span data-ttu-id="d98fa-109">Reimposta VpnGateway</span><span class="sxs-lookup"><span data-stu-id="d98fa-109">Resets the VpnGateway</span></span>

## <span data-ttu-id="d98fa-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d98fa-110">EXAMPLES</span></span>

### <span data-ttu-id="d98fa-111">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="d98fa-111">Example 1:</span></span>
```
$Gateway = Get-AzVpnGateway -Name "ContosoVirtualGateway" -ResourceGroupName "RGName"
Reset-AzVpnGateway -VpnGateway $Gateway
```

## <span data-ttu-id="d98fa-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d98fa-112">PARAMETERS</span></span>

### <span data-ttu-id="d98fa-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d98fa-113">-AsJob</span></span>
<span data-ttu-id="d98fa-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d98fa-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d98fa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d98fa-115">-DefaultProfile</span></span>
<span data-ttu-id="d98fa-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d98fa-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d98fa-117">-VpnGateway</span><span class="sxs-lookup"><span data-stu-id="d98fa-117">-VpnGateway</span></span>
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

### <span data-ttu-id="d98fa-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d98fa-118">CommonParameters</span></span>
<span data-ttu-id="d98fa-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d98fa-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d98fa-120">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d98fa-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d98fa-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="d98fa-121">INPUTS</span></span>

### <span data-ttu-id="d98fa-122">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d98fa-122">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="d98fa-123">System.String</span><span class="sxs-lookup"><span data-stu-id="d98fa-123">System.String</span></span>

## <span data-ttu-id="d98fa-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d98fa-124">OUTPUTS</span></span>

### <span data-ttu-id="d98fa-125">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d98fa-125">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

## <span data-ttu-id="d98fa-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="d98fa-126">NOTES</span></span>

## <span data-ttu-id="d98fa-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d98fa-127">RELATED LINKS</span></span>

[<span data-ttu-id="d98fa-128">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d98fa-128">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="d98fa-129">New-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d98fa-129">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="d98fa-130">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d98fa-130">Remove-AzVpnGateway</span></span>](./Remove-AzVpnGateway.md)

[<span data-ttu-id="d98fa-131">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="d98fa-131">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
