---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzLoadBalancer.md
ms.openlocfilehash: 1602c9e5fb0244239eea4eec53661c3392ac0354
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860317"
---
# <span data-ttu-id="f7470-101">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f7470-101">Remove-AzLoadBalancer</span></span>

## <span data-ttu-id="f7470-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f7470-102">SYNOPSIS</span></span>
<span data-ttu-id="f7470-103">Rimuove un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="f7470-103">Removes a load balancer.</span></span>

## <span data-ttu-id="f7470-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f7470-104">SYNTAX</span></span>

```
Remove-AzLoadBalancer -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7470-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7470-105">DESCRIPTION</span></span>
<span data-ttu-id="f7470-106">Il cmdlet **Remove-AzLoadBalancer** rimuove un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="f7470-106">The **Remove-AzLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="f7470-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f7470-107">EXAMPLES</span></span>

### <span data-ttu-id="f7470-108">Esempio 1: rimuovere un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="f7470-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="f7470-109">Questo comando Elimina un bilanciamento del carico denominato MyLoadBalancer nel gruppo di risorse denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="f7470-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="f7470-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f7470-110">PARAMETERS</span></span>

### <span data-ttu-id="f7470-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7470-111">-AsJob</span></span>
<span data-ttu-id="f7470-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f7470-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f7470-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7470-113">-DefaultProfile</span></span>
<span data-ttu-id="f7470-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f7470-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7470-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f7470-115">-Force</span></span>
<span data-ttu-id="f7470-116">Indica che questo cmdlet rimuove il bilanciamento del carico indipendentemente dal fatto che siano state assegnate risorse.</span><span class="sxs-lookup"><span data-stu-id="f7470-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="f7470-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="f7470-117">-Name</span></span>
<span data-ttu-id="f7470-118">Specifica il nome del bilanciamento del carico da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="f7470-118">Specifies the name of the load balancer to remove.</span></span>

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

### <span data-ttu-id="f7470-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7470-119">-PassThru</span></span>
<span data-ttu-id="f7470-120">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="f7470-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f7470-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="f7470-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f7470-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7470-122">-ResourceGroupName</span></span>
<span data-ttu-id="f7470-123">Specifica il nome del gruppo di risorse che contiene il bilanciamento del carico da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="f7470-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

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

### <span data-ttu-id="f7470-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f7470-124">-Confirm</span></span>
<span data-ttu-id="f7470-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7470-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7470-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7470-126">-WhatIf</span></span>
<span data-ttu-id="f7470-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7470-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7470-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7470-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7470-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7470-129">CommonParameters</span></span>
<span data-ttu-id="f7470-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7470-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7470-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7470-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7470-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f7470-132">INPUTS</span></span>

## <span data-ttu-id="f7470-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f7470-133">OUTPUTS</span></span>

## <span data-ttu-id="f7470-134">Note</span><span class="sxs-lookup"><span data-stu-id="f7470-134">NOTES</span></span>

## <span data-ttu-id="f7470-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f7470-135">RELATED LINKS</span></span>

[<span data-ttu-id="f7470-136">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f7470-136">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="f7470-137">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f7470-137">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="f7470-138">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="f7470-138">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


