---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicy.md
ms.openlocfilehash: 95da37a36c8a97bf507ec8d191728b34a88a25a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006142"
---
# <span data-ttu-id="db6fa-101">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="db6fa-101">Remove-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="db6fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db6fa-102">SYNOPSIS</span></span>
<span data-ttu-id="db6fa-103">Rimuove i criteri dell'endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="db6fa-103">Removes a service endpoint policy.</span></span>

## <span data-ttu-id="db6fa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db6fa-104">SYNTAX</span></span>

### <span data-ttu-id="db6fa-105">RemoveByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="db6fa-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db6fa-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db6fa-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db6fa-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="db6fa-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject <PSServiceEndpointPolicy> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db6fa-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="db6fa-108">DESCRIPTION</span></span>
<span data-ttu-id="db6fa-109">Il cmdlet **Remove-AzServiceEndpointPolicy** rimuove un criterio dell'endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="db6fa-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="db6fa-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db6fa-110">EXAMPLES</span></span>

### <span data-ttu-id="db6fa-111">Esempio 1: Rimuove un criterio dell'endpoint del servizio usando il nome</span><span class="sxs-lookup"><span data-stu-id="db6fa-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicy -Name "Policy1" -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="db6fa-112">Questo comando rimuove un criterio endpoint di servizio con nome Criterio1 che appartiene al gruppo di risorse con nome "resourcegroup1"</span><span class="sxs-lookup"><span data-stu-id="db6fa-112">This command removes a service endpoint policy with name Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

### <span data-ttu-id="db6fa-113">Esempio 2: Rimuovere un criterio endpoint di servizio usando un oggetto di input</span><span class="sxs-lookup"><span data-stu-id="db6fa-113">Example 2: Remove a service endpoint policy using input object</span></span>
```
Remove-AzServiceEndpointPolicy -InputObject $Policy1 -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="db6fa-114">Questo comando rimuove un oggetto criterio endpoint di servizio Policy1 che appartiene al gruppo di risorse con nome "resourcegroup1"</span><span class="sxs-lookup"><span data-stu-id="db6fa-114">This command removes a service endpoint policy object Policy1 which belongs to resourcegroup with name "resourcegroup1"</span></span>

## <span data-ttu-id="db6fa-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db6fa-115">PARAMETERS</span></span>

### <span data-ttu-id="db6fa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db6fa-116">-DefaultProfile</span></span>
<span data-ttu-id="db6fa-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db6fa-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db6fa-118">-Force</span><span class="sxs-lookup"><span data-stu-id="db6fa-118">-Force</span></span>
<span data-ttu-id="db6fa-119">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="db6fa-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="db6fa-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db6fa-120">-InputObject</span></span>
<span data-ttu-id="db6fa-121">Oggetto criterio dell'endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="db6fa-121">The service endpoint policy object.</span></span>

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

### <span data-ttu-id="db6fa-122">-Name</span><span class="sxs-lookup"><span data-stu-id="db6fa-122">-Name</span></span>
<span data-ttu-id="db6fa-123">Nome dei criteri dell'endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="db6fa-123">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="db6fa-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db6fa-124">-PassThru</span></span>
<span data-ttu-id="db6fa-125">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="db6fa-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="db6fa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db6fa-126">-ResourceGroupName</span></span>
<span data-ttu-id="db6fa-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="db6fa-127">The resource group name.</span></span>

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

### <span data-ttu-id="db6fa-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db6fa-128">-ResourceId</span></span>
<span data-ttu-id="db6fa-129">ID dei criteri dell'endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="db6fa-129">The ID of service endpoint policy.</span></span>

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

### <span data-ttu-id="db6fa-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db6fa-130">-Confirm</span></span>
<span data-ttu-id="db6fa-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db6fa-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db6fa-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db6fa-132">-WhatIf</span></span>
<span data-ttu-id="db6fa-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db6fa-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db6fa-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db6fa-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db6fa-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db6fa-135">CommonParameters</span></span>
<span data-ttu-id="db6fa-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db6fa-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db6fa-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db6fa-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db6fa-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="db6fa-138">INPUTS</span></span>

### <span data-ttu-id="db6fa-139">System.String</span><span class="sxs-lookup"><span data-stu-id="db6fa-139">System.String</span></span>

### <span data-ttu-id="db6fa-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="db6fa-140">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="db6fa-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db6fa-141">OUTPUTS</span></span>

### <span data-ttu-id="db6fa-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="db6fa-142">System.Boolean</span></span>

## <span data-ttu-id="db6fa-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="db6fa-143">NOTES</span></span>

## <span data-ttu-id="db6fa-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db6fa-144">RELATED LINKS</span></span>

[<span data-ttu-id="db6fa-145">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="db6fa-145">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="db6fa-146">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="db6fa-146">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="db6fa-147">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="db6fa-147">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
