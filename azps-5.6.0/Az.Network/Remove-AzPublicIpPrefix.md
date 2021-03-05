---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
ms.openlocfilehash: f3072871caa5449606afe18093a463fea58c6dfa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976622"
---
# <span data-ttu-id="9eba8-101">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9eba8-101">Remove-AzPublicIpPrefix</span></span>

## <span data-ttu-id="9eba8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9eba8-102">SYNOPSIS</span></span>
<span data-ttu-id="9eba8-103">Rimuove un prefisso IP pubblico</span><span class="sxs-lookup"><span data-stu-id="9eba8-103">Removes a public IP prefix</span></span>

## <span data-ttu-id="9eba8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9eba8-104">SYNTAX</span></span>

### <span data-ttu-id="9eba8-105">RemoveByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9eba8-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9eba8-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9eba8-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9eba8-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9eba8-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9eba8-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9eba8-108">DESCRIPTION</span></span>
<span data-ttu-id="9eba8-109">Il cmdlet **Remove-AzPublicIpPrefix** rimuove un prefisso IP pubblico di Azure, purché non vi siano indirizzi IP pubblici assegnati.</span><span class="sxs-lookup"><span data-stu-id="9eba8-109">The **Remove-AzPublicIpPrefix** cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="9eba8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9eba8-110">EXAMPLES</span></span>

### <span data-ttu-id="9eba8-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9eba8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="9eba8-112">Rimuove il prefisso IP pubblico con nome $prefixName nome dal gruppo di $rgName</span><span class="sxs-lookup"><span data-stu-id="9eba8-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="9eba8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9eba8-113">PARAMETERS</span></span>

### <span data-ttu-id="9eba8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9eba8-114">-AsJob</span></span>
<span data-ttu-id="9eba8-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9eba8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9eba8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eba8-116">-DefaultProfile</span></span>
<span data-ttu-id="9eba8-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9eba8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9eba8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="9eba8-118">-Force</span></span>
<span data-ttu-id="9eba8-119">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="9eba8-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9eba8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9eba8-120">-InputObject</span></span>
<span data-ttu-id="9eba8-121">Oggetto PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9eba8-121">A PublicIpPrefix object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9eba8-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9eba8-122">-Name</span></span>
<span data-ttu-id="9eba8-123">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="9eba8-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9eba8-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9eba8-124">-PassThru</span></span>
<span data-ttu-id="9eba8-125">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="9eba8-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9eba8-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="9eba8-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9eba8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eba8-127">-ResourceGroupName</span></span>
<span data-ttu-id="9eba8-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9eba8-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9eba8-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9eba8-129">-ResourceId</span></span>
<span data-ttu-id="9eba8-130">L'ID risorsa della risorsa da rimuovere</span><span class="sxs-lookup"><span data-stu-id="9eba8-130">The resourceId for the resource to remove</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9eba8-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9eba8-131">-Confirm</span></span>
<span data-ttu-id="9eba8-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9eba8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9eba8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9eba8-133">-WhatIf</span></span>
<span data-ttu-id="9eba8-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9eba8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9eba8-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9eba8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9eba8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eba8-136">CommonParameters</span></span>
<span data-ttu-id="9eba8-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9eba8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eba8-138">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9eba8-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eba8-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="9eba8-139">INPUTS</span></span>

### <span data-ttu-id="9eba8-140">System.String</span><span class="sxs-lookup"><span data-stu-id="9eba8-140">System.String</span></span>

### <span data-ttu-id="9eba8-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9eba8-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="9eba8-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9eba8-142">OUTPUTS</span></span>

### <span data-ttu-id="9eba8-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9eba8-143">System.Boolean</span></span>

## <span data-ttu-id="9eba8-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="9eba8-144">NOTES</span></span>

## <span data-ttu-id="9eba8-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9eba8-145">RELATED LINKS</span></span>

[<span data-ttu-id="9eba8-146">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9eba8-146">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="9eba8-147">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9eba8-147">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="9eba8-148">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="9eba8-148">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
