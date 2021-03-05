---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/new-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/New-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: 212daeffe2ded2dd2571d78afe79fd238349bf3e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989349"
---
# <span data-ttu-id="98062-101">New-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="98062-101">New-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="98062-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98062-102">SYNOPSIS</span></span>
<span data-ttu-id="98062-103">Creare prefissi registrati per gli oggetti di peering.</span><span class="sxs-lookup"><span data-stu-id="98062-103">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="98062-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="98062-104">SYNTAX</span></span>

### <span data-ttu-id="98062-105">ByResourceGroupAndName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="98062-105">ByResourceGroupAndName (Default)</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98062-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="98062-106">InputObject</span></span>
```
New-AzPeeringRegisteredPrefix -InputObject <PSPeering> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98062-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="98062-107">ByResourceId</span></span>
```
New-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98062-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="98062-108">DESCRIPTION</span></span>
<span data-ttu-id="98062-109">Creare prefissi registrati per gli oggetti di peering.</span><span class="sxs-lookup"><span data-stu-id="98062-109">Create registered prefixes for peering objects.</span></span>

## <span data-ttu-id="98062-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="98062-110">EXAMPLES</span></span>

### <span data-ttu-id="98062-111">Ottenere il peering e creare un prefisso registrato</span><span class="sxs-lookup"><span data-stu-id="98062-111">Get peering and create a registered prefix</span></span>
```powershell
PS C:\>$peering = Get-AzPeering -ResourceGroupName $resourceGroupName -Name $name
PS C:\>$peering | New-AzPeeringRegisteredPrefix -Name $asnName -Asn $asn
```

<span data-ttu-id="98062-112">Ottenere il peering a cui si vuole aggiungere un prefisso registrato.</span><span class="sxs-lookup"><span data-stu-id="98062-112">Get the peering you want to add a registered prefix.</span></span> <span data-ttu-id="98062-113">Passare quindi questo al commandlet.</span><span class="sxs-lookup"><span data-stu-id="98062-113">Then pass that to the commandlet.</span></span>

### <span data-ttu-id="98062-114">Usare resourceId di peering per creare una rete asn registrata</span><span class="sxs-lookup"><span data-stu-id="98062-114">Use peering resourceId to create a registered asn</span></span>
```powershell
PS C:\>New-AzPeeringRegisteredPrefix -ResourceId $resourceId -Name $asnName -Asn $asn
```

## <span data-ttu-id="98062-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98062-115">PARAMETERS</span></span>

### <span data-ttu-id="98062-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98062-116">-AsJob</span></span>
<span data-ttu-id="98062-117">Esegui in background.</span><span class="sxs-lookup"><span data-stu-id="98062-117">Run in the background.</span></span>

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

### <span data-ttu-id="98062-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98062-118">-DefaultProfile</span></span>
<span data-ttu-id="98062-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="98062-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98062-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98062-120">-InputObject</span></span>
<span data-ttu-id="98062-121">Usare un Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="98062-121">Use a Get-AzPeering</span></span>

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

### <span data-ttu-id="98062-122">-Name</span><span class="sxs-lookup"><span data-stu-id="98062-122">-Name</span></span>
<span data-ttu-id="98062-123">Nome del prefisso.</span><span class="sxs-lookup"><span data-stu-id="98062-123">The name of prefix.</span></span>

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

### <span data-ttu-id="98062-124">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="98062-124">-PeeringName</span></span>
<span data-ttu-id="98062-125">Nome univoco di PSCollectioning.</span><span class="sxs-lookup"><span data-stu-id="98062-125">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="98062-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="98062-126">-Prefix</span></span>
<span data-ttu-id="98062-127">Prefisso IPv4 della sessione</span><span class="sxs-lookup"><span data-stu-id="98062-127">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="98062-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98062-128">-ResourceGroupName</span></span>
<span data-ttu-id="98062-129">Creare o usare il nome di un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="98062-129">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="98062-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98062-130">-ResourceId</span></span>
<span data-ttu-id="98062-131">Il nome stringa dell'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="98062-131">The resource id string name.</span></span>

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

### <span data-ttu-id="98062-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98062-132">-Confirm</span></span>
<span data-ttu-id="98062-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98062-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98062-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98062-134">-WhatIf</span></span>
<span data-ttu-id="98062-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98062-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98062-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98062-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98062-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98062-137">CommonParameters</span></span>
<span data-ttu-id="98062-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98062-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98062-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="98062-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98062-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="98062-140">INPUTS</span></span>

### <span data-ttu-id="98062-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSApplicationing</span><span class="sxs-lookup"><span data-stu-id="98062-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="98062-142">System.String</span><span class="sxs-lookup"><span data-stu-id="98062-142">System.String</span></span>

## <span data-ttu-id="98062-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="98062-143">OUTPUTS</span></span>

### <span data-ttu-id="98062-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="98062-144">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="98062-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="98062-145">NOTES</span></span>

## <span data-ttu-id="98062-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="98062-146">RELATED LINKS</span></span>
