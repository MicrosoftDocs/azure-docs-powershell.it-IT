---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
ms.openlocfilehash: fdff53931891ce62b2182f2c8c78d54312141f5c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853657"
---
# <span data-ttu-id="05ff0-101">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="05ff0-101">Get-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="05ff0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="05ff0-102">SYNOPSIS</span></span>
<span data-ttu-id="05ff0-103">Ottiene un criterio endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="05ff0-103">Gets a service endpoint policy.</span></span>

## <span data-ttu-id="05ff0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05ff0-104">SYNTAX</span></span>

### <span data-ttu-id="05ff0-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="05ff0-105">ListParameterSet (Default)</span></span>
```
Get-AzServiceEndpointPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05ff0-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="05ff0-106">GetByResourceIdParameterSet</span></span>
```
Get-AzServiceEndpointPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05ff0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05ff0-107">DESCRIPTION</span></span>
<span data-ttu-id="05ff0-108">Il cmdlet **Get-AzServiceEndpointPolicy** ottiene un criterio endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="05ff0-108">The **Get-AzServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="05ff0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05ff0-109">EXAMPLES</span></span>

### <span data-ttu-id="05ff0-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="05ff0-110">Example 1</span></span>
```
$policy = Get-AzServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="05ff0-111">Questo comando ottiene il criterio endpoint del servizio denominato ServiceEndpointPolicy1 che appartiene al gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $policy.</span><span class="sxs-lookup"><span data-stu-id="05ff0-111">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="05ff0-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="05ff0-112">Example 2</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="05ff0-113">Questo comando consente di ottenere un elenco di tutti i criteri endpoint del servizio nel gruppo di risorse denominato ResourceGroup01 e di archiviarlo nella variabile $policyList.</span><span class="sxs-lookup"><span data-stu-id="05ff0-113">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

### <span data-ttu-id="05ff0-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="05ff0-114">Example 3</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ServiceEndpointPolicy*"
```

<span data-ttu-id="05ff0-115">Questo comando consente di ottenere un elenco di tutti i criteri dell'endpoint del servizio che iniziano con "ServiceEndpointPolicy".</span><span class="sxs-lookup"><span data-stu-id="05ff0-115">This command gets a list of all the service endpoint policies that start with "ServiceEndpointPolicy".</span></span>

## <span data-ttu-id="05ff0-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="05ff0-116">PARAMETERS</span></span>

### <span data-ttu-id="05ff0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05ff0-117">-DefaultProfile</span></span>
<span data-ttu-id="05ff0-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="05ff0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05ff0-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="05ff0-119">-Name</span></span>
<span data-ttu-id="05ff0-120">Nome del criterio endpoint del servizio</span><span class="sxs-lookup"><span data-stu-id="05ff0-120">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="05ff0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05ff0-121">-ResourceGroupName</span></span>
<span data-ttu-id="05ff0-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="05ff0-122">The resource group name.</span></span>

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

### <span data-ttu-id="05ff0-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05ff0-123">-ResourceId</span></span>
<span data-ttu-id="05ff0-124">ID del criterio endpoint del servizio.</span><span class="sxs-lookup"><span data-stu-id="05ff0-124">The ID of the service endpoint policy.</span></span>

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

### <span data-ttu-id="05ff0-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="05ff0-125">-Confirm</span></span>
<span data-ttu-id="05ff0-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05ff0-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05ff0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05ff0-127">-WhatIf</span></span>
<span data-ttu-id="05ff0-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05ff0-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="05ff0-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05ff0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05ff0-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05ff0-130">CommonParameters</span></span>
<span data-ttu-id="05ff0-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05ff0-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05ff0-132">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05ff0-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05ff0-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="05ff0-133">INPUTS</span></span>

### <span data-ttu-id="05ff0-134">System. String</span><span class="sxs-lookup"><span data-stu-id="05ff0-134">System.String</span></span>

## <span data-ttu-id="05ff0-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05ff0-135">OUTPUTS</span></span>

### <span data-ttu-id="05ff0-136">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="05ff0-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="05ff0-137">Note</span><span class="sxs-lookup"><span data-stu-id="05ff0-137">NOTES</span></span>

## <span data-ttu-id="05ff0-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05ff0-138">RELATED LINKS</span></span>

[<span data-ttu-id="05ff0-139">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="05ff0-139">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="05ff0-140">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="05ff0-140">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="05ff0-141">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="05ff0-141">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
