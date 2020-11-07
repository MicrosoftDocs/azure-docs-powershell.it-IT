---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 97a49535ab02b2ccd75a1f7520bcd8a1e3e6264f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687506"
---
# <span data-ttu-id="9b699-101">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9b699-101">New-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="9b699-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9b699-102">SYNOPSIS</span></span>
<span data-ttu-id="9b699-103">Crea un gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b699-103">Creates an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b699-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9b699-104">SYNTAX</span></span>

```
New-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b699-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9b699-105">DESCRIPTION</span></span>
<span data-ttu-id="9b699-106">Il cmdlet **New-AzureRmApplicationSecurityGroup** crea un gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b699-106">The **New-AzureRmApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="9b699-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9b699-107">EXAMPLES</span></span>

### <span data-ttu-id="9b699-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9b699-108">Example 1</span></span>
```
PS C:\> New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="9b699-109">Questo esempio crea un gruppo di sicurezza dell'applicazione senza associazioni.</span><span class="sxs-lookup"><span data-stu-id="9b699-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="9b699-110">Una volta creato, le configurazioni IP nell'interfaccia di rete possono essere incluse nel gruppo.</span><span class="sxs-lookup"><span data-stu-id="9b699-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="9b699-111">Le regole di sicurezza possono anche riferirsi al gruppo come origini o destinazioni.</span><span class="sxs-lookup"><span data-stu-id="9b699-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="9b699-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9b699-112">PARAMETERS</span></span>

### <span data-ttu-id="9b699-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b699-113">-DefaultProfile</span></span>
<span data-ttu-id="9b699-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9b699-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b699-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9b699-115">-Force</span></span>
<span data-ttu-id="9b699-116">Non chiedere conferma se si vuole sovrascrivere una risorsa.</span><span class="sxs-lookup"><span data-stu-id="9b699-116">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="9b699-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="9b699-117">-Location</span></span>
<span data-ttu-id="9b699-118">La posizione.</span><span class="sxs-lookup"><span data-stu-id="9b699-118">The location.</span></span>

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

### <span data-ttu-id="9b699-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="9b699-119">-Name</span></span>
<span data-ttu-id="9b699-120">Nome del gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b699-120">The name of the application security group.</span></span>

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

### <span data-ttu-id="9b699-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b699-121">-ResourceGroupName</span></span>
<span data-ttu-id="9b699-122">Il nome del gruppo di risorse del gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9b699-122">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="9b699-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="9b699-123">-Tag</span></span>
<span data-ttu-id="9b699-124">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="9b699-124">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="9b699-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9b699-125">-Confirm</span></span>
<span data-ttu-id="9b699-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b699-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b699-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b699-127">-WhatIf</span></span>
<span data-ttu-id="9b699-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b699-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b699-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b699-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b699-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b699-130">CommonParameters</span></span>
<span data-ttu-id="9b699-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b699-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b699-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b699-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b699-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9b699-133">INPUTS</span></span>

### <span data-ttu-id="9b699-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9b699-134">System.String</span></span>
<span data-ttu-id="9b699-135">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9b699-135">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9b699-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9b699-136">OUTPUTS</span></span>

### <span data-ttu-id="9b699-137">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9b699-137">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="9b699-138">Note</span><span class="sxs-lookup"><span data-stu-id="9b699-138">NOTES</span></span>

## <span data-ttu-id="9b699-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9b699-139">RELATED LINKS</span></span>

[<span data-ttu-id="9b699-140">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9b699-140">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="9b699-141">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="9b699-141">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="9b699-142">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9b699-142">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="9b699-143">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9b699-143">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="9b699-144">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="9b699-144">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="9b699-145">New-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9b699-145">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="9b699-146">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9b699-146">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="9b699-147">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="9b699-147">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)
