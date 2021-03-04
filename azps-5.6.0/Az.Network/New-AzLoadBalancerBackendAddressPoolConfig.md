---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/powershell/module/az.network/new-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 805afd046505f6b1f6695205e858c6215c57ec7a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955790"
---
# <span data-ttu-id="e82c0-101">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e82c0-101">New-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="e82c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e82c0-102">SYNOPSIS</span></span>
<span data-ttu-id="e82c0-103">Crea una configurazione del pool di indirizzi back-end per una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e82c0-103">Creates a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="e82c0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e82c0-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e82c0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e82c0-105">DESCRIPTION</span></span>
<span data-ttu-id="e82c0-106">Il cmdlet **New-AzLoadBalancerBackendAddressPoolConfig crea** una configurazione del pool di indirizzi back-end per una bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="e82c0-106">The **New-AzLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="e82c0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e82c0-107">EXAMPLES</span></span>

### <span data-ttu-id="e82c0-108">Esempio 1: Creare una configurazione del pool di indirizzi back-end per un servizio di bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="e82c0-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="e82c0-109">Questo comando crea una configurazione del pool di indirizzi back-end denominata BackendAddressPool02 per una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e82c0-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="e82c0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e82c0-110">PARAMETERS</span></span>

### <span data-ttu-id="e82c0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e82c0-111">-DefaultProfile</span></span>
<span data-ttu-id="e82c0-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e82c0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e82c0-113">-Name</span><span class="sxs-lookup"><span data-stu-id="e82c0-113">-Name</span></span>
<span data-ttu-id="e82c0-114">Specifica il nome della configurazione del pool di indirizzi da creare.</span><span class="sxs-lookup"><span data-stu-id="e82c0-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="e82c0-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e82c0-115">-Confirm</span></span>
<span data-ttu-id="e82c0-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e82c0-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e82c0-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e82c0-117">-WhatIf</span></span>
<span data-ttu-id="e82c0-118">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e82c0-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e82c0-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e82c0-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e82c0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e82c0-120">CommonParameters</span></span>
<span data-ttu-id="e82c0-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e82c0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e82c0-122">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e82c0-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e82c0-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="e82c0-123">INPUTS</span></span>

### <span data-ttu-id="e82c0-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e82c0-124">None</span></span>

## <span data-ttu-id="e82c0-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e82c0-125">OUTPUTS</span></span>

### <span data-ttu-id="e82c0-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e82c0-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="e82c0-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="e82c0-127">NOTES</span></span>

## <span data-ttu-id="e82c0-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e82c0-128">RELATED LINKS</span></span>

[<span data-ttu-id="e82c0-129">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e82c0-129">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="e82c0-130">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e82c0-130">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="e82c0-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e82c0-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


