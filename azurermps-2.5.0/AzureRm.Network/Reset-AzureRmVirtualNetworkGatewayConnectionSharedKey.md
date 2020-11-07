---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
ms.openlocfilehash: 160fb1b7455a2440773978ec80741922248a8af4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866986"
---
# <span data-ttu-id="fe627-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="fe627-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="fe627-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fe627-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe627-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fe627-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe627-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe627-104">DESCRIPTION</span></span>

## <span data-ttu-id="fe627-105">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fe627-105">EXAMPLES</span></span>

### <span data-ttu-id="fe627-106">1:</span><span class="sxs-lookup"><span data-stu-id="fe627-106">1:</span></span>
```

```

## <span data-ttu-id="fe627-107">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fe627-107">PARAMETERS</span></span>

### <span data-ttu-id="fe627-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe627-108">-DefaultProfile</span></span>
<span data-ttu-id="fe627-109">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fe627-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe627-110">-Force</span><span class="sxs-lookup"><span data-stu-id="fe627-110">-Force</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe627-111">-Lunghezza</span><span class="sxs-lookup"><span data-stu-id="fe627-111">-KeyLength</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe627-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="fe627-112">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe627-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe627-113">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe627-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fe627-114">-Confirm</span></span>
<span data-ttu-id="fe627-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe627-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe627-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe627-116">-WhatIf</span></span>
<span data-ttu-id="fe627-117">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe627-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe627-118">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe627-118">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe627-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe627-119">CommonParameters</span></span>
<span data-ttu-id="fe627-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe627-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe627-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe627-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe627-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fe627-122">INPUTS</span></span>

## <span data-ttu-id="fe627-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fe627-123">OUTPUTS</span></span>

### <span data-ttu-id="fe627-124">System. String</span><span class="sxs-lookup"><span data-stu-id="fe627-124">System.String</span></span>

## <span data-ttu-id="fe627-125">Note</span><span class="sxs-lookup"><span data-stu-id="fe627-125">NOTES</span></span>

## <span data-ttu-id="fe627-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fe627-126">RELATED LINKS</span></span>

[<span data-ttu-id="fe627-127">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="fe627-127">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="fe627-128">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="fe627-128">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


