---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
ms.openlocfilehash: a0a1ab176c4e38e961f78e0230a46bc2eaea964a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193191"
---
# <span data-ttu-id="693c4-101">Set-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="693c4-101">Set-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="693c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="693c4-102">SYNOPSIS</span></span>
<span data-ttu-id="693c4-103">Imposta o aggiorna un ASN registrato dalla risorsa peering padre.</span><span class="sxs-lookup"><span data-stu-id="693c4-103">Sets or updates a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="693c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="693c4-104">SYNTAX</span></span>

### <span data-ttu-id="693c4-105">ByResourceGroupAndName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="693c4-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="693c4-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="693c4-106">InputObject</span></span>
```
Set-AzPeeringRegisteredAsn -InputObject <PSPeeringRegisteredAsn> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="693c4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="693c4-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="693c4-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="693c4-108">DESCRIPTION</span></span>
<span data-ttu-id="693c4-109">Consente l'aggiornamento di un ASN registrato dalla risorsa peering padre.</span><span class="sxs-lookup"><span data-stu-id="693c4-109">Allows the updating of a registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="693c4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="693c4-110">EXAMPLES</span></span>

### <span data-ttu-id="693c4-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="693c4-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredAsn -ResourceId $resourceId -Asn $asn
```

<span data-ttu-id="693c4-112">Aggiorna l'ASN in base all'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="693c4-112">Updates the ASN by resource id.</span></span>

## <span data-ttu-id="693c4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="693c4-113">PARAMETERS</span></span>

### <span data-ttu-id="693c4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="693c4-114">-AsJob</span></span>
<span data-ttu-id="693c4-115">Esegui in background.</span><span class="sxs-lookup"><span data-stu-id="693c4-115">Run in the background.</span></span>

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

### <span data-ttu-id="693c4-116">-Asn</span><span class="sxs-lookup"><span data-stu-id="693c4-116">-Asn</span></span>
<span data-ttu-id="693c4-117">L'ASN da registrare</span><span class="sxs-lookup"><span data-stu-id="693c4-117">The ASN to be registered</span></span>

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

### <span data-ttu-id="693c4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="693c4-118">-DefaultProfile</span></span>
<span data-ttu-id="693c4-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="693c4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="693c4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="693c4-120">-InputObject</span></span>
<span data-ttu-id="693c4-121">Usare un Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="693c4-121">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="693c4-122">-Name</span><span class="sxs-lookup"><span data-stu-id="693c4-122">-Name</span></span>
<span data-ttu-id="693c4-123">L'ASN da registrare</span><span class="sxs-lookup"><span data-stu-id="693c4-123">The ASN to be registered</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, ByResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="693c4-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="693c4-124">-PeeringName</span></span>
<span data-ttu-id="693c4-125">Nome univoco di PSCollectioning.</span><span class="sxs-lookup"><span data-stu-id="693c4-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="693c4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="693c4-126">-ResourceGroupName</span></span>
<span data-ttu-id="693c4-127">Creare o usare il nome di un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="693c4-127">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="693c4-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="693c4-128">-ResourceId</span></span>
<span data-ttu-id="693c4-129">Il nome stringa dell'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="693c4-129">The resource id string name.</span></span>

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

### <span data-ttu-id="693c4-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="693c4-130">-Confirm</span></span>
<span data-ttu-id="693c4-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="693c4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="693c4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="693c4-132">-WhatIf</span></span>
<span data-ttu-id="693c4-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="693c4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="693c4-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="693c4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="693c4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="693c4-135">CommonParameters</span></span>
<span data-ttu-id="693c4-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="693c4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="693c4-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="693c4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="693c4-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="693c4-138">INPUTS</span></span>

### <span data-ttu-id="693c4-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="693c4-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

### <span data-ttu-id="693c4-140">System.String</span><span class="sxs-lookup"><span data-stu-id="693c4-140">System.String</span></span>

## <span data-ttu-id="693c4-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="693c4-141">OUTPUTS</span></span>

### <span data-ttu-id="693c4-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="693c4-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="693c4-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="693c4-143">NOTES</span></span>

## <span data-ttu-id="693c4-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="693c4-144">RELATED LINKS</span></span>
