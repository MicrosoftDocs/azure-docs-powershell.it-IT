---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
ms.openlocfilehash: e7025a48fd1d83a0018ac18de01673b0deeed742
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678235"
---
# <span data-ttu-id="c9e2e-101">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c9e2e-101">New-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="c9e2e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c9e2e-102">SYNOPSIS</span></span>
<span data-ttu-id="c9e2e-103">Crea un criterio endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-103">Creates a service endpoint policy.</span></span>

## <span data-ttu-id="c9e2e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9e2e-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicy -Name <String>
 [-ServiceEndpointPolicyDefinition <PSServiceEndpointPolicyDefinition[]>] -ResourceGroupName <String>
 -Location <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9e2e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9e2e-105">DESCRIPTION</span></span>
<span data-ttu-id="c9e2e-106">Il cmdlet **New-AzServiceEndpointPolicy** crea un criterio endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-106">The **New-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="c9e2e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9e2e-107">EXAMPLES</span></span>

### <span data-ttu-id="c9e2e-108">Esempio 1: crea un criterio endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="c9e2e-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="c9e2e-109">Questo comando crea un criterio endpoint del servizio denominato Policy1 con le definizioni definite dall'oggetto $serviceEndpointDefinition e lo archivia nella variabile $serviceEndpointPolicy.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="c9e2e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c9e2e-110">PARAMETERS</span></span>

### <span data-ttu-id="c9e2e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9e2e-111">-DefaultProfile</span></span>
<span data-ttu-id="c9e2e-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9e2e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c9e2e-113">-Force</span></span>
<span data-ttu-id="c9e2e-114">Non chiedere conferma se si vuole usare una risorsa per un sovrarito</span><span class="sxs-lookup"><span data-stu-id="c9e2e-114">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="c9e2e-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="c9e2e-115">-Location</span></span>
<span data-ttu-id="c9e2e-116">posizione.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-116">location.</span></span>

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

### <span data-ttu-id="c9e2e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="c9e2e-117">-Name</span></span>
<span data-ttu-id="c9e2e-118">Nome della subnet</span><span class="sxs-lookup"><span data-stu-id="c9e2e-118">The name of the subnet</span></span>

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

### <span data-ttu-id="c9e2e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9e2e-119">-ResourceGroupName</span></span>
<span data-ttu-id="c9e2e-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-120">The resource group name.</span></span>

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

### <span data-ttu-id="c9e2e-121">-ServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c9e2e-121">-ServiceEndpointPolicyDefinition</span></span>
<span data-ttu-id="c9e2e-122">Elenco di definizioni di endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="c9e2e-122">List of service endpoint definitions</span></span>

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

### <span data-ttu-id="c9e2e-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c9e2e-123">-Confirm</span></span>
<span data-ttu-id="c9e2e-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9e2e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9e2e-125">-WhatIf</span></span>
<span data-ttu-id="c9e2e-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9e2e-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9e2e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9e2e-128">CommonParameters</span></span>
<span data-ttu-id="c9e2e-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9e2e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9e2e-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9e2e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9e2e-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c9e2e-131">INPUTS</span></span>

### <span data-ttu-id="c9e2e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c9e2e-132">System.String</span></span>

## <span data-ttu-id="c9e2e-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9e2e-133">OUTPUTS</span></span>

### <span data-ttu-id="c9e2e-134">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c9e2e-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="c9e2e-135">Note</span><span class="sxs-lookup"><span data-stu-id="c9e2e-135">NOTES</span></span>

## <span data-ttu-id="c9e2e-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9e2e-136">RELATED LINKS</span></span>

[<span data-ttu-id="c9e2e-137">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c9e2e-137">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="c9e2e-138">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c9e2e-138">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="c9e2e-139">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c9e2e-139">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
