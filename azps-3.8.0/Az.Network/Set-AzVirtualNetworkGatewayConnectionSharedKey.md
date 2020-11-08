---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78BADAF3-6001-4A25-A74D-F6B50079FCB4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnectionsharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnectionSharedKey.md
ms.openlocfilehash: e1623f645c9a45d0b92b682646b0821729fce6fc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018618"
---
# <span data-ttu-id="37043-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="37043-101">Set-AzVirtualNetworkGatewayConnectionSharedKey</span></span>

## <span data-ttu-id="37043-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="37043-102">SYNOPSIS</span></span>
<span data-ttu-id="37043-103">Configura la chiave condivisa della connessione Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="37043-103">Configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="37043-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="37043-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkGatewayConnectionSharedKey -Name <String> -ResourceGroupName <String> -Value <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37043-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37043-105">DESCRIPTION</span></span>
<span data-ttu-id="37043-106">Il cmdlet **set-AzVirtualNetworkGatewayConnectionSharedKey** configura la chiave condivisa della connessione Virtual Network Gateway.</span><span class="sxs-lookup"><span data-stu-id="37043-106">The **Set-AzVirtualNetworkGatewayConnectionSharedKey** cmdlet configures the shared key of the virtual network gateway connection.</span></span>

## <span data-ttu-id="37043-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="37043-107">EXAMPLES</span></span>

### <span data-ttu-id="37043-108">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="37043-108">Example 1:</span></span>
```
PS C:\Users\alzam> Set-AzVirtualNetworkGatewayConnectionSharedKey -ResourceGroupName VPNGatewayV3 -Name VNet1toVNet2 -Value abcd1234

Confirm
Are you sure you want to overwrite resource 'VNet1toVNet2'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
abcd1234
```

## <span data-ttu-id="37043-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="37043-109">PARAMETERS</span></span>

### <span data-ttu-id="37043-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37043-110">-DefaultProfile</span></span>
<span data-ttu-id="37043-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="37043-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37043-112">-Force</span><span class="sxs-lookup"><span data-stu-id="37043-112">-Force</span></span>
<span data-ttu-id="37043-113">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="37043-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="37043-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="37043-114">-Name</span></span>
<span data-ttu-id="37043-115">Specifica il nome della chiave condivisa del gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="37043-115">Specifies the name of the virtual network gateway shared key.</span></span>

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

### <span data-ttu-id="37043-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37043-116">-ResourceGroupName</span></span>
<span data-ttu-id="37043-117">Specifica il nome del gruppo di risorse a cui appartiene il gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="37043-117">Specifies the name of the resource group that the virtual network gateway belongs to</span></span>

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

### <span data-ttu-id="37043-118">-Valore</span><span class="sxs-lookup"><span data-stu-id="37043-118">-Value</span></span>
<span data-ttu-id="37043-119">Specifica il valore della chiave condivisa.</span><span class="sxs-lookup"><span data-stu-id="37043-119">Specifies the value of the shared key.</span></span>

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

### <span data-ttu-id="37043-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="37043-120">-Confirm</span></span>
<span data-ttu-id="37043-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37043-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37043-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37043-122">-WhatIf</span></span>
<span data-ttu-id="37043-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37043-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37043-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="37043-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37043-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37043-125">CommonParameters</span></span>
<span data-ttu-id="37043-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37043-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37043-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37043-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37043-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="37043-128">INPUTS</span></span>

### <span data-ttu-id="37043-129">System. String</span><span class="sxs-lookup"><span data-stu-id="37043-129">System.String</span></span>

## <span data-ttu-id="37043-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="37043-130">OUTPUTS</span></span>

### <span data-ttu-id="37043-131">System. String</span><span class="sxs-lookup"><span data-stu-id="37043-131">System.String</span></span>

## <span data-ttu-id="37043-132">Note</span><span class="sxs-lookup"><span data-stu-id="37043-132">NOTES</span></span>

## <span data-ttu-id="37043-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="37043-133">RELATED LINKS</span></span>

[<span data-ttu-id="37043-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="37043-134">Get-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Get-AzVirtualNetworkGatewayConnectionSharedKey.md)

[<span data-ttu-id="37043-135">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span><span class="sxs-lookup"><span data-stu-id="37043-135">Reset-AzVirtualNetworkGatewayConnectionSharedKey</span></span>](./Reset-AzVirtualNetworkGatewayConnectionSharedKey.md)
