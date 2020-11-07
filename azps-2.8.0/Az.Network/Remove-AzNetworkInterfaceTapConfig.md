---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 8ad89a0f5fad61fea2ba898ea17f63b6f935ae84
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854250"
---
# <span data-ttu-id="adaab-101">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="adaab-101">Remove-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="adaab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="adaab-102">SYNOPSIS</span></span>
<span data-ttu-id="adaab-103">Rimuove una configurazione di tocco dall'interfaccia di rete specificata</span><span class="sxs-lookup"><span data-stu-id="adaab-103">Removes a tap configuration from given network interface</span></span>

## <span data-ttu-id="adaab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="adaab-104">SYNTAX</span></span>

### <span data-ttu-id="adaab-105">RemoveByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="adaab-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adaab-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="adaab-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="adaab-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="adaab-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -InputObject <PSNetworkInterfaceTapConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adaab-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="adaab-108">DESCRIPTION</span></span>
<span data-ttu-id="adaab-109">Il cmdlet **Remove-AzNetworkInterfaceTapConfig** rimuove una configurazione di Azure tap da un elenco di interfacce di rete.</span><span class="sxs-lookup"><span data-stu-id="adaab-109">The **Remove-AzNetworkInterfaceTapConfig** cmdlet removes an Azure tap configuration from a network interface list.</span></span>

## <span data-ttu-id="adaab-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="adaab-110">EXAMPLES</span></span>

### <span data-ttu-id="adaab-111">Esempio 1: rimuovere una configurazione di tocco</span><span class="sxs-lookup"><span data-stu-id="adaab-111">Example 1: Remove a tap configuration</span></span>
```
PS C:\>Remove-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="adaab-112">Questo comando rimuove il TapConfiguration da NetworkInterface1 in un gruppo di risorse ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="adaab-112">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="adaab-113">Poiché il parametro *Force* non viene usato, all'utente verrà richiesto di confermare questa azione.</span><span class="sxs-lookup"><span data-stu-id="adaab-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="adaab-114">Esempio 2: rimuovere un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="adaab-114">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1" | Remove-AzNetworkInterfaceTapConfig -Force
```

<span data-ttu-id="adaab-115">Questo comando rimuove il TapConfiguration da NetworkInterface1 in un gruppo di risorse ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="adaab-115">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="adaab-116">Poiché viene usato il parametro *Force* , all'utente non viene richiesto di confermare.</span><span class="sxs-lookup"><span data-stu-id="adaab-116">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="adaab-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="adaab-117">PARAMETERS</span></span>

### <span data-ttu-id="adaab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adaab-118">-DefaultProfile</span></span>
<span data-ttu-id="adaab-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="adaab-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adaab-120">-Force</span><span class="sxs-lookup"><span data-stu-id="adaab-120">-Force</span></span>
<span data-ttu-id="adaab-121">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="adaab-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="adaab-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="adaab-122">-InputObject</span></span>
<span data-ttu-id="adaab-123">Riferimento a NetworkInterfaceTapConfig.</span><span class="sxs-lookup"><span data-stu-id="adaab-123">Reference to NetworkInterfaceTapConfig.</span></span>

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

### <span data-ttu-id="adaab-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="adaab-124">-Name</span></span>
<span data-ttu-id="adaab-125">Nome peer di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="adaab-125">The virtual network peering name.</span></span>

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

### <span data-ttu-id="adaab-126">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="adaab-126">-NetworkInterfaceName</span></span>
<span data-ttu-id="adaab-127">Nome della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="adaab-127">The virtual network name.</span></span>

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

### <span data-ttu-id="adaab-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="adaab-128">-PassThru</span></span>
<span data-ttu-id="adaab-129">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="adaab-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="adaab-130">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="adaab-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="adaab-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adaab-131">-ResourceGroupName</span></span>
<span data-ttu-id="adaab-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="adaab-132">The resource group name.</span></span>

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

### <span data-ttu-id="adaab-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="adaab-133">-ResourceId</span></span>
<span data-ttu-id="adaab-134">ID risorsa NetworkInterfaceTapConfig.</span><span class="sxs-lookup"><span data-stu-id="adaab-134">NetworkInterfaceTapConfig resource id.</span></span>

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

### <span data-ttu-id="adaab-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="adaab-135">-Confirm</span></span>
<span data-ttu-id="adaab-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adaab-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adaab-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adaab-137">-WhatIf</span></span>
<span data-ttu-id="adaab-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="adaab-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adaab-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="adaab-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adaab-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adaab-140">CommonParameters</span></span>
<span data-ttu-id="adaab-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adaab-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adaab-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adaab-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adaab-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="adaab-143">INPUTS</span></span>

### <span data-ttu-id="adaab-144">System. String</span><span class="sxs-lookup"><span data-stu-id="adaab-144">System.String</span></span>

### <span data-ttu-id="adaab-145">Microsoft. Azure. Commands. Network. Models. PSNetworkInterfaceTapConfiguration</span><span class="sxs-lookup"><span data-stu-id="adaab-145">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="adaab-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="adaab-146">OUTPUTS</span></span>

### <span data-ttu-id="adaab-147">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="adaab-147">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="adaab-148">Note</span><span class="sxs-lookup"><span data-stu-id="adaab-148">NOTES</span></span>

## <span data-ttu-id="adaab-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="adaab-149">RELATED LINKS</span></span>

[<span data-ttu-id="adaab-150">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="adaab-150">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="adaab-151">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="adaab-151">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="adaab-152">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="adaab-152">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
