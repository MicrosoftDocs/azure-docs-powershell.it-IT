---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: fdcd725c79a6f789879ab3103cec90b09c828e74
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179934"
---
# <span data-ttu-id="cbd29-101">Get-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="cbd29-101">Get-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="cbd29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbd29-102">SYNOPSIS</span></span>
<span data-ttu-id="cbd29-103">Ottiene un criterio firewall del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="cbd29-103">Gets an application gateway firewall policy.</span></span>

## <span data-ttu-id="cbd29-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cbd29-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFirewallPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbd29-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cbd29-105">DESCRIPTION</span></span>
<span data-ttu-id="cbd29-106">Il cmdlet **Get-AzApplicationGatewayFirewallPolicy** ottiene un criterio firewall del gateway di applicazione.</span><span class="sxs-lookup"><span data-stu-id="cbd29-106">The **Get-AzApplicationGatewayFirewallPolicy** cmdlet gets an application gateway firewall policy..</span></span>

## <span data-ttu-id="cbd29-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cbd29-107">EXAMPLES</span></span>

### <span data-ttu-id="cbd29-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cbd29-108">Example 1</span></span>
```powershell
PS C:\> $AppGwFirewallPolicy = Get-AzApplicationGatewayFirewallPolicy -Name "FirewallPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="cbd29-109">Questo comando recupera il criterio firewall del gateway applicazione denominato FirewallPolicy1 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella $AppGwFirewallPolicy variabile.</span><span class="sxs-lookup"><span data-stu-id="cbd29-109">This command gets the application gateway firewall policy named FirewallPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="cbd29-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cbd29-110">PARAMETERS</span></span>

### <span data-ttu-id="cbd29-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbd29-111">-DefaultProfile</span></span>
<span data-ttu-id="cbd29-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cbd29-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbd29-113">-Name</span><span class="sxs-lookup"><span data-stu-id="cbd29-113">-Name</span></span>
<span data-ttu-id="cbd29-114">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="cbd29-114">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbd29-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbd29-115">-ResourceGroupName</span></span>
<span data-ttu-id="cbd29-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cbd29-116">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbd29-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbd29-117">CommonParameters</span></span>
<span data-ttu-id="cbd29-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbd29-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbd29-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cbd29-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbd29-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="cbd29-120">INPUTS</span></span>

### <span data-ttu-id="cbd29-121">System.String</span><span class="sxs-lookup"><span data-stu-id="cbd29-121">System.String</span></span>

## <span data-ttu-id="cbd29-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cbd29-122">OUTPUTS</span></span>

### <span data-ttu-id="cbd29-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="cbd29-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="cbd29-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="cbd29-124">NOTES</span></span>

## <span data-ttu-id="cbd29-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cbd29-125">RELATED LINKS</span></span>
