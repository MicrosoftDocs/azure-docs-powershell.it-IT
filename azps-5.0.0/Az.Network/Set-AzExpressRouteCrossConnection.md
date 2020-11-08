---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
ms.openlocfilehash: 649ae6233f312dab4f18263bb65c4a9cd43b2aee
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200709"
---
# <span data-ttu-id="860cf-101">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="860cf-101">Set-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="860cf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="860cf-102">SYNOPSIS</span></span>
<span data-ttu-id="860cf-103">Modifica una connessione trasversale ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="860cf-103">Modifies an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="860cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="860cf-104">SYNTAX</span></span>

### <span data-ttu-id="860cf-105">ModifyByCircuitReference</span><span class="sxs-lookup"><span data-stu-id="860cf-105">ModifyByCircuitReference</span></span>
```
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="860cf-106">ModifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="860cf-106">ModifyByParameterValues</span></span>
```
Set-AzExpressRouteCrossConnection -ResourceGroupName <String> -Name <String>
 [-ServiceProviderProvisioningState <String>] [-ServiceProviderNotes <String>]
 [-Peerings <PSExpressRouteCrossConnectionPeering[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="860cf-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="860cf-107">DESCRIPTION</span></span>
<span data-ttu-id="860cf-108">Il cmdlet **set-AzExpressRouteCrossConnection** salva la connessione trasversale ExpressRoute modificata in Azure.</span><span class="sxs-lookup"><span data-stu-id="860cf-108">The **Set-AzExpressRouteCrossConnection** cmdlet saves the modified ExpressRoute cross connection to Azure.</span></span>

## <span data-ttu-id="860cf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="860cf-109">EXAMPLES</span></span>

### <span data-ttu-id="860cf-110">Esempio 1: cambiare lo stato di provisioning del provider di servizi di una connessione incrociata ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="860cf-110">Example 1: Change the Service Provider Provisioning State of an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$cc.ServiceProviderProvisioningState = 'Provisioned'
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="860cf-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="860cf-111">PARAMETERS</span></span>

### <span data-ttu-id="860cf-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="860cf-112">-AsJob</span></span>
<span data-ttu-id="860cf-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="860cf-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="860cf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="860cf-114">-DefaultProfile</span></span>
<span data-ttu-id="860cf-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="860cf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="860cf-116">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="860cf-116">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="860cf-117">Specifica l'oggetto **ExpressRouteCrossConnection** che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="860cf-117">Specifies the **ExpressRouteCrossConnection** object that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: ModifyByCircuitReference
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="860cf-118">-Force</span><span class="sxs-lookup"><span data-stu-id="860cf-118">-Force</span></span>
<span data-ttu-id="860cf-119">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="860cf-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="860cf-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="860cf-120">-Name</span></span>
<span data-ttu-id="860cf-121">Nome della connessione trasversale della route espressa.</span><span class="sxs-lookup"><span data-stu-id="860cf-121">The name of express route cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="860cf-122">-Peerings</span><span class="sxs-lookup"><span data-stu-id="860cf-122">-Peerings</span></span>
<span data-ttu-id="860cf-123">Elenco dei peer per la connessione trasversale</span><span class="sxs-lookup"><span data-stu-id="860cf-123">The list of peerings for the cross connection</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionPeering[]
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="860cf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="860cf-124">-ResourceGroupName</span></span>
<span data-ttu-id="860cf-125">ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="860cf-125">The ExpressRouteCrossConnection</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="860cf-126">-ServiceProviderNotes</span><span class="sxs-lookup"><span data-stu-id="860cf-126">-ServiceProviderNotes</span></span>
<span data-ttu-id="860cf-127">Note del provider di servizi</span><span class="sxs-lookup"><span data-stu-id="860cf-127">The service provider notes</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="860cf-128">-ServiceProviderProvisioningState</span><span class="sxs-lookup"><span data-stu-id="860cf-128">-ServiceProviderProvisioningState</span></span>
<span data-ttu-id="860cf-129">Stato di provisioning del provider di servizi da impostare</span><span class="sxs-lookup"><span data-stu-id="860cf-129">The service provider provisioning state to be set</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="860cf-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="860cf-130">-Confirm</span></span>
<span data-ttu-id="860cf-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="860cf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="860cf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="860cf-132">-WhatIf</span></span>
<span data-ttu-id="860cf-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="860cf-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="860cf-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="860cf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="860cf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="860cf-135">CommonParameters</span></span>
<span data-ttu-id="860cf-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="860cf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="860cf-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="860cf-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="860cf-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="860cf-138">INPUTS</span></span>

### <span data-ttu-id="860cf-139">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="860cf-139">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="860cf-140">Il parametro ' ExpressRouteCrossConnection ' accetta il valore di tipo ' PSExpressRouteCrossConnection ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="860cf-140">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="860cf-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="860cf-141">OUTPUTS</span></span>

### <span data-ttu-id="860cf-142">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="860cf-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="860cf-143">Note</span><span class="sxs-lookup"><span data-stu-id="860cf-143">NOTES</span></span>

## <span data-ttu-id="860cf-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="860cf-144">RELATED LINKS</span></span>

[<span data-ttu-id="860cf-145">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="860cf-145">Get-AzExpressRouteCrossConnection</span></span>](./Get-AzExpressRouteCrossConnection.md)
