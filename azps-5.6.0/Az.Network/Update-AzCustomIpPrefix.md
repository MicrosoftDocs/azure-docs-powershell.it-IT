---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
ms.openlocfilehash: 9d0bca8be88c0448916df27544ce35bf7a6ddee1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951709"
---
# <span data-ttu-id="57491-101">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="57491-101">Update-AzCustomIpPrefix</span></span>

## <span data-ttu-id="57491-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57491-102">SYNOPSIS</span></span>
<span data-ttu-id="57491-103">Aggiorna un formato CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="57491-103">Updates a CustomIpPrefix</span></span>

## <span data-ttu-id="57491-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="57491-104">SYNTAX</span></span>

### <span data-ttu-id="57491-105">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="57491-105">UpdateByNameParameterSet</span></span>
```
Update-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Commission] [-Decomission]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57491-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57491-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Commission] [-Decomission] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57491-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="57491-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzCustomIpPrefix -ResourceId <String> [-Commission] [-Decomission] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57491-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="57491-108">DESCRIPTION</span></span>
<span data-ttu-id="57491-109">Il cmdlet **Update-AzCustomIpPrefix** consente all'utente di commissionare o rimuovere il proprio nome CustomIpPrefix oppure di modificare i tag della risorsa.</span><span class="sxs-lookup"><span data-stu-id="57491-109">The **Update-AzCustomIpPrefix** cmdlet allows the user to either commission or decommission their CustomIpPrefix, or edit the tags of the resource.</span></span>

## <span data-ttu-id="57491-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="57491-110">EXAMPLES</span></span>

### <span data-ttu-id="57491-111">Esempio 1: Commissione del suffisso CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="57491-111">Example 1 : Commission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Commission
```

<span data-ttu-id="57491-112">Il comando precedente avvia il processo di commissioning di CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="57491-112">The above command will start the commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="57491-113">Esempio 2: Rimuovere lo strumento CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="57491-113">Example 2 : Decommission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Decommission
```

<span data-ttu-id="57491-114">Il comando precedente avvia il processo di de-commissioning di CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="57491-114">The above command will start the de-commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="57491-115">Esempio 3: Tag di aggiornamento per CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="57491-115">Example 3 : Update tags for the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Tag $tags
```

<span data-ttu-id="57491-116">Il comando precedente aggiornerà i tag per CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="57491-116">The above command will update the tags for the CustomIpPrefix.</span></span>

## <span data-ttu-id="57491-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57491-117">PARAMETERS</span></span>

### <span data-ttu-id="57491-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57491-118">-AsJob</span></span>
<span data-ttu-id="57491-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="57491-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="57491-120">-Commission</span><span class="sxs-lookup"><span data-stu-id="57491-120">-Commission</span></span>
<span data-ttu-id="57491-121">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="57491-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="57491-122">-Decomission</span><span class="sxs-lookup"><span data-stu-id="57491-122">-Decomission</span></span>
<span data-ttu-id="57491-123">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="57491-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="57491-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57491-124">-DefaultProfile</span></span>
<span data-ttu-id="57491-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="57491-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57491-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57491-126">-InputObject</span></span>
<span data-ttu-id="57491-127">Lo strumento CustomIpPrefix da impostare.</span><span class="sxs-lookup"><span data-stu-id="57491-127">The CustomIpPrefix to set.</span></span>

```yaml
Type: PSCustomIpPrefix
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57491-128">-Name</span><span class="sxs-lookup"><span data-stu-id="57491-128">-Name</span></span>
<span data-ttu-id="57491-129">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="57491-129">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57491-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57491-130">-ResourceGroupName</span></span>
<span data-ttu-id="57491-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="57491-131">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57491-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57491-132">-ResourceId</span></span>
<span data-ttu-id="57491-133">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="57491-133">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57491-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="57491-134">-Tag</span></span>
<span data-ttu-id="57491-135">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="57491-135">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Hashtable
Parameter Sets: SetByInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57491-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57491-136">-Confirm</span></span>
<span data-ttu-id="57491-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57491-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57491-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57491-138">-WhatIf</span></span>
<span data-ttu-id="57491-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="57491-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57491-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="57491-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57491-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57491-141">CommonParameters</span></span>
<span data-ttu-id="57491-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57491-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57491-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="57491-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57491-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="57491-144">INPUTS</span></span>

### <span data-ttu-id="57491-145">System.String</span><span class="sxs-lookup"><span data-stu-id="57491-145">System.String</span></span>

### <span data-ttu-id="57491-146">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="57491-146">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

### <span data-ttu-id="57491-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="57491-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="57491-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="57491-148">OUTPUTS</span></span>

### <span data-ttu-id="57491-149">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="57491-149">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="57491-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="57491-150">NOTES</span></span>

## <span data-ttu-id="57491-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="57491-151">RELATED LINKS</span></span>

[<span data-ttu-id="57491-152">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="57491-152">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="57491-153">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="57491-153">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="57491-154">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="57491-154">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)