---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPublicIpAddress.md
ms.openlocfilehash: c4bc5e9fcc7d0ca405a8031af29d16283f963ad2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202809"
---
# <span data-ttu-id="f4c0c-101">New-AzFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f4c0c-101">New-AzFirewallPublicIpAddress</span></span>

## <span data-ttu-id="f4c0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4c0c-102">SYNOPSIS</span></span>
<span data-ttu-id="f4c0c-103">Segnaposto per l'indirizzo IP che può essere usato per il pip multi-pip in Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-103">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="f4c0c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4c0c-104">SYNTAX</span></span>

```
New-AzFirewallPublicIpAddress [-Address <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4c0c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f4c0c-105">DESCRIPTION</span></span>
<span data-ttu-id="f4c0c-106">Segnaposto per l'indirizzo IP che può essere usato per il pip multi-pip in Azure Firewall.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-106">This is the placeholder for the Ip Address that can be used for multi pip on azure firewall.</span></span>

## <span data-ttu-id="f4c0c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4c0c-107">EXAMPLES</span></span>

### <span data-ttu-id="f4c0c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f4c0c-108">Example 1</span></span>
```powershell
PS C:\> $publicIp = New-AzFirewallPublicIpAddress -Address 20.2.3.4
```

<span data-ttu-id="f4c0c-109">$publicIp segnaposto per l'indirizzo IP 20.2.3.4</span><span class="sxs-lookup"><span data-stu-id="f4c0c-109">$publicIp will be the placeholder for the ip address 20.2.3.4</span></span>

## <span data-ttu-id="f4c0c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4c0c-110">PARAMETERS</span></span>

### <span data-ttu-id="f4c0c-111">-Address</span><span class="sxs-lookup"><span data-stu-id="f4c0c-111">-Address</span></span>
<span data-ttu-id="f4c0c-112">Gli indirizzi IP del firewall collegati a un hub</span><span class="sxs-lookup"><span data-stu-id="f4c0c-112">The IP Addresses of the Firewall attached to a hub</span></span>

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

### <span data-ttu-id="f4c0c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4c0c-113">-DefaultProfile</span></span>
<span data-ttu-id="f4c0c-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4c0c-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4c0c-115">-Confirm</span></span>
<span data-ttu-id="f4c0c-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4c0c-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4c0c-117">-WhatIf</span></span>
<span data-ttu-id="f4c0c-118">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4c0c-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4c0c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4c0c-120">CommonParameters</span></span>
<span data-ttu-id="f4c0c-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4c0c-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f4c0c-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4c0c-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="f4c0c-123">INPUTS</span></span>

### <span data-ttu-id="f4c0c-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f4c0c-124">None</span></span>

## <span data-ttu-id="f4c0c-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4c0c-125">OUTPUTS</span></span>

### <span data-ttu-id="f4c0c-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f4c0c-126">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPublicIpAddress</span></span>

## <span data-ttu-id="f4c0c-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="f4c0c-127">NOTES</span></span>

## <span data-ttu-id="f4c0c-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4c0c-128">RELATED LINKS</span></span>
