---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
ms.openlocfilehash: 2cb7bc759847af456286bfc611904922a26dc443
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207018"
---
# <span data-ttu-id="79e10-101">Add-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="79e10-101">Add-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="79e10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79e10-102">SYNOPSIS</span></span>
<span data-ttu-id="79e10-103">Aggiungere un peer a un VirtualRouter di Azure</span><span class="sxs-lookup"><span data-stu-id="79e10-103">Add a Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="79e10-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79e10-104">SYNTAX</span></span>

```
Add-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79e10-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="79e10-105">DESCRIPTION</span></span>
<span data-ttu-id="79e10-106">Il cmdlet **Add-AzVirtualRouterRouter Consente** di aggiungere un peer VirtualRouter a un peer Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="79e10-106">The **Add-AzVirtualRouterPeer** cmdlet adds a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="79e10-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79e10-107">EXAMPLES</span></span>

### <span data-ttu-id="79e10-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="79e10-108">Example 1</span></span>
```powershell
Add-AzVirtualRouterPeer 1ResourceGroupName virtualRouterRG -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="79e10-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79e10-109">PARAMETERS</span></span>

### <span data-ttu-id="79e10-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79e10-110">-AsJob</span></span>
<span data-ttu-id="79e10-111">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="79e10-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="79e10-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79e10-112">-DefaultProfile</span></span>
<span data-ttu-id="79e10-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="79e10-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79e10-114">-Force</span><span class="sxs-lookup"><span data-stu-id="79e10-114">-Force</span></span>
<span data-ttu-id="79e10-115">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="79e10-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="79e10-116">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="79e10-116">-PeerAsn</span></span>
<span data-ttu-id="79e10-117">Peer ASN.</span><span class="sxs-lookup"><span data-stu-id="79e10-117">Peer ASN.</span></span>

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

### <span data-ttu-id="79e10-118">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="79e10-118">-PeerIp</span></span>
<span data-ttu-id="79e10-119">Ip peer.</span><span class="sxs-lookup"><span data-stu-id="79e10-119">Peer Ip.</span></span>

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

### <span data-ttu-id="79e10-120">-PeerName</span><span class="sxs-lookup"><span data-stu-id="79e10-120">-PeerName</span></span>
<span data-ttu-id="79e10-121">Nome del peer del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="79e10-121">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="79e10-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79e10-122">-ResourceGroupName</span></span>
<span data-ttu-id="79e10-123">Nome del gruppo di risorse del router/peer virtuale.</span><span class="sxs-lookup"><span data-stu-id="79e10-123">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="79e10-124">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="79e10-124">-VirtualRouterName</span></span>
<span data-ttu-id="79e10-125">Router virtuale in cui esiste il peer.</span><span class="sxs-lookup"><span data-stu-id="79e10-125">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="79e10-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79e10-126">-Confirm</span></span>
<span data-ttu-id="79e10-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79e10-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79e10-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79e10-128">-WhatIf</span></span>
<span data-ttu-id="79e10-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79e10-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79e10-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79e10-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79e10-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79e10-131">CommonParameters</span></span>
<span data-ttu-id="79e10-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79e10-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79e10-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="79e10-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79e10-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="79e10-134">INPUTS</span></span>

### <span data-ttu-id="79e10-135">System.String</span><span class="sxs-lookup"><span data-stu-id="79e10-135">System.String</span></span>

### <span data-ttu-id="79e10-136">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="79e10-136">System.UInt32</span></span>

## <span data-ttu-id="79e10-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79e10-137">OUTPUTS</span></span>

### <span data-ttu-id="79e10-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="79e10-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="79e10-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="79e10-139">NOTES</span></span>

## <span data-ttu-id="79e10-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79e10-140">RELATED LINKS</span></span>
