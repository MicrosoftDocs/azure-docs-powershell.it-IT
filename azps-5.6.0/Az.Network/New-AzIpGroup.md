---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
ms.openlocfilehash: c8959d281c5eda7e2dd3f40941f5c727a000c588
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982397"
---
# <span data-ttu-id="1cc9f-101">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="1cc9f-101">New-AzIpGroup</span></span>

## <span data-ttu-id="1cc9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cc9f-102">SYNOPSIS</span></span>
<span data-ttu-id="1cc9f-103">Crea un IpGroup di Azure.</span><span class="sxs-lookup"><span data-stu-id="1cc9f-103">Creates an Azure IpGroup.</span></span>

## <span data-ttu-id="1cc9f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1cc9f-104">SYNTAX</span></span>

```
New-AzIpGroup -Name <String> -ResourceGroupName <String> [-IpAddress <String[]>] -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1cc9f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1cc9f-105">DESCRIPTION</span></span>
<span data-ttu-id="1cc9f-106">Il cmdlet **New-AzIpGroup** crea un Gruppo IpGroup di Azure</span><span class="sxs-lookup"><span data-stu-id="1cc9f-106">The **New-AzIpGroup** cmdlet creates an Azure IpGroup</span></span>

## <span data-ttu-id="1cc9f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1cc9f-107">EXAMPLES</span></span>

### <span data-ttu-id="1cc9f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1cc9f-108">Example 1</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US'
```

### <span data-ttu-id="1cc9f-109">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1cc9f-109">Example 2</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US' -IpAddress 10.0.0.0/24,11.9.0.0/24
```

## <span data-ttu-id="1cc9f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1cc9f-110">PARAMETERS</span></span>

### <span data-ttu-id="1cc9f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1cc9f-111">-AsJob</span></span>
<span data-ttu-id="1cc9f-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1cc9f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1cc9f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cc9f-113">-DefaultProfile</span></span>
<span data-ttu-id="1cc9f-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1cc9f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cc9f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1cc9f-115">-Force</span></span>
<span data-ttu-id="1cc9f-116">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="1cc9f-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="1cc9f-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="1cc9f-117">-IpAddress</span></span>
<span data-ttu-id="1cc9f-118">IpAddresses definito nel gruppo IpGroup</span><span class="sxs-lookup"><span data-stu-id="1cc9f-118">IpAddresses defined in the IpGroup</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cc9f-119">-Location</span><span class="sxs-lookup"><span data-stu-id="1cc9f-119">-Location</span></span>
<span data-ttu-id="1cc9f-120">Posizione.</span><span class="sxs-lookup"><span data-stu-id="1cc9f-120">The location.</span></span>

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

### <span data-ttu-id="1cc9f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1cc9f-121">-Name</span></span>
<span data-ttu-id="1cc9f-122">Nome del gruppo ipgroup.</span><span class="sxs-lookup"><span data-stu-id="1cc9f-122">The name of the ipgroup.</span></span>

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

### <span data-ttu-id="1cc9f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cc9f-123">-ResourceGroupName</span></span>
<span data-ttu-id="1cc9f-124">Nome del gruppo di risorse dell'ipgroup.</span><span class="sxs-lookup"><span data-stu-id="1cc9f-124">The resource group name of the ipgroup.</span></span>

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

### <span data-ttu-id="1cc9f-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="1cc9f-125">-Tag</span></span>
<span data-ttu-id="1cc9f-126">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="1cc9f-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="1cc9f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1cc9f-127">-Confirm</span></span>
<span data-ttu-id="1cc9f-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cc9f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cc9f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cc9f-129">-WhatIf</span></span>
<span data-ttu-id="1cc9f-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1cc9f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cc9f-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1cc9f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cc9f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cc9f-132">CommonParameters</span></span>
<span data-ttu-id="1cc9f-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cc9f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cc9f-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1cc9f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cc9f-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="1cc9f-135">INPUTS</span></span>

### <span data-ttu-id="1cc9f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="1cc9f-136">System.String</span></span>

### <span data-ttu-id="1cc9f-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="1cc9f-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="1cc9f-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1cc9f-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1cc9f-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1cc9f-139">OUTPUTS</span></span>

### <span data-ttu-id="1cc9f-140">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="1cc9f-140">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="1cc9f-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="1cc9f-141">NOTES</span></span>

## <span data-ttu-id="1cc9f-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1cc9f-142">RELATED LINKS</span></span>
