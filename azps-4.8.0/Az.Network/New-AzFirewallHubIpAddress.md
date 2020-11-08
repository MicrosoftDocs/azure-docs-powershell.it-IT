---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallhubipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallHubIpAddress.md
ms.openlocfilehash: efb3641f5c2a06ea64eed8d8b92e5e032a0809df
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192811"
---
# <span data-ttu-id="3e643-101">New-AzFirewallHubIpAddress</span><span class="sxs-lookup"><span data-stu-id="3e643-101">New-AzFirewallHubIpAddress</span></span>

## <span data-ttu-id="3e643-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3e643-102">SYNOPSIS</span></span>
<span data-ttu-id="3e643-103">Indirizzi IP assoicated al firewall nell'hub virtuale</span><span class="sxs-lookup"><span data-stu-id="3e643-103">Ip addresses assoicated to the firewall on virtual hub</span></span>

## <span data-ttu-id="3e643-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e643-104">SYNTAX</span></span>

```
New-AzFirewallHubIpAddress [-PrivateIPAddress <String>] [-PublicIPs <PSAzureFirewallHubPublicIpAddresses>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e643-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e643-105">DESCRIPTION</span></span>
<span data-ttu-id="3e643-106">Indirizzi IP assoicated al firewall nell'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="3e643-106">Ip addresses assoicated to the firewall on virtual hub.</span></span> <span data-ttu-id="3e643-107">Possono essere indirizzi pubblici e privati</span><span class="sxs-lookup"><span data-stu-id="3e643-107">These can be public and private addresses</span></span>

## <span data-ttu-id="3e643-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e643-108">EXAMPLES</span></span>

### <span data-ttu-id="3e643-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3e643-109">Example 1</span></span>
```powershell
PS C:\> $fwpips = New-AzFirewallHubPublicIpAddress -Count 2
PS C:\> New-AzFirewallHubIpAddress -PublicIPs $fwpips
```

<span data-ttu-id="3e643-110">Questo esempio crea un oggetto indirizzo IP Hub con un conteggio di 2 IP pubblici.</span><span class="sxs-lookup"><span data-stu-id="3e643-110">This example creates a Hub Ip address object with a count of 2 public IPs.</span></span> <span data-ttu-id="3e643-111">L'oggetto HubIPAddress viene ssociated al firewall nell'hub virtuale.</span><span class="sxs-lookup"><span data-stu-id="3e643-111">The HubIPAddress object is ssociated to the firewall on the virtual hub.</span></span>

## <span data-ttu-id="3e643-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3e643-112">PARAMETERS</span></span>

### <span data-ttu-id="3e643-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e643-113">-DefaultProfile</span></span>
<span data-ttu-id="3e643-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3e643-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e643-115">-PrivateIPAddress</span><span class="sxs-lookup"><span data-stu-id="3e643-115">-PrivateIPAddress</span></span>
<span data-ttu-id="3e643-116">Indirizzo IP privato del firewall allegato a un hub</span><span class="sxs-lookup"><span data-stu-id="3e643-116">The private Ip Address of the Firewall attached to a Hub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e643-117">-PublicIPs</span><span class="sxs-lookup"><span data-stu-id="3e643-117">-PublicIPs</span></span>
<span data-ttu-id="3e643-118">Indirizzi IP del firewall allegato a un hub</span><span class="sxs-lookup"><span data-stu-id="3e643-118">The IP Addresses of the Firewall attached to a hub</span></span>

```yaml
Type: PSAzureFirewallHubPublicIpAddresses
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e643-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3e643-119">-Confirm</span></span>
<span data-ttu-id="3e643-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e643-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e643-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e643-121">-WhatIf</span></span>
<span data-ttu-id="3e643-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e643-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3e643-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e643-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e643-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e643-124">CommonParameters</span></span>
<span data-ttu-id="3e643-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e643-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e643-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e643-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e643-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3e643-127">INPUTS</span></span>

### <span data-ttu-id="3e643-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3e643-128">None</span></span>

## <span data-ttu-id="3e643-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e643-129">OUTPUTS</span></span>

### <span data-ttu-id="3e643-130">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallHubIpAddresses</span><span class="sxs-lookup"><span data-stu-id="3e643-130">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallHubIpAddresses</span></span>

## <span data-ttu-id="3e643-131">Note</span><span class="sxs-lookup"><span data-stu-id="3e643-131">NOTES</span></span>

## <span data-ttu-id="3e643-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e643-132">RELATED LINKS</span></span>