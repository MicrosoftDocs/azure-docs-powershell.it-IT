---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: abeeabcc3930a2f18822dbf3d9986e17fbc01c88
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993647"
---
# <span data-ttu-id="32cb1-101">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="32cb1-101">Remove-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="32cb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32cb1-102">SYNOPSIS</span></span>
<span data-ttu-id="32cb1-103">Rimuove una configurazione IP dell'interfaccia di rete da un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="32cb1-103">Removes a network interface IP configuration from a network interface.</span></span>

## <span data-ttu-id="32cb1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32cb1-104">SYNTAX</span></span>

```
Remove-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32cb1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="32cb1-105">DESCRIPTION</span></span>
<span data-ttu-id="32cb1-106">Il cmdlet **Remove-AzNetworkInterfaceIpConfig rimuove** una configurazione IP dell'interfaccia di rete da un'interfaccia di rete di Azure.</span><span class="sxs-lookup"><span data-stu-id="32cb1-106">The **Remove-AzNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="32cb1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32cb1-107">EXAMPLES</span></span>

### <span data-ttu-id="32cb1-108">Esempio 1: Eliminare una configurazione IP da un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="32cb1-108">Example 1: Delete an IP configuration from a network interface</span></span>
```powershell
$nic = Get-AzNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic

Set-AzNetworkInterface -NetworkInterface $nic
```

<span data-ttu-id="32cb1-109">Il primo comando ottiene un'interfaccia di rete denominata mynic e la archivia nella variabile $nic.</span><span class="sxs-lookup"><span data-stu-id="32cb1-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="32cb1-110">Il secondo comando rimuove la configurazione IP denominata IPConfig-1 associata a questa interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="32cb1-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span> <span data-ttu-id="32cb1-111">Il terzo comando imposta le modifiche apportate all'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="32cb1-111">The third command sets changes made to the network interface.</span></span>

## <span data-ttu-id="32cb1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32cb1-112">PARAMETERS</span></span>

### <span data-ttu-id="32cb1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32cb1-113">-DefaultProfile</span></span>
<span data-ttu-id="32cb1-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="32cb1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32cb1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="32cb1-115">-Name</span></span>
<span data-ttu-id="32cb1-116">Specifica il nome della configurazione IP dell'interfaccia di rete da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="32cb1-116">Specifies the name of the network interface IP configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32cb1-117">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="32cb1-117">-NetworkInterface</span></span>
<span data-ttu-id="32cb1-118">Specifica un **oggetto NetworkInterface.**</span><span class="sxs-lookup"><span data-stu-id="32cb1-118">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="32cb1-119">Questo oggetto contiene la configurazione IP dell'interfaccia di rete da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="32cb1-119">This object contains the network interface IP configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32cb1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32cb1-120">CommonParameters</span></span>
<span data-ttu-id="32cb1-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32cb1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32cb1-122">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32cb1-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32cb1-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="32cb1-123">INPUTS</span></span>

### <span data-ttu-id="32cb1-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="32cb1-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="32cb1-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32cb1-125">OUTPUTS</span></span>

### <span data-ttu-id="32cb1-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="32cb1-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="32cb1-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="32cb1-127">NOTES</span></span>
* <span data-ttu-id="32cb1-128">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, rete, rete</span><span class="sxs-lookup"><span data-stu-id="32cb1-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="32cb1-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32cb1-129">RELATED LINKS</span></span>

[<span data-ttu-id="32cb1-130">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="32cb1-130">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="32cb1-131">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="32cb1-131">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="32cb1-132">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="32cb1-132">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="32cb1-133">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="32cb1-133">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


