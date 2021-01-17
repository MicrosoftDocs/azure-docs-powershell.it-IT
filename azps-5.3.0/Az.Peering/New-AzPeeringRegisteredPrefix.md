---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/new-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: ec3e37cafca19aefce7634bf84be41cd00e4e04d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384747"
---
# <span data-ttu-id="b8c4f-101">New-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="b8c4f-101">New-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="b8c4f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b8c4f-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c4f-103">Creare prefissi registrati per gli oggetti peering.</span><span class="sxs-lookup"><span data-stu-id="b8c4f-103">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="b8c4f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b8c4f-104">SYNTAX</span></span>

### <span data-ttu-id="b8c4f-105">ByResourceGroupAndName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b8c4f-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8c4f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b8c4f-106">InputObject</span></span>
```
New-AzPeeringRegisteredPrefix -InputObject <PSPeering> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8c4f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b8c4f-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8c4f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8c4f-108">DESCRIPTION</span></span>
<span data-ttu-id="b8c4f-109">Creare prefissi registrati per gli oggetti peering.</span><span class="sxs-lookup"><span data-stu-id="b8c4f-109">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="b8c4f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b8c4f-110">EXAMPLES</span></span>

### <span data-ttu-id="b8c4f-111">Ottenere il peering e creare un prefisso registrato</span><span class="sxs-lookup"><span data-stu-id="b8c4f-111">Get peering and create a registered prefix</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredPrefix -Name $asnName -Asn $asn
```

<span data-ttu-id="b8c4f-112">Ottenere il peering che si vuole aggiungere un prefisso registrato.</span><span class="sxs-lookup"><span data-stu-id="b8c4f-112">Get the peering you want to add a registered prefix.</span></span> <span data-ttu-id="b8c4f-113">Passa quindi a unifiedgroup.</span><span class="sxs-lookup"><span data-stu-id="b8c4f-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="b8c4f-114">Usare il peering resourceId per creare un ASN registrato</span><span class="sxs-lookup"><span data-stu-id="b8c4f-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredPrefix -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="b8c4f-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b8c4f-115">PARAMETERS</span></span>

### <span data-ttu-id="b8c4f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b8c4f-116">-AsJob</span></span>
<span data-ttu-id="b8c4f-117">Eseguire in background.</span><span class="sxs-lookup"><span data-stu-id="b8c4f-117">Run in the background.</span></span>

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

### <span data-ttu-id="b8c4f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8c4f-118">-DefaultProfile</span></span>
<span data-ttu-id="b8c4f-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b8c4f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8c4f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8c4f-120">-InputObject</span></span>
<span data-ttu-id="b8c4f-121">Usare un Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="b8c4f-121">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="b8c4f-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="b8c4f-122">-Name</span></span>
<span data-ttu-id="b8c4f-123">Il nome del prefisso.</span><span class="sxs-lookup"><span data-stu-id="b8c4f-123">The name of prefix.</span></span>

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

### <span data-ttu-id="b8c4f-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="b8c4f-124">-PeeringName</span></span>
<span data-ttu-id="b8c4f-125">Nome univoco di PSPeering.</span><span class="sxs-lookup"><span data-stu-id="b8c4f-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="b8c4f-126">-Prefisso</span><span class="sxs-lookup"><span data-stu-id="b8c4f-126">-Prefix</span></span>
<span data-ttu-id="b8c4f-127">Prefisso IPv4 della sessione</span><span class="sxs-lookup"><span data-stu-id="b8c4f-127">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="b8c4f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8c4f-128">-ResourceGroupName</span></span>
<span data-ttu-id="b8c4f-129">Il nome della risorsa crea o usa un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="b8c4f-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="b8c4f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8c4f-130">-ResourceId</span></span>
<span data-ttu-id="b8c4f-131">Nome della stringa ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="b8c4f-131">The resource id string name.</span></span>

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

### <span data-ttu-id="b8c4f-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b8c4f-132">-Confirm</span></span>
<span data-ttu-id="b8c4f-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8c4f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8c4f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8c4f-134">-WhatIf</span></span>
<span data-ttu-id="b8c4f-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b8c4f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8c4f-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b8c4f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8c4f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c4f-137">CommonParameters</span></span>
<span data-ttu-id="b8c4f-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8c4f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c4f-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8c4f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c4f-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b8c4f-140">INPUTS</span></span>

### <span data-ttu-id="b8c4f-141">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeering</span><span class="sxs-lookup"><span data-stu-id="b8c4f-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="b8c4f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b8c4f-142">System.String</span></span>

## <span data-ttu-id="b8c4f-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b8c4f-143">OUTPUTS</span></span>

### <span data-ttu-id="b8c4f-144">Microsoft. Azure. PowerShell. Cmdlets. peering. Models. PSPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="b8c4f-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="b8c4f-145">Note</span><span class="sxs-lookup"><span data-stu-id="b8c4f-145">NOTES</span></span>

## <span data-ttu-id="b8c4f-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b8c4f-146">RELATED LINKS</span></span>
