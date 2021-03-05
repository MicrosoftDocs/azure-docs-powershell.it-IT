---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringserviceprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringServicePrefix.md
ms.openlocfilehash: 8b62189848583d11738a39555bc80ed0a52776fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989475"
---
# <span data-ttu-id="3af57-101">Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="3af57-101">Get-AzPeeringServicePrefix</span></span>

## <span data-ttu-id="3af57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3af57-102">SYNOPSIS</span></span>
<span data-ttu-id="3af57-103">Ottiene un elenco di prefissi del servizio di peering per una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="3af57-103">Gets a list of peering service prefixes for a subscription.</span></span>

## <span data-ttu-id="3af57-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3af57-104">SYNTAX</span></span>

### <span data-ttu-id="3af57-105">ByResourceGroupAndName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3af57-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringServicePrefix [-ResourceGroupName] <String> [-PeeringServiceName] <String> [-Name <String>]
 [-Expand] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3af57-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="3af57-106">InputObject</span></span>
```
Get-AzPeeringServicePrefix [-PeeringServiceObject] <PSPeeringService> [-Name <String>] [-Expand]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3af57-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3af57-107">ByResourceId</span></span>
```
Get-AzPeeringServicePrefix [-ResourceId] <String> [-Expand] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3af57-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3af57-108">DESCRIPTION</span></span>
<span data-ttu-id="3af57-109">Elencare i prefissi del servizio di peering per gli oggetti del servizio di peering</span><span class="sxs-lookup"><span data-stu-id="3af57-109">List peering service prefixes for peering service objects</span></span>

## <span data-ttu-id="3af57-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3af57-110">EXAMPLES</span></span>

### <span data-ttu-id="3af57-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3af57-111">Example 1</span></span>
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

<span data-ttu-id="3af57-112">Ottiene i prefissi per un servizio di peering in base ai comandi di piping.</span><span class="sxs-lookup"><span data-stu-id="3af57-112">Gets the prefixes for a peering service based on piping commands.</span></span>

### <span data-ttu-id="3af57-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3af57-113">Example 2</span></span>
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

<span data-ttu-id="3af57-114">Ottiene un prefisso specifico per un servizio di peering in base all'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="3af57-114">Gets a specific prefix for a peering service by resource id.</span></span>

### <span data-ttu-id="3af57-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="3af57-115">Example 3</span></span>
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

<span data-ttu-id="3af57-116">Ottiene un prefisso specifico per un servizio di peering in base all'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="3af57-116">Gets a specific prefix for a peering service by resource id.</span></span>

### <span data-ttu-id="3af57-117">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="3af57-117">Example 4</span></span>
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

<span data-ttu-id="3af57-118">Ottiene un prefisso specifico per un servizio di peering con attributi espansi</span><span class="sxs-lookup"><span data-stu-id="3af57-118">Gets a specific prefix for a peering service with expanded attributes</span></span>

## <span data-ttu-id="3af57-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3af57-119">PARAMETERS</span></span>

### <span data-ttu-id="3af57-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3af57-120">-DefaultProfile</span></span>
<span data-ttu-id="3af57-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3af57-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3af57-122">-Expand</span><span class="sxs-lookup"><span data-stu-id="3af57-122">-Expand</span></span>
<span data-ttu-id="3af57-123">Visualizzare gli eventi per il prefisso di un servizio di peering</span><span class="sxs-lookup"><span data-stu-id="3af57-123">View the events for a peering service prefix</span></span>

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

### <span data-ttu-id="3af57-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3af57-124">-Name</span></span>
<span data-ttu-id="3af57-125">Nome univoco di PSCollectioning.</span><span class="sxs-lookup"><span data-stu-id="3af57-125">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, InputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af57-126">-PeeringServiceName</span><span class="sxs-lookup"><span data-stu-id="3af57-126">-PeeringServiceName</span></span>
<span data-ttu-id="3af57-127">Nome del servizio di peering.</span><span class="sxs-lookup"><span data-stu-id="3af57-127">The peering service name.</span></span> <span data-ttu-id="3af57-128">Usare New-AzPeeringService cmdlet per un nuovo servizio di peering o un Get-AzPeeringService per un elenco.</span><span class="sxs-lookup"><span data-stu-id="3af57-128">Use New-AzPeeringService cmdlet for a new peering service or Get-AzPeeringService for a list.</span></span>

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

### <span data-ttu-id="3af57-129">-PeeringServiceObject</span><span class="sxs-lookup"><span data-stu-id="3af57-129">-PeeringServiceObject</span></span>
<span data-ttu-id="3af57-130">Usare un Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="3af57-130">Use a Get-AzPeeringService</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3af57-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3af57-131">-ResourceGroupName</span></span>
<span data-ttu-id="3af57-132">Creare o usare il nome di un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="3af57-132">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="3af57-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3af57-133">-ResourceId</span></span>
<span data-ttu-id="3af57-134">Il nome stringa dell'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="3af57-134">The resource id string name.</span></span>

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

### <span data-ttu-id="3af57-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3af57-135">CommonParameters</span></span>
<span data-ttu-id="3af57-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3af57-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3af57-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3af57-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3af57-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="3af57-138">INPUTS</span></span>

### <span data-ttu-id="3af57-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSCollectioningService</span><span class="sxs-lookup"><span data-stu-id="3af57-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

### <span data-ttu-id="3af57-140">System.String</span><span class="sxs-lookup"><span data-stu-id="3af57-140">System.String</span></span>

## <span data-ttu-id="3af57-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3af57-141">OUTPUTS</span></span>

### <span data-ttu-id="3af57-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSCollectioningServicePrefix</span><span class="sxs-lookup"><span data-stu-id="3af57-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

## <span data-ttu-id="3af57-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="3af57-143">NOTES</span></span>

## <span data-ttu-id="3af57-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3af57-144">RELATED LINKS</span></span>
