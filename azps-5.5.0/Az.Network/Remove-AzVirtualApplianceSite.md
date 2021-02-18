---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
ms.openlocfilehash: 0b29719dee8a1e69d27dd36cee2888df4575eefc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202508"
---
# <span data-ttu-id="0a803-101">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="0a803-101">Remove-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="0a803-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a803-102">SYNOPSIS</span></span>
<span data-ttu-id="0a803-103">Rimuovere un sito di appliance virtuali da una risorsa Appliance virtuale di rete.</span><span class="sxs-lookup"><span data-stu-id="0a803-103">Remove a virtual appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="0a803-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0a803-104">SYNTAX</span></span>

### <span data-ttu-id="0a803-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0a803-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzVirtualApplianceSite -Name <String> -NetworkVirtualApplianceId <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a803-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a803-106">ResourceIdParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a803-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0a803-107">ResourceObjectParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -VirtualApplianceSite <PSVirtualApplianceSite> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a803-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0a803-108">DESCRIPTION</span></span>
<span data-ttu-id="0a803-109">Il Remove-AzVirtualApplianceSite rimuove un sito appliance virtuale da una risorsa Appliance virtuali di rete.</span><span class="sxs-lookup"><span data-stu-id="0a803-109">The Remove-AzVirtualApplianceSite command removes a Virtual Appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="0a803-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0a803-110">EXAMPLES</span></span>

### <span data-ttu-id="0a803-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0a803-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="0a803-112">Eliminare una risorsa del sito Appliance virtuale.</span><span class="sxs-lookup"><span data-stu-id="0a803-112">Delete a Virtual Appliance site resource.</span></span> 

## <span data-ttu-id="0a803-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a803-113">PARAMETERS</span></span>

### <span data-ttu-id="0a803-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a803-114">-AsJob</span></span>
<span data-ttu-id="0a803-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="0a803-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a803-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a803-116">-DefaultProfile</span></span>
<span data-ttu-id="0a803-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0a803-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a803-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0a803-118">-Force</span></span>
<span data-ttu-id="0a803-119">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="0a803-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0a803-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0a803-120">-Name</span></span>
<span data-ttu-id="0a803-121">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0a803-121">The resource name.</span></span>

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

### <span data-ttu-id="0a803-122">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="0a803-122">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="0a803-123">ID risorsa dell'appliance virtuale di rete associato al sito.</span><span class="sxs-lookup"><span data-stu-id="0a803-123">The resource ID of the Network Virtual Appliance associated with this site.</span></span>

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

### <span data-ttu-id="0a803-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a803-124">-PassThru</span></span>
<span data-ttu-id="0a803-125">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="0a803-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="0a803-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="0a803-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0a803-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a803-127">-ResourceGroupName</span></span>
<span data-ttu-id="0a803-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0a803-128">The resource group name.</span></span>

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

### <span data-ttu-id="0a803-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0a803-129">-ResourceId</span></span>
<span data-ttu-id="0a803-130">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0a803-130">The resource id.</span></span>

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

### <span data-ttu-id="0a803-131">-VirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="0a803-131">-VirtualApplianceSite</span></span>
<span data-ttu-id="0a803-132">Oggetto sito dell'appliance virtuale.</span><span class="sxs-lookup"><span data-stu-id="0a803-132">The virtual appliance site object.</span></span>

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

### <span data-ttu-id="0a803-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a803-133">-Confirm</span></span>
<span data-ttu-id="0a803-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a803-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a803-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a803-135">-WhatIf</span></span>
<span data-ttu-id="0a803-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0a803-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a803-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0a803-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a803-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a803-138">CommonParameters</span></span>
<span data-ttu-id="0a803-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a803-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a803-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0a803-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a803-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="0a803-141">INPUTS</span></span>

### <span data-ttu-id="0a803-142">System.String</span><span class="sxs-lookup"><span data-stu-id="0a803-142">System.String</span></span>

### <span data-ttu-id="0a803-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="0a803-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="0a803-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0a803-144">OUTPUTS</span></span>

### <span data-ttu-id="0a803-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0a803-145">System.Boolean</span></span>

## <span data-ttu-id="0a803-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="0a803-146">NOTES</span></span>

## <span data-ttu-id="0a803-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0a803-147">RELATED LINKS</span></span>
