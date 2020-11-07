---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 652583ff4425c0403440856a32be3b8107d771ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678616"
---
# <span data-ttu-id="325ad-101">Get-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="325ad-101">Get-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="325ad-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="325ad-102">SYNOPSIS</span></span>
<span data-ttu-id="325ad-103">Ottiene un criterio firewall di Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="325ad-103">Gets an application gateway firewall policy.</span></span>

## <span data-ttu-id="325ad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="325ad-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFirewallPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="325ad-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="325ad-105">DESCRIPTION</span></span>
<span data-ttu-id="325ad-106">Il cmdlet **Get-AzApplicationGatewayFirewallPolicy** ottiene un criterio del firewall di gateway applicativo.</span><span class="sxs-lookup"><span data-stu-id="325ad-106">The **Get-AzApplicationGatewayFirewallPolicy** cmdlet gets an application gateway firewall policy..</span></span>

## <span data-ttu-id="325ad-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="325ad-107">EXAMPLES</span></span>

### <span data-ttu-id="325ad-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="325ad-108">Example 1</span></span>
```powershell
PS C:\> $AppGwFirewallPolicy = Get-AzApplicationGatewayFirewallPolicy -Name "FirewallPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="325ad-109">Questo comando consente di ottenere il criterio firewall Application Gateway denominato FirewallPolicy1 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGwFirewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="325ad-109">This command gets the application gateway firewall policy named FirewallPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="325ad-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="325ad-110">PARAMETERS</span></span>

### <span data-ttu-id="325ad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="325ad-111">-DefaultProfile</span></span>
<span data-ttu-id="325ad-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="325ad-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="325ad-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="325ad-113">-Name</span></span>
<span data-ttu-id="325ad-114">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="325ad-114">The resource name.</span></span>

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

### <span data-ttu-id="325ad-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="325ad-115">-ResourceGroupName</span></span>
<span data-ttu-id="325ad-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="325ad-116">The resource group name.</span></span>

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

### <span data-ttu-id="325ad-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="325ad-117">CommonParameters</span></span>
<span data-ttu-id="325ad-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="325ad-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="325ad-119">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="325ad-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="325ad-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="325ad-120">INPUTS</span></span>

### <span data-ttu-id="325ad-121">System. String</span><span class="sxs-lookup"><span data-stu-id="325ad-121">System.String</span></span>

## <span data-ttu-id="325ad-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="325ad-122">OUTPUTS</span></span>

### <span data-ttu-id="325ad-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="325ad-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="325ad-124">Note</span><span class="sxs-lookup"><span data-stu-id="325ad-124">NOTES</span></span>

## <span data-ttu-id="325ad-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="325ad-125">RELATED LINKS</span></span>
