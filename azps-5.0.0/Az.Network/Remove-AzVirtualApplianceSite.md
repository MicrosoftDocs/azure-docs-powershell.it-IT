---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
ms.openlocfilehash: 0b29719dee8a1e69d27dd36cee2888df4575eefc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203092"
---
# <span data-ttu-id="0592e-101">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="0592e-101">Remove-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="0592e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0592e-102">SYNOPSIS</span></span>
<span data-ttu-id="0592e-103">Rimuovere un sito di Virtual Appliance da una risorsa di Virtual Appliance di rete.</span><span class="sxs-lookup"><span data-stu-id="0592e-103">Remove a virtual appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="0592e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0592e-104">SYNTAX</span></span>

### <span data-ttu-id="0592e-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0592e-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzVirtualApplianceSite -Name <String> -NetworkVirtualApplianceId <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0592e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0592e-106">ResourceIdParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0592e-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0592e-107">ResourceObjectParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -VirtualApplianceSite <PSVirtualApplianceSite> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0592e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0592e-108">DESCRIPTION</span></span>
<span data-ttu-id="0592e-109">Il comando Remove-AzVirtualApplianceSite rimuove un sito Virtual Appliance da una risorsa di Virtual Appliance di rete.</span><span class="sxs-lookup"><span data-stu-id="0592e-109">The Remove-AzVirtualApplianceSite command removes a Virtual Appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="0592e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0592e-110">EXAMPLES</span></span>

### <span data-ttu-id="0592e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0592e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="0592e-112">Eliminare una risorsa sito di Virtual Appliance.</span><span class="sxs-lookup"><span data-stu-id="0592e-112">Delete a Virtual Appliance site resource.</span></span> 

## <span data-ttu-id="0592e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0592e-113">PARAMETERS</span></span>

### <span data-ttu-id="0592e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0592e-114">-AsJob</span></span>
<span data-ttu-id="0592e-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="0592e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0592e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0592e-116">-DefaultProfile</span></span>
<span data-ttu-id="0592e-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0592e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0592e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0592e-118">-Force</span></span>
<span data-ttu-id="0592e-119">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="0592e-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0592e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="0592e-120">-Name</span></span>
<span data-ttu-id="0592e-121">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0592e-121">The resource name.</span></span>

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

### <span data-ttu-id="0592e-122">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="0592e-122">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="0592e-123">ID risorsa dell'appliance virtuale di rete associato al sito.</span><span class="sxs-lookup"><span data-stu-id="0592e-123">The resource ID of the Network Virtual Appliance associated with this site.</span></span>

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

### <span data-ttu-id="0592e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0592e-124">-PassThru</span></span>
<span data-ttu-id="0592e-125">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="0592e-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="0592e-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="0592e-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0592e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0592e-127">-ResourceGroupName</span></span>
<span data-ttu-id="0592e-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0592e-128">The resource group name.</span></span>

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

### <span data-ttu-id="0592e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0592e-129">-ResourceId</span></span>
<span data-ttu-id="0592e-130">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="0592e-130">The resource id.</span></span>

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

### <span data-ttu-id="0592e-131">-VirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="0592e-131">-VirtualApplianceSite</span></span>
<span data-ttu-id="0592e-132">Oggetto sito Virtual Appliance.</span><span class="sxs-lookup"><span data-stu-id="0592e-132">The virtual appliance site object.</span></span>

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

### <span data-ttu-id="0592e-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0592e-133">-Confirm</span></span>
<span data-ttu-id="0592e-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0592e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0592e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0592e-135">-WhatIf</span></span>
<span data-ttu-id="0592e-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0592e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0592e-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0592e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0592e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0592e-138">CommonParameters</span></span>
<span data-ttu-id="0592e-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0592e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0592e-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0592e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0592e-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0592e-141">INPUTS</span></span>

### <span data-ttu-id="0592e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="0592e-142">System.String</span></span>

### <span data-ttu-id="0592e-143">Microsoft. Azure. Commands. Network. Models. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="0592e-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="0592e-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0592e-144">OUTPUTS</span></span>

### <span data-ttu-id="0592e-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0592e-145">System.Boolean</span></span>

## <span data-ttu-id="0592e-146">Note</span><span class="sxs-lookup"><span data-stu-id="0592e-146">NOTES</span></span>

## <span data-ttu-id="0592e-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0592e-147">RELATED LINKS</span></span>
