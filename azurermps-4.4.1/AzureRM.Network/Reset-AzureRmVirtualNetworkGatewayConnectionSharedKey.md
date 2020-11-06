---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: AB370DAD-CED9-479D-BE08-B32EFF924A37
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: 65540c331074b5c140bafe9e87d625dfaec2f252
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522105"
---
# <span data-ttu-id="cb27f-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="cb27f-101">Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="cb27f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cb27f-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb27f-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cb27f-103">SYNTAX</span></span>

```
Reset-AzureRmVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String>
 -KeyLength <UInt32> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cb27f-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb27f-104">DESCRIPTION</span></span>

## <span data-ttu-id="cb27f-105">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cb27f-105">EXAMPLES</span></span>

## <span data-ttu-id="cb27f-106">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cb27f-106">PARAMETERS</span></span>

### <span data-ttu-id="cb27f-107">-Force</span><span class="sxs-lookup"><span data-stu-id="cb27f-107">-Force</span></span>
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

### <span data-ttu-id="cb27f-108">-Lunghezza</span><span class="sxs-lookup"><span data-stu-id="cb27f-108">-KeyLength</span></span>
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

### <span data-ttu-id="cb27f-109">-Nome</span><span class="sxs-lookup"><span data-stu-id="cb27f-109">-Name</span></span>
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

### <span data-ttu-id="cb27f-110">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb27f-110">-ResourceGroupName</span></span>
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

### <span data-ttu-id="cb27f-111">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cb27f-111">-Confirm</span></span>
<span data-ttu-id="cb27f-112">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb27f-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb27f-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb27f-113">-WhatIf</span></span>
<span data-ttu-id="cb27f-114">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cb27f-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb27f-115">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cb27f-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb27f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb27f-116">-DefaultProfile</span></span>
<span data-ttu-id="cb27f-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cb27f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb27f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb27f-118">CommonParameters</span></span>
<span data-ttu-id="cb27f-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb27f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb27f-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb27f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb27f-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cb27f-121">INPUTS</span></span>

## <span data-ttu-id="cb27f-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cb27f-122">OUTPUTS</span></span>

### <span data-ttu-id="cb27f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="cb27f-123">System.String</span></span>

## <span data-ttu-id="cb27f-124">Note</span><span class="sxs-lookup"><span data-stu-id="cb27f-124">NOTES</span></span>

## <span data-ttu-id="cb27f-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cb27f-125">RELATED LINKS</span></span>

[<span data-ttu-id="cb27f-126">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="cb27f-126">Get-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="cb27f-127">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="cb27f-127">Set-AzureRmVirtualNetworkGatewayConnectionSharedKey</span></span>](./Set-AzureRmVirtualNetworkGatewayConnectionSharedKey.md)


