---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
ms.openlocfilehash: 9bfaea690ab23df6e7ba5480aaeb28ca00dfa20c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362683"
---
# <span data-ttu-id="b66db-101">New-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="b66db-101">New-AzVirtualRouter</span></span>

## <span data-ttu-id="b66db-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b66db-102">SYNOPSIS</span></span>
<span data-ttu-id="b66db-103">Crea un VirtualRouter di Azure.</span><span class="sxs-lookup"><span data-stu-id="b66db-103">Creates an Azure VirtualRouter.</span></span>

## <span data-ttu-id="b66db-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b66db-104">SYNTAX</span></span>

```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedSubnet <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b66db-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b66db-105">DESCRIPTION</span></span>
<span data-ttu-id="b66db-106">Il cmdlet **New-AzVirtualRouter** crea un VirtualRouter di Azure</span><span class="sxs-lookup"><span data-stu-id="b66db-106">The **New-AzVirtualRouter** cmdlet creates an Azure VirtualRouter</span></span>

## <span data-ttu-id="b66db-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b66db-107">EXAMPLES</span></span>

### <span data-ttu-id="b66db-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b66db-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.0.0/24
$vnet = New-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -AddressPrefix 10.0.0.0/16 -Subnet $subnet
$subnetId = (Get-AzVirtualNetworkSubnetConfig -Name $subnetName -VirtualNetwork $vnet).Id
New-AzVirtualRouter -Name $virtualRouterName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -HostedSubnet $subnetId
```

## <span data-ttu-id="b66db-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b66db-109">PARAMETERS</span></span>

### <span data-ttu-id="b66db-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b66db-110">-AsJob</span></span>
<span data-ttu-id="b66db-111">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b66db-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b66db-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b66db-112">-DefaultProfile</span></span>
<span data-ttu-id="b66db-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b66db-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b66db-114">-Force</span><span class="sxs-lookup"><span data-stu-id="b66db-114">-Force</span></span>
<span data-ttu-id="b66db-115">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="b66db-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b66db-116">-HostedSubnet</span><span class="sxs-lookup"><span data-stu-id="b66db-116">-HostedSubnet</span></span>
<span data-ttu-id="b66db-117">Subnet in cui è ospitato il router virtuale.</span><span class="sxs-lookup"><span data-stu-id="b66db-117">The subnet where the virtual router is hosted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b66db-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b66db-118">-Location</span></span>
<span data-ttu-id="b66db-119">La posizione.</span><span class="sxs-lookup"><span data-stu-id="b66db-119">The location.</span></span>

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

### <span data-ttu-id="b66db-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b66db-120">-Name</span></span>
<span data-ttu-id="b66db-121">Nome del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="b66db-121">The name of the virtual router.</span></span>

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

### <span data-ttu-id="b66db-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b66db-122">-ResourceGroupName</span></span>
<span data-ttu-id="b66db-123">Il nome del gruppo di risorse del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="b66db-123">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="b66db-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="b66db-124">-Tag</span></span>
<span data-ttu-id="b66db-125">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="b66db-125">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b66db-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b66db-126">-Confirm</span></span>
<span data-ttu-id="b66db-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b66db-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b66db-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b66db-128">-WhatIf</span></span>
<span data-ttu-id="b66db-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b66db-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b66db-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b66db-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b66db-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b66db-131">CommonParameters</span></span>
<span data-ttu-id="b66db-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b66db-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b66db-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b66db-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b66db-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b66db-134">INPUTS</span></span>

### <span data-ttu-id="b66db-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b66db-135">System.String</span></span>

### <span data-ttu-id="b66db-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b66db-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b66db-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b66db-137">OUTPUTS</span></span>

### <span data-ttu-id="b66db-138">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="b66db-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="b66db-139">Note</span><span class="sxs-lookup"><span data-stu-id="b66db-139">NOTES</span></span>

## <span data-ttu-id="b66db-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b66db-140">RELATED LINKS</span></span>
