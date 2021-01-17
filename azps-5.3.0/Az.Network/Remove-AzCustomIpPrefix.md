---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
ms.openlocfilehash: bcb250c8967c10e5b200e62d843e99eab374d81d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474481"
---
# <span data-ttu-id="437bd-101">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="437bd-101">Remove-AzCustomIpPrefix</span></span>

## <span data-ttu-id="437bd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="437bd-102">SYNOPSIS</span></span>
<span data-ttu-id="437bd-103">Rimuove un CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="437bd-103">Removes a CustomIpPrefix</span></span>

## <span data-ttu-id="437bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="437bd-104">SYNTAX</span></span>

### <span data-ttu-id="437bd-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="437bd-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="437bd-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="437bd-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzCustomIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="437bd-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="437bd-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="437bd-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="437bd-108">DESCRIPTION</span></span>
<span data-ttu-id="437bd-109">Il cmdlet **Remove-AzCustomIpPrefix** rimuove un CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="437bd-109">The **Remove-AzCustomIpPrefix** cmdlet removes a CustomIpPrefix.</span></span>

## <span data-ttu-id="437bd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="437bd-110">EXAMPLES</span></span>

### <span data-ttu-id="437bd-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="437bd-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="437bd-112">Rimuove il CustomIpPrefix con il nome $prefixName dal gruppo di risorse $rgName</span><span class="sxs-lookup"><span data-stu-id="437bd-112">Removes the CustomIpPrefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="437bd-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="437bd-113">PARAMETERS</span></span>

### <span data-ttu-id="437bd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="437bd-114">-AsJob</span></span>
<span data-ttu-id="437bd-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="437bd-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="437bd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="437bd-116">-DefaultProfile</span></span>
<span data-ttu-id="437bd-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="437bd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="437bd-118">-Force</span><span class="sxs-lookup"><span data-stu-id="437bd-118">-Force</span></span>
<span data-ttu-id="437bd-119">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="437bd-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="437bd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="437bd-120">-InputObject</span></span>
<span data-ttu-id="437bd-121">Un oggetto customIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="437bd-121">A customIpPrefix object.</span></span>

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

### <span data-ttu-id="437bd-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="437bd-122">-Name</span></span>
<span data-ttu-id="437bd-123">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="437bd-123">The resource name.</span></span>

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

### <span data-ttu-id="437bd-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="437bd-124">-PassThru</span></span>
<span data-ttu-id="437bd-125">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="437bd-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="437bd-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="437bd-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="437bd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="437bd-127">-ResourceGroupName</span></span>
<span data-ttu-id="437bd-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="437bd-128">The resource group name.</span></span>

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

### <span data-ttu-id="437bd-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="437bd-129">-ResourceId</span></span>
<span data-ttu-id="437bd-130">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="437bd-130">The resource id.</span></span>

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

### <span data-ttu-id="437bd-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="437bd-131">-Confirm</span></span>
<span data-ttu-id="437bd-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="437bd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="437bd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="437bd-133">-WhatIf</span></span>
<span data-ttu-id="437bd-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="437bd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="437bd-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="437bd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="437bd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="437bd-136">CommonParameters</span></span>
<span data-ttu-id="437bd-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="437bd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="437bd-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="437bd-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="437bd-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="437bd-139">INPUTS</span></span>

### <span data-ttu-id="437bd-140">System. String</span><span class="sxs-lookup"><span data-stu-id="437bd-140">System.String</span></span>

### <span data-ttu-id="437bd-141">Microsoft. Azure. Commands. Network. Models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="437bd-141">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="437bd-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="437bd-142">OUTPUTS</span></span>

### <span data-ttu-id="437bd-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="437bd-143">System.Boolean</span></span>

## <span data-ttu-id="437bd-144">Note</span><span class="sxs-lookup"><span data-stu-id="437bd-144">NOTES</span></span>

## <span data-ttu-id="437bd-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="437bd-145">RELATED LINKS</span></span>

[<span data-ttu-id="437bd-146">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="437bd-146">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="437bd-147">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="437bd-147">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="437bd-148">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="437bd-148">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)