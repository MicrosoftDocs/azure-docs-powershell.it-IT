---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
ms.openlocfilehash: 9b03a33ebea52e57950e46c894e95ffefe520b4e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852889"
---
# <span data-ttu-id="3459d-101">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="3459d-101">New-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="3459d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3459d-102">SYNOPSIS</span></span>
<span data-ttu-id="3459d-103">Crea un criterio endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="3459d-103">Creates a service endpoint policy.</span></span>

## <span data-ttu-id="3459d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3459d-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicy -Name <String>
 [-ServiceEndpointPolicyDefinition <PSServiceEndpointPolicyDefinition[]>] -ResourceGroupName <String>
 -Location <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3459d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3459d-105">DESCRIPTION</span></span>
<span data-ttu-id="3459d-106">Il cmdlet **New-AzServiceEndpointPolicy** crea un criterio endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="3459d-106">The **New-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="3459d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3459d-107">EXAMPLES</span></span>

### <span data-ttu-id="3459d-108">Esempio 1: crea un criterio endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="3459d-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="3459d-109">Questo comando crea un criterio endpoint del servizio denominato Policy1 con le definizioni definite dall'oggetto $serviceEndpointDefinition e lo archivia nella variabile $serviceEndpointPolicy.</span><span class="sxs-lookup"><span data-stu-id="3459d-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="3459d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3459d-110">PARAMETERS</span></span>

### <span data-ttu-id="3459d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3459d-111">-DefaultProfile</span></span>
<span data-ttu-id="3459d-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3459d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3459d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3459d-113">-Force</span></span>
<span data-ttu-id="3459d-114">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="3459d-114">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="3459d-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="3459d-115">-Location</span></span>
<span data-ttu-id="3459d-116">posizione.</span><span class="sxs-lookup"><span data-stu-id="3459d-116">location.</span></span>

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

### <span data-ttu-id="3459d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="3459d-117">-Name</span></span>
<span data-ttu-id="3459d-118">Nome della subnet</span><span class="sxs-lookup"><span data-stu-id="3459d-118">The name of the subnet</span></span>

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

### <span data-ttu-id="3459d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3459d-119">-ResourceGroupName</span></span>
<span data-ttu-id="3459d-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3459d-120">The resource group name.</span></span>

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

### <span data-ttu-id="3459d-121">-ServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3459d-121">-ServiceEndpointPolicyDefinition</span></span>
<span data-ttu-id="3459d-122">Elenco di definizioni di endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="3459d-122">List of service endpoint definitions</span></span>

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

### <span data-ttu-id="3459d-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3459d-123">-Confirm</span></span>
<span data-ttu-id="3459d-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3459d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3459d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3459d-125">-WhatIf</span></span>
<span data-ttu-id="3459d-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3459d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3459d-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3459d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3459d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3459d-128">CommonParameters</span></span>
<span data-ttu-id="3459d-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3459d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3459d-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3459d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3459d-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3459d-131">INPUTS</span></span>

### <span data-ttu-id="3459d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3459d-132">System.String</span></span>

## <span data-ttu-id="3459d-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3459d-133">OUTPUTS</span></span>

### <span data-ttu-id="3459d-134">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="3459d-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="3459d-135">Note</span><span class="sxs-lookup"><span data-stu-id="3459d-135">NOTES</span></span>

## <span data-ttu-id="3459d-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3459d-136">RELATED LINKS</span></span>

[<span data-ttu-id="3459d-137">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="3459d-137">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="3459d-138">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="3459d-138">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="3459d-139">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="3459d-139">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
