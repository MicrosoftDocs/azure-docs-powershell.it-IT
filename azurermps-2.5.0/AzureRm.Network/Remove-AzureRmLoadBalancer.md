---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancer
schema: 2.0.0
ms.openlocfilehash: 96f6acdda93de63486f117c99572b4680fb025e6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865746"
---
# <span data-ttu-id="c7c73-101">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c7c73-101">Remove-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="c7c73-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c7c73-102">SYNOPSIS</span></span>
<span data-ttu-id="c7c73-103">Rimuove un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="c7c73-103">Removes a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7c73-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7c73-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7c73-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7c73-105">DESCRIPTION</span></span>
<span data-ttu-id="c7c73-106">Il cmdlet **Remove-AzureRmLoadBalancer** rimuove un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="c7c73-106">The **Remove-AzureRmLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="c7c73-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7c73-107">EXAMPLES</span></span>

### <span data-ttu-id="c7c73-108">Esempio 1: rimuovere un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="c7c73-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="c7c73-109">Questo comando Elimina un bilanciamento del carico denominato MyLoadBalancer nel gruppo di risorse denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c7c73-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="c7c73-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c7c73-110">PARAMETERS</span></span>

### <span data-ttu-id="c7c73-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7c73-111">-AsJob</span></span>
<span data-ttu-id="c7c73-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c7c73-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c7c73-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7c73-113">-DefaultProfile</span></span>
<span data-ttu-id="c7c73-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c7c73-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7c73-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c7c73-115">-Force</span></span>
<span data-ttu-id="c7c73-116">Indica che questo cmdlet rimuove il bilanciamento del carico indipendentemente dal fatto che siano state assegnate risorse.</span><span class="sxs-lookup"><span data-stu-id="c7c73-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7c73-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="c7c73-117">-Name</span></span>
<span data-ttu-id="c7c73-118">Specifica il nome del bilanciamento del carico da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="c7c73-118">Specifies the name of the load balancer to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7c73-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7c73-119">-PassThru</span></span>
<span data-ttu-id="c7c73-120">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="c7c73-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c7c73-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="c7c73-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c7c73-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7c73-122">-ResourceGroupName</span></span>
<span data-ttu-id="c7c73-123">Specifica il nome del gruppo di risorse che contiene il bilanciamento del carico da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="c7c73-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7c73-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c7c73-124">-Confirm</span></span>
<span data-ttu-id="c7c73-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7c73-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7c73-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7c73-126">-WhatIf</span></span>
<span data-ttu-id="c7c73-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c7c73-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7c73-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c7c73-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7c73-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7c73-129">CommonParameters</span></span>
<span data-ttu-id="c7c73-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7c73-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7c73-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7c73-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7c73-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c7c73-132">INPUTS</span></span>

## <span data-ttu-id="c7c73-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7c73-133">OUTPUTS</span></span>

## <span data-ttu-id="c7c73-134">Note</span><span class="sxs-lookup"><span data-stu-id="c7c73-134">NOTES</span></span>

## <span data-ttu-id="c7c73-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7c73-135">RELATED LINKS</span></span>

[<span data-ttu-id="c7c73-136">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c7c73-136">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="c7c73-137">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c7c73-137">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="c7c73-138">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c7c73-138">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


