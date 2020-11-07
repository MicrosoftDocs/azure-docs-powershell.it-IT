---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 1fa793396fba139d1aa08e760c9aa780f8e0f166
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854174"
---
# <span data-ttu-id="db4a0-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="db4a0-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="db4a0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db4a0-102">SYNOPSIS</span></span>
<span data-ttu-id="db4a0-103">Reimposta la chiave condivisa della connessione del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="db4a0-103">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="db4a0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db4a0-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -KeyLength <UInt32>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db4a0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db4a0-105">DESCRIPTION</span></span>
<span data-ttu-id="db4a0-106">Reimposta la chiave condivisa della connessione del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="db4a0-106">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="db4a0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db4a0-107">EXAMPLES</span></span>

### <span data-ttu-id="db4a0-108">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="db4a0-108">Example 1:</span></span>
```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName myRG -Name myConnection -KeyLength 32

Confirm
Are you sure you want to overwrite resource 'myConnection'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
h0FmZA3BzXHqRE00J0wie0Mti0cCZwJm
```

## <span data-ttu-id="db4a0-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db4a0-109">PARAMETERS</span></span>

### <span data-ttu-id="db4a0-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db4a0-110">-DefaultProfile</span></span>
<span data-ttu-id="db4a0-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db4a0-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db4a0-112">-Force</span><span class="sxs-lookup"><span data-stu-id="db4a0-112">-Force</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db4a0-113">-Lunghezza</span><span class="sxs-lookup"><span data-stu-id="db4a0-113">-KeyLength</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db4a0-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="db4a0-114">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db4a0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db4a0-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="db4a0-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="db4a0-116">-Confirm</span></span>
<span data-ttu-id="db4a0-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db4a0-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db4a0-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db4a0-118">-WhatIf</span></span>
<span data-ttu-id="db4a0-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db4a0-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db4a0-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db4a0-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db4a0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db4a0-121">CommonParameters</span></span>
<span data-ttu-id="db4a0-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db4a0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db4a0-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db4a0-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db4a0-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db4a0-124">INPUTS</span></span>

### <span data-ttu-id="db4a0-125">System. String</span><span class="sxs-lookup"><span data-stu-id="db4a0-125">System.String</span></span>

### <span data-ttu-id="db4a0-126">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="db4a0-126">System.UInt32</span></span>

## <span data-ttu-id="db4a0-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db4a0-127">OUTPUTS</span></span>

### <span data-ttu-id="db4a0-128">System. String</span><span class="sxs-lookup"><span data-stu-id="db4a0-128">System.String</span></span>

## <span data-ttu-id="db4a0-129">Note</span><span class="sxs-lookup"><span data-stu-id="db4a0-129">NOTES</span></span>

## <span data-ttu-id="db4a0-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db4a0-130">RELATED LINKS</span></span>

[<span data-ttu-id="db4a0-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="db4a0-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="db4a0-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="db4a0-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
