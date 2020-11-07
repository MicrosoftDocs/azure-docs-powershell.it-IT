---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: e051bd56aa8c5b5da27e2179b8f4d58ec4e4196d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687788"
---
# <span data-ttu-id="2033d-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="2033d-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="2033d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2033d-102">SYNOPSIS</span></span>
<span data-ttu-id="2033d-103">Reimposta la chiave condivisa della connessione del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="2033d-103">Resets the shared key of the virtual network gateway connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2033d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2033d-104">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2033d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2033d-105">DESCRIPTION</span></span>
<span data-ttu-id="2033d-106">Reimposta la chiave condivisa della connessione del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="2033d-106">Resets the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="2033d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2033d-107">EXAMPLES</span></span>

### <span data-ttu-id="2033d-108">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="2033d-108">Example 1:</span></span>
```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName myRG -Name myConnection -KeyLength 32

Confirm
Are you sure you want to overwrite resource 'myConnection'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
h0FmZA3BzXHqRE00J0wie0Mti0cCZwJm
```

## <span data-ttu-id="2033d-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2033d-109">PARAMETERS</span></span>

### <span data-ttu-id="2033d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2033d-110">-DefaultProfile</span></span>
<span data-ttu-id="2033d-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2033d-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2033d-112">-Force</span><span class="sxs-lookup"><span data-stu-id="2033d-112">-Force</span></span>
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

### <span data-ttu-id="2033d-113">-Lunghezza</span><span class="sxs-lookup"><span data-stu-id="2033d-113">-KeyLength</span></span>
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

### <span data-ttu-id="2033d-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="2033d-114">-Name</span></span>
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

### <span data-ttu-id="2033d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2033d-115">-ResourceGroupName</span></span>
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

### <span data-ttu-id="2033d-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2033d-116">-Confirm</span></span>
<span data-ttu-id="2033d-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2033d-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2033d-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2033d-118">-WhatIf</span></span>
<span data-ttu-id="2033d-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2033d-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2033d-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2033d-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2033d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2033d-121">CommonParameters</span></span>
<span data-ttu-id="2033d-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2033d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2033d-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2033d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2033d-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2033d-124">INPUTS</span></span>

### <span data-ttu-id="2033d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="2033d-125">System.String</span></span>

### <span data-ttu-id="2033d-126">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="2033d-126">System.UInt32</span></span>

## <span data-ttu-id="2033d-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2033d-127">OUTPUTS</span></span>

### <span data-ttu-id="2033d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2033d-128">System.String</span></span>

## <span data-ttu-id="2033d-129">Note</span><span class="sxs-lookup"><span data-stu-id="2033d-129">NOTES</span></span>

## <span data-ttu-id="2033d-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2033d-130">RELATED LINKS</span></span>

[<span data-ttu-id="2033d-131">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="2033d-131">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="2033d-132">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="2033d-132">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


