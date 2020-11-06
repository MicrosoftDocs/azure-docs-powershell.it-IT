---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/reset-azurermvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: a805145445f8bd17ac60497e2c7d7e89ea56a3c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521421"
---
# <span data-ttu-id="30dc0-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="30dc0-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="30dc0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="30dc0-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30dc0-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30dc0-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="30dc0-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30dc0-104">DESCRIPTION</span></span>

## <span data-ttu-id="30dc0-105">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30dc0-105">EXAMPLES</span></span>

## <span data-ttu-id="30dc0-106">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="30dc0-106">PARAMETERS</span></span>

### <span data-ttu-id="30dc0-107">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30dc0-107">-DefaultProfile</span></span>
<span data-ttu-id="30dc0-108">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="30dc0-108">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30dc0-109">-Force</span><span class="sxs-lookup"><span data-stu-id="30dc0-109">-Force</span></span>
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

### <span data-ttu-id="30dc0-110">-Lunghezza</span><span class="sxs-lookup"><span data-stu-id="30dc0-110">-KeyLength</span></span>
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

### <span data-ttu-id="30dc0-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="30dc0-111">-Name</span></span>
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

### <span data-ttu-id="30dc0-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30dc0-112">-ResourceGroupName</span></span>
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

### <span data-ttu-id="30dc0-113">-Confermare</span><span class="sxs-lookup"><span data-stu-id="30dc0-113">-Confirm</span></span>
<span data-ttu-id="30dc0-114">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30dc0-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30dc0-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30dc0-115">-WhatIf</span></span>
<span data-ttu-id="30dc0-116">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30dc0-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30dc0-117">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30dc0-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30dc0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30dc0-118">CommonParameters</span></span>
<span data-ttu-id="30dc0-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30dc0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30dc0-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30dc0-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30dc0-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="30dc0-121">INPUTS</span></span>

### <span data-ttu-id="30dc0-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="30dc0-122">None</span></span>
<span data-ttu-id="30dc0-123">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="30dc0-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="30dc0-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30dc0-124">OUTPUTS</span></span>

### <span data-ttu-id="30dc0-125">System. String</span><span class="sxs-lookup"><span data-stu-id="30dc0-125">System.String</span></span>

## <span data-ttu-id="30dc0-126">Note</span><span class="sxs-lookup"><span data-stu-id="30dc0-126">NOTES</span></span>

## <span data-ttu-id="30dc0-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30dc0-127">RELATED LINKS</span></span>

[<span data-ttu-id="30dc0-128">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="30dc0-128">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="30dc0-129">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="30dc0-129">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


