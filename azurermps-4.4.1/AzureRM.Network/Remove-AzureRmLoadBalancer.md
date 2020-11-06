---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 31B0FBEF-366A-41AF-9182-2EB087019F36
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancer.md
ms.openlocfilehash: 6757c9c0b9eeb0b3408a07713c62812d361d814a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521574"
---
# <span data-ttu-id="2b6ee-101">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2b6ee-101">Remove-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="2b6ee-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2b6ee-102">SYNOPSIS</span></span>
<span data-ttu-id="2b6ee-103">Rimuove un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="2b6ee-103">Removes a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b6ee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b6ee-104">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b6ee-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b6ee-105">DESCRIPTION</span></span>
<span data-ttu-id="2b6ee-106">Il cmdlet **Remove-AzureRmLoadBalancer** rimuove un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="2b6ee-106">The **Remove-AzureRmLoadBalancer** cmdlet removes an Azure load balancer.</span></span>

## <span data-ttu-id="2b6ee-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b6ee-107">EXAMPLES</span></span>

### <span data-ttu-id="2b6ee-108">Esempio 1: rimuovere un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="2b6ee-108">Example 1: Remove a load balancer</span></span>
```
PS C:\>Remove-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="2b6ee-109">Questo comando Elimina un bilanciamento del carico denominato MyLoadBalancer nel gruppo di risorse denominato MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2b6ee-109">This command deletes a load balancer named MyLoadBalancer in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="2b6ee-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2b6ee-110">PARAMETERS</span></span>

### <span data-ttu-id="2b6ee-111">-Force</span><span class="sxs-lookup"><span data-stu-id="2b6ee-111">-Force</span></span>
<span data-ttu-id="2b6ee-112">Indica che questo cmdlet rimuove il bilanciamento del carico indipendentemente dal fatto che siano state assegnate risorse.</span><span class="sxs-lookup"><span data-stu-id="2b6ee-112">Indicates that this cmdlet removes the load balancer regardless of whether resources are assigned to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b6ee-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="2b6ee-113">-Name</span></span>
<span data-ttu-id="2b6ee-114">Specifica il nome del bilanciamento del carico da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="2b6ee-114">Specifies the name of the load balancer to remove.</span></span>

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

### <span data-ttu-id="2b6ee-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b6ee-115">-PassThru</span></span>
<span data-ttu-id="2b6ee-116">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="2b6ee-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2b6ee-117">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="2b6ee-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2b6ee-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b6ee-118">-ResourceGroupName</span></span>
<span data-ttu-id="2b6ee-119">Specifica il nome del gruppo di risorse che contiene il bilanciamento del carico da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="2b6ee-119">Specifies the name of the resource group that contains the load balancer to remove.</span></span>

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

### <span data-ttu-id="2b6ee-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2b6ee-120">-Confirm</span></span>
<span data-ttu-id="2b6ee-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b6ee-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b6ee-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b6ee-122">-WhatIf</span></span>
<span data-ttu-id="2b6ee-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b6ee-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b6ee-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b6ee-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b6ee-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b6ee-125">-DefaultProfile</span></span>
<span data-ttu-id="2b6ee-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2b6ee-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b6ee-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b6ee-127">CommonParameters</span></span>
<span data-ttu-id="2b6ee-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b6ee-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b6ee-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b6ee-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b6ee-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2b6ee-130">INPUTS</span></span>

## <span data-ttu-id="2b6ee-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b6ee-131">OUTPUTS</span></span>

## <span data-ttu-id="2b6ee-132">Note</span><span class="sxs-lookup"><span data-stu-id="2b6ee-132">NOTES</span></span>

## <span data-ttu-id="2b6ee-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b6ee-133">RELATED LINKS</span></span>

[<span data-ttu-id="2b6ee-134">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2b6ee-134">Get-AzureRmLoadBalancer</span></span>](./Get-AzureRmLoadBalancer.md)

[<span data-ttu-id="2b6ee-135">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2b6ee-135">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="2b6ee-136">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2b6ee-136">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


