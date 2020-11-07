---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
ms.openlocfilehash: 645eed141375dce0c27d389b721f7487c8a7c71f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678077"
---
# <span data-ttu-id="87d65-101">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="87d65-101">Remove-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="87d65-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="87d65-102">SYNOPSIS</span></span>
<span data-ttu-id="87d65-103">Rimuove un criterio endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="87d65-103">Removes a service endpoint policy.</span></span>

## <span data-ttu-id="87d65-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="87d65-104">SYNTAX</span></span>

### <span data-ttu-id="87d65-105">RemoveByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="87d65-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87d65-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="87d65-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87d65-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="87d65-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject <PSServiceEndpointPolicy> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87d65-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87d65-108">DESCRIPTION</span></span>
<span data-ttu-id="87d65-109">Il cmdlet **Remove-AzServiceEndpointPolicy** rimuove un criterio endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="87d65-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="87d65-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="87d65-110">EXAMPLES</span></span>

### <span data-ttu-id="87d65-111">Esempio 1: rimuove un criterio endpoint di servizio tramite Name</span><span class="sxs-lookup"><span data-stu-id="87d65-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="87d65-112">Questo comando rimuove un criterio endpoint del servizio con il nome Policy1 che appartiene a ResourceGroup con nome "resourcegroup1"</span><span class="sxs-lookup"><span data-stu-id="87d65-112">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="87d65-113">Esempio 2: rimuovere un criterio endpoint del servizio usando l'oggetto di input</span><span class="sxs-lookup"><span data-stu-id="87d65-113">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="87d65-114">Questo comando rimuove un oggetto Criteri endpoint servizio Policy1 che appartiene a ResourceGroup con nome "resourcegroup1"</span><span class="sxs-lookup"><span data-stu-id="87d65-114">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="87d65-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="87d65-115">PARAMETERS</span></span>

### <span data-ttu-id="87d65-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87d65-116">-DefaultProfile</span></span>
<span data-ttu-id="87d65-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="87d65-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87d65-118">-Force</span><span class="sxs-lookup"><span data-stu-id="87d65-118">-Force</span></span>
<span data-ttu-id="87d65-119">Non chiedere conferma se si vuole usare una risorsa per un sovrarito</span><span class="sxs-lookup"><span data-stu-id="87d65-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="87d65-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87d65-120">-InputObject</span></span>
<span data-ttu-id="87d65-121">Oggetto Criteri endpoint servizio.</span><span class="sxs-lookup"><span data-stu-id="87d65-121">The service endpoint policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87d65-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="87d65-122">-Name</span></span>
<span data-ttu-id="87d65-123">Nome del criterio endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="87d65-123">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87d65-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87d65-124">-PassThru</span></span>
<span data-ttu-id="87d65-125">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="87d65-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="87d65-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87d65-126">-ResourceGroupName</span></span>
<span data-ttu-id="87d65-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="87d65-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87d65-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87d65-128">-ResourceId</span></span>
<span data-ttu-id="87d65-129">ID dei criteri endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="87d65-129">The ID of service endpoint policy.</span></span>

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

### <span data-ttu-id="87d65-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="87d65-130">-Confirm</span></span>
<span data-ttu-id="87d65-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87d65-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87d65-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87d65-132">-WhatIf</span></span>
<span data-ttu-id="87d65-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="87d65-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87d65-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="87d65-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87d65-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87d65-135">CommonParameters</span></span>
<span data-ttu-id="87d65-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87d65-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87d65-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87d65-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87d65-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="87d65-138">INPUTS</span></span>

### <span data-ttu-id="87d65-139">System. String</span><span class="sxs-lookup"><span data-stu-id="87d65-139">System.String</span></span>

### <span data-ttu-id="87d65-140">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="87d65-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="87d65-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="87d65-141">OUTPUTS</span></span>

### <span data-ttu-id="87d65-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="87d65-142">System.Boolean</span></span>

## <span data-ttu-id="87d65-143">Note</span><span class="sxs-lookup"><span data-stu-id="87d65-143">NOTES</span></span>

## <span data-ttu-id="87d65-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="87d65-144">RELATED LINKS</span></span>

[<span data-ttu-id="87d65-145">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="87d65-145">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="87d65-146">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="87d65-146">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="87d65-147">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="87d65-147">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)