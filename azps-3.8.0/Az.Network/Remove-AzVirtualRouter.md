---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
ms.openlocfilehash: 6d879357a71e18d9f1b6beb25044bd5d4394a497
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021927"
---
# <span data-ttu-id="1d27a-101">Remove-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="1d27a-101">Remove-AzVirtualRouter</span></span>

## <span data-ttu-id="1d27a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1d27a-102">SYNOPSIS</span></span>
<span data-ttu-id="1d27a-103">Elimina un VirtualRouter di Azure.</span><span class="sxs-lookup"><span data-stu-id="1d27a-103">Deletes an Azure VirtualRouter.</span></span>

## <span data-ttu-id="1d27a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1d27a-104">SYNTAX</span></span>

### <span data-ttu-id="1d27a-105">VirtualRouterNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1d27a-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d27a-106">VirtualRouterInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d27a-106">VirtualRouterInputObjectParameterSet</span></span>
```
Remove-AzVirtualRouter -InputObject <PSVirtualRouter> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d27a-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d27a-107">VirtualRouterResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouter -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d27a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1d27a-108">DESCRIPTION</span></span>
<span data-ttu-id="1d27a-109">Il cmdlet **Remove-AzVirtualRouter** Elimina un VirtualRouter di Azure</span><span class="sxs-lookup"><span data-stu-id="1d27a-109">The **Remove-AzVirtualRouter** cmdlet deletes an Azure VirtualRouter</span></span>

## <span data-ttu-id="1d27a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1d27a-110">EXAMPLES</span></span>

### <span data-ttu-id="1d27a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1d27a-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter 
```

### <span data-ttu-id="1d27a-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1d27a-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Remove-AzVirtualRouter -ResourceId $virtualRouterId
```

### <span data-ttu-id="1d27a-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="1d27a-113">Example 3</span></span>
```powershell
$virtualRouter = Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
Remove-AzVirtualRouter -InputObject $virtualRouter
```

## <span data-ttu-id="1d27a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1d27a-114">PARAMETERS</span></span>

### <span data-ttu-id="1d27a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d27a-115">-AsJob</span></span>
<span data-ttu-id="1d27a-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1d27a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1d27a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d27a-117">-DefaultProfile</span></span>
<span data-ttu-id="1d27a-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1d27a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d27a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="1d27a-119">-Force</span></span>
<span data-ttu-id="1d27a-120">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="1d27a-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="1d27a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d27a-121">-InputObject</span></span>
<span data-ttu-id="1d27a-122">L'oggetto di input del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="1d27a-122">The virtual router input object.</span></span>

```yaml
Type: PSVirtualRouter
Parameter Sets: VirtualRouterInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d27a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d27a-123">-PassThru</span></span>
<span data-ttu-id="1d27a-124">Restituisce un oggetto che rappresenta l'elemento in cui viene eseguita l'operazione.</span><span class="sxs-lookup"><span data-stu-id="1d27a-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="1d27a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d27a-125">-ResourceGroupName</span></span>
<span data-ttu-id="1d27a-126">Il nome del gruppo di risorse del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="1d27a-126">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d27a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d27a-127">-ResourceId</span></span>
<span data-ttu-id="1d27a-128">ID risorsa del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="1d27a-128">The virtual router resource Id.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d27a-129">-Routername</span><span class="sxs-lookup"><span data-stu-id="1d27a-129">-RouterName</span></span>
<span data-ttu-id="1d27a-130">Nome del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="1d27a-130">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d27a-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1d27a-131">-Confirm</span></span>
<span data-ttu-id="1d27a-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d27a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d27a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d27a-133">-WhatIf</span></span>
<span data-ttu-id="1d27a-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d27a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d27a-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d27a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d27a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d27a-136">CommonParameters</span></span>
<span data-ttu-id="1d27a-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d27a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d27a-138">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d27a-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d27a-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1d27a-139">INPUTS</span></span>

### <span data-ttu-id="1d27a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1d27a-140">System.String</span></span>

### <span data-ttu-id="1d27a-141">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="1d27a-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="1d27a-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1d27a-142">OUTPUTS</span></span>

### <span data-ttu-id="1d27a-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1d27a-143">System.Boolean</span></span>

## <span data-ttu-id="1d27a-144">Note</span><span class="sxs-lookup"><span data-stu-id="1d27a-144">NOTES</span></span>

## <span data-ttu-id="1d27a-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1d27a-145">RELATED LINKS</span></span>
