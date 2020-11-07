---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/reset-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Reset-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 3519fd616be92e2404ef7b4d51241b675240470c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862886"
---
# <span data-ttu-id="68220-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="68220-101">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="68220-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="68220-102">SYNOPSIS</span></span>

## <span data-ttu-id="68220-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68220-103">SYNTAX</span></span>

```
Reset-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="68220-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68220-104">DESCRIPTION</span></span>

## <span data-ttu-id="68220-105">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68220-105">EXAMPLES</span></span>

### <span data-ttu-id="68220-106">1:</span><span class="sxs-lookup"><span data-stu-id="68220-106">1:</span></span>
```

```

## <span data-ttu-id="68220-107">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="68220-107">PARAMETERS</span></span>

### <span data-ttu-id="68220-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68220-108">-DefaultProfile</span></span>
<span data-ttu-id="68220-109">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="68220-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68220-110">-Force</span><span class="sxs-lookup"><span data-stu-id="68220-110">-Force</span></span>
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

### <span data-ttu-id="68220-111">-Lunghezza</span><span class="sxs-lookup"><span data-stu-id="68220-111">-KeyLength</span></span>
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

### <span data-ttu-id="68220-112">-Nome</span><span class="sxs-lookup"><span data-stu-id="68220-112">-Name</span></span>
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

### <span data-ttu-id="68220-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68220-113">-ResourceGroupName</span></span>
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

### <span data-ttu-id="68220-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="68220-114">-Confirm</span></span>
<span data-ttu-id="68220-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68220-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68220-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68220-116">-WhatIf</span></span>
<span data-ttu-id="68220-117">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="68220-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68220-118">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="68220-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68220-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68220-119">CommonParameters</span></span>
<span data-ttu-id="68220-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68220-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68220-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68220-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68220-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="68220-122">INPUTS</span></span>

## <span data-ttu-id="68220-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68220-123">OUTPUTS</span></span>

### <span data-ttu-id="68220-124">System. String</span><span class="sxs-lookup"><span data-stu-id="68220-124">System.String</span></span>

## <span data-ttu-id="68220-125">Note</span><span class="sxs-lookup"><span data-stu-id="68220-125">NOTES</span></span>

## <span data-ttu-id="68220-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68220-126">RELATED LINKS</span></span>

[<span data-ttu-id="68220-127">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="68220-127">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="68220-128">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="68220-128">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzVirtualNetworkGatewayConnectionSharedKey.md)


