---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: ca54d2a8969313742711306c701de3aefe54b30c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191455"
---
# <span data-ttu-id="f22f9-101">Get-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="f22f9-101">Get-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="f22f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f22f9-102">SYNOPSIS</span></span>
<span data-ttu-id="f22f9-103">Ottiene o elenca il prefisso registrato per i peering.</span><span class="sxs-lookup"><span data-stu-id="f22f9-103">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="f22f9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f22f9-104">SYNTAX</span></span>

### <span data-ttu-id="f22f9-105">ByResourceGroupAndName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f22f9-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f22f9-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f22f9-106">InputObject</span></span>
```
Get-AzPeeringRegisteredPrefix [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f22f9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f22f9-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f22f9-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f22f9-108">DESCRIPTION</span></span>
<span data-ttu-id="f22f9-109">Ottiene o elenca il prefisso registrato per i peering.</span><span class="sxs-lookup"><span data-stu-id="f22f9-109">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="f22f9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f22f9-110">EXAMPLES</span></span>

### <span data-ttu-id="f22f9-111">Elenco di NOMI registrati per il peering</span><span class="sxs-lookup"><span data-stu-id="f22f9-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="f22f9-112">Elenchi registrati comen.</span><span class="sxs-lookup"><span data-stu-id="f22f9-112">Lists registered asn.</span></span>

### <span data-ttu-id="f22f9-113">Viene registrato ASN per il peering in base al nome</span><span class="sxs-lookup"><span data-stu-id="f22f9-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredPrefixName
```

<span data-ttu-id="f22f9-114">Ottiene l'asn di peering registrato.</span><span class="sxs-lookup"><span data-stu-id="f22f9-114">Gets registered peering asn.</span></span>

<span data-ttu-id="f22f9-115">{{ Aggiungi la descrizione di esempio qui }}</span><span class="sxs-lookup"><span data-stu-id="f22f9-115">{{ Add example description here }}</span></span>

## <span data-ttu-id="f22f9-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f22f9-116">PARAMETERS</span></span>

### <span data-ttu-id="f22f9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f22f9-117">-DefaultProfile</span></span>
<span data-ttu-id="f22f9-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f22f9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f22f9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f22f9-119">-InputObject</span></span>
<span data-ttu-id="f22f9-120">Usare un Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="f22f9-120">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f22f9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f22f9-121">-Name</span></span>
<span data-ttu-id="f22f9-122">Nome del prefisso.</span><span class="sxs-lookup"><span data-stu-id="f22f9-122">The name of prefix.</span></span>

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

### <span data-ttu-id="f22f9-123">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="f22f9-123">-PeeringName</span></span>
<span data-ttu-id="f22f9-124">Nome univoco di PSCollectioning.</span><span class="sxs-lookup"><span data-stu-id="f22f9-124">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="f22f9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f22f9-125">-ResourceGroupName</span></span>
<span data-ttu-id="f22f9-126">Creare o usare il nome di un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="f22f9-126">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="f22f9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f22f9-127">-ResourceId</span></span>
<span data-ttu-id="f22f9-128">Il nome stringa dell'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="f22f9-128">The resource id string name.</span></span>

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

### <span data-ttu-id="f22f9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f22f9-129">CommonParameters</span></span>
<span data-ttu-id="f22f9-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f22f9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f22f9-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f22f9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f22f9-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="f22f9-132">INPUTS</span></span>

### <span data-ttu-id="f22f9-133">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSApplicationing</span><span class="sxs-lookup"><span data-stu-id="f22f9-133">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="f22f9-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f22f9-134">System.String</span></span>

## <span data-ttu-id="f22f9-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f22f9-135">OUTPUTS</span></span>

### <span data-ttu-id="f22f9-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="f22f9-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="f22f9-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="f22f9-137">NOTES</span></span>

## <span data-ttu-id="f22f9-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f22f9-138">RELATED LINKS</span></span>
