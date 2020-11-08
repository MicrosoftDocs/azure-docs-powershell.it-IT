---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNatGateway.md
ms.openlocfilehash: 4940936a50156f8515885099a205a4fa3566a7b4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193916"
---
# <span data-ttu-id="e10af-101">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="e10af-101">Remove-AzNatGateway</span></span>

## <span data-ttu-id="e10af-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e10af-102">SYNOPSIS</span></span>
<span data-ttu-id="e10af-103">Rimuovere la risorsa gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="e10af-103">Remove Nat Gateway resource.</span></span>

## <span data-ttu-id="e10af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e10af-104">SYNTAX</span></span>

### <span data-ttu-id="e10af-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e10af-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzNatGateway -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e10af-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e10af-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNatGateway -InputObject <PSNatGateway> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e10af-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e10af-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNatGateway -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e10af-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e10af-108">DESCRIPTION</span></span>
<span data-ttu-id="e10af-109">Rimuovere la risorsa gateway NAT</span><span class="sxs-lookup"><span data-stu-id="e10af-109">Remove Nat Gateway Resource</span></span>

## <span data-ttu-id="e10af-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e10af-110">EXAMPLES</span></span>

### <span data-ttu-id="e10af-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e10af-111">Example 1</span></span>
```powershell
PS C:> $nat = Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway"
PS C:> Remove-AzNatGateway -InputObject $nat
PS C:> Remove-AzNatGateway -ResourceId "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/natgateway"
```

## <span data-ttu-id="e10af-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e10af-112">PARAMETERS</span></span>

### <span data-ttu-id="e10af-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e10af-113">-AsJob</span></span>
<span data-ttu-id="e10af-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e10af-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e10af-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e10af-115">-DefaultProfile</span></span>
<span data-ttu-id="e10af-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e10af-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e10af-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e10af-117">-Force</span></span>
<span data-ttu-id="e10af-118">Non chiedere conferma se si vuole eliminare una risorsa.</span><span class="sxs-lookup"><span data-stu-id="e10af-118">Do not ask for confirmation if you want to delete resource.</span></span>

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

### <span data-ttu-id="e10af-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e10af-119">-InputObject</span></span>
<span data-ttu-id="e10af-120">Specifica la risorsa gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="e10af-120">Specifies the Nat Gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNatGateway
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: NatGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e10af-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e10af-121">-Name</span></span>
<span data-ttu-id="e10af-122">Nome della risorsa gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="e10af-122">Name of the Nat Gateway resource.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e10af-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e10af-123">-PassThru</span></span>
<span data-ttu-id="e10af-124">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="e10af-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e10af-125">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="e10af-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e10af-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e10af-126">-ResourceGroupName</span></span>
<span data-ttu-id="e10af-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e10af-127">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e10af-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e10af-128">-ResourceId</span></span>
<span data-ttu-id="e10af-129">ID risorsa associato al gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="e10af-129">Resource Id associated with the Nat Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases: NatGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e10af-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e10af-130">-Confirm</span></span>
<span data-ttu-id="e10af-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e10af-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e10af-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e10af-132">-WhatIf</span></span>
<span data-ttu-id="e10af-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e10af-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e10af-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e10af-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e10af-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e10af-135">CommonParameters</span></span>
<span data-ttu-id="e10af-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e10af-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e10af-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e10af-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e10af-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e10af-138">INPUTS</span></span>

### <span data-ttu-id="e10af-139">Microsoft. Azure. Commands. Network. Models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="e10af-139">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

### <span data-ttu-id="e10af-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e10af-140">System.String</span></span>

## <span data-ttu-id="e10af-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e10af-141">OUTPUTS</span></span>

### <span data-ttu-id="e10af-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e10af-142">System.Boolean</span></span>

## <span data-ttu-id="e10af-143">Note</span><span class="sxs-lookup"><span data-stu-id="e10af-143">NOTES</span></span>

## <span data-ttu-id="e10af-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e10af-144">RELATED LINKS</span></span>