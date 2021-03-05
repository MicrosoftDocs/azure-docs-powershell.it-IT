---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredAsn.md
ms.openlocfilehash: 8d5567d99d7ba7470fb44738bed128d8a438c733
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989350"
---
# <span data-ttu-id="b6c7e-101">New-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="b6c7e-101">New-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="b6c7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6c7e-102">SYNOPSIS</span></span>
<span data-ttu-id="b6c7e-103">Creare un ASN registrato per il peering</span><span class="sxs-lookup"><span data-stu-id="b6c7e-103">Create registered ASN for peering</span></span>

## <span data-ttu-id="b6c7e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b6c7e-104">SYNTAX</span></span>

### <span data-ttu-id="b6c7e-105">ByResourceGroupAndName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b6c7e-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6c7e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b6c7e-106">InputObject</span></span>
```
New-AzPeeringRegisteredAsn -InputObject <PSPeering> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6c7e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b6c7e-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6c7e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b6c7e-108">DESCRIPTION</span></span>
<span data-ttu-id="b6c7e-109">Creare asN registrati per gli oggetti di peering.</span><span class="sxs-lookup"><span data-stu-id="b6c7e-109">Create registered ASNs for peering objects.</span></span>

## <span data-ttu-id="b6c7e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b6c7e-110">EXAMPLES</span></span>

### <span data-ttu-id="b6c7e-111">Ottenere il peering e creare un ASN registrato</span><span class="sxs-lookup"><span data-stu-id="b6c7e-111">Get peering and create a registered ASN</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredAsn -Name $asnName -Asn $asn
```

<span data-ttu-id="b6c7e-112">Ottenere il peering a cui si vuole aggiungere un asN registrato.</span><span class="sxs-lookup"><span data-stu-id="b6c7e-112">Get the peering you want to add a registered ASN.</span></span> <span data-ttu-id="b6c7e-113">Passare quindi questo al commandlet.</span><span class="sxs-lookup"><span data-stu-id="b6c7e-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="b6c7e-114">Usare l'ID risorsa peering per creare una rete asn registrata</span><span class="sxs-lookup"><span data-stu-id="b6c7e-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredAsn -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="b6c7e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b6c7e-115">PARAMETERS</span></span>

### <span data-ttu-id="b6c7e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6c7e-116">-AsJob</span></span>
<span data-ttu-id="b6c7e-117">Esegui in background.</span><span class="sxs-lookup"><span data-stu-id="b6c7e-117">Run in the background.</span></span>

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

### <span data-ttu-id="b6c7e-118">-Asn</span><span class="sxs-lookup"><span data-stu-id="b6c7e-118">-Asn</span></span>
<span data-ttu-id="b6c7e-119">L'ASN da registrare</span><span class="sxs-lookup"><span data-stu-id="b6c7e-119">The ASN to be registered</span></span>

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

### <span data-ttu-id="b6c7e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6c7e-120">-DefaultProfile</span></span>
<span data-ttu-id="b6c7e-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b6c7e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6c7e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6c7e-122">-InputObject</span></span>
<span data-ttu-id="b6c7e-123">Usare un Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="b6c7e-123">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="b6c7e-124">-Name</span><span class="sxs-lookup"><span data-stu-id="b6c7e-124">-Name</span></span>
<span data-ttu-id="b6c7e-125">L'ASN da registrare</span><span class="sxs-lookup"><span data-stu-id="b6c7e-125">The ASN to be registered</span></span>

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

### <span data-ttu-id="b6c7e-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="b6c7e-126">-PeeringName</span></span>
<span data-ttu-id="b6c7e-127">Nome univoco di PSCollectioning.</span><span class="sxs-lookup"><span data-stu-id="b6c7e-127">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="b6c7e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6c7e-128">-ResourceGroupName</span></span>
<span data-ttu-id="b6c7e-129">Creare o usare il nome di un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="b6c7e-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="b6c7e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6c7e-130">-ResourceId</span></span>
<span data-ttu-id="b6c7e-131">Il nome stringa dell'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="b6c7e-131">The resource id string name.</span></span>

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

### <span data-ttu-id="b6c7e-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b6c7e-132">-Confirm</span></span>
<span data-ttu-id="b6c7e-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6c7e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6c7e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6c7e-134">-WhatIf</span></span>
<span data-ttu-id="b6c7e-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6c7e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6c7e-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b6c7e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6c7e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6c7e-137">CommonParameters</span></span>
<span data-ttu-id="b6c7e-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6c7e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6c7e-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b6c7e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6c7e-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="b6c7e-140">INPUTS</span></span>

### <span data-ttu-id="b6c7e-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSCollectioning</span><span class="sxs-lookup"><span data-stu-id="b6c7e-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="b6c7e-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b6c7e-142">System.String</span></span>

## <span data-ttu-id="b6c7e-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b6c7e-143">OUTPUTS</span></span>

### <span data-ttu-id="b6c7e-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="b6c7e-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="b6c7e-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="b6c7e-145">NOTES</span></span>

## <span data-ttu-id="b6c7e-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b6c7e-146">RELATED LINKS</span></span>
