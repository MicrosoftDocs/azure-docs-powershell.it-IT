---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d4521c06cafac21c554620bbc55f7555db6e0279
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032259"
---
# <span data-ttu-id="83aa6-101">New-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="83aa6-101">New-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="83aa6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="83aa6-102">SYNOPSIS</span></span>
<span data-ttu-id="83aa6-103">Creare un ASN registrato per il peering</span><span class="sxs-lookup"><span data-stu-id="83aa6-103">Create registered ASN for peering</span></span>

## <span data-ttu-id="83aa6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83aa6-104">SYNTAX</span></span>

### <span data-ttu-id="83aa6-105">ByResourceGroupAndName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="83aa6-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83aa6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="83aa6-106">InputObject</span></span>
```
New-AzPeeringRegisteredAsn -InputObject <PSPeering> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83aa6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="83aa6-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83aa6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83aa6-108">DESCRIPTION</span></span>
<span data-ttu-id="83aa6-109">Creare ASN registrati per gli oggetti peering.</span><span class="sxs-lookup"><span data-stu-id="83aa6-109">Create registered ASNs for peering objects.</span></span>

## <span data-ttu-id="83aa6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83aa6-110">EXAMPLES</span></span>

### <span data-ttu-id="83aa6-111">Ottenere peering e creare un ASN registrato</span><span class="sxs-lookup"><span data-stu-id="83aa6-111">Get peering and create a registered ASN</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredAsn -Name $asnName -Asn $asn
```

<span data-ttu-id="83aa6-112">Ottenere il peering che si desidera aggiungere un ASN registrato.</span><span class="sxs-lookup"><span data-stu-id="83aa6-112">Get the peering you want to add a registered ASN.</span></span> <span data-ttu-id="83aa6-113">Passa quindi a unifiedgroup.</span><span class="sxs-lookup"><span data-stu-id="83aa6-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="83aa6-114">Usare il peering resourceId per creare un ASN registrato</span><span class="sxs-lookup"><span data-stu-id="83aa6-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredAsn -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="83aa6-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="83aa6-115">PARAMETERS</span></span>

### <span data-ttu-id="83aa6-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="83aa6-116">-AsJob</span></span>
<span data-ttu-id="83aa6-117">Eseguire in background.</span><span class="sxs-lookup"><span data-stu-id="83aa6-117">Run in the background.</span></span>

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

### <span data-ttu-id="83aa6-118">-ASN</span><span class="sxs-lookup"><span data-stu-id="83aa6-118">-Asn</span></span>
<span data-ttu-id="83aa6-119">L'ASN da registrare</span><span class="sxs-lookup"><span data-stu-id="83aa6-119">The ASN to be registered</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83aa6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83aa6-120">-DefaultProfile</span></span>
<span data-ttu-id="83aa6-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="83aa6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83aa6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83aa6-122">-InputObject</span></span>
<span data-ttu-id="83aa6-123">Usare un Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="83aa6-123">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83aa6-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="83aa6-124">-Name</span></span>
<span data-ttu-id="83aa6-125">L'ASN da registrare</span><span class="sxs-lookup"><span data-stu-id="83aa6-125">The ASN to be registered</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83aa6-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="83aa6-126">-PeeringName</span></span>
<span data-ttu-id="83aa6-127">Nome univoco di PSPeering.</span><span class="sxs-lookup"><span data-stu-id="83aa6-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="83aa6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83aa6-128">-ResourceGroupName</span></span>
<span data-ttu-id="83aa6-129">Il nome della risorsa crea o usa un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="83aa6-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="83aa6-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83aa6-130">-ResourceId</span></span>
<span data-ttu-id="83aa6-131">Nome della stringa ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="83aa6-131">The resource id string name.</span></span>

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

### <span data-ttu-id="83aa6-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="83aa6-132">-Confirm</span></span>
<span data-ttu-id="83aa6-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83aa6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83aa6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83aa6-134">-WhatIf</span></span>
<span data-ttu-id="83aa6-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83aa6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83aa6-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83aa6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83aa6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83aa6-137">CommonParameters</span></span>
<span data-ttu-id="83aa6-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83aa6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83aa6-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83aa6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83aa6-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="83aa6-140">INPUTS</span></span>

### <span data-ttu-id="83aa6-141">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="83aa6-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="83aa6-142">System. String</span><span class="sxs-lookup"><span data-stu-id="83aa6-142">System.String</span></span>

## <span data-ttu-id="83aa6-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83aa6-143">OUTPUTS</span></span>

### <span data-ttu-id="83aa6-144">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="83aa6-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="83aa6-145">Note</span><span class="sxs-lookup"><span data-stu-id="83aa6-145">NOTES</span></span>

## <span data-ttu-id="83aa6-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83aa6-146">RELATED LINKS</span></span>
