---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringServicePrefix.md
ms.openlocfilehash: e488baacb4e9412cb4e3e5be2b6a595629495b16
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020720"
---
# <span data-ttu-id="19230-101">New-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="19230-101">New-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="19230-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="19230-102">SYNOPSIS</span></span>
<span data-ttu-id="19230-103">Crea un nuovo prefisso del servizio peering</span><span class="sxs-lookup"><span data-stu-id="19230-103">Creates a new peering service prefix</span></span>

## <span data-ttu-id="19230-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="19230-104">SYNTAX</span></span>

### <span data-ttu-id="19230-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="19230-105">Default (Default)</span></span>
```
New-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19230-106">ByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19230-106">ByResourceGroupName</span></span>
```
New-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name] <String> -Prefix <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19230-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="19230-107">ByResourceId</span></span>
```
New-AzPeeringServicePrefix [-Name] <String> -Prefix <String> [-PeeringServiceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19230-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19230-108">DESCRIPTION</span></span>
<span data-ttu-id="19230-109">Crea il prefisso del servizio peer associato a un oggetto servizio peering.</span><span class="sxs-lookup"><span data-stu-id="19230-109">Creates peering service prefix associated with a peering service object.</span></span>

## <span data-ttu-id="19230-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="19230-110">EXAMPLES</span></span>

### <span data-ttu-id="19230-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="19230-111">Example 1</span></span>
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

<span data-ttu-id="19230-112">Crea un prefisso da un oggetto servizio peering</span><span class="sxs-lookup"><span data-stu-id="19230-112">Creates a prefix from a peering service object</span></span>

### <span data-ttu-id="19230-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="19230-113">Example 2</span></span>
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

<span data-ttu-id="19230-114">Crea un prefisso da un ID di risorsa del servizio peering.</span><span class="sxs-lookup"><span data-stu-id="19230-114">Creates a prefix from a peering service resource id.</span></span>

### <span data-ttu-id="19230-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="19230-115">Example 3</span></span>
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

<span data-ttu-id="19230-116">Crea un prefisso da un nome e un nome del gruppo di risorse del servizio peer</span><span class="sxs-lookup"><span data-stu-id="19230-116">Creates a prefix from a peering service resource group name and name</span></span>

## <span data-ttu-id="19230-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="19230-117">PARAMETERS</span></span>

### <span data-ttu-id="19230-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19230-118">-AsJob</span></span>
<span data-ttu-id="19230-119">Eseguire in background.</span><span class="sxs-lookup"><span data-stu-id="19230-119">Run in the background.</span></span>

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

### <span data-ttu-id="19230-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19230-120">-DefaultProfile</span></span>
<span data-ttu-id="19230-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="19230-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19230-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="19230-122">-Name</span></span>
<span data-ttu-id="19230-123">Nome univoco di PSPeering.</span><span class="sxs-lookup"><span data-stu-id="19230-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="19230-124">-PeeringServiceId</span><span class="sxs-lookup"><span data-stu-id="19230-124">-PeeringServiceId</span></span>
<span data-ttu-id="19230-125">Nome della stringa ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="19230-125">The resource id string name.</span></span>

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

### <span data-ttu-id="19230-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="19230-126">-PeeringServiceName</span></span>
<span data-ttu-id="19230-127">Nome del servizio peering.</span><span class="sxs-lookup"><span data-stu-id="19230-127">The peering service name.</span></span>
<span data-ttu-id="19230-128">Usare New-AzPeeringService cmdlet per un nuovo servizio peering o Get-AzPeeringService per un elenco.</span><span class="sxs-lookup"><span data-stu-id="19230-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

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

### <span data-ttu-id="19230-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="19230-129">-PeeringServiceObject</span></span>
<span data-ttu-id="19230-130">Usare un Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="19230-130">Use a Get-AzPeeringService</span></span>

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

### <span data-ttu-id="19230-131">-Prefisso</span><span class="sxs-lookup"><span data-stu-id="19230-131">-Prefix</span></span>
<span data-ttu-id="19230-132">Prefisso IPv4 della sessione</span><span class="sxs-lookup"><span data-stu-id="19230-132">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="19230-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19230-133">-ResourceGroupName</span></span>
<span data-ttu-id="19230-134">Il nome della risorsa crea o usa un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="19230-134">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="19230-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="19230-135">-Confirm</span></span>
<span data-ttu-id="19230-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19230-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19230-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19230-137">-WhatIf</span></span>
<span data-ttu-id="19230-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19230-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19230-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19230-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19230-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19230-140">CommonParameters</span></span>
<span data-ttu-id="19230-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19230-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19230-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19230-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19230-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="19230-143">INPUTS</span></span>

### <span data-ttu-id="19230-144">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="19230-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="19230-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="19230-145">OUTPUTS</span></span>

### <span data-ttu-id="19230-146">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="19230-146">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="19230-147">Note</span><span class="sxs-lookup"><span data-stu-id="19230-147">NOTES</span></span>

## <span data-ttu-id="19230-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="19230-148">RELATED LINKS</span></span>
