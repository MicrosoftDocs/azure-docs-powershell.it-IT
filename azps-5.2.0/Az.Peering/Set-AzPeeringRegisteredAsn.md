---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredAsn.md
ms.openlocfilehash: a0a1ab176c4e38e961f78e0230a46bc2eaea964a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352168"
---
# <span data-ttu-id="e3c22-101">Set-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="e3c22-101">Set-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="e3c22-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e3c22-102">SYNOPSIS</span></span>
<span data-ttu-id="e3c22-103">Imposta o aggiorna un ASN registrato dalla risorsa peering padre.</span><span class="sxs-lookup"><span data-stu-id="e3c22-103">Sets or updates a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="e3c22-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3c22-104">SYNTAX</span></span>

### <span data-ttu-id="e3c22-105">ByResourceGroupAndName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e3c22-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> -Asn <Int32>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3c22-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e3c22-106">InputObject</span></span>
```
Set-AzPeeringRegisteredAsn -InputObject <PSPeeringRegisteredAsn> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3c22-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e3c22-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredAsn [-ResourceId] <String> [-Name] <String> -Asn <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3c22-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3c22-108">DESCRIPTION</span></span>
<span data-ttu-id="e3c22-109">Consente l'aggiornamento di un oggetto ASN registrato dalla risorsa peering padre.</span><span class="sxs-lookup"><span data-stu-id="e3c22-109">Allows the updating of a registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="e3c22-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3c22-110">EXAMPLES</span></span>

### <span data-ttu-id="e3c22-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e3c22-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredAsn -ResourceId $resourceId -Asn $asn
```

<span data-ttu-id="e3c22-112">Aggiorna l'ID della risorsa ASN per.</span><span class="sxs-lookup"><span data-stu-id="e3c22-112">Updates the ASN by resource id.</span></span>

## <span data-ttu-id="e3c22-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e3c22-113">PARAMETERS</span></span>

### <span data-ttu-id="e3c22-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3c22-114">-AsJob</span></span>
<span data-ttu-id="e3c22-115">Eseguire in background.</span><span class="sxs-lookup"><span data-stu-id="e3c22-115">Run in the background.</span></span>

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

### <span data-ttu-id="e3c22-116">-ASN</span><span class="sxs-lookup"><span data-stu-id="e3c22-116">-Asn</span></span>
<span data-ttu-id="e3c22-117">L'ASN da registrare</span><span class="sxs-lookup"><span data-stu-id="e3c22-117">The ASN to be registered</span></span>

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

### <span data-ttu-id="e3c22-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3c22-118">-DefaultProfile</span></span>
<span data-ttu-id="e3c22-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3c22-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3c22-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3c22-120">-InputObject</span></span>
<span data-ttu-id="e3c22-121">Usare un Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="e3c22-121">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="e3c22-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3c22-122">-Name</span></span>
<span data-ttu-id="e3c22-123">L'ASN da registrare</span><span class="sxs-lookup"><span data-stu-id="e3c22-123">The ASN to be registered</span></span>

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

### <span data-ttu-id="e3c22-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="e3c22-124">-PeeringName</span></span>
<span data-ttu-id="e3c22-125">Nome univoco di PSPeering.</span><span class="sxs-lookup"><span data-stu-id="e3c22-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="e3c22-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3c22-126">-ResourceGroupName</span></span>
<span data-ttu-id="e3c22-127">Il nome della risorsa crea o usa un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="e3c22-127">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="e3c22-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3c22-128">-ResourceId</span></span>
<span data-ttu-id="e3c22-129">Nome della stringa ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="e3c22-129">The resource id string name.</span></span>

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

### <span data-ttu-id="e3c22-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e3c22-130">-Confirm</span></span>
<span data-ttu-id="e3c22-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3c22-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3c22-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3c22-132">-WhatIf</span></span>
<span data-ttu-id="e3c22-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3c22-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3c22-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3c22-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3c22-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3c22-135">CommonParameters</span></span>
<span data-ttu-id="e3c22-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3c22-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3c22-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3c22-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3c22-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e3c22-138">INPUTS</span></span>

### <span data-ttu-id="e3c22-139">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="e3c22-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

### <span data-ttu-id="e3c22-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e3c22-140">System.String</span></span>

## <span data-ttu-id="e3c22-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3c22-141">OUTPUTS</span></span>

### <span data-ttu-id="e3c22-142">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="e3c22-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredAsn</span></span>

## <span data-ttu-id="e3c22-143">Note</span><span class="sxs-lookup"><span data-stu-id="e3c22-143">NOTES</span></span>

## <span data-ttu-id="e3c22-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3c22-144">RELATED LINKS</span></span>
