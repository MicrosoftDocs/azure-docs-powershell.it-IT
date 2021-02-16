---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: fa4c6db39de9f0d27fa80c4ee09e4decb319e2aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179871"
---
# <span data-ttu-id="38d47-101">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="38d47-101">Get-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="38d47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38d47-102">SYNOPSIS</span></span>
<span data-ttu-id="38d47-103">Ottiene una risorsa di configurazione Tocco.</span><span class="sxs-lookup"><span data-stu-id="38d47-103">Gets a Tap configuration resource.</span></span>

## <span data-ttu-id="38d47-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38d47-104">SYNTAX</span></span>

### <span data-ttu-id="38d47-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="38d47-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38d47-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="38d47-106">GetByResourceIdParameterSet</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38d47-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="38d47-107">DESCRIPTION</span></span>
<span data-ttu-id="38d47-108">Il cmdlet **Get-AzNetworkInterfaceTapConfig** ottiene una configurazione di Azure Tap per un determinato gruppo di risorse, un'interfaccia di rete e il nome di configurazione o un elenco di configurazioni di tocco in un gruppo di risorse e un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="38d47-108">The **Get-AzNetworkInterfaceTapConfig** cmdlet gets an Azure Tap Configuration for a given resource group, network interface and tap configuration name or list of tap configurations in a resource group and network interface.</span></span>

## <span data-ttu-id="38d47-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38d47-109">EXAMPLES</span></span>

### <span data-ttu-id="38d47-110">Esempio 1: Ottenere tutte le configurazioni di tocco per una determinata interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="38d47-110">Example 1: Get all tap configurations for a given network interface</span></span>
```
PS C:\> Get-AzNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

<span data-ttu-id="38d47-111">Questo comando consente di aggiungere le configurazioni di tocco per l'interfaccia di rete specificata.</span><span class="sxs-lookup"><span data-stu-id="38d47-111">This command gets tap configurations added for the given network interface.</span></span>

### <span data-ttu-id="38d47-112">Esempio 2: Ottenere una determinata configurazione di tocco</span><span class="sxs-lookup"><span data-stu-id="38d47-112">Example 2: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

<span data-ttu-id="38d47-113">Questo comando viene aggiunto alla configurazione della tocco specifica per l'interfaccia di rete specificata.</span><span class="sxs-lookup"><span data-stu-id="38d47-113">This command gets specific tap configuration added for the given network interface.</span></span>

### <span data-ttu-id="38d47-114">Esempio 3: Ottenere una determinata configurazione di tocco</span><span class="sxs-lookup"><span data-stu-id="38d47-114">Example 3: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfig*"
```

<span data-ttu-id="38d47-115">Questo comando consente di aggiungere le configurazioni di tocco per l'interfaccia di rete specificata con il nome che inizia con "tapconfig".</span><span class="sxs-lookup"><span data-stu-id="38d47-115">This command gets tap configurations added for the given network interface with name starting with "tapconfig".</span></span>

## <span data-ttu-id="38d47-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38d47-116">PARAMETERS</span></span>

### <span data-ttu-id="38d47-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38d47-117">-DefaultProfile</span></span>
<span data-ttu-id="38d47-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38d47-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38d47-119">-Name</span><span class="sxs-lookup"><span data-stu-id="38d47-119">-Name</span></span>
<span data-ttu-id="38d47-120">Nome della configurazione di tocco specifica.</span><span class="sxs-lookup"><span data-stu-id="38d47-120">Name of the specific tap configuration.</span></span>

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

### <span data-ttu-id="38d47-121">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="38d47-121">-NetworkInterfaceName</span></span>
<span data-ttu-id="38d47-122">Nome dell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="38d47-122">The Network Interface name.</span></span>

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

### <span data-ttu-id="38d47-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38d47-123">-ResourceGroupName</span></span>
<span data-ttu-id="38d47-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="38d47-124">The resource group name.</span></span>

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

### <span data-ttu-id="38d47-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38d47-125">-ResourceId</span></span>
<span data-ttu-id="38d47-126">ResourceId della risorsa TapConfiguration</span><span class="sxs-lookup"><span data-stu-id="38d47-126">ResourceId of the TapConfiguration resource</span></span>

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

### <span data-ttu-id="38d47-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38d47-127">-Confirm</span></span>
<span data-ttu-id="38d47-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38d47-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38d47-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38d47-129">-WhatIf</span></span>
<span data-ttu-id="38d47-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38d47-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="38d47-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38d47-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38d47-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38d47-132">CommonParameters</span></span>
<span data-ttu-id="38d47-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38d47-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38d47-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="38d47-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38d47-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="38d47-135">INPUTS</span></span>

### <span data-ttu-id="38d47-136">System.String</span><span class="sxs-lookup"><span data-stu-id="38d47-136">System.String</span></span>

## <span data-ttu-id="38d47-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38d47-137">OUTPUTS</span></span>

### <span data-ttu-id="38d47-138">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="38d47-138">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="38d47-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="38d47-139">NOTES</span></span>

## <span data-ttu-id="38d47-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38d47-140">RELATED LINKS</span></span>

[<span data-ttu-id="38d47-141">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="38d47-141">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="38d47-142">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="38d47-142">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="38d47-143">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="38d47-143">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
