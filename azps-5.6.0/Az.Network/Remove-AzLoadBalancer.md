---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancer.md
ms.openlocfilehash: efe24ad1feae60ed71bd65206c52cfbf0b27df18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996294"
---
# <span data-ttu-id="85826-101">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="85826-101">Remove-AzLoadBalancer</span></span>

## <span data-ttu-id="85826-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85826-102">SYNOPSIS</span></span>
<span data-ttu-id="85826-103">Rimuove una bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="85826-103">Removes a load balancer.</span></span>

## <span data-ttu-id="85826-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85826-104">SYNTAX</span></span>

```
Remove-AzLoadBalancer -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85826-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="85826-105">DESCRIPTION</span></span>
<span data-ttu-id="85826-106">Il cmdlet **Remove-AzLoadBalancer** rimuove una bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="85826-106">The **Remove-AzLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="85826-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85826-107">EXAMPLES</span></span>

### <span data-ttu-id="85826-108">Esempio 1: Rimuovere una bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="85826-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="85826-109">Questo comando elimina una bilanciamento del carico denominata MyLoadBalancer nel gruppo di risorse denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="85826-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="85826-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85826-110">PARAMETERS</span></span>

### <span data-ttu-id="85826-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85826-111">-AsJob</span></span>
<span data-ttu-id="85826-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="85826-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="85826-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85826-113">-DefaultProfile</span></span>
<span data-ttu-id="85826-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="85826-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85826-115">-Force</span><span class="sxs-lookup"><span data-stu-id="85826-115">-Force</span></span>
<span data-ttu-id="85826-116">Indica che questo cmdlet rimuove la bilanciamento del carico indipendentemente dall'assegnazione o meno di risorse.</span><span class="sxs-lookup"><span data-stu-id="85826-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="85826-117">-Name</span><span class="sxs-lookup"><span data-stu-id="85826-117">-Name</span></span>
<span data-ttu-id="85826-118">Specifica il nome della bilanciamento del carico da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="85826-118">Specifies the name of the load balancer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85826-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85826-119">-PassThru</span></span>
<span data-ttu-id="85826-120">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="85826-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="85826-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="85826-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="85826-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85826-122">-ResourceGroupName</span></span>
<span data-ttu-id="85826-123">Specifica il nome del gruppo di risorse che contiene la bilanciamento del carico da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="85826-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85826-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85826-124">-Confirm</span></span>
<span data-ttu-id="85826-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85826-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85826-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85826-126">-WhatIf</span></span>
<span data-ttu-id="85826-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85826-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85826-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85826-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85826-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85826-129">CommonParameters</span></span>
<span data-ttu-id="85826-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85826-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85826-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85826-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85826-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="85826-132">INPUTS</span></span>

### <span data-ttu-id="85826-133">System.String</span><span class="sxs-lookup"><span data-stu-id="85826-133">System.String</span></span>

## <span data-ttu-id="85826-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85826-134">OUTPUTS</span></span>

### <span data-ttu-id="85826-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="85826-135">System.Boolean</span></span>

## <span data-ttu-id="85826-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="85826-136">NOTES</span></span>

## <span data-ttu-id="85826-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85826-137">RELATED LINKS</span></span>

[<span data-ttu-id="85826-138">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="85826-138">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="85826-139">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="85826-139">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="85826-140">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="85826-140">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


