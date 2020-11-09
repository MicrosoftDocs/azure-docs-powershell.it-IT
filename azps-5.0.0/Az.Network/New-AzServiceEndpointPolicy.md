---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
ms.openlocfilehash: 4fbc1729debb7f5cf822f152107797e10b1f7ba9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301879"
---
# <span data-ttu-id="cf880-101">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="cf880-101">New-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="cf880-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cf880-102">SYNOPSIS</span></span>
<span data-ttu-id="cf880-103">Crea un criterio endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="cf880-103">Creates a service endpoint policy.</span></span>

## <span data-ttu-id="cf880-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cf880-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicy -Name <String>
 [-ServiceEndpointPolicyDefinition <PSServiceEndpointPolicyDefinition[]>] -ResourceGroupName <String>
 -Location <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cf880-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf880-105">DESCRIPTION</span></span>
<span data-ttu-id="cf880-106">Il cmdlet **New-AzServiceEndpointPolicy** crea un criterio endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="cf880-106">The **New-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="cf880-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cf880-107">EXAMPLES</span></span>

### <span data-ttu-id="cf880-108">Esempio 1: crea un criterio endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="cf880-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="cf880-109">Questo comando crea un criterio endpoint del servizio denominato Policy1 con le definizioni definite dall'oggetto $serviceEndpointDefinition e lo archivia nella variabile $serviceEndpointPolicy.</span><span class="sxs-lookup"><span data-stu-id="cf880-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="cf880-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cf880-110">PARAMETERS</span></span>

### <span data-ttu-id="cf880-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf880-111">-DefaultProfile</span></span>
<span data-ttu-id="cf880-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cf880-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf880-113">-Force</span><span class="sxs-lookup"><span data-stu-id="cf880-113">-Force</span></span>
<span data-ttu-id="cf880-114">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="cf880-114">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="cf880-115">-Posizione</span><span class="sxs-lookup"><span data-stu-id="cf880-115">-Location</span></span>
<span data-ttu-id="cf880-116">posizione.</span><span class="sxs-lookup"><span data-stu-id="cf880-116">location.</span></span>

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

### <span data-ttu-id="cf880-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="cf880-117">-Name</span></span>
<span data-ttu-id="cf880-118">Nome della subnet</span><span class="sxs-lookup"><span data-stu-id="cf880-118">The name of the subnet</span></span>

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

### <span data-ttu-id="cf880-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf880-119">-ResourceGroupName</span></span>
<span data-ttu-id="cf880-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cf880-120">The resource group name.</span></span>

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

### <span data-ttu-id="cf880-121">-ServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cf880-121">-ServiceEndpointPolicyDefinition</span></span>
<span data-ttu-id="cf880-122">Elenco di definizioni di endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="cf880-122">List of service endpoint definitions</span></span>

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

### <span data-ttu-id="cf880-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cf880-123">-Confirm</span></span>
<span data-ttu-id="cf880-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf880-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf880-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf880-125">-WhatIf</span></span>
<span data-ttu-id="cf880-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf880-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf880-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf880-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf880-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf880-128">CommonParameters</span></span>
<span data-ttu-id="cf880-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf880-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf880-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf880-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf880-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cf880-131">INPUTS</span></span>

### <span data-ttu-id="cf880-132">System. String</span><span class="sxs-lookup"><span data-stu-id="cf880-132">System.String</span></span>

## <span data-ttu-id="cf880-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cf880-133">OUTPUTS</span></span>

### <span data-ttu-id="cf880-134">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="cf880-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="cf880-135">Note</span><span class="sxs-lookup"><span data-stu-id="cf880-135">NOTES</span></span>

## <span data-ttu-id="cf880-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cf880-136">RELATED LINKS</span></span>

[<span data-ttu-id="cf880-137">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="cf880-137">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="cf880-138">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="cf880-138">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="cf880-139">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="cf880-139">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
