---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
ms.openlocfilehash: e57b68db7e2ee285ef75e0ada33a6564574bb4ed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475845"
---
# <span data-ttu-id="6b516-101">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="6b516-101">Remove-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="6b516-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6b516-102">SYNOPSIS</span></span>
<span data-ttu-id="6b516-103">Rimuovere una risorsa di Virtual Appliance di rete.</span><span class="sxs-lookup"><span data-stu-id="6b516-103">Remove a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="6b516-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6b516-104">SYNTAX</span></span>

### <span data-ttu-id="6b516-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6b516-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b516-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b516-106">ResourceIdParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b516-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b516-107">ResourceObjectParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -NetworkVirtualAppliance <PSNetworkVirtualAppliance> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b516-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b516-108">DESCRIPTION</span></span>
<span data-ttu-id="6b516-109">Il comando Remove-AzNetworkVirtualAppliance rimuove una risorsa di Virtual Appliance di rete.</span><span class="sxs-lookup"><span data-stu-id="6b516-109">The Remove-AzNetworkVirtualAppliance command removes a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="6b516-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6b516-110">EXAMPLES</span></span>

### <span data-ttu-id="6b516-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6b516-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
```

<span data-ttu-id="6b516-112">Eliminare una risorsa di Virtual Appliance di rete.</span><span class="sxs-lookup"><span data-stu-id="6b516-112">Delete a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="6b516-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6b516-113">PARAMETERS</span></span>

### <span data-ttu-id="6b516-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b516-114">-AsJob</span></span>
<span data-ttu-id="6b516-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6b516-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b516-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b516-116">-DefaultProfile</span></span>
<span data-ttu-id="6b516-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6b516-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b516-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6b516-118">-Force</span></span>
<span data-ttu-id="6b516-119">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="6b516-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6b516-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="6b516-120">-Name</span></span>
<span data-ttu-id="6b516-121">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6b516-121">The resource name.</span></span>

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

### <span data-ttu-id="6b516-122">-NetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="6b516-122">-NetworkVirtualAppliance</span></span>
<span data-ttu-id="6b516-123">Oggetto Resource.</span><span class="sxs-lookup"><span data-stu-id="6b516-123">The resource object.</span></span>

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

### <span data-ttu-id="6b516-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b516-124">-PassThru</span></span>
<span data-ttu-id="6b516-125">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="6b516-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="6b516-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="6b516-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6b516-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b516-127">-ResourceGroupName</span></span>
<span data-ttu-id="6b516-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6b516-128">The resource group name.</span></span>

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

### <span data-ttu-id="6b516-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b516-129">-ResourceId</span></span>
<span data-ttu-id="6b516-130">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="6b516-130">The Resource Id.</span></span>

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

### <span data-ttu-id="6b516-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6b516-131">-Confirm</span></span>
<span data-ttu-id="6b516-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b516-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b516-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b516-133">-WhatIf</span></span>
<span data-ttu-id="6b516-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b516-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b516-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b516-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b516-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b516-136">CommonParameters</span></span>
<span data-ttu-id="6b516-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b516-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b516-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b516-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b516-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6b516-139">INPUTS</span></span>

### <span data-ttu-id="6b516-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6b516-140">System.String</span></span>

### <span data-ttu-id="6b516-141">Microsoft. Azure. Commands. Network. Models. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="6b516-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="6b516-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6b516-142">OUTPUTS</span></span>

### <span data-ttu-id="6b516-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6b516-143">System.Boolean</span></span>

## <span data-ttu-id="6b516-144">Note</span><span class="sxs-lookup"><span data-stu-id="6b516-144">NOTES</span></span>

## <span data-ttu-id="6b516-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6b516-145">RELATED LINKS</span></span>
