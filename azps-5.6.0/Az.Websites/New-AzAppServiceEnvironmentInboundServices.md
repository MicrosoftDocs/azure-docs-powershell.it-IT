---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azappserviceenvironmentinboundservices
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironmentInboundServices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzAppServiceEnvironmentInboundServices.md
ms.openlocfilehash: 68b2957e959365187ad82980bd2be2f055632a57
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002110"
---
# <span data-ttu-id="a6a67-101">New-AzAppServiceEnvironmentInboundServices</span><span class="sxs-lookup"><span data-stu-id="a6a67-101">New-AzAppServiceEnvironmentInboundServices</span></span>

## <span data-ttu-id="a6a67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6a67-102">SYNOPSIS</span></span>
<span data-ttu-id="a6a67-103">Crea servizi in ingresso per l'ambiente del servizio app.</span><span class="sxs-lookup"><span data-stu-id="a6a67-103">Creates inbound services for App Service Environment.</span></span> <span data-ttu-id="a6a67-104">Per ASEv2 ILB verrà creata un'area DNS privata di Azure e i record da mappare all'indirizzo IP interno.</span><span class="sxs-lookup"><span data-stu-id="a6a67-104">For ASEv2 ILB, this will create an Azure Private DNS Zone and records to map to the internal IP.</span></span> <span data-ttu-id="a6a67-105">Per ASEv3, inoltre, la subnet ha disabilitato i criteri di rete e creerà un endpoint privato.</span><span class="sxs-lookup"><span data-stu-id="a6a67-105">For ASEv3 it will in addition ensure subnet has Network Policy disabled and will create a private endpoint.</span></span>

## <span data-ttu-id="a6a67-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6a67-106">SYNTAX</span></span>

### <span data-ttu-id="a6a67-107">SubnetNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6a67-107">SubnetNameParameterSet</span></span>
```
New-AzAppServiceEnvironmentInboundServices [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkName <String> -SubnetName <String> [-SkipDns] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6a67-108">SubnetIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6a67-108">SubnetIdParameterSet</span></span>
```
New-AzAppServiceEnvironmentInboundServices [-ResourceGroupName] <String> [-Name] <String> -SubnetId <String>
 [-SkipDns] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6a67-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a6a67-109">DESCRIPTION</span></span>
<span data-ttu-id="a6a67-110">Il cmdlet **New-AzAppServiceEnvironmentInboundServices** crea servizi in ingresso per un ambiente del servizio app.</span><span class="sxs-lookup"><span data-stu-id="a6a67-110">The **New-AzAppServiceEnvironmentInboundServices** cmdlet create inbound services for an App Service Environment.</span></span>

## <span data-ttu-id="a6a67-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6a67-111">EXAMPLES</span></span>

### <span data-ttu-id="a6a67-112">Esempio 1: Creare record e un'area DNS privata per ASEv2</span><span class="sxs-lookup"><span data-stu-id="a6a67-112">Example 1: Create Private DNS Zone and records for ASEv2</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironmentInboundServices -ResourceGroupName AseResourceGroup -Name AseV2Name
-VirtualNetworkName MyVirtualNetwork -SubnetName InboundSubnet
```

<span data-ttu-id="a6a67-113">Creare record e zona DNS privati per ASEv2</span><span class="sxs-lookup"><span data-stu-id="a6a67-113">Create Private DNS Zone and records for ASEv2</span></span>

### <span data-ttu-id="a6a67-114">Esempio 2: Creare un endpoint privato, un'area DNS privata e record per ASEv3</span><span class="sxs-lookup"><span data-stu-id="a6a67-114">Example 2: Create private endpoint, Private DNS Zone and records for ASEv3</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironmentInboundServices -ResourceGroupName AseResourceGroup -Name AseV2Name
-VirtualNetworkName MyVirtualNetwork -SubnetName InboundSubnet
```

<span data-ttu-id="a6a67-115">Creare endpoint privati, zona DNS privata e record per ASEv3</span><span class="sxs-lookup"><span data-stu-id="a6a67-115">Create private endpoint, Private DNS Zone and records for ASEv3</span></span>

### <span data-ttu-id="a6a67-116">Esempio 3: Creare un endpoint privato per ASEv3</span><span class="sxs-lookup"><span data-stu-id="a6a67-116">Example 3: Create private endpoint for ASEv3</span></span>
```powershell
PS C:\> New-AzAppServiceEnvironmentInboundServices -ResourceGroupName AseResourceGroup -Name AseV2Name
-VirtualNetworkName MyVirtualNetwork -SubnetName InboundSubnet -SkipDns
```

<span data-ttu-id="a6a67-117">Creare un endpoint privato per ASEv3</span><span class="sxs-lookup"><span data-stu-id="a6a67-117">Create private endpoint for ASEv3</span></span>

## <span data-ttu-id="a6a67-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6a67-118">PARAMETERS</span></span>

### <span data-ttu-id="a6a67-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6a67-119">-DefaultProfile</span></span>
<span data-ttu-id="a6a67-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a6a67-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6a67-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a6a67-121">-Name</span></span>
<span data-ttu-id="a6a67-122">Nome dell'ambiente del servizio app.</span><span class="sxs-lookup"><span data-stu-id="a6a67-122">The name of the app service environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a67-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6a67-123">-PassThru</span></span>
<span data-ttu-id="a6a67-124">Stato reso.</span><span class="sxs-lookup"><span data-stu-id="a6a67-124">Return status.</span></span>

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

### <span data-ttu-id="a6a67-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6a67-125">-ResourceGroupName</span></span>
<span data-ttu-id="a6a67-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a6a67-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a67-127">-SkipDns</span><span class="sxs-lookup"><span data-stu-id="a6a67-127">-SkipDns</span></span>
<span data-ttu-id="a6a67-128">Non creare record e zona DNS privata di Azure.</span><span class="sxs-lookup"><span data-stu-id="a6a67-128">Do not create Azure Private DNS Zone and records.</span></span>

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

### <span data-ttu-id="a6a67-129">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="a6a67-129">-SubnetId</span></span>
<span data-ttu-id="a6a67-130">ID subnet.</span><span class="sxs-lookup"><span data-stu-id="a6a67-130">The subnet id.</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a67-131">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="a6a67-131">-SubnetName</span></span>
<span data-ttu-id="a6a67-132">Il nome della subnet.</span><span class="sxs-lookup"><span data-stu-id="a6a67-132">The subnet name.</span></span> <span data-ttu-id="a6a67-133">Usato in combinazione con -VirtualNetworkName e deve essere nello stesso gruppo di risorse di ASE.</span><span class="sxs-lookup"><span data-stu-id="a6a67-133">Used in combination with -VirtualNetworkName and must be in same resource group as ASE.</span></span> <span data-ttu-id="a6a67-134">In caso contrario, usa -SubnetId</span><span class="sxs-lookup"><span data-stu-id="a6a67-134">If not, use -SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a67-135">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="a6a67-135">-VirtualNetworkName</span></span>
<span data-ttu-id="a6a67-136">Il nome vNet.</span><span class="sxs-lookup"><span data-stu-id="a6a67-136">The vNet name.</span></span> <span data-ttu-id="a6a67-137">Usato in combinazione con -SubnetName e deve essere nello stesso gruppo di risorse di ASE.</span><span class="sxs-lookup"><span data-stu-id="a6a67-137">Used in combination with -SubnetName and must be in same resource group as ASE.</span></span> <span data-ttu-id="a6a67-138">In caso contrario, usa -SubnetId</span><span class="sxs-lookup"><span data-stu-id="a6a67-138">If not, use -SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: SubnetNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a67-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6a67-139">-Confirm</span></span>
<span data-ttu-id="a6a67-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6a67-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6a67-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6a67-141">-WhatIf</span></span>
<span data-ttu-id="a6a67-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6a67-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6a67-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6a67-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6a67-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6a67-144">CommonParameters</span></span>
<span data-ttu-id="a6a67-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6a67-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6a67-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a6a67-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6a67-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="a6a67-147">INPUTS</span></span>

### <span data-ttu-id="a6a67-148">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a6a67-148">None</span></span>

## <span data-ttu-id="a6a67-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6a67-149">OUTPUTS</span></span>

### <span data-ttu-id="a6a67-150">System.Object</span><span class="sxs-lookup"><span data-stu-id="a6a67-150">System.Object</span></span>
## <span data-ttu-id="a6a67-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="a6a67-151">NOTES</span></span>

## <span data-ttu-id="a6a67-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6a67-152">RELATED LINKS</span></span>

[<span data-ttu-id="a6a67-153">New-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="a6a67-153">New-AzAppServiceEnvironment</span></span>](./New-AzAppServiceEnvironment.md)

[<span data-ttu-id="a6a67-154">Get-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="a6a67-154">Get-AzAppServiceEnvironment</span></span>](./Get-AzAppServiceEnvironment.md)

[<span data-ttu-id="a6a67-155">Remove-AzAppServiceEnvironment</span><span class="sxs-lookup"><span data-stu-id="a6a67-155">Remove-AzAppServiceEnvironment</span></span>](./Remove-AzAppServiceEnvironment.md)