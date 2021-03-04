---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
ms.openlocfilehash: eac0d67e2c9ffc77d9387eeb599ad624ac01fbbe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006285"
---
# <span data-ttu-id="8b946-101">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8b946-101">Get-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="8b946-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b946-102">SYNOPSIS</span></span>
<span data-ttu-id="8b946-103">Ottiene i criteri dell'endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="8b946-103">Gets a service endpoint policy.</span></span>

## <span data-ttu-id="8b946-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8b946-104">SYNTAX</span></span>

### <span data-ttu-id="8b946-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8b946-105">ListParameterSet (Default)</span></span>
```
Get-AzServiceEndpointPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b946-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b946-106">GetByResourceIdParameterSet</span></span>
```
Get-AzServiceEndpointPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b946-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8b946-107">DESCRIPTION</span></span>
<span data-ttu-id="8b946-108">Il cmdlet **Get-AzServiceEndpointPolicy** ottiene un criterio dell'endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="8b946-108">The **Get-AzServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="8b946-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8b946-109">EXAMPLES</span></span>

### <span data-ttu-id="8b946-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8b946-110">Example 1</span></span>
```
$policy = Get-AzServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8b946-111">Questo comando recupera il criterio dell'endpoint del servizio denominato ServiceEndpointPolicy1 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $policy servizio.</span><span class="sxs-lookup"><span data-stu-id="8b946-111">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="8b946-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8b946-112">Example 2</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8b946-113">Questo comando ottiene un elenco di tutti i criteri degli endpoint del servizio nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $policyList servizio.</span><span class="sxs-lookup"><span data-stu-id="8b946-113">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

### <span data-ttu-id="8b946-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="8b946-114">Example 3</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ServiceEndpointPolicy*"
```

<span data-ttu-id="8b946-115">Questo comando ottiene un elenco di tutti i criteri dell'endpoint del servizio che iniziano con "ServiceEndpointPolicy".</span><span class="sxs-lookup"><span data-stu-id="8b946-115">This command gets a list of all the service endpoint policies that start with "ServiceEndpointPolicy".</span></span>

## <span data-ttu-id="8b946-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b946-116">PARAMETERS</span></span>

### <span data-ttu-id="8b946-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b946-117">-DefaultProfile</span></span>
<span data-ttu-id="8b946-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8b946-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b946-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8b946-119">-Name</span></span>
<span data-ttu-id="8b946-120">Nome dei criteri dell'endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="8b946-120">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="8b946-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b946-121">-ResourceGroupName</span></span>
<span data-ttu-id="8b946-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8b946-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="8b946-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b946-123">-ResourceId</span></span>
<span data-ttu-id="8b946-124">ID dei criteri dell'endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="8b946-124">The ID of the service endpoint policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b946-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b946-125">-Confirm</span></span>
<span data-ttu-id="8b946-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b946-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b946-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b946-127">-WhatIf</span></span>
<span data-ttu-id="8b946-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8b946-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8b946-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8b946-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b946-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b946-130">CommonParameters</span></span>
<span data-ttu-id="8b946-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b946-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b946-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8b946-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b946-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="8b946-133">INPUTS</span></span>

### <span data-ttu-id="8b946-134">System.String</span><span class="sxs-lookup"><span data-stu-id="8b946-134">System.String</span></span>

## <span data-ttu-id="8b946-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8b946-135">OUTPUTS</span></span>

### <span data-ttu-id="8b946-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8b946-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="8b946-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="8b946-137">NOTES</span></span>

## <span data-ttu-id="8b946-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8b946-138">RELATED LINKS</span></span>

[<span data-ttu-id="8b946-139">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8b946-139">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="8b946-140">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8b946-140">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="8b946-141">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="8b946-141">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
