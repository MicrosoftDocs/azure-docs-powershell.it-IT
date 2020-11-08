---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
ms.openlocfilehash: e57b68db7e2ee285ef75e0ada33a6564574bb4ed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200346"
---
# <span data-ttu-id="6ffcf-101">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="6ffcf-101">Remove-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="6ffcf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6ffcf-102">SYNOPSIS</span></span>
<span data-ttu-id="6ffcf-103">Rimuovere una risorsa di Virtual Appliance di rete.</span><span class="sxs-lookup"><span data-stu-id="6ffcf-103">Remove a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="6ffcf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ffcf-104">SYNTAX</span></span>

### <span data-ttu-id="6ffcf-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6ffcf-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ffcf-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ffcf-106">ResourceIdParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ffcf-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ffcf-107">ResourceObjectParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -NetworkVirtualAppliance <PSNetworkVirtualAppliance> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ffcf-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ffcf-108">DESCRIPTION</span></span>
<span data-ttu-id="6ffcf-109">Il comando Remove-AzNetworkVirtualAppliance rimuove una risorsa di Virtual Appliance di rete.</span><span class="sxs-lookup"><span data-stu-id="6ffcf-109">The Remove-AzNetworkVirtualAppliance command removes a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="6ffcf-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ffcf-110">EXAMPLES</span></span>

### <span data-ttu-id="6ffcf-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6ffcf-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
```

<span data-ttu-id="6ffcf-112">Eliminare una risorsa di Virtual Appliance di rete.</span><span class="sxs-lookup"><span data-stu-id="6ffcf-112">Delete a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="6ffcf-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6ffcf-113">PARAMETERS</span></span>

### <span data-ttu-id="6ffcf-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ffcf-114">-AsJob</span></span>
<span data-ttu-id="6ffcf-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6ffcf-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6ffcf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ffcf-116">-DefaultProfile</span></span>
<span data-ttu-id="6ffcf-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6ffcf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ffcf-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6ffcf-118">-Force</span></span>
<span data-ttu-id="6ffcf-119">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="6ffcf-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6ffcf-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="6ffcf-120">-Name</span></span>
<span data-ttu-id="6ffcf-121">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6ffcf-121">The resource name.</span></span>

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

### <span data-ttu-id="6ffcf-122">-NetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="6ffcf-122">-NetworkVirtualAppliance</span></span>
<span data-ttu-id="6ffcf-123">Oggetto Resource.</span><span class="sxs-lookup"><span data-stu-id="6ffcf-123">The resource object.</span></span>

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

### <span data-ttu-id="6ffcf-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ffcf-124">-PassThru</span></span>
<span data-ttu-id="6ffcf-125">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="6ffcf-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="6ffcf-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="6ffcf-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6ffcf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ffcf-127">-ResourceGroupName</span></span>
<span data-ttu-id="6ffcf-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6ffcf-128">The resource group name.</span></span>

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

### <span data-ttu-id="6ffcf-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ffcf-129">-ResourceId</span></span>
<span data-ttu-id="6ffcf-130">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="6ffcf-130">The Resource Id.</span></span>

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

### <span data-ttu-id="6ffcf-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6ffcf-131">-Confirm</span></span>
<span data-ttu-id="6ffcf-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ffcf-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ffcf-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ffcf-133">-WhatIf</span></span>
<span data-ttu-id="6ffcf-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ffcf-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ffcf-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ffcf-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ffcf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ffcf-136">CommonParameters</span></span>
<span data-ttu-id="6ffcf-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ffcf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ffcf-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ffcf-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ffcf-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6ffcf-139">INPUTS</span></span>

### <span data-ttu-id="6ffcf-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6ffcf-140">System.String</span></span>

### <span data-ttu-id="6ffcf-141">Microsoft. Azure. Commands. Network. Models. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="6ffcf-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="6ffcf-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ffcf-142">OUTPUTS</span></span>

### <span data-ttu-id="6ffcf-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6ffcf-143">System.Boolean</span></span>

## <span data-ttu-id="6ffcf-144">Note</span><span class="sxs-lookup"><span data-stu-id="6ffcf-144">NOTES</span></span>

## <span data-ttu-id="6ffcf-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ffcf-145">RELATED LINKS</span></span>
