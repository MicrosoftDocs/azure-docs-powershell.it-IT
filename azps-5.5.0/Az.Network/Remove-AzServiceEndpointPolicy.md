---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
ms.openlocfilehash: 207a07186cd7284059e0824da1f86afbc22873f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186927"
---
# <span data-ttu-id="9257e-101">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="9257e-101">Remove-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="9257e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9257e-102">SYNOPSIS</span></span>
<span data-ttu-id="9257e-103">Rimuove i criteri dell'endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="9257e-103">Removes a service endpoint policy.</span></span>

## <span data-ttu-id="9257e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9257e-104">SYNTAX</span></span>

### <span data-ttu-id="9257e-105">RemoveByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9257e-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9257e-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9257e-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9257e-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9257e-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject <PSServiceEndpointPolicy> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9257e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9257e-108">DESCRIPTION</span></span>
<span data-ttu-id="9257e-109">Il cmdlet **Remove-AzServiceEndpointPolicy** rimuove un criterio dell'endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="9257e-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="9257e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9257e-110">EXAMPLES</span></span>

### <span data-ttu-id="9257e-111">Esempio 1: Rimuove un criterio dell'endpoint del servizio usando il nome</span><span class="sxs-lookup"><span data-stu-id="9257e-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="9257e-112">Questo comando rimuove un criterio endpoint di servizio con nome Criterio1 che appartiene al gruppo di risorse con nome "resourcegroup1"</span><span class="sxs-lookup"><span data-stu-id="9257e-112">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="9257e-113">Esempio 2: Rimuovere un criterio endpoint di servizio usando un oggetto di input</span><span class="sxs-lookup"><span data-stu-id="9257e-113">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="9257e-114">Questo comando rimuove un oggetto criterio endpoint di servizio Policy1 che appartiene al gruppo di risorse con nome "resourcegroup1"</span><span class="sxs-lookup"><span data-stu-id="9257e-114">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="9257e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9257e-115">PARAMETERS</span></span>

### <span data-ttu-id="9257e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9257e-116">-DefaultProfile</span></span>
<span data-ttu-id="9257e-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9257e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9257e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="9257e-118">-Force</span></span>
<span data-ttu-id="9257e-119">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="9257e-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="9257e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9257e-120">-InputObject</span></span>
<span data-ttu-id="9257e-121">Oggetto criterio dell'endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="9257e-121">The service endpoint policy object.</span></span>

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

### <span data-ttu-id="9257e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9257e-122">-Name</span></span>
<span data-ttu-id="9257e-123">Nome dei criteri dell'endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="9257e-123">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="9257e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9257e-124">-PassThru</span></span>
<span data-ttu-id="9257e-125">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="9257e-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="9257e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9257e-126">-ResourceGroupName</span></span>
<span data-ttu-id="9257e-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9257e-127">The resource group name.</span></span>

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

### <span data-ttu-id="9257e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9257e-128">-ResourceId</span></span>
<span data-ttu-id="9257e-129">ID dei criteri dell'endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="9257e-129">The ID of service endpoint policy.</span></span>

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

### <span data-ttu-id="9257e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9257e-130">-Confirm</span></span>
<span data-ttu-id="9257e-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9257e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9257e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9257e-132">-WhatIf</span></span>
<span data-ttu-id="9257e-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9257e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9257e-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9257e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9257e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9257e-135">CommonParameters</span></span>
<span data-ttu-id="9257e-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9257e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9257e-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9257e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9257e-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="9257e-138">INPUTS</span></span>

### <span data-ttu-id="9257e-139">System.String</span><span class="sxs-lookup"><span data-stu-id="9257e-139">System.String</span></span>

### <span data-ttu-id="9257e-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="9257e-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="9257e-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9257e-141">OUTPUTS</span></span>

### <span data-ttu-id="9257e-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9257e-142">System.Boolean</span></span>

## <span data-ttu-id="9257e-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="9257e-143">NOTES</span></span>

## <span data-ttu-id="9257e-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9257e-144">RELATED LINKS</span></span>

[<span data-ttu-id="9257e-145">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="9257e-145">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="9257e-146">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="9257e-146">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="9257e-147">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="9257e-147">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
