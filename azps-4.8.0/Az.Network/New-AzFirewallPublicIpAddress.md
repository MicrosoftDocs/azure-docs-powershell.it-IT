---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
ms.openlocfilehash: c4bc5e9fcc7d0ca405a8031af29d16283f963ad2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189543"
---
# <span data-ttu-id="137d3-101">New-AzFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="137d3-101">New-AzFirewallPublicIpAddress</span></span>

## <span data-ttu-id="137d3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="137d3-102">SYNOPSIS</span></span>
<span data-ttu-id="137d3-103">Questo è il segnaposto per l'indirizzo IP che può essere usato per multi PIP in Azure firewall.</span><span class="sxs-lookup"><span data-stu-id="137d3-103">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="137d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="137d3-104">SYNTAX</span></span>

```
New-AzFirewallPublicIpAddress [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="137d3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="137d3-105">DESCRIPTION</span></span>
<span data-ttu-id="137d3-106">Questo è il segnaposto per l'indirizzo IP che può essere usato per multi PIP in Azure firewall.</span><span class="sxs-lookup"><span data-stu-id="137d3-106">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="137d3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="137d3-107">EXAMPLES</span></span>

### <span data-ttu-id="137d3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="137d3-108">Example 1</span></span>
```powershell
PS C:\> $publicIp = New-AzFirewallPublicIpAddress -Address 20.2.3.4
```

<span data-ttu-id="137d3-109">$publicIp sarà il segnaposto per l'indirizzo IP 20.2.3.4</span><span class="sxs-lookup"><span data-stu-id="137d3-109">$publicIp will be the placeholder for the ip address 20.2.3.4</span></span>

## <span data-ttu-id="137d3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="137d3-110">PARAMETERS</span></span>

### <span data-ttu-id="137d3-111">-Address</span><span class="sxs-lookup"><span data-stu-id="137d3-111">-Address</span></span>
<span data-ttu-id="137d3-112">Indirizzi IP del firewall allegato a un hub</span><span class="sxs-lookup"><span data-stu-id="137d3-112">The IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="137d3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="137d3-113">-DefaultProfile</span></span>
<span data-ttu-id="137d3-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="137d3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="137d3-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="137d3-115">-Confirm</span></span>
<span data-ttu-id="137d3-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="137d3-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="137d3-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="137d3-117">-WhatIf</span></span>
<span data-ttu-id="137d3-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="137d3-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="137d3-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="137d3-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="137d3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="137d3-120">CommonParameters</span></span>
<span data-ttu-id="137d3-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="137d3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="137d3-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="137d3-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="137d3-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="137d3-123">INPUTS</span></span>

### <span data-ttu-id="137d3-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="137d3-124">None</span></span>

## <span data-ttu-id="137d3-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="137d3-125">OUTPUTS</span></span>

### <span data-ttu-id="137d3-126">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="137d3-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPublicIpAddress</span></span>

## <span data-ttu-id="137d3-127">Note</span><span class="sxs-lookup"><span data-stu-id="137d3-127">NOTES</span></span>

## <span data-ttu-id="137d3-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="137d3-128">RELATED LINKS</span></span>
