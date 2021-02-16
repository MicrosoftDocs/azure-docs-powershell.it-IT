---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientipsecparameter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientIpsecParameter.md
ms.openlocfilehash: ad0db70d513ffeea688344df612cab942ae6ec53
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191918"
---
# <span data-ttu-id="bebfe-101">Get-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="bebfe-101">Get-AzVpnClientIpsecParameter</span></span>

## <span data-ttu-id="bebfe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bebfe-102">SYNOPSIS</span></span>
<span data-ttu-id="bebfe-103">Recupera i parametri Ipsec vpn impostati su Gateway di rete virtuale per le connessioni Punto a sito.</span><span class="sxs-lookup"><span data-stu-id="bebfe-103">Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>

## <span data-ttu-id="bebfe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bebfe-104">SYNTAX</span></span>

```
Get-AzVpnClientIpsecParameter [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bebfe-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bebfe-105">DESCRIPTION</span></span>
<span data-ttu-id="bebfe-106">Gateway di rete virtuale è l'oggetto che rappresenta il gateway in Azure.</span><span class="sxs-lookup"><span data-stu-id="bebfe-106">The Virtual Network Gateway is the object representing your gateway in Azure.</span></span>
<span data-ttu-id="bebfe-107">Il cmdlet **Get-AzVpnClientIpsecParameter** restituisce l'oggetto dei parametri ipsec vpn impostati sul gateway in Azure in base al nome del gateway e al nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bebfe-107">The **Get-AzVpnClientIpsecParameter** cmdlet returns the object of your vpn ipsec parameters set on gateway in Azure based on Gateway Name and Resource Group Name.</span></span>

## <span data-ttu-id="bebfe-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bebfe-108">EXAMPLES</span></span>

### <span data-ttu-id="bebfe-109">Esempio 1: recupera i parametri Ipsec vpn impostati su Gateway di rete virtuale per le connessioni Punto a sito.</span><span class="sxs-lookup"><span data-stu-id="bebfe-109">Example 1: Gets the vpn Ipsec parameters set on Virtual Network Gateway for Point to site connections.</span></span>
```powershell
PS C:\> $VpnClientIPsecParameters = Get-AzVpnClientIpsecParameter -Name myGateway -ResourceGroupName myRG
```

<span data-ttu-id="bebfe-110">Restituisce l'oggetto dei parametri ipsec vpn impostati nel Gateway di rete virtuale con il nome "myGateway" all'interno del gruppo di risorse "myRG"</span><span class="sxs-lookup"><span data-stu-id="bebfe-110">Returns the object of the vpn ipsec parameters set on the Virtual Network Gateway with the name "myGateway" within the resource group "myRG"</span></span>

## <span data-ttu-id="bebfe-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bebfe-111">PARAMETERS</span></span>

### <span data-ttu-id="bebfe-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bebfe-112">-DefaultProfile</span></span>
<span data-ttu-id="bebfe-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bebfe-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bebfe-114">-Name</span><span class="sxs-lookup"><span data-stu-id="bebfe-114">-Name</span></span>
<span data-ttu-id="bebfe-115">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="bebfe-115">The resource name.</span></span>

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

### <span data-ttu-id="bebfe-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bebfe-116">-ResourceGroupName</span></span>
<span data-ttu-id="bebfe-117">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bebfe-117">The resource group name.</span></span>

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

### <span data-ttu-id="bebfe-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bebfe-118">CommonParameters</span></span>
<span data-ttu-id="bebfe-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bebfe-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bebfe-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bebfe-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bebfe-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="bebfe-121">INPUTS</span></span>

### <span data-ttu-id="bebfe-122">System.String</span><span class="sxs-lookup"><span data-stu-id="bebfe-122">System.String</span></span>

## <span data-ttu-id="bebfe-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bebfe-123">OUTPUTS</span></span>

### <span data-ttu-id="bebfe-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="bebfe-124">Microsoft.Azure.Commands.Network.Models.PSVpnClientIPsecParameters</span></span>

## <span data-ttu-id="bebfe-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="bebfe-125">NOTES</span></span>

## <span data-ttu-id="bebfe-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bebfe-126">RELATED LINKS</span></span>

[<span data-ttu-id="bebfe-127">New-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="bebfe-127">New-AzVpnClientIpsecParameter</span></span>](./New-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="bebfe-128">Remove-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="bebfe-128">Remove-AzVpnClientIpsecParameter</span></span>](./Remove-AzVpnClientIpsecParameter.md)

[<span data-ttu-id="bebfe-129">Set-AzVpnClientIpsecParameter</span><span class="sxs-lookup"><span data-stu-id="bebfe-129">Set-AzVpnClientIpsecParameter</span></span>](./Set-AzVpnClientIpsecParameter.md)
