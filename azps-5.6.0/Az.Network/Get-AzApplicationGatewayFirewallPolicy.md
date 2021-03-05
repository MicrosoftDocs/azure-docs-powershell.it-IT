---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 122e011336b9fcdb8b8eb19622632e1ff295a01c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996559"
---
# <span data-ttu-id="a4c32-101">Get-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="a4c32-101">Get-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="a4c32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4c32-102">SYNOPSIS</span></span>
<span data-ttu-id="a4c32-103">Ottiene un criterio firewall del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4c32-103">Gets an application gateway firewall policy.</span></span>

## <span data-ttu-id="a4c32-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4c32-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFirewallPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4c32-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a4c32-105">DESCRIPTION</span></span>
<span data-ttu-id="a4c32-106">Il cmdlet **Get-AzApplicationGatewayFirewallPolicy** ottiene un criterio firewall del gateway di applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4c32-106">The **Get-AzApplicationGatewayFirewallPolicy** cmdlet gets an application gateway firewall policy..</span></span>

## <span data-ttu-id="a4c32-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4c32-107">EXAMPLES</span></span>

### <span data-ttu-id="a4c32-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a4c32-108">Example 1</span></span>
```powershell
PS C:\> $AppGwFirewallPolicy = Get-AzApplicationGatewayFirewallPolicy -Name "FirewallPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a4c32-109">Questo comando recupera il criterio firewall del gateway applicazione denominato FirewallPolicy1 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella $AppGwFirewallPolicy variabile.</span><span class="sxs-lookup"><span data-stu-id="a4c32-109">This command gets the application gateway firewall policy named FirewallPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="a4c32-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4c32-110">PARAMETERS</span></span>

### <span data-ttu-id="a4c32-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4c32-111">-DefaultProfile</span></span>
<span data-ttu-id="a4c32-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a4c32-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4c32-113">-Name</span><span class="sxs-lookup"><span data-stu-id="a4c32-113">-Name</span></span>
<span data-ttu-id="a4c32-114">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="a4c32-114">The resource name.</span></span>

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

### <span data-ttu-id="a4c32-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4c32-115">-ResourceGroupName</span></span>
<span data-ttu-id="a4c32-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a4c32-116">The resource group name.</span></span>

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

### <span data-ttu-id="a4c32-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4c32-117">CommonParameters</span></span>
<span data-ttu-id="a4c32-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4c32-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4c32-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a4c32-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4c32-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="a4c32-120">INPUTS</span></span>

### <span data-ttu-id="a4c32-121">System.String</span><span class="sxs-lookup"><span data-stu-id="a4c32-121">System.String</span></span>

## <span data-ttu-id="a4c32-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4c32-122">OUTPUTS</span></span>

### <span data-ttu-id="a4c32-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="a4c32-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="a4c32-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="a4c32-124">NOTES</span></span>

## <span data-ttu-id="a4c32-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4c32-125">RELATED LINKS</span></span>
