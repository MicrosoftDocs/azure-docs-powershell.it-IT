---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
ms.openlocfilehash: ad0db70d513ffeea688344df612cab942ae6ec53
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94199668"
---
# <span data-ttu-id="cb944-101">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="cb944-101">Get-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="cb944-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cb944-102">SYNOPSIS</span></span>
<span data-ttu-id="cb944-103">Ottiene i parametri IPSec VPN impostati sul gateway di rete virtuale per le connessioni punto a sito.</span><span class="sxs-lookup"><span data-stu-id="cb944-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

## <span data-ttu-id="cb944-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cb944-104">SYNTAX</span></span>

```
Get-AzVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb944-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb944-105">DESCRIPTION</span></span>
<span data-ttu-id="cb944-106">Il gateway di rete virtuale è l'oggetto che rappresenta il gateway in Azure.</span><span class="sxs-lookup"><span data-stu-id="cb944-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="cb944-107">Il cmdlet **Get-AzVpnClientIpsecParameter** restituisce l'oggetto dei parametri IPSec VPN impostati nel gateway in Azure in base al nome del gateway e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cb944-107">The **Get-AzVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="cb944-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cb944-108">EXAMPLES</span></span>

### <span data-ttu-id="cb944-109">Esempio 1: ottiene i parametri IPSec VPN impostati nel gateway di rete virtuale per le connessioni a un punto.</span><span class="sxs-lookup"><span data-stu-id="cb944-109">Example 1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```powershell
PS C:\> $VpnClientIPsecParameters = Get-AzVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="cb944-110">Restituisce l'oggetto dei parametri IPSec VPN impostati nel gateway di rete virtuale con il nome "gateway" nel gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="cb944-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="cb944-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cb944-111">PARAMETERS</span></span>

### <span data-ttu-id="cb944-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb944-112">-DefaultProfile</span></span>
<span data-ttu-id="cb944-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cb944-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb944-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="cb944-114">-Name</span></span>
<span data-ttu-id="cb944-115">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="cb944-115">The resource name.</span></span>

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

### <span data-ttu-id="cb944-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb944-116">-ResourceGroupName</span></span>
<span data-ttu-id="cb944-117">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cb944-117">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb944-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb944-118">CommonParameters</span></span>
<span data-ttu-id="cb944-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb944-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb944-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb944-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb944-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cb944-121">INPUTS</span></span>

### <span data-ttu-id="cb944-122">System. String</span><span class="sxs-lookup"><span data-stu-id="cb944-122">System.String</span></span>

## <span data-ttu-id="cb944-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cb944-123">OUTPUTS</span></span>

### <span data-ttu-id="cb944-124">Microsoft. Azure. Commands. Network. Models. PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="cb944-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="cb944-125">Note</span><span class="sxs-lookup"><span data-stu-id="cb944-125">NOTES</span></span>

## <span data-ttu-id="cb944-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cb944-126">RELATED LINKS</span></span>

[<span data-ttu-id="cb944-127">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="cb944-127">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="cb944-128">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="cb944-128">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="cb944-129">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="cb944-129">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)