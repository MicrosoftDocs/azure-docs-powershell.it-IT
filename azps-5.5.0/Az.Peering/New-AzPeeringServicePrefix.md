---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
ms.openlocfilehash: 4d78c738dd5670f3b7be479751868eff29111b28
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206315"
---
# <span data-ttu-id="d7158-101">New-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="d7158-101">New-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="d7158-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7158-102">SYNOPSIS</span></span>
<span data-ttu-id="d7158-103">Crea un nuovo prefisso del servizio di peering</span><span class="sxs-lookup"><span data-stu-id="d7158-103">Creates a new peering service prefix</span></span>

## <span data-ttu-id="d7158-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d7158-104">SYNTAX</span></span>

### <span data-ttu-id="d7158-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d7158-105">Default (Default)</span></span>
```
New-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name] <String>
 -Prefix <String> -ServiceKey <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7158-106">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7158-106">ByResourceGroupName</span></span>
```
New-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name] <String> -Prefix <String>
 -ServiceKey <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7158-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d7158-107">ByResourceId</span></span>
```
New-AzPeeringServicePrefix [-Name] <String> -Prefix <String> -ServiceKey <String> [-PeeringServiceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7158-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d7158-108">DESCRIPTION</span></span>
<span data-ttu-id="d7158-109">Crea il prefisso del servizio di peering associato a un oggetto servizio di peering.</span><span class="sxs-lookup"><span data-stu-id="d7158-109">Creates peering service prefix associated with a peering service object.</span></span>

## <span data-ttu-id="d7158-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d7158-110">EXAMPLES</span></span>

### <span data-ttu-id="d7158-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d7158-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $peeringServiceName | New-AzPeeringServicePrefix -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="d7158-112">Crea un prefisso da un oggetto servizio di peering</span><span class="sxs-lookup"><span data-stu-id="d7158-112">Creates a prefix from a peering service object</span></span>

### <span data-ttu-id="d7158-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d7158-113">Example 2</span></span>
```powershell
PS C:\> New-AzPeeringServicePrefix -PeeringServiceId $peeringServiceResourceId -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="d7158-114">Crea un prefisso da un ID di risorsa del servizio di peering.</span><span class="sxs-lookup"><span data-stu-id="d7158-114">Creates a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="d7158-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="d7158-115">Example 3</span></span>
```powershell
PS C:\> New-AzPeeringServicePrefix -ResourceGroupName $peeringServiceGroup -PeeringServiceName $peeringServiceName -Name $prefixName -Prefix "10.0.0.0/24"

Prefix                : 10.0.0.0/24
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="d7158-116">Crea un prefisso dal nome e dal nome di un gruppo di risorse del servizio di peering</span><span class="sxs-lookup"><span data-stu-id="d7158-116">Creates a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="d7158-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7158-117">PARAMETERS</span></span>

### <span data-ttu-id="d7158-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7158-118">-AsJob</span></span>
<span data-ttu-id="d7158-119">Esegui in background.</span><span class="sxs-lookup"><span data-stu-id="d7158-119">Run in the background.</span></span>

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

### <span data-ttu-id="d7158-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7158-120">-DefaultProfile</span></span>
<span data-ttu-id="d7158-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d7158-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7158-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d7158-122">-Name</span></span>
<span data-ttu-id="d7158-123">Nome univoco di PSCollectioning.</span><span class="sxs-lookup"><span data-stu-id="d7158-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7158-124">-PeeringServiceId</span><span class="sxs-lookup"><span data-stu-id="d7158-124">-PeeringServiceId</span></span>
<span data-ttu-id="d7158-125">Il nome stringa dell'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="d7158-125">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7158-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="d7158-126">-PeeringServiceName</span></span>
<span data-ttu-id="d7158-127">Nome del servizio di peering.</span><span class="sxs-lookup"><span data-stu-id="d7158-127">The peering service name.</span></span>
<span data-ttu-id="d7158-128">Usare New-AzPeeringService cmdlet per un nuovo servizio di peering o un Get-AzPeeringService per un elenco.</span><span class="sxs-lookup"><span data-stu-id="d7158-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7158-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="d7158-129">-PeeringServiceObject</span></span>
<span data-ttu-id="d7158-130">Usare un Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="d7158-130">Use a Get-AzPeeringService</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService
Parameter Sets: ByResourceGroupName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7158-131">-Prefix</span><span class="sxs-lookup"><span data-stu-id="d7158-131">-Prefix</span></span>
<span data-ttu-id="d7158-132">Prefisso IPv4 della sessione</span><span class="sxs-lookup"><span data-stu-id="d7158-132">The session IPv4 prefix</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7158-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7158-133">-ResourceGroupName</span></span>
<span data-ttu-id="d7158-134">Creare o usare il nome di un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="d7158-134">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7158-135">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="d7158-135">-ServiceKey</span></span>
<span data-ttu-id="d7158-136">Si tratta di un GUID univoco fornito dal provider di servizi</span><span class="sxs-lookup"><span data-stu-id="d7158-136">This is a unique GUID provided by your service provider</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7158-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7158-137">-Confirm</span></span>
<span data-ttu-id="d7158-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7158-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7158-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7158-139">-WhatIf</span></span>
<span data-ttu-id="d7158-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d7158-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7158-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d7158-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7158-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7158-142">CommonParameters</span></span>
<span data-ttu-id="d7158-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7158-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7158-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d7158-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7158-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="d7158-145">INPUTS</span></span>

### <span data-ttu-id="d7158-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSCollectioningService</span><span class="sxs-lookup"><span data-stu-id="d7158-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="d7158-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d7158-147">OUTPUTS</span></span>

### <span data-ttu-id="d7158-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPreingServicePrefix</span><span class="sxs-lookup"><span data-stu-id="d7158-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="d7158-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="d7158-149">NOTES</span></span>

## <span data-ttu-id="d7158-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d7158-150">RELATED LINKS</span></span>
