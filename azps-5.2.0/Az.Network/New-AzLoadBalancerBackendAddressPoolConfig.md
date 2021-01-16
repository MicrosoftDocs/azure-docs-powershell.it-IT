---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 7030fcef733b9bfb8e59f1bc79a373f89bddfc61
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341308"
---
# <span data-ttu-id="e0f96-101">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e0f96-101">New-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="e0f96-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e0f96-102">SYNOPSIS</span></span>
<span data-ttu-id="e0f96-103">Crea una configurazione del pool di indirizzi back-end per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e0f96-103">Creates a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="e0f96-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e0f96-104">SYNTAX</span></span>

```
New-AzLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0f96-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0f96-105">DESCRIPTION</span></span>
<span data-ttu-id="e0f96-106">Il cmdlet **New-AzLoadBalancerBackendAddressPoolConfig** crea una configurazione del pool di indirizzi back-end per un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="e0f96-106">The **New-AzLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="e0f96-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e0f96-107">EXAMPLES</span></span>

### <span data-ttu-id="e0f96-108">Esempio 1: creare una configurazione del pool di indirizzi back-end per un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="e0f96-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="e0f96-109">Questo comando crea una configurazione del pool di indirizzi back-end denominata BackendAddressPool02 per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e0f96-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="e0f96-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e0f96-110">PARAMETERS</span></span>

### <span data-ttu-id="e0f96-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0f96-111">-DefaultProfile</span></span>
<span data-ttu-id="e0f96-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e0f96-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0f96-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="e0f96-113">-Name</span></span>
<span data-ttu-id="e0f96-114">Specifica il nome della configurazione del pool di indirizzi da creare.</span><span class="sxs-lookup"><span data-stu-id="e0f96-114">Specifies the name of the address pool configuration to create.</span></span>

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

### <span data-ttu-id="e0f96-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e0f96-115">-Confirm</span></span>
<span data-ttu-id="e0f96-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0f96-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0f96-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0f96-117">-WhatIf</span></span>
<span data-ttu-id="e0f96-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0f96-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0f96-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0f96-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0f96-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0f96-120">CommonParameters</span></span>
<span data-ttu-id="e0f96-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0f96-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0f96-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0f96-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0f96-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e0f96-123">INPUTS</span></span>

### <span data-ttu-id="e0f96-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e0f96-124">None</span></span>

## <span data-ttu-id="e0f96-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e0f96-125">OUTPUTS</span></span>

### <span data-ttu-id="e0f96-126">Microsoft. Azure. Commands. Network. Models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="e0f96-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="e0f96-127">Note</span><span class="sxs-lookup"><span data-stu-id="e0f96-127">NOTES</span></span>

## <span data-ttu-id="e0f96-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e0f96-128">RELATED LINKS</span></span>

[<span data-ttu-id="e0f96-129">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e0f96-129">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="e0f96-130">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e0f96-130">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="e0f96-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e0f96-131">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


