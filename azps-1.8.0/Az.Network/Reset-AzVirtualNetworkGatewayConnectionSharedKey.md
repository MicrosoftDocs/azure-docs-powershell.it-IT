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
ms.locfileid: "93678034"
---
# <span data-ttu-id="af43a-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="af43a-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="af43a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="af43a-102">SYNOPSIS</span></span>
<span data-ttu-id="af43a-103">Reimposta la chiave condivisa della connessione del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="af43a-103">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="af43a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af43a-104">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -KeyLength <UInt32>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af43a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af43a-105">DESCRIPTION</span></span>
<span data-ttu-id="af43a-106">Reimposta la chiave condivisa della connessione del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="af43a-106">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="af43a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af43a-107">EXAMPLES</span></span>

### <span data-ttu-id="af43a-108">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="af43a-108">Example 1:</span></span>
```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName myRG -Name myConnection -KeyLength 32

Confirm
Are you sure you want to overwrite resource 'myConnection'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
h0FmZA3BzXHqRE00J0wie0Mti0cCZwJm
```

## <span data-ttu-id="af43a-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="af43a-109">PARAMETERS</span></span>

### <span data-ttu-id="af43a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af43a-110">-DefaultProfile</span></span>
<span data-ttu-id="af43a-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="af43a-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af43a-112">-Force</span><span class="sxs-lookup"><span data-stu-id="af43a-112">-Force</span></span>
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

### <span data-ttu-id="af43a-113">-Lunghezza</span><span class="sxs-lookup"><span data-stu-id="af43a-113">-KeyLength</span></span>
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

### <span data-ttu-id="af43a-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="af43a-114">-Name</span></span>
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

### <span data-ttu-id="af43a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af43a-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="af43a-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="af43a-116">-Confirm</span></span>
<span data-ttu-id="af43a-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af43a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af43a-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af43a-118">-WhatIf</span></span>
<span data-ttu-id="af43a-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af43a-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af43a-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af43a-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af43a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af43a-121">CommonParameters</span></span>
<span data-ttu-id="af43a-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af43a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af43a-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af43a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af43a-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="af43a-124">INPUTS</span></span>

### <span data-ttu-id="af43a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="af43a-125">System.String</span></span>

### <span data-ttu-id="af43a-126">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="af43a-126">System.UInt32</span></span>

## <span data-ttu-id="af43a-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af43a-127">OUTPUTS</span></span>

### <span data-ttu-id="af43a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="af43a-128">System.String</span></span>

## <span data-ttu-id="af43a-129">Note</span><span class="sxs-lookup"><span data-stu-id="af43a-129">NOTES</span></span>

## <span data-ttu-id="af43a-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af43a-130">RELATED LINKS</span></span>

[<span data-ttu-id="af43a-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="af43a-131">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="af43a-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="af43a-132">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)
