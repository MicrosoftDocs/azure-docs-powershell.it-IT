---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
ms.openlocfilehash: b5f555a0df848c86dbbc0a04297d45b4132e6972
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953790"
---
# <span data-ttu-id="5f239-101">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5f239-101">New-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="5f239-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f239-102">SYNOPSIS</span></span>
<span data-ttu-id="5f239-103">Crea criteri dell'endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="5f239-103">Creates a service endpoint policy.</span></span>

## <span data-ttu-id="5f239-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5f239-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicy -Name <String>
 [-ServiceEndpointPolicyDefinition <PSServiceEndpointPolicyDefinition[]>] -ResourceGroupName <String>
 -Location <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5f239-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5f239-105">DESCRIPTION</span></span>
<span data-ttu-id="5f239-106">Il cmdlet **New-AzServiceEndpointPolicy** crea un criterio dell'endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="5f239-106">The **New-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="5f239-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5f239-107">EXAMPLES</span></span>

### <span data-ttu-id="5f239-108">Esempio 1: Crea un criterio endpoint di servizio</span><span class="sxs-lookup"><span data-stu-id="5f239-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="5f239-109">Questo comando crea un criterio endpoint di servizio denominato Criterio1 con le definizioni definite dall'oggetto $serviceEndpointDefinition e lo archivia nella variabile $serviceEndpointPolicy servizio.</span><span class="sxs-lookup"><span data-stu-id="5f239-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="5f239-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f239-110">PARAMETERS</span></span>

### <span data-ttu-id="5f239-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f239-111">-DefaultProfile</span></span>
<span data-ttu-id="5f239-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5f239-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f239-113">-Force</span><span class="sxs-lookup"><span data-stu-id="5f239-113">-Force</span></span>
<span data-ttu-id="5f239-114">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="5f239-114">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="5f239-115">-Location</span><span class="sxs-lookup"><span data-stu-id="5f239-115">-Location</span></span>
<span data-ttu-id="5f239-116">posizione.</span><span class="sxs-lookup"><span data-stu-id="5f239-116">location.</span></span>

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

### <span data-ttu-id="5f239-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5f239-117">-Name</span></span>
<span data-ttu-id="5f239-118">Nome della subnet</span><span class="sxs-lookup"><span data-stu-id="5f239-118">The name of the subnet</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f239-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f239-119">-ResourceGroupName</span></span>
<span data-ttu-id="5f239-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5f239-120">The resource group name.</span></span>

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

### <span data-ttu-id="5f239-121">-ServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5f239-121">-ServiceEndpointPolicyDefinition</span></span>
<span data-ttu-id="5f239-122">Elenco delle definizioni degli endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="5f239-122">List of service endpoint definitions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f239-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5f239-123">-Confirm</span></span>
<span data-ttu-id="5f239-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f239-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f239-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f239-125">-WhatIf</span></span>
<span data-ttu-id="5f239-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5f239-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f239-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5f239-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f239-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f239-128">CommonParameters</span></span>
<span data-ttu-id="5f239-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f239-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f239-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f239-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f239-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="5f239-131">INPUTS</span></span>

### <span data-ttu-id="5f239-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5f239-132">System.String</span></span>

## <span data-ttu-id="5f239-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5f239-133">OUTPUTS</span></span>

### <span data-ttu-id="5f239-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5f239-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="5f239-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="5f239-135">NOTES</span></span>

## <span data-ttu-id="5f239-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5f239-136">RELATED LINKS</span></span>

[<span data-ttu-id="5f239-137">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5f239-137">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="5f239-138">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5f239-138">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="5f239-139">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="5f239-139">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
