---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
ms.openlocfilehash: d36561e2090e5b98bed5a5051715fe3e868bde4c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022438"
---
# <span data-ttu-id="e4db9-101">Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="e4db9-101">Get-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="e4db9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e4db9-102">SYNOPSIS</span></span>
<span data-ttu-id="e4db9-103">Ottiene un elenco dei prefissi del servizio peer per un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="e4db9-103">Gets a list of peering service prefixes for a subscription.</span></span>

## <span data-ttu-id="e4db9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e4db9-104">SYNTAX</span></span>

### <span data-ttu-id="e4db9-105">ByResourceGroupAndName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e4db9-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name <String>]
 [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4db9-106">Predefinita</span><span class="sxs-lookup"><span data-stu-id="e4db9-106">Default</span></span>
```
Get-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name <String>] [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4db9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e4db9-107">ByResourceId</span></span>
```
Get-AzPeeringServicePrefix [-ResourceId] <String> [-Expand] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e4db9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4db9-108">DESCRIPTION</span></span>
<span data-ttu-id="e4db9-109">Prefissi del servizio di peering elenco per gli oggetti del servizio peer</span><span class="sxs-lookup"><span data-stu-id="e4db9-109">List peering service prefixes for peering service objects</span></span>

## <span data-ttu-id="e4db9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e4db9-110">EXAMPLES</span></span>

### <span data-ttu-id="e4db9-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e4db9-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $name | Get-AzPeeringServicePrefix

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes

Prefix                : 200.25.71.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix3463
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService4084/pre
                        fixes/myPrefix3463
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="e4db9-112">Ottiene i prefissi per un servizio peering basato sui comandi di piping.</span><span class="sxs-lookup"><span data-stu-id="e4db9-112">Gets the prefixes for a peering service based on piping commands.</span></span>

### <span data-ttu-id="e4db9-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e4db9-113">Example 2</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceId $peeringServicePrefixResourceId 

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="e4db9-114">Ottiene un prefisso specifico per un servizio peering in base all'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="e4db9-114">Gets a specific prefix for a peering service by resource id.</span></span>

### <span data-ttu-id="e4db9-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="e4db9-115">Example 3</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceGroupName $rgName -PeeringServiceName $peeringServiceName -Name $prefixName

Prefix                : 200.25.69.0/31
PrefixValidationState : Pending
LearnedType           : None
ProvisioningState     : Succeeded
Name                  : myPrefix9055
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService707/pref
                        ixes/myPrefix9055
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="e4db9-116">Ottiene un prefisso specifico per un servizio peering in base all'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="e4db9-116">Gets a specific prefix for a peering service by resource id.</span></span>

### <span data-ttu-id="e4db9-117">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="e4db9-117">Example 4</span></span>
```powershell
PS C:\> Get-AzPeeringServicePrefix -ResourceGroupName $rgName -PeeringServiceName $peeringServiceName -Name $prefixName -Expand

Prefix                : 10.2.6.0/24
PrefixValidationState : Failed
LearnedType           : None
ErrorMessage          :
Events                : {}
ProvisioningState     : Succeeded
Name                  : ps0
Id                    : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService6616/pre
                        fixes/ps0
Type                  : Microsoft.Peering/peeringServices/prefixes
```

<span data-ttu-id="e4db9-118">Ottiene un prefisso specifico per un servizio peer con attributi espansi</span><span class="sxs-lookup"><span data-stu-id="e4db9-118">Gets a specific prefix for a peering service with expanded attributes</span></span>

## <span data-ttu-id="e4db9-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e4db9-119">PARAMETERS</span></span>

### <span data-ttu-id="e4db9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4db9-120">-DefaultProfile</span></span>
<span data-ttu-id="e4db9-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e4db9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4db9-122">-Espandi</span><span class="sxs-lookup"><span data-stu-id="e4db9-122">-Expand</span></span>
<span data-ttu-id="e4db9-123">Visualizzare gli eventi per un prefisso del servizio peering</span><span class="sxs-lookup"><span data-stu-id="e4db9-123">View the events for a peering service prefix</span></span>

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

### <span data-ttu-id="e4db9-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4db9-124">-Name</span></span>
<span data-ttu-id="e4db9-125">Nome univoco di PSPeering.</span><span class="sxs-lookup"><span data-stu-id="e4db9-125">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4db9-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="e4db9-126">-PeeringServiceName</span></span>
<span data-ttu-id="e4db9-127">Nome del servizio peering.</span><span class="sxs-lookup"><span data-stu-id="e4db9-127">The peering service name.</span></span> <span data-ttu-id="e4db9-128">Usare New-AzPeeringService cmdlet per un nuovo servizio peering o Get-AzPeeringService per un elenco.</span><span class="sxs-lookup"><span data-stu-id="e4db9-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4db9-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="e4db9-129">-PeeringServiceObject</span></span>
<span data-ttu-id="e4db9-130">Usare un Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="e4db9-130">Use a Get-AzPeeringService</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4db9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4db9-131">-ResourceGroupName</span></span>
<span data-ttu-id="e4db9-132">Il nome della risorsa crea o usa un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="e4db9-132">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4db9-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4db9-133">-ResourceId</span></span>
<span data-ttu-id="e4db9-134">Nome della stringa ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="e4db9-134">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4db9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4db9-135">CommonParameters</span></span>
<span data-ttu-id="e4db9-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4db9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4db9-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4db9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4db9-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e4db9-138">INPUTS</span></span>

### <span data-ttu-id="e4db9-139">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeeringService</span><span class="sxs-lookup"><span data-stu-id="e4db9-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

### <span data-ttu-id="e4db9-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e4db9-140">System.String</span></span>

## <span data-ttu-id="e4db9-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e4db9-141">OUTPUTS</span></span>

### <span data-ttu-id="e4db9-142">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="e4db9-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="e4db9-143">Note</span><span class="sxs-lookup"><span data-stu-id="e4db9-143">NOTES</span></span>

## <span data-ttu-id="e4db9-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e4db9-144">RELATED LINKS</span></span>
