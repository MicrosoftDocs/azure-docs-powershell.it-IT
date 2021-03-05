---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
ms.openlocfilehash: d4fcdb1ad5606753980ea323137d0b77a8580ce4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976654"
---
# <span data-ttu-id="c5259-101">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c5259-101">Remove-AzCustomIpPrefix</span></span>

## <span data-ttu-id="c5259-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5259-102">SYNOPSIS</span></span>
<span data-ttu-id="c5259-103">Rimuove un suffisso CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c5259-103">Removes a CustomIpPrefix</span></span>

## <span data-ttu-id="c5259-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5259-104">SYNTAX</span></span>

### <span data-ttu-id="c5259-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c5259-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5259-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5259-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzCustomIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c5259-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5259-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5259-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c5259-108">DESCRIPTION</span></span>
<span data-ttu-id="c5259-109">Il cmdlet **Remove-AzCustomIpPrefix** rimuove un suffisso CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="c5259-109">The **Remove-AzCustomIpPrefix** cmdlet removes a CustomIpPrefix.</span></span>

## <span data-ttu-id="c5259-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5259-110">EXAMPLES</span></span>

### <span data-ttu-id="c5259-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c5259-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="c5259-112">Rimuove lo strumento CustomIpPrefix con nome $prefixName gruppo di risorse $rgName</span><span class="sxs-lookup"><span data-stu-id="c5259-112">Removes the CustomIpPrefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="c5259-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5259-113">PARAMETERS</span></span>

### <span data-ttu-id="c5259-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5259-114">-AsJob</span></span>
<span data-ttu-id="c5259-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c5259-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5259-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5259-116">-DefaultProfile</span></span>
<span data-ttu-id="c5259-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c5259-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5259-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c5259-118">-Force</span></span>
<span data-ttu-id="c5259-119">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="c5259-119">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5259-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5259-120">-InputObject</span></span>
<span data-ttu-id="c5259-121">Oggetto customIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="c5259-121">A customIpPrefix object.</span></span>

```yaml
Type: PSCustomIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5259-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c5259-122">-Name</span></span>
<span data-ttu-id="c5259-123">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="c5259-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5259-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c5259-124">-PassThru</span></span>
<span data-ttu-id="c5259-125">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="c5259-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c5259-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="c5259-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5259-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5259-127">-ResourceGroupName</span></span>
<span data-ttu-id="c5259-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c5259-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5259-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5259-129">-ResourceId</span></span>
<span data-ttu-id="c5259-130">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="c5259-130">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5259-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5259-131">-Confirm</span></span>
<span data-ttu-id="c5259-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5259-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5259-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5259-133">-WhatIf</span></span>
<span data-ttu-id="c5259-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5259-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5259-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c5259-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5259-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5259-136">CommonParameters</span></span>
<span data-ttu-id="c5259-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5259-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5259-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c5259-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5259-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="c5259-139">INPUTS</span></span>

### <span data-ttu-id="c5259-140">System.String</span><span class="sxs-lookup"><span data-stu-id="c5259-140">System.String</span></span>

### <span data-ttu-id="c5259-141">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c5259-141">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="c5259-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5259-142">OUTPUTS</span></span>

### <span data-ttu-id="c5259-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c5259-143">System.Boolean</span></span>

## <span data-ttu-id="c5259-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="c5259-144">NOTES</span></span>

## <span data-ttu-id="c5259-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5259-145">RELATED LINKS</span></span>

[<span data-ttu-id="c5259-146">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c5259-146">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="c5259-147">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c5259-147">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="c5259-148">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="c5259-148">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)