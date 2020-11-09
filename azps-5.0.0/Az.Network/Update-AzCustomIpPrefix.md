---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
ms.openlocfilehash: 65d47c57720e66ecad8267ae45f9e08eb3e4c4ca
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310746"
---
# <span data-ttu-id="85c57-101">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="85c57-101">Update-AzCustomIpPrefix</span></span>

## <span data-ttu-id="85c57-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="85c57-102">SYNOPSIS</span></span>
<span data-ttu-id="85c57-103">Aggiorna un CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="85c57-103">Updates a CustomIpPrefix</span></span>

## <span data-ttu-id="85c57-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85c57-104">SYNTAX</span></span>

### <span data-ttu-id="85c57-105">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="85c57-105">UpdateByNameParameterSet</span></span>
```
Update-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Commission] [-Decomission]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="85c57-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85c57-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Commission] [-Decomission] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85c57-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="85c57-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzCustomIpPrefix -ResourceId <String> [-Commission] [-Decomission] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85c57-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85c57-108">DESCRIPTION</span></span>
<span data-ttu-id="85c57-109">Il cmdlet **Update-AzCustomIpPrefix** consente all'utente di commissionare o rimuovere il proprio CustomIpPrefix o modificare i tag della risorsa.</span><span class="sxs-lookup"><span data-stu-id="85c57-109">The **Update-AzCustomIpPrefix** cmdlet allows the user to either commission or decommission their CustomIpPrefix, or edit the tags of the resource.</span></span>

## <span data-ttu-id="85c57-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85c57-110">EXAMPLES</span></span>

### <span data-ttu-id="85c57-111">Esempio 1: commissiona il CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="85c57-111">Example 1 : Commission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Commission
```

<span data-ttu-id="85c57-112">Il comando precedente avvierà il processo di messa in servizio della CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="85c57-112">The above command will start the commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="85c57-113">Esempio 2: rimuovere la CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="85c57-113">Example 2 : Decommission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Decommission
```

<span data-ttu-id="85c57-114">Il comando precedente avvierà il processo di disattivazione della CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="85c57-114">The above command will start the de-commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="85c57-115">Esempio 3: aggiornare i tag per CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="85c57-115">Example 3 : Update tags for the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Tag $tags
```

<span data-ttu-id="85c57-116">Il comando sopra aggiornerà i tag per CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="85c57-116">The above command will update the tags for the CustomIpPrefix.</span></span>

## <span data-ttu-id="85c57-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="85c57-117">PARAMETERS</span></span>

### <span data-ttu-id="85c57-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85c57-118">-AsJob</span></span>
<span data-ttu-id="85c57-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="85c57-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="85c57-120">-Commissione</span><span class="sxs-lookup"><span data-stu-id="85c57-120">-Commission</span></span>
<span data-ttu-id="85c57-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="85c57-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="85c57-122">-Decomission</span><span class="sxs-lookup"><span data-stu-id="85c57-122">-Decomission</span></span>
<span data-ttu-id="85c57-123">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="85c57-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="85c57-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85c57-124">-DefaultProfile</span></span>
<span data-ttu-id="85c57-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="85c57-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85c57-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85c57-126">-InputObject</span></span>
<span data-ttu-id="85c57-127">CustomIpPrefix da impostare.</span><span class="sxs-lookup"><span data-stu-id="85c57-127">The CustomIpPrefix to set.</span></span>

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

### <span data-ttu-id="85c57-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="85c57-128">-Name</span></span>
<span data-ttu-id="85c57-129">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="85c57-129">The resource name.</span></span>

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

### <span data-ttu-id="85c57-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85c57-130">-ResourceGroupName</span></span>
<span data-ttu-id="85c57-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="85c57-131">The resource group name.</span></span>

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

### <span data-ttu-id="85c57-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85c57-132">-ResourceId</span></span>
<span data-ttu-id="85c57-133">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="85c57-133">The resource Id.</span></span>

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

### <span data-ttu-id="85c57-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="85c57-134">-Tag</span></span>
<span data-ttu-id="85c57-135">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="85c57-135">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="85c57-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="85c57-136">-Confirm</span></span>
<span data-ttu-id="85c57-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85c57-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85c57-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85c57-138">-WhatIf</span></span>
<span data-ttu-id="85c57-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85c57-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85c57-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85c57-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85c57-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85c57-141">CommonParameters</span></span>
<span data-ttu-id="85c57-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85c57-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85c57-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85c57-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85c57-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="85c57-144">INPUTS</span></span>

### <span data-ttu-id="85c57-145">System. String</span><span class="sxs-lookup"><span data-stu-id="85c57-145">System.String</span></span>

### <span data-ttu-id="85c57-146">Microsoft. Azure. Commands. Network. Models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="85c57-146">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

### <span data-ttu-id="85c57-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="85c57-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="85c57-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85c57-148">OUTPUTS</span></span>

### <span data-ttu-id="85c57-149">Microsoft. Azure. Commands. Network. Models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="85c57-149">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="85c57-150">Note</span><span class="sxs-lookup"><span data-stu-id="85c57-150">NOTES</span></span>

## <span data-ttu-id="85c57-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85c57-151">RELATED LINKS</span></span>

[<span data-ttu-id="85c57-152">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="85c57-152">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="85c57-153">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="85c57-153">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="85c57-154">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="85c57-154">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)