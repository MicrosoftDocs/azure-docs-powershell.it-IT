---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
ms.openlocfilehash: 75315de4e6ca2cf799f6cefb1d3b9c143631f5a3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021180"
---
# <span data-ttu-id="23b3a-101">New-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="23b3a-101">New-AzVirtualRouter</span></span>

## <span data-ttu-id="23b3a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="23b3a-102">SYNOPSIS</span></span>
<span data-ttu-id="23b3a-103">Crea un VirtualRouter di Azure.</span><span class="sxs-lookup"><span data-stu-id="23b3a-103">Creates an Azure VirtualRouter.</span></span>

## <span data-ttu-id="23b3a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="23b3a-104">SYNTAX</span></span>

### <span data-ttu-id="23b3a-105">HostedGatewayParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="23b3a-105">HostedGatewayParameterSet (Default)</span></span>
```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedGateway <PSVirtualNetworkGateway>
 -Location <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23b3a-106">HostedGatewayIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23b3a-106">HostedGatewayIdParameterSet</span></span>
```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedGatewayId <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="23b3a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23b3a-107">DESCRIPTION</span></span>
<span data-ttu-id="23b3a-108">Il cmdlet **New-AzVirtualRouter** crea un VirtualRouter di Azure</span><span class="sxs-lookup"><span data-stu-id="23b3a-108">The **New-AzVirtualRouter** cmdlet creates an Azure VirtualRouter</span></span>


## <span data-ttu-id="23b3a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="23b3a-109">EXAMPLES</span></span>

### <span data-ttu-id="23b3a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="23b3a-110">Example 1</span></span>
```powershell
$gatewayId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualNetworkGateways/erGateway'
New-AzVirtualRouter -RouterName virtualRouter -ResourceGroupName virtualRouterRG -Location 'West US'  -HostedGatewayId $gatewayId
```

### <span data-ttu-id="23b3a-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="23b3a-111">Example 2</span></span>
```powershell
$gateway = Get-AzVirtualNetworkGateway -Name erGateway -ResourceGroupName virtualRouterRG
New-AzVirtualRouter -RouterName virtualRouter -ResourceGroupName virtualRouterRG -Location 'West US'  -HostedGateway $gateway
```

## <span data-ttu-id="23b3a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="23b3a-112">PARAMETERS</span></span>

### <span data-ttu-id="23b3a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23b3a-113">-AsJob</span></span>
<span data-ttu-id="23b3a-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="23b3a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="23b3a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23b3a-115">-DefaultProfile</span></span>
<span data-ttu-id="23b3a-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="23b3a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23b3a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="23b3a-117">-Force</span></span>
<span data-ttu-id="23b3a-118">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="23b3a-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="23b3a-119">-HostedGateway</span><span class="sxs-lookup"><span data-stu-id="23b3a-119">-HostedGateway</span></span>
<span data-ttu-id="23b3a-120">Il gateway in cui è necessario ospitare il router virtuale.</span><span class="sxs-lookup"><span data-stu-id="23b3a-120">The gateway where Virtual Router needs to be hosted.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: HostedGatewayParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23b3a-121">-HostedGatewayId</span><span class="sxs-lookup"><span data-stu-id="23b3a-121">-HostedGatewayId</span></span>
<span data-ttu-id="23b3a-122">ID del gateway in cui è necessario ospitare il router virtuale.</span><span class="sxs-lookup"><span data-stu-id="23b3a-122">The id of gateway where Virtual Router needs to be hosted.</span></span>

```yaml
Type: String
Parameter Sets: HostedGatewayIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23b3a-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="23b3a-123">-Location</span></span>
<span data-ttu-id="23b3a-124">La posizione.</span><span class="sxs-lookup"><span data-stu-id="23b3a-124">The location.</span></span>

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

### <span data-ttu-id="23b3a-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="23b3a-125">-Name</span></span>
<span data-ttu-id="23b3a-126">Nome del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="23b3a-126">The name of the virtual router.</span></span>

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

### <span data-ttu-id="23b3a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23b3a-127">-ResourceGroupName</span></span>
<span data-ttu-id="23b3a-128">Il nome del gruppo di risorse del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="23b3a-128">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="23b3a-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="23b3a-129">-Tag</span></span>
<span data-ttu-id="23b3a-130">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="23b3a-130">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23b3a-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="23b3a-131">-Confirm</span></span>
<span data-ttu-id="23b3a-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23b3a-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23b3a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23b3a-133">-WhatIf</span></span>
<span data-ttu-id="23b3a-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="23b3a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23b3a-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="23b3a-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23b3a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23b3a-136">CommonParameters</span></span>
<span data-ttu-id="23b3a-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23b3a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="23b3a-138">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23b3a-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23b3a-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="23b3a-139">INPUTS</span></span>

### <span data-ttu-id="23b3a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="23b3a-140">System.String</span></span>

### <span data-ttu-id="23b3a-141">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="23b3a-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="23b3a-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="23b3a-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="23b3a-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="23b3a-143">OUTPUTS</span></span>

### <span data-ttu-id="23b3a-144">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="23b3a-144">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="23b3a-145">Note</span><span class="sxs-lookup"><span data-stu-id="23b3a-145">NOTES</span></span>

## <span data-ttu-id="23b3a-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="23b3a-146">RELATED LINKS</span></span>
