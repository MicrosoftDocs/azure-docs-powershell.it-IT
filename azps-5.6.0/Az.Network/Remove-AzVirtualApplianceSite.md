---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
ms.openlocfilehash: 1456acb101302297e807d6d46bf83183e8a6e523
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006125"
---
# <span data-ttu-id="dc98c-101">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="dc98c-101">Remove-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="dc98c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc98c-102">SYNOPSIS</span></span>
<span data-ttu-id="dc98c-103">Rimuovere un sito di appliance virtuali da una risorsa Appliance virtuale di rete.</span><span class="sxs-lookup"><span data-stu-id="dc98c-103">Remove a virtual appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="dc98c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dc98c-104">SYNTAX</span></span>

### <span data-ttu-id="dc98c-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dc98c-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzVirtualApplianceSite -Name <String> -NetworkVirtualApplianceId <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dc98c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc98c-106">ResourceIdParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc98c-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc98c-107">ResourceObjectParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -VirtualApplianceSite <PSVirtualApplianceSite> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc98c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dc98c-108">DESCRIPTION</span></span>
<span data-ttu-id="dc98c-109">Il Remove-AzVirtualApplianceSite rimuove un sito appliance virtuale da una risorsa Appliance virtuali di rete.</span><span class="sxs-lookup"><span data-stu-id="dc98c-109">The Remove-AzVirtualApplianceSite command removes a Virtual Appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="dc98c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dc98c-110">EXAMPLES</span></span>

### <span data-ttu-id="dc98c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dc98c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="dc98c-112">Eliminare una risorsa del sito Appliance virtuale.</span><span class="sxs-lookup"><span data-stu-id="dc98c-112">Delete a Virtual Appliance site resource.</span></span> 

## <span data-ttu-id="dc98c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc98c-113">PARAMETERS</span></span>

### <span data-ttu-id="dc98c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc98c-114">-AsJob</span></span>
<span data-ttu-id="dc98c-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="dc98c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dc98c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc98c-116">-DefaultProfile</span></span>
<span data-ttu-id="dc98c-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dc98c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc98c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="dc98c-118">-Force</span></span>
<span data-ttu-id="dc98c-119">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="dc98c-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="dc98c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="dc98c-120">-Name</span></span>
<span data-ttu-id="dc98c-121">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="dc98c-121">The resource name.</span></span>

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

### <span data-ttu-id="dc98c-122">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="dc98c-122">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="dc98c-123">ID risorsa dell'appliance virtuale di rete associato al sito.</span><span class="sxs-lookup"><span data-stu-id="dc98c-123">The resource ID of the Network Virtual Appliance associated with this site.</span></span>

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

### <span data-ttu-id="dc98c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc98c-124">-PassThru</span></span>
<span data-ttu-id="dc98c-125">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="dc98c-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="dc98c-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="dc98c-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dc98c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc98c-127">-ResourceGroupName</span></span>
<span data-ttu-id="dc98c-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dc98c-128">The resource group name.</span></span>

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

### <span data-ttu-id="dc98c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc98c-129">-ResourceId</span></span>
<span data-ttu-id="dc98c-130">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="dc98c-130">The resource id.</span></span>

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

### <span data-ttu-id="dc98c-131">-VirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="dc98c-131">-VirtualApplianceSite</span></span>
<span data-ttu-id="dc98c-132">Oggetto sito dell'appliance virtuale.</span><span class="sxs-lookup"><span data-stu-id="dc98c-132">The virtual appliance site object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc98c-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc98c-133">-Confirm</span></span>
<span data-ttu-id="dc98c-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc98c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc98c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc98c-135">-WhatIf</span></span>
<span data-ttu-id="dc98c-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dc98c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc98c-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dc98c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc98c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc98c-138">CommonParameters</span></span>
<span data-ttu-id="dc98c-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc98c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc98c-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dc98c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc98c-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="dc98c-141">INPUTS</span></span>

### <span data-ttu-id="dc98c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="dc98c-142">System.String</span></span>

### <span data-ttu-id="dc98c-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="dc98c-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="dc98c-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dc98c-144">OUTPUTS</span></span>

### <span data-ttu-id="dc98c-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dc98c-145">System.Boolean</span></span>

## <span data-ttu-id="dc98c-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="dc98c-146">NOTES</span></span>

## <span data-ttu-id="dc98c-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dc98c-147">RELATED LINKS</span></span>
