---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
ms.openlocfilehash: a74edbec0051e3a77ab3ac10595f787dd45a2dfc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203058"
---
# <span data-ttu-id="f7f3a-101">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f7f3a-101">Get-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="f7f3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7f3a-102">SYNOPSIS</span></span>
<span data-ttu-id="f7f3a-103">Ottiene i criteri dell'endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="f7f3a-103">Gets a service endpoint policy.</span></span>

## <span data-ttu-id="f7f3a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f7f3a-104">SYNTAX</span></span>

### <span data-ttu-id="f7f3a-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f7f3a-105">ListParameterSet (Default)</span></span>
```
Get-AzServiceEndpointPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7f3a-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7f3a-106">GetByResourceIdParameterSet</span></span>
```
Get-AzServiceEndpointPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7f3a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f7f3a-107">DESCRIPTION</span></span>
<span data-ttu-id="f7f3a-108">Il cmdlet **Get-AzServiceEndpointPolicy** ottiene un criterio dell'endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="f7f3a-108">The **Get-AzServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="f7f3a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f7f3a-109">EXAMPLES</span></span>

### <span data-ttu-id="f7f3a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f7f3a-110">Example 1</span></span>
```
$policy = Get-AzServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f7f3a-111">Questo comando recupera il criterio dell'endpoint del servizio denominato ServiceEndpointPolicy1 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $policy servizio.</span><span class="sxs-lookup"><span data-stu-id="f7f3a-111">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="f7f3a-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f7f3a-112">Example 2</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f7f3a-113">Questo comando ottiene un elenco di tutti i criteri degli endpoint del servizio nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $policyList servizio.</span><span class="sxs-lookup"><span data-stu-id="f7f3a-113">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

### <span data-ttu-id="f7f3a-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="f7f3a-114">Example 3</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ServiceEndpointPolicy*"
```

<span data-ttu-id="f7f3a-115">Questo comando ottiene un elenco di tutti i criteri dell'endpoint del servizio che iniziano con "ServiceEndpointPolicy".</span><span class="sxs-lookup"><span data-stu-id="f7f3a-115">This command gets a list of all the service endpoint policies that start with "ServiceEndpointPolicy".</span></span>

## <span data-ttu-id="f7f3a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7f3a-116">PARAMETERS</span></span>

### <span data-ttu-id="f7f3a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7f3a-117">-DefaultProfile</span></span>
<span data-ttu-id="f7f3a-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f7f3a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7f3a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f7f3a-119">-Name</span></span>
<span data-ttu-id="f7f3a-120">Nome dei criteri dell'endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="f7f3a-120">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="f7f3a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7f3a-121">-ResourceGroupName</span></span>
<span data-ttu-id="f7f3a-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f7f3a-122">The resource group name.</span></span>

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

### <span data-ttu-id="f7f3a-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7f3a-123">-ResourceId</span></span>
<span data-ttu-id="f7f3a-124">ID dei criteri dell'endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="f7f3a-124">The ID of the service endpoint policy.</span></span>

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

### <span data-ttu-id="f7f3a-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7f3a-125">-Confirm</span></span>
<span data-ttu-id="f7f3a-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7f3a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7f3a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7f3a-127">-WhatIf</span></span>
<span data-ttu-id="f7f3a-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7f3a-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7f3a-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7f3a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7f3a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7f3a-130">CommonParameters</span></span>
<span data-ttu-id="f7f3a-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7f3a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7f3a-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f7f3a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7f3a-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="f7f3a-133">INPUTS</span></span>

### <span data-ttu-id="f7f3a-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f7f3a-134">System.String</span></span>

## <span data-ttu-id="f7f3a-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f7f3a-135">OUTPUTS</span></span>

### <span data-ttu-id="f7f3a-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f7f3a-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="f7f3a-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="f7f3a-137">NOTES</span></span>

## <span data-ttu-id="f7f3a-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f7f3a-138">RELATED LINKS</span></span>

[<span data-ttu-id="f7f3a-139">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f7f3a-139">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="f7f3a-140">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f7f3a-140">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="f7f3a-141">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f7f3a-141">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
