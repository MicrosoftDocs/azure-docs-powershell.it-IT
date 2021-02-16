---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
ms.openlocfilehash: fc60a983e06e632912e43291f7b60980ff34a8cd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206754"
---
# <span data-ttu-id="fc3d9-101">New-AzFirewallHubPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fc3d9-101">New-AzFirewallHubPublicIpAddress</span></span>

## <span data-ttu-id="fc3d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc3d9-102">SYNOPSIS</span></span>
<span data-ttu-id="fc3d9-103">Ip pubblico associato al firewall nell'hub virtuale</span><span class="sxs-lookup"><span data-stu-id="fc3d9-103">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="fc3d9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fc3d9-104">SYNTAX</span></span>

```
New-AzFirewallHubPublicIpAddress [-Count <Int32>] [-Addresses <PSAzureFirewallPublicIpAddress[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc3d9-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fc3d9-105">DESCRIPTION</span></span>
<span data-ttu-id="fc3d9-106">Ip pubblico associato al firewall nell'hub virtuale</span><span class="sxs-lookup"><span data-stu-id="fc3d9-106">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="fc3d9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fc3d9-107">EXAMPLES</span></span>

### <span data-ttu-id="fc3d9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fc3d9-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallHubPublicIpAddress -Count 2
```

<span data-ttu-id="fc3d9-109">Verranno creati 2 ip pubblici nel firewall collegato all'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="fc3d9-109">This will create 2 public ips on the firewall attached to the virtual hub.</span></span> <span data-ttu-id="fc3d9-110">L'indirizzo IP verrà creato nel back-end. Non è possibile fornire gli ipaddress in modo esplicito per un nuovo firewall.</span><span class="sxs-lookup"><span data-stu-id="fc3d9-110">This will create the ip address in the backend.We cannot provide the ipaddresses explicitly for a new firewall.</span></span>

### <span data-ttu-id="fc3d9-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="fc3d9-111">Example 2</span></span>
```powershell
PS C:\> $publicIp1 = New-AzFirewallPublicIpAddress -Address 10.2.3.4
PS C:\> $publicIp2 = New-AzFirewallPublicIpAddress -Address 20.56.37.46
PS C:\> New-AzFirewallHubPublicIpAddress -Count 3 -Addresses $publicIp1, $publicIp2
```

<span data-ttu-id="fc3d9-112">Verrà creato 1 nuovo ip pubblico nel firewall conservando $publicIp 1, $publicIp 2 già esistenti nel firewall.</span><span class="sxs-lookup"><span data-stu-id="fc3d9-112">This will create 1 new public ip on the firewall by retain $publicIp1, $publicIp2 which are already exist on the firewall.</span></span>

## <span data-ttu-id="fc3d9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc3d9-113">PARAMETERS</span></span>

### <span data-ttu-id="fc3d9-114">-Addresses</span><span class="sxs-lookup"><span data-stu-id="fc3d9-114">-Addresses</span></span>
<span data-ttu-id="fc3d9-115">Gli indirizzi IP pubblici del firewall collegati a un hub</span><span class="sxs-lookup"><span data-stu-id="fc3d9-115">The Public IP Addresses of the Firewall attached to a hub</span></span>

```yaml
Type: PSAzureFirewallPublicIpAddress[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc3d9-116">-Count</span><span class="sxs-lookup"><span data-stu-id="fc3d9-116">-Count</span></span>
<span data-ttu-id="fc3d9-117">Il numero di indirizzi IP pubblici</span><span class="sxs-lookup"><span data-stu-id="fc3d9-117">The count of public Ip addresses</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc3d9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc3d9-118">-DefaultProfile</span></span>
<span data-ttu-id="fc3d9-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fc3d9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc3d9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc3d9-120">CommonParameters</span></span>
<span data-ttu-id="fc3d9-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc3d9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc3d9-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fc3d9-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc3d9-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="fc3d9-123">INPUTS</span></span>

### <span data-ttu-id="fc3d9-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fc3d9-124">None</span></span>

## <span data-ttu-id="fc3d9-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fc3d9-125">OUTPUTS</span></span>

### <span data-ttu-id="fc3d9-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span><span class="sxs-lookup"><span data-stu-id="fc3d9-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span></span>

## <span data-ttu-id="fc3d9-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="fc3d9-127">NOTES</span></span>

## <span data-ttu-id="fc3d9-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fc3d9-128">RELATED LINKS</span></span>
