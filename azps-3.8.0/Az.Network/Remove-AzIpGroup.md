---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
ms.openlocfilehash: 35cf06e23a533970b14b439be5d55a64476330be
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022001"
---
# <span data-ttu-id="7165a-101">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7165a-101">Remove-AzIpGroup</span></span>

## <span data-ttu-id="7165a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7165a-102">SYNOPSIS</span></span>
<span data-ttu-id="7165a-103">Elimina un IpGroup di Azure.</span><span class="sxs-lookup"><span data-stu-id="7165a-103">Deletes an Azure IpGroup.</span></span>

## <span data-ttu-id="7165a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7165a-104">SYNTAX</span></span>

### <span data-ttu-id="7165a-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7165a-105">IpGroupNameParameterSet</span></span>
```
Remove-AzIpGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7165a-106">IpGroupInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7165a-106">IpGroupInputObjectParameterSet</span></span>
```
Remove-AzIpGroup -IpGroup <PSIpGroup> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7165a-107">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7165a-107">IpGroupResourceIdParameterSet</span></span>
```
Remove-AzIpGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7165a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7165a-108">DESCRIPTION</span></span>
<span data-ttu-id="7165a-109">Il cmdlet **Remove-AzIpGroup** Elimina un IpGroup di Azure</span><span class="sxs-lookup"><span data-stu-id="7165a-109">The **Remove-AzIpGroup** cmdlet deletes an Azure IpGroup</span></span>

## <span data-ttu-id="7165a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7165a-110">EXAMPLES</span></span>

### <span data-ttu-id="7165a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7165a-111">Example 1</span></span>
```powershell
Remove-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="7165a-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7165a-112">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Remove-AzIpGroup -ResourceId $ipGroupId
```

### <span data-ttu-id="7165a-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="7165a-113">Example 3</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
Remove-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="7165a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7165a-114">PARAMETERS</span></span>

### <span data-ttu-id="7165a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7165a-115">-AsJob</span></span>
<span data-ttu-id="7165a-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7165a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7165a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7165a-117">-DefaultProfile</span></span>
<span data-ttu-id="7165a-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7165a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7165a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="7165a-119">-Force</span></span>
<span data-ttu-id="7165a-120">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="7165a-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7165a-121">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="7165a-121">-IpGroup</span></span>
<span data-ttu-id="7165a-122">L'oggetto di input ipGroup.</span><span class="sxs-lookup"><span data-stu-id="7165a-122">The ipGroup input object.</span></span>

```yaml
Type: PSIpGroup
Parameter Sets: IpGroupInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7165a-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="7165a-123">-Name</span></span>
<span data-ttu-id="7165a-124">Il nome del ipgroup.</span><span class="sxs-lookup"><span data-stu-id="7165a-124">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7165a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7165a-125">-PassThru</span></span>
<span data-ttu-id="7165a-126">Restituisce un oggetto che rappresenta l'elemento in cui viene eseguita l'operazione.</span><span class="sxs-lookup"><span data-stu-id="7165a-126">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="7165a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7165a-127">-ResourceGroupName</span></span>
<span data-ttu-id="7165a-128">Nome del gruppo di risorse di ipgroup.</span><span class="sxs-lookup"><span data-stu-id="7165a-128">The resource group name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7165a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7165a-129">-ResourceId</span></span>
<span data-ttu-id="7165a-130">ID risorsa ipgroup.</span><span class="sxs-lookup"><span data-stu-id="7165a-130">The ipgroup resource Id.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7165a-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7165a-131">-Confirm</span></span>
<span data-ttu-id="7165a-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7165a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7165a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7165a-133">-WhatIf</span></span>
<span data-ttu-id="7165a-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7165a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7165a-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7165a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7165a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7165a-136">CommonParameters</span></span>
<span data-ttu-id="7165a-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7165a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7165a-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7165a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7165a-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7165a-139">INPUTS</span></span>

### <span data-ttu-id="7165a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7165a-140">System.String</span></span>

### <span data-ttu-id="7165a-141">Microsoft. Azure. Commands. Network. Models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="7165a-141">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="7165a-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7165a-142">OUTPUTS</span></span>

### <span data-ttu-id="7165a-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7165a-143">System.Boolean</span></span>

## <span data-ttu-id="7165a-144">Note</span><span class="sxs-lookup"><span data-stu-id="7165a-144">NOTES</span></span>

## <span data-ttu-id="7165a-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7165a-145">RELATED LINKS</span></span>
