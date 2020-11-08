---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
ms.openlocfilehash: ce0d27bb091192db8f1cbc157daf1bb847f869d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020478"
---
# <span data-ttu-id="11330-101">Add-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="11330-101">Add-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="11330-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="11330-102">SYNOPSIS</span></span>
<span data-ttu-id="11330-103">Aggiungere un peer a un VirtualRouter di Azure</span><span class="sxs-lookup"><span data-stu-id="11330-103">Add a Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="11330-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="11330-104">SYNTAX</span></span>

```
Add-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11330-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11330-105">DESCRIPTION</span></span>
<span data-ttu-id="11330-106">Il cmdlet **Add-AzVirtualRouterPeer** aggiunge un peer VirtualRouter a un VirtualRouter di Azure</span><span class="sxs-lookup"><span data-stu-id="11330-106">The **Add-AzVirtualRouterPeer** cmdlet adds a VirtualRouter Peer to an Azure VirtualRouter</span></span>


## <span data-ttu-id="11330-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="11330-107">EXAMPLES</span></span>

### <span data-ttu-id="11330-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="11330-108">Example 1</span></span>
```powershell
Add-AzVirtualRouterPeer 1ResourceGroupName virtualRouterRG -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="11330-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="11330-109">PARAMETERS</span></span>

### <span data-ttu-id="11330-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="11330-110">-AsJob</span></span>
<span data-ttu-id="11330-111">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="11330-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11330-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11330-112">-DefaultProfile</span></span>
<span data-ttu-id="11330-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="11330-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11330-114">-Force</span><span class="sxs-lookup"><span data-stu-id="11330-114">-Force</span></span>
<span data-ttu-id="11330-115">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="11330-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="11330-116">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="11330-116">-PeerAsn</span></span>
<span data-ttu-id="11330-117">Peer ASN.</span><span class="sxs-lookup"><span data-stu-id="11330-117">Peer ASN.</span></span>

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

### <span data-ttu-id="11330-118">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="11330-118">-PeerIp</span></span>
<span data-ttu-id="11330-119">IP peer.</span><span class="sxs-lookup"><span data-stu-id="11330-119">Peer Ip.</span></span>

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

### <span data-ttu-id="11330-120">-PeerName</span><span class="sxs-lookup"><span data-stu-id="11330-120">-PeerName</span></span>
<span data-ttu-id="11330-121">Nome del peer del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="11330-121">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="11330-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11330-122">-ResourceGroupName</span></span>
<span data-ttu-id="11330-123">Nome del gruppo di risorse del router virtuale/peer.</span><span class="sxs-lookup"><span data-stu-id="11330-123">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="11330-124">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="11330-124">-VirtualRouterName</span></span>
<span data-ttu-id="11330-125">Il router virtuale in cui esiste peer.</span><span class="sxs-lookup"><span data-stu-id="11330-125">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="11330-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="11330-126">-Confirm</span></span>
<span data-ttu-id="11330-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11330-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11330-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11330-128">-WhatIf</span></span>
<span data-ttu-id="11330-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="11330-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11330-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="11330-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11330-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11330-131">CommonParameters</span></span>
<span data-ttu-id="11330-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11330-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11330-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11330-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11330-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="11330-134">INPUTS</span></span>

### <span data-ttu-id="11330-135">System. String</span><span class="sxs-lookup"><span data-stu-id="11330-135">System.String</span></span>

### <span data-ttu-id="11330-136">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="11330-136">System.UInt32</span></span>

## <span data-ttu-id="11330-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="11330-137">OUTPUTS</span></span>

### <span data-ttu-id="11330-138">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="11330-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="11330-139">Note</span><span class="sxs-lookup"><span data-stu-id="11330-139">NOTES</span></span>

## <span data-ttu-id="11330-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="11330-140">RELATED LINKS</span></span>
