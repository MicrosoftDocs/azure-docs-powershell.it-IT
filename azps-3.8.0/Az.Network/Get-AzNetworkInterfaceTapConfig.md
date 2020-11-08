---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: fa4c6db39de9f0d27fa80c4ee09e4decb319e2aa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021277"
---
# <span data-ttu-id="d877d-101">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="d877d-101">Get-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="d877d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d877d-102">SYNOPSIS</span></span>
<span data-ttu-id="d877d-103">Ottiene una risorsa di configurazione tap.</span><span class="sxs-lookup"><span data-stu-id="d877d-103">Gets a Tap configuration resource.</span></span>

## <span data-ttu-id="d877d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d877d-104">SYNTAX</span></span>

### <span data-ttu-id="d877d-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d877d-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d877d-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d877d-106">GetByResourceIdParameterSet</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d877d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d877d-107">DESCRIPTION</span></span>
<span data-ttu-id="d877d-108">Il cmdlet **Get-AzNetworkInterfaceTapConfig** ottiene una configurazione di Azure tap per un gruppo di risorse specifico, un'interfaccia di rete e un nome di configurazione di tocco o un elenco di configurazioni di tocco in un gruppo di risorse e in un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="d877d-108">The **Get-AzNetworkInterfaceTapConfig** cmdlet gets an Azure Tap Configuration for a given resource group, network interface and tap configuration name or list of tap configurations in a resource group and network interface.</span></span>

## <span data-ttu-id="d877d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d877d-109">EXAMPLES</span></span>

### <span data-ttu-id="d877d-110">Esempio 1: ottenere tutte le configurazioni di tocco per una determinata interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="d877d-110">Example 1: Get all tap configurations for a given network interface</span></span>
```
PS C:\> Get-AzNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

<span data-ttu-id="d877d-111">Questo comando ottiene il tocco delle configurazioni aggiunte per l'interfaccia di rete specificata.</span><span class="sxs-lookup"><span data-stu-id="d877d-111">This command gets tap configurations added for the given network interface.</span></span>

### <span data-ttu-id="d877d-112">Esempio 2: ottenere una configurazione di tocco specificata</span><span class="sxs-lookup"><span data-stu-id="d877d-112">Example 2: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

<span data-ttu-id="d877d-113">Con questo comando viene aggiunta una configurazione di tocco specifica per l'interfaccia di rete specificata.</span><span class="sxs-lookup"><span data-stu-id="d877d-113">This command gets specific tap configuration added for the given network interface.</span></span>

### <span data-ttu-id="d877d-114">Esempio 3: ottenere una configurazione di tocco specificata</span><span class="sxs-lookup"><span data-stu-id="d877d-114">Example 3: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfig*"
```

<span data-ttu-id="d877d-115">Questo comando ottiene il tocco delle configurazioni aggiunte per l'interfaccia di rete specificata con il nome che inizia con "tapconfig".</span><span class="sxs-lookup"><span data-stu-id="d877d-115">This command gets tap configurations added for the given network interface with name starting with "tapconfig".</span></span>

## <span data-ttu-id="d877d-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d877d-116">PARAMETERS</span></span>

### <span data-ttu-id="d877d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d877d-117">-DefaultProfile</span></span>
<span data-ttu-id="d877d-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d877d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d877d-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="d877d-119">-Name</span></span>
<span data-ttu-id="d877d-120">Nome della configurazione del tocco specifico.</span><span class="sxs-lookup"><span data-stu-id="d877d-120">Name of the specific tap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="d877d-121">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="d877d-121">-NetworkInterfaceName</span></span>
<span data-ttu-id="d877d-122">Nome dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="d877d-122">The Network Interface name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d877d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d877d-123">-ResourceGroupName</span></span>
<span data-ttu-id="d877d-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d877d-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d877d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d877d-125">-ResourceId</span></span>
<span data-ttu-id="d877d-126">ResourceId della risorsa TapConfiguration</span><span class="sxs-lookup"><span data-stu-id="d877d-126">ResourceId of the TapConfiguration resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d877d-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d877d-127">-Confirm</span></span>
<span data-ttu-id="d877d-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d877d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d877d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d877d-129">-WhatIf</span></span>
<span data-ttu-id="d877d-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d877d-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d877d-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d877d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d877d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d877d-132">CommonParameters</span></span>
<span data-ttu-id="d877d-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d877d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d877d-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d877d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d877d-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d877d-135">INPUTS</span></span>

### <span data-ttu-id="d877d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d877d-136">System.String</span></span>

## <span data-ttu-id="d877d-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d877d-137">OUTPUTS</span></span>

### <span data-ttu-id="d877d-138">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="d877d-138">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="d877d-139">Note</span><span class="sxs-lookup"><span data-stu-id="d877d-139">NOTES</span></span>

## <span data-ttu-id="d877d-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d877d-140">RELATED LINKS</span></span>

[<span data-ttu-id="d877d-141">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="d877d-141">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="d877d-142">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="d877d-142">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="d877d-143">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="d877d-143">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
