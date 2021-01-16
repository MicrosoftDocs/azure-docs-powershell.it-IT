---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
ms.openlocfilehash: 7a81ce555ed99de1504dc0625c0c83cdab6ab881
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363467"
---
# <span data-ttu-id="1eaa3-101">Remove-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="1eaa3-101">Remove-AzIpAllocation</span></span>

## <span data-ttu-id="1eaa3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1eaa3-102">SYNOPSIS</span></span>
<span data-ttu-id="1eaa3-103">Elimina un IpAllocation di Azure.</span><span class="sxs-lookup"><span data-stu-id="1eaa3-103">Deletes an Azure IpAllocation.</span></span>

## <span data-ttu-id="1eaa3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1eaa3-104">SYNTAX</span></span>

### <span data-ttu-id="1eaa3-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1eaa3-105">DeleteByNameParameterSet</span></span>
```
Remove-AzIpAllocation [-Name] <String> [-ResourceGroupName] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1eaa3-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1eaa3-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzIpAllocation [-InputObject] <PSTopLevelResource> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1eaa3-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1eaa3-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzIpAllocation [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1eaa3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1eaa3-108">DESCRIPTION</span></span>
<span data-ttu-id="1eaa3-109">Il cmdlet **Remove-AzIpAllocation** Elimina un IpAllocation di Azure</span><span class="sxs-lookup"><span data-stu-id="1eaa3-109">The **Remove-AzIpAllocation** cmdlet deletes an Azure IpAllocation</span></span>

## <span data-ttu-id="1eaa3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1eaa3-110">EXAMPLES</span></span>

### <span data-ttu-id="1eaa3-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1eaa3-111">Example 1</span></span>
```powershell
Remove-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="1eaa3-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1eaa3-112">PARAMETERS</span></span>

### <span data-ttu-id="1eaa3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1eaa3-113">-AsJob</span></span>
<span data-ttu-id="1eaa3-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1eaa3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1eaa3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eaa3-115">-DefaultProfile</span></span>
<span data-ttu-id="1eaa3-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1eaa3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1eaa3-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1eaa3-117">-Force</span></span>
<span data-ttu-id="1eaa3-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="1eaa3-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1eaa3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1eaa3-119">-InputObject</span></span>
<span data-ttu-id="1eaa3-120">{{Fill InputObject Description}}</span><span class="sxs-lookup"><span data-stu-id="1eaa3-120">{{ Fill InputObject Description }}</span></span>

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

### <span data-ttu-id="1eaa3-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="1eaa3-121">-Name</span></span>
<span data-ttu-id="1eaa3-122">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="1eaa3-122">The resource name.</span></span>

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

### <span data-ttu-id="1eaa3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1eaa3-123">-PassThru</span></span>
<span data-ttu-id="1eaa3-124">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="1eaa3-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1eaa3-125">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="1eaa3-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1eaa3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1eaa3-126">-ResourceGroupName</span></span>
<span data-ttu-id="1eaa3-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1eaa3-127">The resource group name.</span></span>

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

### <span data-ttu-id="1eaa3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1eaa3-128">-ResourceId</span></span>
<span data-ttu-id="1eaa3-129">ID risorsa IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="1eaa3-129">IpAllocation resource id.</span></span>

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

### <span data-ttu-id="1eaa3-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1eaa3-130">-Confirm</span></span>
<span data-ttu-id="1eaa3-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1eaa3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1eaa3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1eaa3-132">-WhatIf</span></span>
<span data-ttu-id="1eaa3-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1eaa3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1eaa3-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1eaa3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1eaa3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eaa3-135">CommonParameters</span></span>
<span data-ttu-id="1eaa3-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1eaa3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eaa3-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1eaa3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eaa3-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1eaa3-138">INPUTS</span></span>

### <span data-ttu-id="1eaa3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1eaa3-139">System.String</span></span>

## <span data-ttu-id="1eaa3-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1eaa3-140">OUTPUTS</span></span>

### <span data-ttu-id="1eaa3-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1eaa3-141">System.Boolean</span></span>

## <span data-ttu-id="1eaa3-142">Note</span><span class="sxs-lookup"><span data-stu-id="1eaa3-142">NOTES</span></span>

## <span data-ttu-id="1eaa3-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1eaa3-143">RELATED LINKS</span></span>
