---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpGroup.md
ms.openlocfilehash: 6ae61090f98cbb9929cc5ad1b2745fbf88f21a2a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189532"
---
# <span data-ttu-id="760f9-101">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="760f9-101">New-AzIpGroup</span></span>

## <span data-ttu-id="760f9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="760f9-102">SYNOPSIS</span></span>
<span data-ttu-id="760f9-103">Crea un IpGroup di Azure.</span><span class="sxs-lookup"><span data-stu-id="760f9-103">Creates an Azure IpGroup.</span></span>

## <span data-ttu-id="760f9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="760f9-104">SYNTAX</span></span>

```
New-AzIpGroup -Name <String> -ResourceGroupName <String> [-IpAddress <String[]>] -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="760f9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="760f9-105">DESCRIPTION</span></span>
<span data-ttu-id="760f9-106">Il cmdlet **New-AzIpGroup** crea un IpGroup di Azure</span><span class="sxs-lookup"><span data-stu-id="760f9-106">The **New-AzIpGroup** cmdlet creates an Azure IpGroup</span></span>

## <span data-ttu-id="760f9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="760f9-107">EXAMPLES</span></span>

### <span data-ttu-id="760f9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="760f9-108">Example 1</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US'
```

### <span data-ttu-id="760f9-109">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="760f9-109">Example 2</span></span>
```powershell
New-AzIpGroup -Name ipGroup -ResourceGroupName ipGroupRG -Location 'West US' -IpAddress 10.0.0.0/24,11.9.0.0/24
```

## <span data-ttu-id="760f9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="760f9-110">PARAMETERS</span></span>

### <span data-ttu-id="760f9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="760f9-111">-AsJob</span></span>
<span data-ttu-id="760f9-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="760f9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="760f9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="760f9-113">-DefaultProfile</span></span>
<span data-ttu-id="760f9-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="760f9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="760f9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="760f9-115">-Force</span></span>
<span data-ttu-id="760f9-116">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="760f9-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="760f9-117">-IpAddress</span><span class="sxs-lookup"><span data-stu-id="760f9-117">-IpAddress</span></span>
<span data-ttu-id="760f9-118">IpAddresses definiti in IpGroup</span><span class="sxs-lookup"><span data-stu-id="760f9-118">IpAddresses defined in the IpGroup</span></span>

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

### <span data-ttu-id="760f9-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="760f9-119">-Location</span></span>
<span data-ttu-id="760f9-120">La posizione.</span><span class="sxs-lookup"><span data-stu-id="760f9-120">The location.</span></span>

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

### <span data-ttu-id="760f9-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="760f9-121">-Name</span></span>
<span data-ttu-id="760f9-122">Il nome del ipgroup.</span><span class="sxs-lookup"><span data-stu-id="760f9-122">The name of the ipgroup.</span></span>

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

### <span data-ttu-id="760f9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="760f9-123">-ResourceGroupName</span></span>
<span data-ttu-id="760f9-124">Nome del gruppo di risorse di ipgroup.</span><span class="sxs-lookup"><span data-stu-id="760f9-124">The resource group name of the ipgroup.</span></span>

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

### <span data-ttu-id="760f9-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="760f9-125">-Tag</span></span>
<span data-ttu-id="760f9-126">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="760f9-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="760f9-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="760f9-127">-Confirm</span></span>
<span data-ttu-id="760f9-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="760f9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="760f9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="760f9-129">-WhatIf</span></span>
<span data-ttu-id="760f9-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="760f9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="760f9-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="760f9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="760f9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="760f9-132">CommonParameters</span></span>
<span data-ttu-id="760f9-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="760f9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="760f9-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="760f9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="760f9-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="760f9-135">INPUTS</span></span>

### <span data-ttu-id="760f9-136">System. String</span><span class="sxs-lookup"><span data-stu-id="760f9-136">System.String</span></span>

### <span data-ttu-id="760f9-137">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="760f9-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="760f9-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="760f9-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="760f9-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="760f9-139">OUTPUTS</span></span>

### <span data-ttu-id="760f9-140">Microsoft. Azure. Commands. Network. Models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="760f9-140">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="760f9-141">Note</span><span class="sxs-lookup"><span data-stu-id="760f9-141">NOTES</span></span>

## <span data-ttu-id="760f9-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="760f9-142">RELATED LINKS</span></span>
