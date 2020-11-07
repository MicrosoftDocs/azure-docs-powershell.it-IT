---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
ms.openlocfilehash: 175082a90a1a494eb4508bc83d71584326c9eb97
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677978"
---
# <span data-ttu-id="5ca2e-101">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="5ca2e-101">Set-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="5ca2e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5ca2e-102">SYNOPSIS</span></span>
<span data-ttu-id="5ca2e-103">Modifica una connessione trasversale ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="5ca2e-103">Modifies an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="5ca2e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ca2e-104">SYNTAX</span></span>

### <span data-ttu-id="5ca2e-105">ModifyByCircuitReference</span><span class="sxs-lookup"><span data-stu-id="5ca2e-105">ModifyByCircuitReference</span></span>
```
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ca2e-106">ModifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="5ca2e-106">ModifyByParameterValues</span></span>
```
Set-AzExpressRouteCrossConnection -ResourceGroupName <String> -Name <String>
 [-ServiceProviderProvisioningState <String>] [-ServiceProviderNotes <String>]
 [-Peerings <PSExpressRouteCrossConnectionPeering[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ca2e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ca2e-107">DESCRIPTION</span></span>
<span data-ttu-id="5ca2e-108">Il cmdlet **set-AzExpressRouteCrossConnection** salva la connessione trasversale ExpressRoute modificata in Azure.</span><span class="sxs-lookup"><span data-stu-id="5ca2e-108">The **Set-AzExpressRouteCrossConnection** cmdlet saves the modified ExpressRoute cross connection to Azure.</span></span>

## <span data-ttu-id="5ca2e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ca2e-109">EXAMPLES</span></span>

### <span data-ttu-id="5ca2e-110">Esempio 1: cambiare lo stato di provisioning del provider di servizi di una connessione incrociata ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="5ca2e-110">Example 1: Change the Service Provider Provisioning State of an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$cc.ServiceProviderProvisioningState = 'Provisioned'
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="5ca2e-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5ca2e-111">PARAMETERS</span></span>

### <span data-ttu-id="5ca2e-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ca2e-112">-AsJob</span></span>
<span data-ttu-id="5ca2e-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5ca2e-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5ca2e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ca2e-114">-DefaultProfile</span></span>
<span data-ttu-id="5ca2e-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5ca2e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ca2e-116">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="5ca2e-116">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="5ca2e-117">Specifica l'oggetto **ExpressRouteCrossConnection** che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="5ca2e-117">Specifies the **ExpressRouteCrossConnection** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5ca2e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="5ca2e-118">-Force</span></span>
<span data-ttu-id="5ca2e-119">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="5ca2e-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="5ca2e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="5ca2e-120">-Name</span></span>
<span data-ttu-id="5ca2e-121">Nome della connessione trasversale della route espressa.</span><span class="sxs-lookup"><span data-stu-id="5ca2e-121">The name of express route cross connection.</span></span>

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

### <span data-ttu-id="5ca2e-122">-Peerings</span><span class="sxs-lookup"><span data-stu-id="5ca2e-122">-Peerings</span></span>
<span data-ttu-id="5ca2e-123">Elenco dei peer per la connessione trasversale</span><span class="sxs-lookup"><span data-stu-id="5ca2e-123">The list of peerings for the cross connection</span></span>

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

### <span data-ttu-id="5ca2e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ca2e-124">-ResourceGroupName</span></span>
<span data-ttu-id="5ca2e-125">ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="5ca2e-125">The ExpressRouteCrossConnection</span></span>

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

### <span data-ttu-id="5ca2e-126">-ServiceProviderNotes</span><span class="sxs-lookup"><span data-stu-id="5ca2e-126">-ServiceProviderNotes</span></span>
<span data-ttu-id="5ca2e-127">Note del provider di servizi</span><span class="sxs-lookup"><span data-stu-id="5ca2e-127">The service provider notes</span></span>

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

### <span data-ttu-id="5ca2e-128">-ServiceProviderProvisioningState</span><span class="sxs-lookup"><span data-stu-id="5ca2e-128">-ServiceProviderProvisioningState</span></span>
<span data-ttu-id="5ca2e-129">Stato di provisioning del provider di servizi da impostare</span><span class="sxs-lookup"><span data-stu-id="5ca2e-129">The service provider provisioning state to be set</span></span>

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

### <span data-ttu-id="5ca2e-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5ca2e-130">-Confirm</span></span>
<span data-ttu-id="5ca2e-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ca2e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ca2e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ca2e-132">-WhatIf</span></span>
<span data-ttu-id="5ca2e-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5ca2e-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ca2e-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5ca2e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ca2e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ca2e-135">CommonParameters</span></span>
<span data-ttu-id="5ca2e-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ca2e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ca2e-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ca2e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ca2e-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5ca2e-138">INPUTS</span></span>

### <span data-ttu-id="5ca2e-139">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="5ca2e-139">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="5ca2e-140">Il parametro ' ExpressRouteCrossConnection ' accetta il valore di tipo ' PSExpressRouteCrossConnection ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="5ca2e-140">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="5ca2e-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ca2e-141">OUTPUTS</span></span>

### <span data-ttu-id="5ca2e-142">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="5ca2e-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="5ca2e-143">Note</span><span class="sxs-lookup"><span data-stu-id="5ca2e-143">NOTES</span></span>

## <span data-ttu-id="5ca2e-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ca2e-144">RELATED LINKS</span></span>

[<span data-ttu-id="5ca2e-145">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="5ca2e-145">Get-AzExpressRouteCrossConnection</span></span>](./Get-AzExpressRouteCrossConnection.md)
