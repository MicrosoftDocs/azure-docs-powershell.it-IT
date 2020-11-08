---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubPublicIpAddress.md
ms.openlocfilehash: fc60a983e06e632912e43291f7b60980ff34a8cd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192816"
---
# <span data-ttu-id="14b8b-101">New-AzFirewallHubPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="14b8b-101">New-AzFirewallHubPublicIpAddress</span></span>

## <span data-ttu-id="14b8b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="14b8b-102">SYNOPSIS</span></span>
<span data-ttu-id="14b8b-103">Assoicated IP pubblici al firewall nell'hub virtuale</span><span class="sxs-lookup"><span data-stu-id="14b8b-103">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="14b8b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14b8b-104">SYNTAX</span></span>

```
New-AzFirewallHubPublicIpAddress [-Count <Int32>] [-Addresses <PSAzureFirewallPublicIpAddress[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14b8b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14b8b-105">DESCRIPTION</span></span>
<span data-ttu-id="14b8b-106">Assoicated IP pubblici al firewall nell'hub virtuale</span><span class="sxs-lookup"><span data-stu-id="14b8b-106">Public Ip assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="14b8b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14b8b-107">EXAMPLES</span></span>

### <span data-ttu-id="14b8b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="14b8b-108">Example 1</span></span>
```powershell
PS C:\> New-AzFirewallHubPublicIpAddress -Count 2
```

<span data-ttu-id="14b8b-109">In questo modo verranno creati 2 IPS pubblici sul firewall collegato all'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="14b8b-109">This will create 2 public ips on the firewall attached to the virtual hub.</span></span> <span data-ttu-id="14b8b-110">In questo modo verrà creato l'indirizzo IP nel backend. Non è possibile specificare in modo esplicito i IPAddress per un nuovo firewall.</span><span class="sxs-lookup"><span data-stu-id="14b8b-110">This will create the ip address in the backend.We cannot provide the ipaddresses explicitly for a new firewall.</span></span>

### <span data-ttu-id="14b8b-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="14b8b-111">Example 2</span></span>
```powershell
PS C:\> $publicIp1 = New-AzFirewallPublicIpAddress -Address 10.2.3.4
PS C:\> $publicIp2 = New-AzFirewallPublicIpAddress -Address 20.56.37.46
PS C:\> New-AzFirewallHubPublicIpAddress -Count 3 -Addresses $publicIp1, $publicIp2
```

<span data-ttu-id="14b8b-112">In questo modo verrà creato un nuovo IP pubblico sul firewall mantenendo $publicIp 1, $publicIp 2 già presenti nel firewall.</span><span class="sxs-lookup"><span data-stu-id="14b8b-112">This will create 1 new public ip on the firewall by retain $publicIp1, $publicIp2 which are already exist on the firewall.</span></span>

## <span data-ttu-id="14b8b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="14b8b-113">PARAMETERS</span></span>

### <span data-ttu-id="14b8b-114">-Indirizzi</span><span class="sxs-lookup"><span data-stu-id="14b8b-114">-Addresses</span></span>
<span data-ttu-id="14b8b-115">Indirizzi IP pubblici del firewall allegato a un hub</span><span class="sxs-lookup"><span data-stu-id="14b8b-115">The Public IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="14b8b-116">-Conteggio</span><span class="sxs-lookup"><span data-stu-id="14b8b-116">-Count</span></span>
<span data-ttu-id="14b8b-117">Conteggio degli indirizzi IP pubblici</span><span class="sxs-lookup"><span data-stu-id="14b8b-117">The count of public Ip addresses</span></span>

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

### <span data-ttu-id="14b8b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14b8b-118">-DefaultProfile</span></span>
<span data-ttu-id="14b8b-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="14b8b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14b8b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14b8b-120">CommonParameters</span></span>
<span data-ttu-id="14b8b-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14b8b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14b8b-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14b8b-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14b8b-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="14b8b-123">INPUTS</span></span>

### <span data-ttu-id="14b8b-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="14b8b-124">None</span></span>

## <span data-ttu-id="14b8b-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14b8b-125">OUTPUTS</span></span>

### <span data-ttu-id="14b8b-126">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallHubPublicIpAddresses</span><span class="sxs-lookup"><span data-stu-id="14b8b-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubPublicIpAddresses</span></span>

## <span data-ttu-id="14b8b-127">Note</span><span class="sxs-lookup"><span data-stu-id="14b8b-127">NOTES</span></span>

## <span data-ttu-id="14b8b-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14b8b-128">RELATED LINKS</span></span>