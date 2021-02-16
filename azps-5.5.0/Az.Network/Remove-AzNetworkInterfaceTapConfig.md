---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 52fc2a3c84c70d52c173bc256ca2b0d952307e91
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179479"
---
# <span data-ttu-id="586aa-101">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="586aa-101">Remove-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="586aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="586aa-102">SYNOPSIS</span></span>
<span data-ttu-id="586aa-103">Rimuove una configurazione di tocco da un'interfaccia di rete specifica</span><span class="sxs-lookup"><span data-stu-id="586aa-103">Removes a tap configuration from given network interface</span></span>

## <span data-ttu-id="586aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="586aa-104">SYNTAX</span></span>

### <span data-ttu-id="586aa-105">RemoveByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="586aa-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="586aa-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="586aa-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="586aa-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="586aa-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -InputObject <PSNetworkInterfaceTapConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="586aa-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="586aa-108">DESCRIPTION</span></span>
<span data-ttu-id="586aa-109">Il cmdlet **Remove-AzNetworkInterfaceTapConfig rimuove** una configurazione di Azure Tap da un elenco di interfacce di rete.</span><span class="sxs-lookup"><span data-stu-id="586aa-109">The **Remove-AzNetworkInterfaceTapConfig** cmdlet removes an Azure tap configuration from a network interface list.</span></span>

## <span data-ttu-id="586aa-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="586aa-110">EXAMPLES</span></span>

### <span data-ttu-id="586aa-111">Esempio 1: Rimuovere una configurazione di tocco</span><span class="sxs-lookup"><span data-stu-id="586aa-111">Example 1: Remove a tap configuration</span></span>
```
PS C:\>Remove-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="586aa-112">Questo comando rimuove TapConfiguration da NetworkInterface1 in un gruppo di risorse ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="586aa-112">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="586aa-113">Poiché il *parametro Force* non viene usato, all'utente verrà chiesto di confermare l'azione.</span><span class="sxs-lookup"><span data-stu-id="586aa-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="586aa-114">Esempio 2: Rimuovere un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="586aa-114">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1" | Remove-AzNetworkInterfaceTapConfig -Force
```

<span data-ttu-id="586aa-115">Questo comando rimuove TapConfiguration da NetworkInterface1 in un gruppo di risorse ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="586aa-115">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="586aa-116">Poiché viene *usato* il parametro Force, all'utente non viene richiesta conferma.</span><span class="sxs-lookup"><span data-stu-id="586aa-116">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="586aa-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="586aa-117">PARAMETERS</span></span>

### <span data-ttu-id="586aa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="586aa-118">-DefaultProfile</span></span>
<span data-ttu-id="586aa-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="586aa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="586aa-120">-Force</span><span class="sxs-lookup"><span data-stu-id="586aa-120">-Force</span></span>
<span data-ttu-id="586aa-121">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="586aa-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="586aa-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="586aa-122">-InputObject</span></span>
<span data-ttu-id="586aa-123">Riferimento a NetworkInterfaceTapConfig.</span><span class="sxs-lookup"><span data-stu-id="586aa-123">Reference to NetworkInterfaceTapConfig.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="586aa-124">-Name</span><span class="sxs-lookup"><span data-stu-id="586aa-124">-Name</span></span>
<span data-ttu-id="586aa-125">Nome del peering della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="586aa-125">The virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="586aa-126">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="586aa-126">-NetworkInterfaceName</span></span>
<span data-ttu-id="586aa-127">Nome della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="586aa-127">The virtual network name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="586aa-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="586aa-128">-PassThru</span></span>
<span data-ttu-id="586aa-129">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="586aa-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="586aa-130">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="586aa-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="586aa-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="586aa-131">-ResourceGroupName</span></span>
<span data-ttu-id="586aa-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="586aa-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="586aa-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="586aa-133">-ResourceId</span></span>
<span data-ttu-id="586aa-134">ID risorsa NetworkInterfaceTapConfig.</span><span class="sxs-lookup"><span data-stu-id="586aa-134">NetworkInterfaceTapConfig resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="586aa-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="586aa-135">-Confirm</span></span>
<span data-ttu-id="586aa-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="586aa-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="586aa-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="586aa-137">-WhatIf</span></span>
<span data-ttu-id="586aa-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="586aa-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="586aa-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="586aa-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="586aa-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="586aa-140">CommonParameters</span></span>
<span data-ttu-id="586aa-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="586aa-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="586aa-142">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="586aa-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="586aa-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="586aa-143">INPUTS</span></span>

### <span data-ttu-id="586aa-144">System.String</span><span class="sxs-lookup"><span data-stu-id="586aa-144">System.String</span></span>

### <span data-ttu-id="586aa-145">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="586aa-145">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="586aa-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="586aa-146">OUTPUTS</span></span>

### <span data-ttu-id="586aa-147">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="586aa-147">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="586aa-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="586aa-148">NOTES</span></span>

## <span data-ttu-id="586aa-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="586aa-149">RELATED LINKS</span></span>

[<span data-ttu-id="586aa-150">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="586aa-150">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="586aa-151">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="586aa-151">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="586aa-152">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="586aa-152">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
