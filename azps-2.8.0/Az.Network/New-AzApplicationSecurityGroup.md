---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
ms.openlocfilehash: 0bccee6b8242e3480ad405837f9c2a661eb97431
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853517"
---
# <span data-ttu-id="27591-101">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="27591-101">New-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="27591-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="27591-102">SYNOPSIS</span></span>
<span data-ttu-id="27591-103">Crea un gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="27591-103">Creates an application security group.</span></span>

## <span data-ttu-id="27591-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27591-104">SYNTAX</span></span>

```
New-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27591-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27591-105">DESCRIPTION</span></span>
<span data-ttu-id="27591-106">Il cmdlet **New-AzApplicationSecurityGroup** crea un gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="27591-106">The **New-AzApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="27591-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27591-107">EXAMPLES</span></span>

### <span data-ttu-id="27591-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="27591-108">Example 1</span></span>
```
PS C:\> New-AzApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="27591-109">Questo esempio crea un gruppo di sicurezza dell'applicazione senza associazioni.</span><span class="sxs-lookup"><span data-stu-id="27591-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="27591-110">Una volta creato, le configurazioni IP nell'interfaccia di rete possono essere incluse nel gruppo.</span><span class="sxs-lookup"><span data-stu-id="27591-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="27591-111">Le regole di sicurezza possono anche riferirsi al gruppo come origini o destinazioni.</span><span class="sxs-lookup"><span data-stu-id="27591-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="27591-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="27591-112">PARAMETERS</span></span>

### <span data-ttu-id="27591-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27591-113">-AsJob</span></span>
<span data-ttu-id="27591-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="27591-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="27591-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27591-115">-DefaultProfile</span></span>
<span data-ttu-id="27591-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="27591-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27591-117">-Force</span><span class="sxs-lookup"><span data-stu-id="27591-117">-Force</span></span>
<span data-ttu-id="27591-118">Non chiedere conferma se si vuole sovrascrivere una risorsa.</span><span class="sxs-lookup"><span data-stu-id="27591-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="27591-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="27591-119">-Location</span></span>
<span data-ttu-id="27591-120">La posizione.</span><span class="sxs-lookup"><span data-stu-id="27591-120">The location.</span></span>

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

### <span data-ttu-id="27591-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="27591-121">-Name</span></span>
<span data-ttu-id="27591-122">Nome del gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="27591-122">The name of the application security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27591-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27591-123">-ResourceGroupName</span></span>
<span data-ttu-id="27591-124">Il nome del gruppo di risorse del gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="27591-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="27591-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="27591-125">-Tag</span></span>
<span data-ttu-id="27591-126">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="27591-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27591-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="27591-127">-Confirm</span></span>
<span data-ttu-id="27591-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27591-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27591-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27591-129">-WhatIf</span></span>
<span data-ttu-id="27591-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27591-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27591-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27591-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27591-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27591-132">CommonParameters</span></span>
<span data-ttu-id="27591-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27591-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27591-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27591-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27591-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="27591-135">INPUTS</span></span>

### <span data-ttu-id="27591-136">System. String</span><span class="sxs-lookup"><span data-stu-id="27591-136">System.String</span></span>

### <span data-ttu-id="27591-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="27591-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="27591-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27591-138">OUTPUTS</span></span>

### <span data-ttu-id="27591-139">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="27591-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="27591-140">Note</span><span class="sxs-lookup"><span data-stu-id="27591-140">NOTES</span></span>

## <span data-ttu-id="27591-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27591-141">RELATED LINKS</span></span>

[<span data-ttu-id="27591-142">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="27591-142">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)

[<span data-ttu-id="27591-143">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="27591-143">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="27591-144">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="27591-144">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="27591-145">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="27591-145">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="27591-146">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="27591-146">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="27591-147">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="27591-147">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="27591-148">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="27591-148">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="27591-149">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="27591-149">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
