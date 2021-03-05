---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/get-azpeeringservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringService.md
ms.openlocfilehash: 4ce8e54b2ee5f43b9196263af5285af826aa9d01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989490"
---
# <span data-ttu-id="c4bac-101">Get-AzPeeringService</span><span class="sxs-lookup"><span data-stu-id="c4bac-101">Get-AzPeeringService</span></span>

## <span data-ttu-id="c4bac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4bac-102">SYNOPSIS</span></span>
<span data-ttu-id="c4bac-103">Ottenere un elenco di oggetti servizio di peering di un singolo oggetto.</span><span class="sxs-lookup"><span data-stu-id="c4bac-103">Get a list of peering service objects of a single object.</span></span>

## <span data-ttu-id="c4bac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4bac-104">SYNTAX</span></span>

### <span data-ttu-id="c4bac-105">ByResourceGroupName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c4bac-105">ByResourceGroupName (Default)</span></span>
```
Get-AzPeeringService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4bac-106">ByResourceGroupAndName</span><span class="sxs-lookup"><span data-stu-id="c4bac-106">ByResourceGroupAndName</span></span>
```
Get-AzPeeringService [-ResourceGroupName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c4bac-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c4bac-107">ByResourceId</span></span>
```
Get-AzPeeringService [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4bac-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c4bac-108">DESCRIPTION</span></span>
<span data-ttu-id="c4bac-109">Recupera i servizi di peering per un abbonamento</span><span class="sxs-lookup"><span data-stu-id="c4bac-109">Gets peering services for a subscription</span></span>

## <span data-ttu-id="c4bac-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4bac-110">EXAMPLES</span></span>

### <span data-ttu-id="c4bac-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c4bac-111">Example 1</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService3990
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService3990
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="c4bac-112">Ottiene un servizio di peering per un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="c4bac-112">Gets a peering service for a resource group</span></span>

### <span data-ttu-id="c4bac-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c4bac-113">Example 2</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceGroupName $rgName -Name $name

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="c4bac-114">Ottiene un servizio di peering per un gruppo di risorse e il nome</span><span class="sxs-lookup"><span data-stu-id="c4bac-114">Gets a peering service for a resource group and name</span></span>

### <span data-ttu-id="c4bac-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="c4bac-115">Example 3</span></span>
```powershell
PS C:\> Get-AzPeeringService -ResourceId $rid

PeeringServiceLocation : Washington
PeeringServiceProvider : TestPeer1
ProvisioningState      : Succeeded
Location               : centralus
Tags                   : {}
Name                   : myPeeringService312
Id                     : /subscriptions/resourceGroups/Building40/providers/Microsoft.Peering/peeringServices/myPeeringService312
Type                   : Microsoft.Peering/peeringServices
```

<span data-ttu-id="c4bac-116">Ottiene un servizio di peering in base all'ID risorsa</span><span class="sxs-lookup"><span data-stu-id="c4bac-116">Gets a peering service by resource id</span></span>

## <span data-ttu-id="c4bac-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4bac-117">PARAMETERS</span></span>

### <span data-ttu-id="c4bac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4bac-118">-DefaultProfile</span></span>
<span data-ttu-id="c4bac-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c4bac-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4bac-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c4bac-120">-Name</span></span>
<span data-ttu-id="c4bac-121">Nome univoco di PSCollectioning.</span><span class="sxs-lookup"><span data-stu-id="c4bac-121">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4bac-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4bac-122">-ResourceGroupName</span></span>
<span data-ttu-id="c4bac-123">Creare o usare il nome di un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="c4bac-123">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="c4bac-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4bac-124">-ResourceId</span></span>
<span data-ttu-id="c4bac-125">Il nome stringa dell'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="c4bac-125">The resource id string name.</span></span>

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

### <span data-ttu-id="c4bac-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4bac-126">CommonParameters</span></span>
<span data-ttu-id="c4bac-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4bac-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4bac-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c4bac-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4bac-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="c4bac-129">INPUTS</span></span>

### <span data-ttu-id="c4bac-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c4bac-130">System.String</span></span>

## <span data-ttu-id="c4bac-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4bac-131">OUTPUTS</span></span>

### <span data-ttu-id="c4bac-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSCollectioningService</span><span class="sxs-lookup"><span data-stu-id="c4bac-132">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringService</span></span>

## <span data-ttu-id="c4bac-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="c4bac-133">NOTES</span></span>

## <span data-ttu-id="c4bac-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4bac-134">RELATED LINKS</span></span>
