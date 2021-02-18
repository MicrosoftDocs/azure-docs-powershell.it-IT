---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: 83d36cfdb892cc5366aabb589f3536e18e79eace
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202238"
---
# <span data-ttu-id="ecb23-101">Set-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="ecb23-101">Set-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="ecb23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecb23-102">SYNOPSIS</span></span>
<span data-ttu-id="ecb23-103">Imposta o aggiorna un prefisso registrato dalla risorsa peering padre.</span><span class="sxs-lookup"><span data-stu-id="ecb23-103">Sets or updates a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="ecb23-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ecb23-104">SYNTAX</span></span>

### <span data-ttu-id="ecb23-105">ByResourceGroupAndName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ecb23-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecb23-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ecb23-106">InputObject</span></span>
```
Set-AzPeeringRegisteredPrefix -InputObject <PSPeeringRegisteredPrefix> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecb23-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ecb23-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecb23-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ecb23-108">DESCRIPTION</span></span>
<span data-ttu-id="ecb23-109">Consente l'aggiornamento di un prefisso registrato dalla risorsa peering padre.</span><span class="sxs-lookup"><span data-stu-id="ecb23-109">Allows the updating of a registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="ecb23-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ecb23-110">EXAMPLES</span></span>

### <span data-ttu-id="ecb23-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ecb23-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredPrefix -ResourceId $resourceId -Prefix $newPrefix
```

<span data-ttu-id="ecb23-112">Aggiorna il prefisso in base all'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="ecb23-112">Updates the prefix by resource id.</span></span>

## <span data-ttu-id="ecb23-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ecb23-113">PARAMETERS</span></span>

### <span data-ttu-id="ecb23-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ecb23-114">-AsJob</span></span>
<span data-ttu-id="ecb23-115">Esegui in background.</span><span class="sxs-lookup"><span data-stu-id="ecb23-115">Run in the background.</span></span>

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

### <span data-ttu-id="ecb23-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecb23-116">-DefaultProfile</span></span>
<span data-ttu-id="ecb23-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ecb23-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecb23-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ecb23-118">-InputObject</span></span>
<span data-ttu-id="ecb23-119">Usare un Get-AzPeering</span><span class="sxs-lookup"><span data-stu-id="ecb23-119">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecb23-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ecb23-120">-Name</span></span>
<span data-ttu-id="ecb23-121">Nome del prefisso.</span><span class="sxs-lookup"><span data-stu-id="ecb23-121">The name of prefix.</span></span>

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

### <span data-ttu-id="ecb23-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="ecb23-122">-PeeringName</span></span>
<span data-ttu-id="ecb23-123">Nome univoco di PSCollectioning.</span><span class="sxs-lookup"><span data-stu-id="ecb23-123">The unique name of the PSPeering.</span></span>

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

### <span data-ttu-id="ecb23-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="ecb23-124">-Prefix</span></span>
<span data-ttu-id="ecb23-125">Prefisso IPv4 della sessione</span><span class="sxs-lookup"><span data-stu-id="ecb23-125">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="ecb23-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecb23-126">-ResourceGroupName</span></span>
<span data-ttu-id="ecb23-127">Creare o usare il nome di un gruppo di risorse esistente.</span><span class="sxs-lookup"><span data-stu-id="ecb23-127">The create or use an existing resource group name.</span></span>

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

### <span data-ttu-id="ecb23-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecb23-128">-ResourceId</span></span>
<span data-ttu-id="ecb23-129">Il nome stringa dell'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="ecb23-129">The resource id string name.</span></span>

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

### <span data-ttu-id="ecb23-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ecb23-130">-Confirm</span></span>
<span data-ttu-id="ecb23-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecb23-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecb23-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecb23-132">-WhatIf</span></span>
<span data-ttu-id="ecb23-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ecb23-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecb23-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ecb23-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecb23-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecb23-135">CommonParameters</span></span>
<span data-ttu-id="ecb23-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecb23-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecb23-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ecb23-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecb23-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="ecb23-138">INPUTS</span></span>

### <span data-ttu-id="ecb23-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="ecb23-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

### <span data-ttu-id="ecb23-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ecb23-140">System.String</span></span>

## <span data-ttu-id="ecb23-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ecb23-141">OUTPUTS</span></span>

### <span data-ttu-id="ecb23-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="ecb23-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="ecb23-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="ecb23-143">NOTES</span></span>

## <span data-ttu-id="ecb23-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ecb23-144">RELATED LINKS</span></span>
