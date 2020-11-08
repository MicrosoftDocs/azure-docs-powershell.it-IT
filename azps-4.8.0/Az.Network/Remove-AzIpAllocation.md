---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
ms.openlocfilehash: 7a81ce555ed99de1504dc0625c0c83cdab6ab881
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032901"
---
# <span data-ttu-id="1f700-101">Remove-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="1f700-101">Remove-AzIpAllocation</span></span>

## <span data-ttu-id="1f700-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1f700-102">SYNOPSIS</span></span>
<span data-ttu-id="1f700-103">Elimina un IpAllocation di Azure.</span><span class="sxs-lookup"><span data-stu-id="1f700-103">Deletes an Azure IpAllocation.</span></span>

## <span data-ttu-id="1f700-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f700-104">SYNTAX</span></span>

### <span data-ttu-id="1f700-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f700-105">DeleteByNameParameterSet</span></span>
```
Remove-AzIpAllocation [-Name] <String> [-ResourceGroupName] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f700-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f700-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzIpAllocation [-InputObject] <PSTopLevelResource> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f700-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f700-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzIpAllocation [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f700-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f700-108">DESCRIPTION</span></span>
<span data-ttu-id="1f700-109">Il cmdlet **Remove-AzIpAllocation** Elimina un IpAllocation di Azure</span><span class="sxs-lookup"><span data-stu-id="1f700-109">The **Remove-AzIpAllocation** cmdlet deletes an Azure IpAllocation</span></span>

## <span data-ttu-id="1f700-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f700-110">EXAMPLES</span></span>

### <span data-ttu-id="1f700-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1f700-111">Example 1</span></span>
```powershell
Remove-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="1f700-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f700-112">PARAMETERS</span></span>

### <span data-ttu-id="1f700-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f700-113">-AsJob</span></span>
<span data-ttu-id="1f700-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1f700-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1f700-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f700-115">-DefaultProfile</span></span>
<span data-ttu-id="1f700-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1f700-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f700-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1f700-117">-Force</span></span>
<span data-ttu-id="1f700-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="1f700-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1f700-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f700-119">-InputObject</span></span>
<span data-ttu-id="1f700-120">{{Fill InputObject Description}}</span><span class="sxs-lookup"><span data-stu-id="1f700-120">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTopLevelResource
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f700-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f700-121">-Name</span></span>
<span data-ttu-id="1f700-122">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="1f700-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f700-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f700-123">-PassThru</span></span>
<span data-ttu-id="1f700-124">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="1f700-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1f700-125">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="1f700-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1f700-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f700-126">-ResourceGroupName</span></span>
<span data-ttu-id="1f700-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1f700-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f700-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f700-128">-ResourceId</span></span>
<span data-ttu-id="1f700-129">ID risorsa IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="1f700-129">IpAllocation resource id.</span></span>

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

### <span data-ttu-id="1f700-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1f700-130">-Confirm</span></span>
<span data-ttu-id="1f700-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f700-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f700-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f700-132">-WhatIf</span></span>
<span data-ttu-id="1f700-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f700-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f700-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f700-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f700-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f700-135">CommonParameters</span></span>
<span data-ttu-id="1f700-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f700-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f700-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f700-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f700-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1f700-138">INPUTS</span></span>

### <span data-ttu-id="1f700-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1f700-139">System.String</span></span>

## <span data-ttu-id="1f700-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f700-140">OUTPUTS</span></span>

### <span data-ttu-id="1f700-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1f700-141">System.Boolean</span></span>

## <span data-ttu-id="1f700-142">Note</span><span class="sxs-lookup"><span data-stu-id="1f700-142">NOTES</span></span>

## <span data-ttu-id="1f700-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f700-143">RELATED LINKS</span></span>
