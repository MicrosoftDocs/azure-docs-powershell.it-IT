---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
ms.openlocfilehash: bcb250c8967c10e5b200e62d843e99eab374d81d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179494"
---
# <span data-ttu-id="d8bd5-101">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d8bd5-101">Remove-AzCustomIpPrefix</span></span>

## <span data-ttu-id="d8bd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8bd5-102">SYNOPSIS</span></span>
<span data-ttu-id="d8bd5-103">Rimuove un suffisso CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d8bd5-103">Removes a CustomIpPrefix</span></span>

## <span data-ttu-id="d8bd5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d8bd5-104">SYNTAX</span></span>

### <span data-ttu-id="d8bd5-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d8bd5-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8bd5-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8bd5-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzCustomIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8bd5-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8bd5-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8bd5-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d8bd5-108">DESCRIPTION</span></span>
<span data-ttu-id="d8bd5-109">Il cmdlet **Remove-AzCustomIpPrefix** rimuove un suffisso CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="d8bd5-109">The **Remove-AzCustomIpPrefix** cmdlet removes a CustomIpPrefix.</span></span>

## <span data-ttu-id="d8bd5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d8bd5-110">EXAMPLES</span></span>

### <span data-ttu-id="d8bd5-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d8bd5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="d8bd5-112">Rimuove lo strumento CustomIpPrefix con nome $prefixName gruppo di risorse $rgName</span><span class="sxs-lookup"><span data-stu-id="d8bd5-112">Removes the CustomIpPrefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="d8bd5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8bd5-113">PARAMETERS</span></span>

### <span data-ttu-id="d8bd5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8bd5-114">-AsJob</span></span>
<span data-ttu-id="d8bd5-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d8bd5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8bd5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8bd5-116">-DefaultProfile</span></span>
<span data-ttu-id="d8bd5-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d8bd5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8bd5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d8bd5-118">-Force</span></span>
<span data-ttu-id="d8bd5-119">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="d8bd5-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d8bd5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8bd5-120">-InputObject</span></span>
<span data-ttu-id="d8bd5-121">Oggetto customIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="d8bd5-121">A customIpPrefix object.</span></span>

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

### <span data-ttu-id="d8bd5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d8bd5-122">-Name</span></span>
<span data-ttu-id="d8bd5-123">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d8bd5-123">The resource name.</span></span>

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

### <span data-ttu-id="d8bd5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8bd5-124">-PassThru</span></span>
<span data-ttu-id="d8bd5-125">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="d8bd5-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d8bd5-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="d8bd5-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d8bd5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8bd5-127">-ResourceGroupName</span></span>
<span data-ttu-id="d8bd5-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d8bd5-128">The resource group name.</span></span>

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

### <span data-ttu-id="d8bd5-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8bd5-129">-ResourceId</span></span>
<span data-ttu-id="d8bd5-130">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d8bd5-130">The resource id.</span></span>

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

### <span data-ttu-id="d8bd5-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8bd5-131">-Confirm</span></span>
<span data-ttu-id="d8bd5-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8bd5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8bd5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8bd5-133">-WhatIf</span></span>
<span data-ttu-id="d8bd5-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d8bd5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8bd5-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d8bd5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8bd5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8bd5-136">CommonParameters</span></span>
<span data-ttu-id="d8bd5-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8bd5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8bd5-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d8bd5-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8bd5-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="d8bd5-139">INPUTS</span></span>

### <span data-ttu-id="d8bd5-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d8bd5-140">System.String</span></span>

### <span data-ttu-id="d8bd5-141">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d8bd5-141">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="d8bd5-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d8bd5-142">OUTPUTS</span></span>

### <span data-ttu-id="d8bd5-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d8bd5-143">System.Boolean</span></span>

## <span data-ttu-id="d8bd5-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="d8bd5-144">NOTES</span></span>

## <span data-ttu-id="d8bd5-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d8bd5-145">RELATED LINKS</span></span>

[<span data-ttu-id="d8bd5-146">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d8bd5-146">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="d8bd5-147">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d8bd5-147">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="d8bd5-148">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="d8bd5-148">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)