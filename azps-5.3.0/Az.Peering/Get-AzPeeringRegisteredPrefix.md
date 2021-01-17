---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/get-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Get-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: ca54d2a8969313742711306c701de3aefe54b30c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488793"
---
# <span data-ttu-id="56347-101">Get-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="56347-101">Get-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="56347-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="56347-102">SYNOPSIS</span></span>
<span data-ttu-id="56347-103">Ottiene o elenca il prefisso registrato per i peer.</span><span class="sxs-lookup"><span data-stu-id="56347-103">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="56347-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56347-104">SYNTAX</span></span>

### <span data-ttu-id="56347-105">ByResourceGroupAndName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="56347-105">ByResourceGroupAndName (Default)</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56347-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="56347-106">InputObject</span></span>
```
Get-AzPeeringRegisteredPrefix [-InputObject] <PSPeering> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56347-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="56347-107">ByResourceId</span></span>
```
Get-AzPeeringRegisteredPrefix [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56347-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56347-108">DESCRIPTION</span></span>
<span data-ttu-id="56347-109">Ottiene o elenca il prefisso registrato per i peer.</span><span class="sxs-lookup"><span data-stu-id="56347-109">Gets or lists the registered prefix for peerings.</span></span>

## <span data-ttu-id="56347-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56347-110">EXAMPLES</span></span>

### <span data-ttu-id="56347-111">Elenco di ASN registrati per il peering</span><span class="sxs-lookup"><span data-stu-id="56347-111">List registered ASNs for peering</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName
```

<span data-ttu-id="56347-112">Elenca gli elenchi ASN registrati.</span><span class="sxs-lookup"><span data-stu-id="56347-112">Lists registered asn.</span></span>

### <span data-ttu-id="56347-113">Ottiene l'ASN registrato per il peering per nome</span><span class="sxs-lookup"><span data-stu-id="56347-113">Gets registered ASN for peering by name</span></span>
```powershell
PS C:\> Get-AzPeeringRegisteredPrefix -ResourceGroupName $resourceGroupName -PeeringName $peeringName -Name $registeredPrefixName
```

<span data-ttu-id="56347-114">Ottiene il peering ASN registrato.</span><span class="sxs-lookup"><span data-stu-id="56347-114">Gets registered peering asn.</span></span>

<span data-ttu-id="56347-115">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="56347-115">{{ Add example description here }}</span></span>

## <span data-ttu-id="56347-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="56347-116">PARAMETERS</span></span>

### <span data-ttu-id="56347-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56347-117">-DefaultProfile</span></span>
<span data-ttu-id="56347-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="56347-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56347-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56347-119">-InputObject</span></span>
<span data-ttu-id="56347-120">Usare un Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="56347-120">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="56347-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="56347-121">-Name</span></span>
<span data-ttu-id="56347-122">Il nome del prefisso.</span><span class="sxs-lookup"><span data-stu-id="56347-122">The name of prefix.</span></span>

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

### <span data-ttu-id="56347-123">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="56347-123">-PeeringName</span></span>
<span data-ttu-id="56347-124">Nome univoco di PSPeering.</span><span class="sxs-lookup"><span data-stu-id="56347-124">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="56347-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56347-125">-ResourceGroupName</span></span>
<span data-ttu-id="56347-126">Il nome della risorsa crea o usa un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="56347-126">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="56347-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56347-127">-ResourceId</span></span>
<span data-ttu-id="56347-128">Nome della stringa ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="56347-128">The resource id string name.</span></span>

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

### <span data-ttu-id="56347-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56347-129">CommonParameters</span></span>
<span data-ttu-id="56347-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56347-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56347-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56347-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56347-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="56347-132">INPUTS</span></span>

### <span data-ttu-id="56347-133">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="56347-133">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="56347-134">System. String</span><span class="sxs-lookup"><span data-stu-id="56347-134">System.String</span></span>

## <span data-ttu-id="56347-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56347-135">OUTPUTS</span></span>

### <span data-ttu-id="56347-136">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="56347-136">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="56347-137">Note</span><span class="sxs-lookup"><span data-stu-id="56347-137">NOTES</span></span>

## <span data-ttu-id="56347-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56347-138">RELATED LINKS</span></span>
