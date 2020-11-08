---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
ms.openlocfilehash: 4d78c738dd5670f3b7be479751868eff29111b28
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188320"
---
# <span data-ttu-id="3e0c3-101">New-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="3e0c3-101">New-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="3e0c3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3e0c3-102">SYNOPSIS</span></span>
<span data-ttu-id="3e0c3-103">Crea un nuovo prefisso del servizio peering</span><span class="sxs-lookup"><span data-stu-id="3e0c3-103">Creates a new peering service prefix</span></span>

## <span data-ttu-id="3e0c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e0c3-104">SYNTAX</span></span>

### <span data-ttu-id="3e0c3-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3e0c3-105">Default (Default)</span></span>
```
New-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name] <String>
 -Prefix <String> -ServiceKey <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e0c3-106">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e0c3-106">ByResourceGroupName</span></span>
```
New-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name] <String> -Prefix <String>
 -ServiceKey <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e0c3-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3e0c3-107">ByResourceId</span></span>
```
New-AzPeeringServicePrefix [-Name] <String> -Prefix <String> -ServiceKey <String> [-PeeringServiceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e0c3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e0c3-108">DESCRIPTION</span></span>
<span data-ttu-id="3e0c3-109">Crea il prefisso del servizio peer associato a un oggetto servizio peering.</span><span class="sxs-lookup"><span data-stu-id="3e0c3-109">Creates peering service prefix associated with a peering service object.</span></span>

## <span data-ttu-id="3e0c3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e0c3-110">EXAMPLES</span></span>

### <span data-ttu-id="3e0c3-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3e0c3-111">Example 1</span></span>
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

<span data-ttu-id="3e0c3-112">Crea un prefisso da un oggetto servizio peering</span><span class="sxs-lookup"><span data-stu-id="3e0c3-112">Creates a prefix from a peering service object</span></span>

### <span data-ttu-id="3e0c3-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3e0c3-113">Example 2</span></span>
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

<span data-ttu-id="3e0c3-114">Crea un prefisso da un ID di risorsa del servizio peering.</span><span class="sxs-lookup"><span data-stu-id="3e0c3-114">Creates a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="3e0c3-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="3e0c3-115">Example 3</span></span>
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

<span data-ttu-id="3e0c3-116">Crea un prefisso da un nome e un nome del gruppo di risorse del servizio peer</span><span class="sxs-lookup"><span data-stu-id="3e0c3-116">Creates a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="3e0c3-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3e0c3-117">PARAMETERS</span></span>

### <span data-ttu-id="3e0c3-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e0c3-118">-AsJob</span></span>
<span data-ttu-id="3e0c3-119">Eseguire in background.</span><span class="sxs-lookup"><span data-stu-id="3e0c3-119">Run in the background.</span></span>

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

### <span data-ttu-id="3e0c3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e0c3-120">-DefaultProfile</span></span>
<span data-ttu-id="3e0c3-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3e0c3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e0c3-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e0c3-122">-Name</span></span>
<span data-ttu-id="3e0c3-123">Nome univoco di PSPeering.</span><span class="sxs-lookup"><span data-stu-id="3e0c3-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="3e0c3-124">-PeeringServiceId</span><span class="sxs-lookup"><span data-stu-id="3e0c3-124">-PeeringServiceId</span></span>
<span data-ttu-id="3e0c3-125">Nome della stringa ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="3e0c3-125">The resource id string name.</span></span>

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

### <span data-ttu-id="3e0c3-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="3e0c3-126">-PeeringServiceName</span></span>
<span data-ttu-id="3e0c3-127">Nome del servizio peering.</span><span class="sxs-lookup"><span data-stu-id="3e0c3-127">The peering service name.</span></span>
<span data-ttu-id="3e0c3-128">Usare New-AzPeeringService cmdlet per un nuovo servizio peering o Get-AzPeeringService per un elenco.</span><span class="sxs-lookup"><span data-stu-id="3e0c3-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

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

### <span data-ttu-id="3e0c3-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="3e0c3-129">-PeeringServiceObject</span></span>
<span data-ttu-id="3e0c3-130">Usare un Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="3e0c3-130">Use a Get-AzPeeringService</span></span>

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

### <span data-ttu-id="3e0c3-131">-Prefisso</span><span class="sxs-lookup"><span data-stu-id="3e0c3-131">-Prefix</span></span>
<span data-ttu-id="3e0c3-132">Prefisso IPv4 della sessione</span><span class="sxs-lookup"><span data-stu-id="3e0c3-132">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="3e0c3-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e0c3-133">-ResourceGroupName</span></span>
<span data-ttu-id="3e0c3-134">Il nome della risorsa crea o usa un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="3e0c3-134">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="3e0c3-135">-ServiceKey</span><span class="sxs-lookup"><span data-stu-id="3e0c3-135">-ServiceKey</span></span>
<span data-ttu-id="3e0c3-136">Questo è un GUID univoco fornito dal provider di servizi</span><span class="sxs-lookup"><span data-stu-id="3e0c3-136">This is a unique GUID provided by your service provider</span></span>

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

### <span data-ttu-id="3e0c3-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3e0c3-137">-Confirm</span></span>
<span data-ttu-id="3e0c3-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e0c3-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e0c3-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e0c3-139">-WhatIf</span></span>
<span data-ttu-id="3e0c3-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e0c3-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e0c3-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e0c3-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e0c3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e0c3-142">CommonParameters</span></span>
<span data-ttu-id="3e0c3-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e0c3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e0c3-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e0c3-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e0c3-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3e0c3-145">INPUTS</span></span>

### <span data-ttu-id="3e0c3-146">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="3e0c3-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="3e0c3-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e0c3-147">OUTPUTS</span></span>

### <span data-ttu-id="3e0c3-148">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="3e0c3-148">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="3e0c3-149">Note</span><span class="sxs-lookup"><span data-stu-id="3e0c3-149">NOTES</span></span>

## <span data-ttu-id="3e0c3-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e0c3-150">RELATED LINKS</span></span>