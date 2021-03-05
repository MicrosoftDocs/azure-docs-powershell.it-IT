---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
ms.openlocfilehash: b75eb7e9bbac3efddc49bcccf384f288c01960a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996223"
---
# <span data-ttu-id="38c39-101">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="38c39-101">Remove-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="38c39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38c39-102">SYNOPSIS</span></span>
<span data-ttu-id="38c39-103">Rimuovere una risorsa Appliance virtuale di rete.</span><span class="sxs-lookup"><span data-stu-id="38c39-103">Remove a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="38c39-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38c39-104">SYNTAX</span></span>

### <span data-ttu-id="38c39-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="38c39-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38c39-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="38c39-106">ResourceIdParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38c39-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="38c39-107">ResourceObjectParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -NetworkVirtualAppliance <PSNetworkVirtualAppliance> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38c39-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="38c39-108">DESCRIPTION</span></span>
<span data-ttu-id="38c39-109">Il Remove-AzNetworkVirtualAppliance rimuove una risorsa Appliance virtuale di rete.</span><span class="sxs-lookup"><span data-stu-id="38c39-109">The Remove-AzNetworkVirtualAppliance command removes a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="38c39-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38c39-110">EXAMPLES</span></span>

### <span data-ttu-id="38c39-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="38c39-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
```

<span data-ttu-id="38c39-112">Eliminare una risorsa Appliance virtuale di rete.</span><span class="sxs-lookup"><span data-stu-id="38c39-112">Delete a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="38c39-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38c39-113">PARAMETERS</span></span>

### <span data-ttu-id="38c39-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38c39-114">-AsJob</span></span>
<span data-ttu-id="38c39-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="38c39-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38c39-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38c39-116">-DefaultProfile</span></span>
<span data-ttu-id="38c39-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38c39-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38c39-118">-Force</span><span class="sxs-lookup"><span data-stu-id="38c39-118">-Force</span></span>
<span data-ttu-id="38c39-119">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="38c39-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="38c39-120">-Name</span><span class="sxs-lookup"><span data-stu-id="38c39-120">-Name</span></span>
<span data-ttu-id="38c39-121">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="38c39-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38c39-122">-NetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="38c39-122">-NetworkVirtualAppliance</span></span>
<span data-ttu-id="38c39-123">Oggetto risorsa.</span><span class="sxs-lookup"><span data-stu-id="38c39-123">The resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38c39-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38c39-124">-PassThru</span></span>
<span data-ttu-id="38c39-125">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="38c39-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="38c39-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="38c39-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="38c39-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38c39-127">-ResourceGroupName</span></span>
<span data-ttu-id="38c39-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="38c39-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38c39-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38c39-129">-ResourceId</span></span>
<span data-ttu-id="38c39-130">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="38c39-130">The Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38c39-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38c39-131">-Confirm</span></span>
<span data-ttu-id="38c39-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38c39-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38c39-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38c39-133">-WhatIf</span></span>
<span data-ttu-id="38c39-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38c39-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38c39-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38c39-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38c39-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38c39-136">CommonParameters</span></span>
<span data-ttu-id="38c39-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38c39-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38c39-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="38c39-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38c39-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="38c39-139">INPUTS</span></span>

### <span data-ttu-id="38c39-140">System.String</span><span class="sxs-lookup"><span data-stu-id="38c39-140">System.String</span></span>

### <span data-ttu-id="38c39-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="38c39-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="38c39-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38c39-142">OUTPUTS</span></span>

### <span data-ttu-id="38c39-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="38c39-143">System.Boolean</span></span>

## <span data-ttu-id="38c39-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="38c39-144">NOTES</span></span>

## <span data-ttu-id="38c39-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38c39-145">RELATED LINKS</span></span>
