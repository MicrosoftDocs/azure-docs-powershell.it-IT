---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallhubpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
ms.openlocfilehash: 43a92375126411d392623095a6753072757f49a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985808"
---
# <span data-ttu-id="45014-101">New-AzFirewallHubPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="45014-101">New-AzFirewallHubPublicIpAddress</span></span>

## <span data-ttu-id="45014-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45014-102">SYNOPSIS</span></span>
<span data-ttu-id="45014-103">Ip pubblico associato al firewall nell'hub virtuale</span><span class="sxs-lookup"><span data-stu-id="45014-103">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="45014-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="45014-104">SYNTAX</span></span>

```
New-AzFirewallHubPublicIpAddress [-Count <Int32>] [-Addresses <PSAzureFirewallPublicIpAddress[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45014-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="45014-105">DESCRIPTION</span></span>
<span data-ttu-id="45014-106">Ip pubblico associato al firewall nell'hub virtuale</span><span class="sxs-lookup"><span data-stu-id="45014-106">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="45014-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="45014-107">EXAMPLES</span></span>

### <span data-ttu-id="45014-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="45014-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallHubPublicIpAddress -Count 2
```

<span data-ttu-id="45014-109">Verranno creati 2 ip pubblici nel firewall collegato all'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="45014-109">This will create 2 public ips on the firewall attached to the virtual hub.</span></span> <span data-ttu-id="45014-110">L'indirizzo IP verrà creato nel back-end. Non è possibile fornire gli ipaddress in modo esplicito per un nuovo firewall.</span><span class="sxs-lookup"><span data-stu-id="45014-110">This will create the ip address in the backend.We cannot provide the ipaddresses explicitly for a new firewall.</span></span>

### <span data-ttu-id="45014-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="45014-111">Example 2</span></span>
```powershell
PS C:\> $publicIp1 = New-AzFirewallPublicIpAddress -Address 10.2.3.4
PS C:\> $publicIp2 = New-AzFirewallPublicIpAddress -Address 20.56.37.46
PS C:\> New-AzFirewallHubPublicIpAddress -Count 3 -Addresses $publicIp1, $publicIp2
```

<span data-ttu-id="45014-112">Verrà creato 1 nuovo ip pubblico nel firewall conservando $publicIp 1, $publicIp 2 già esistenti nel firewall.</span><span class="sxs-lookup"><span data-stu-id="45014-112">This will create 1 new public ip on the firewall by retain $publicIp1, $publicIp2 which are already exist on the firewall.</span></span>

## <span data-ttu-id="45014-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45014-113">PARAMETERS</span></span>

### <span data-ttu-id="45014-114">-Addresses</span><span class="sxs-lookup"><span data-stu-id="45014-114">-Addresses</span></span>
<span data-ttu-id="45014-115">Gli indirizzi IP pubblici del firewall collegati a un hub</span><span class="sxs-lookup"><span data-stu-id="45014-115">The Public IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="45014-116">-Count</span><span class="sxs-lookup"><span data-stu-id="45014-116">-Count</span></span>
<span data-ttu-id="45014-117">Il numero di indirizzi IP pubblici</span><span class="sxs-lookup"><span data-stu-id="45014-117">The count of public Ip addresses</span></span>

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

### <span data-ttu-id="45014-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45014-118">-DefaultProfile</span></span>
<span data-ttu-id="45014-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="45014-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45014-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45014-120">CommonParameters</span></span>
<span data-ttu-id="45014-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45014-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45014-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="45014-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45014-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="45014-123">INPUTS</span></span>

### <span data-ttu-id="45014-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="45014-124">None</span></span>

## <span data-ttu-id="45014-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="45014-125">OUTPUTS</span></span>

### <span data-ttu-id="45014-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span><span class="sxs-lookup"><span data-stu-id="45014-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span></span>

## <span data-ttu-id="45014-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="45014-127">NOTES</span></span>

## <span data-ttu-id="45014-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="45014-128">RELATED LINKS</span></span>
