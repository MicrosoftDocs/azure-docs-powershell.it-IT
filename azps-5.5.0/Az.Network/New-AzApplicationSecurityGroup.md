---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationSecurityGroup.md
ms.openlocfilehash: 32d7767ac5bd43be8fb9a3129966a0a88d761953
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179719"
---
# <span data-ttu-id="14da0-101">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="14da0-101">New-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="14da0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14da0-102">SYNOPSIS</span></span>
<span data-ttu-id="14da0-103">Crea un gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="14da0-103">Creates an application security group.</span></span>

## <span data-ttu-id="14da0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14da0-104">SYNTAX</span></span>

```
New-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14da0-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="14da0-105">DESCRIPTION</span></span>
<span data-ttu-id="14da0-106">Il cmdlet **New-AzApplicationSecurityGroup** crea un gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="14da0-106">The **New-AzApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="14da0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14da0-107">EXAMPLES</span></span>

### <span data-ttu-id="14da0-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="14da0-108">Example 1</span></span>
```
PS C:\> New-AzApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="14da0-109">Questo esempio crea un gruppo di sicurezza dell'applicazione senza associazioni.</span><span class="sxs-lookup"><span data-stu-id="14da0-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="14da0-110">Dopo la creazione, le configurazioni IP nell'interfaccia di rete possono essere incluse nel gruppo.</span><span class="sxs-lookup"><span data-stu-id="14da0-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="14da0-111">Le regole di sicurezza possono anche fare riferimento al gruppo come origini o destinazioni.</span><span class="sxs-lookup"><span data-stu-id="14da0-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="14da0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14da0-112">PARAMETERS</span></span>

### <span data-ttu-id="14da0-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14da0-113">-AsJob</span></span>
<span data-ttu-id="14da0-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="14da0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14da0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14da0-115">-DefaultProfile</span></span>
<span data-ttu-id="14da0-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="14da0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14da0-117">-Force</span><span class="sxs-lookup"><span data-stu-id="14da0-117">-Force</span></span>
<span data-ttu-id="14da0-118">Non chiedere conferma se si vuole sovrascrivere una risorsa.</span><span class="sxs-lookup"><span data-stu-id="14da0-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="14da0-119">-Location</span><span class="sxs-lookup"><span data-stu-id="14da0-119">-Location</span></span>
<span data-ttu-id="14da0-120">Posizione.</span><span class="sxs-lookup"><span data-stu-id="14da0-120">The location.</span></span>

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

### <span data-ttu-id="14da0-121">-Name</span><span class="sxs-lookup"><span data-stu-id="14da0-121">-Name</span></span>
<span data-ttu-id="14da0-122">Nome del gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="14da0-122">The name of the application security group.</span></span>

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

### <span data-ttu-id="14da0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14da0-123">-ResourceGroupName</span></span>
<span data-ttu-id="14da0-124">Nome del gruppo di risorse del gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="14da0-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="14da0-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="14da0-125">-Tag</span></span>
<span data-ttu-id="14da0-126">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="14da0-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="14da0-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14da0-127">-Confirm</span></span>
<span data-ttu-id="14da0-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14da0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14da0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14da0-129">-WhatIf</span></span>
<span data-ttu-id="14da0-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14da0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14da0-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14da0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14da0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14da0-132">CommonParameters</span></span>
<span data-ttu-id="14da0-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14da0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14da0-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14da0-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14da0-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="14da0-135">INPUTS</span></span>

### <span data-ttu-id="14da0-136">System.String</span><span class="sxs-lookup"><span data-stu-id="14da0-136">System.String</span></span>

### <span data-ttu-id="14da0-137">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="14da0-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="14da0-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14da0-138">OUTPUTS</span></span>

### <span data-ttu-id="14da0-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="14da0-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="14da0-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="14da0-140">NOTES</span></span>

## <span data-ttu-id="14da0-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14da0-141">RELATED LINKS</span></span>

[<span data-ttu-id="14da0-142">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="14da0-142">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)

[<span data-ttu-id="14da0-143">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="14da0-143">Remove-AzApplicationSecurityGroup</span></span>](./Remove-AzApplicationSecurityGroup.md)

[<span data-ttu-id="14da0-144">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="14da0-144">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="14da0-145">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="14da0-145">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="14da0-146">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="14da0-146">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="14da0-147">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="14da0-147">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="14da0-148">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="14da0-148">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="14da0-149">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="14da0-149">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
