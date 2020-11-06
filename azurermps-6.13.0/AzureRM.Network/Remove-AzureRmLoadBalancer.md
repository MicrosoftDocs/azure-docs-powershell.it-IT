---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
ms.openlocfilehash: d725735caf7806233688e6f0bcdddb4edb0f62b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513631"
---
# <span data-ttu-id="e7a64-101">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e7a64-101">Remove-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="e7a64-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e7a64-102">SYNOPSIS</span></span>
<span data-ttu-id="e7a64-103">Rimuove un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="e7a64-103">Removes a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7a64-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e7a64-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancer -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7a64-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7a64-105">DESCRIPTION</span></span>
<span data-ttu-id="e7a64-106">Il cmdlet **Remove-AzureRmLoadBalancer** rimuove un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="e7a64-106">The **Remove-AzureRmLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="e7a64-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e7a64-107">EXAMPLES</span></span>

### <span data-ttu-id="e7a64-108">Esempio 1: rimuovere un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="e7a64-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="e7a64-109">Questo comando Elimina un bilanciamento del carico denominato MyLoadBalancer nel gruppo di risorse denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e7a64-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="e7a64-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e7a64-110">PARAMETERS</span></span>

### <span data-ttu-id="e7a64-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e7a64-111">-AsJob</span></span>
<span data-ttu-id="e7a64-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e7a64-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e7a64-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7a64-113">-DefaultProfile</span></span>
<span data-ttu-id="e7a64-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e7a64-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7a64-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e7a64-115">-Force</span></span>
<span data-ttu-id="e7a64-116">Indica che questo cmdlet rimuove il bilanciamento del carico indipendentemente dal fatto che siano state assegnate risorse.</span><span class="sxs-lookup"><span data-stu-id="e7a64-116">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="e7a64-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="e7a64-117">-Name</span></span>
<span data-ttu-id="e7a64-118">Specifica il nome del bilanciamento del carico da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="e7a64-118">Specifies the name of the load balancer to remove.</span></span>

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

### <span data-ttu-id="e7a64-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7a64-119">-PassThru</span></span>
<span data-ttu-id="e7a64-120">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="e7a64-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e7a64-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="e7a64-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e7a64-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7a64-122">-ResourceGroupName</span></span>
<span data-ttu-id="e7a64-123">Specifica il nome del gruppo di risorse che contiene il bilanciamento del carico da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="e7a64-123">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

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

### <span data-ttu-id="e7a64-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e7a64-124">-Confirm</span></span>
<span data-ttu-id="e7a64-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7a64-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7a64-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7a64-126">-WhatIf</span></span>
<span data-ttu-id="e7a64-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e7a64-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7a64-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e7a64-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7a64-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7a64-129">CommonParameters</span></span>
<span data-ttu-id="e7a64-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7a64-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7a64-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7a64-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7a64-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e7a64-132">INPUTS</span></span>

### <span data-ttu-id="e7a64-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e7a64-133">System.String</span></span>

### <span data-ttu-id="e7a64-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e7a64-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e7a64-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e7a64-135">OUTPUTS</span></span>

### <span data-ttu-id="e7a64-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e7a64-136">System.Boolean</span></span>

## <span data-ttu-id="e7a64-137">Note</span><span class="sxs-lookup"><span data-stu-id="e7a64-137">NOTES</span></span>

## <span data-ttu-id="e7a64-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e7a64-138">RELATED LINKS</span></span>

[<span data-ttu-id="e7a64-139">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e7a64-139">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="e7a64-140">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e7a64-140">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="e7a64-141">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e7a64-141">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


