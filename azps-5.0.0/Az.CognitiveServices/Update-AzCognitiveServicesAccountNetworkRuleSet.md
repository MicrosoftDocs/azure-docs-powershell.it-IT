---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/update-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 0f094ba8bdfa8dbf40f2af8495ee2f8cfa6fca16
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202551"
---
# <span data-ttu-id="1ff78-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="1ff78-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="1ff78-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1ff78-102">SYNOPSIS</span></span>
<span data-ttu-id="1ff78-103">Aggiornare la proprietà NetworkRule di un account di servizi cognitivi</span><span class="sxs-lookup"><span data-stu-id="1ff78-103">Update the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="1ff78-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1ff78-104">SYNTAX</span></span>

```
Update-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IpRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1ff78-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ff78-105">DESCRIPTION</span></span>
<span data-ttu-id="1ff78-106">Il cmdlet **Update-AzCognitiveServicesAccountNetworkRuleSet** aggiorna la proprietà NetworkRule di un account di servizi cognitivi</span><span class="sxs-lookup"><span data-stu-id="1ff78-106">The **Update-AzCognitiveServicesAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="1ff78-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1ff78-107">EXAMPLES</span></span>

### <span data-ttu-id="1ff78-108">Esempio 1: aggiornare tutte le proprietà di NetworkRule, regole di input con JSON</span><span class="sxs-lookup"><span data-stu-id="1ff78-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -DefaultAction Allow -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2"})
```

<span data-ttu-id="1ff78-109">Questo comando Aggiorna tutte le proprietà di NetworkRule, regole di input con JSON.</span><span class="sxs-lookup"><span data-stu-id="1ff78-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="1ff78-110">Esempio 2: Proprietà Update bypass di NetworkRule</span><span class="sxs-lookup"><span data-stu-id="1ff78-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="1ff78-111">Questa proprietà di aggiornamento dei comandi di NetworkRule (altre proprietà non cambieranno).</span><span class="sxs-lookup"><span data-stu-id="1ff78-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="1ff78-112">Esempio 3: pulire le regole di NetworkRule di un account di servizi cognitivi</span><span class="sxs-lookup"><span data-stu-id="1ff78-112">Example 3: Clean up rules of NetworkRule of a Cognitive Services account</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="1ff78-113">Questo comando pulisce le regole di NetworkRule di un account di servizi cognitivi (altre proprietà non cambiano).</span><span class="sxs-lookup"><span data-stu-id="1ff78-113">This command clean up rules of NetworkRule of a Cognitive Services account (other properties not change).</span></span>

## <span data-ttu-id="1ff78-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1ff78-114">PARAMETERS</span></span>

### <span data-ttu-id="1ff78-115">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="1ff78-115">-DefaultAction</span></span>
<span data-ttu-id="1ff78-116">Account dei servizi cognitivi NetworkRule DefaultAction.</span><span class="sxs-lookup"><span data-stu-id="1ff78-116">Cognitive Services Account NetworkRule DefaultAction.</span></span> <span data-ttu-id="1ff78-117">Valore predefinito `Deny` .</span><span class="sxs-lookup"><span data-stu-id="1ff78-117">Default value `Deny`.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Deny, Allow

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ff78-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ff78-118">-DefaultProfile</span></span>
<span data-ttu-id="1ff78-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1ff78-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ff78-120">-IpRule</span><span class="sxs-lookup"><span data-stu-id="1ff78-120">-IpRule</span></span>
<span data-ttu-id="1ff78-121">Account di servizi cognitivi NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="1ff78-121">Cognitive Services Account NetworkRule IpRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ff78-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="1ff78-122">-Name</span></span>
<span data-ttu-id="1ff78-123">Nome account servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="1ff78-123">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ff78-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ff78-124">-ResourceGroupName</span></span>
<span data-ttu-id="1ff78-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1ff78-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ff78-126">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1ff78-126">-VirtualNetworkRule</span></span>
<span data-ttu-id="1ff78-127">Account di servizi cognitivi NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="1ff78-127">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ff78-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1ff78-128">-Confirm</span></span>
<span data-ttu-id="1ff78-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ff78-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ff78-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ff78-130">-WhatIf</span></span>
<span data-ttu-id="1ff78-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1ff78-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ff78-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1ff78-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ff78-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ff78-133">CommonParameters</span></span>
<span data-ttu-id="1ff78-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ff78-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ff78-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ff78-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ff78-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1ff78-136">INPUTS</span></span>

### <span data-ttu-id="1ff78-137">System. String</span><span class="sxs-lookup"><span data-stu-id="1ff78-137">System.String</span></span>

### <span data-ttu-id="1ff78-138">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="1ff78-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="1ff78-139">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="1ff78-139">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="1ff78-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1ff78-140">OUTPUTS</span></span>

### <span data-ttu-id="1ff78-141">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="1ff78-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="1ff78-142">Note</span><span class="sxs-lookup"><span data-stu-id="1ff78-142">NOTES</span></span>

## <span data-ttu-id="1ff78-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1ff78-143">RELATED LINKS</span></span>
