---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
ms.openlocfilehash: 4fbc1729debb7f5cf822f152107797e10b1f7ba9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021204"
---
# <span data-ttu-id="52368-101">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="52368-101">New-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="52368-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="52368-102">SYNOPSIS</span></span>
<span data-ttu-id="52368-103">Crea un criterio endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="52368-103">Creates a service endpoint policy.</span></span>

## <span data-ttu-id="52368-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52368-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicy -Name <String>
 [-ServiceEndpointPolicyDefinition <PSServiceEndpointPolicyDefinition[]>] -ResourceGroupName <String>
 -Location <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="52368-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52368-105">DESCRIPTION</span></span>
<span data-ttu-id="52368-106">Il cmdlet **New-AzServiceEndpointPolicy** crea un criterio endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="52368-106">The **New-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="52368-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52368-107">EXAMPLES</span></span>

### <span data-ttu-id="52368-108">Esempio 1: crea un criterio endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="52368-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="52368-109">Questo comando crea un criterio endpoint del servizio denominato Policy1 con le definizioni definite dall'oggetto $serviceEndpointDefinition e lo archivia nella variabile $serviceEndpointPolicy.</span><span class="sxs-lookup"><span data-stu-id="52368-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="52368-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="52368-110">PARAMETERS</span></span>

### <span data-ttu-id="52368-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52368-111">-DefaultProfile</span></span>
<span data-ttu-id="52368-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="52368-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52368-113">-Force</span><span class="sxs-lookup"><span data-stu-id="52368-113">-Force</span></span>
<span data-ttu-id="52368-114">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="52368-114">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="52368-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="52368-115">-Location</span></span>
<span data-ttu-id="52368-116">posizione.</span><span class="sxs-lookup"><span data-stu-id="52368-116">location.</span></span>

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

### <span data-ttu-id="52368-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="52368-117">-Name</span></span>
<span data-ttu-id="52368-118">Nome della subnet</span><span class="sxs-lookup"><span data-stu-id="52368-118">The name of the subnet</span></span>

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

### <span data-ttu-id="52368-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52368-119">-ResourceGroupName</span></span>
<span data-ttu-id="52368-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="52368-120">The resource group name.</span></span>

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

### <span data-ttu-id="52368-121">-ServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="52368-121">-ServiceEndpointPolicyDefinition</span></span>
<span data-ttu-id="52368-122">Elenco di definizioni di endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="52368-122">List of service endpoint definitions</span></span>

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

### <span data-ttu-id="52368-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="52368-123">-Confirm</span></span>
<span data-ttu-id="52368-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52368-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52368-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52368-125">-WhatIf</span></span>
<span data-ttu-id="52368-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52368-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52368-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52368-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52368-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52368-128">CommonParameters</span></span>
<span data-ttu-id="52368-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52368-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52368-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52368-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52368-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="52368-131">INPUTS</span></span>

### <span data-ttu-id="52368-132">System. String</span><span class="sxs-lookup"><span data-stu-id="52368-132">System.String</span></span>

## <span data-ttu-id="52368-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52368-133">OUTPUTS</span></span>

### <span data-ttu-id="52368-134">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="52368-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="52368-135">Note</span><span class="sxs-lookup"><span data-stu-id="52368-135">NOTES</span></span>

## <span data-ttu-id="52368-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52368-136">RELATED LINKS</span></span>

[<span data-ttu-id="52368-137">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="52368-137">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="52368-138">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="52368-138">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="52368-139">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="52368-139">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
