---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationSecurityGroup.md
ms.openlocfilehash: 359b98d19edfdbdd3c1ce8d6ab7286f13cf5dbfa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688394"
---
# <span data-ttu-id="4a062-101">New-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4a062-101">New-AzureRmApplicationSecurityGroup</span></span>

## <span data-ttu-id="4a062-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4a062-102">SYNOPSIS</span></span>
<span data-ttu-id="4a062-103">Crea un gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4a062-103">Creates an application security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a062-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a062-104">SYNTAX</span></span>

```
New-AzureRmApplicationSecurityGroup -ResourceGroupName <String> -Name <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4a062-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a062-105">DESCRIPTION</span></span>
<span data-ttu-id="4a062-106">Il cmdlet **New-AzureRmApplicationSecurityGroup** crea un gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4a062-106">The **New-AzureRmApplicationSecurityGroup** cmdlet creates an application security group.</span></span>

## <span data-ttu-id="4a062-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a062-107">EXAMPLES</span></span>

### <span data-ttu-id="4a062-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4a062-108">Example 1</span></span>
```
PS C:\> New-AzureRmApplicationSecurityGroup -ResourceGroupName "MyResourceGroup" -Name "MyApplicationSecurityGroup" -Location "West US"
```

<span data-ttu-id="4a062-109">Questo esempio crea un gruppo di sicurezza dell'applicazione senza associazioni.</span><span class="sxs-lookup"><span data-stu-id="4a062-109">This example creates an application security group with no associations.</span></span> <span data-ttu-id="4a062-110">Una volta creato, le configurazioni IP nell'interfaccia di rete possono essere incluse nel gruppo.</span><span class="sxs-lookup"><span data-stu-id="4a062-110">Once it is created, IP configurations in the network interface can be included in the group.</span></span> <span data-ttu-id="4a062-111">Le regole di sicurezza possono anche riferirsi al gruppo come origini o destinazioni.</span><span class="sxs-lookup"><span data-stu-id="4a062-111">Security rules may also refer to the group as their sources or destinations.</span></span>

## <span data-ttu-id="4a062-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4a062-112">PARAMETERS</span></span>

### <span data-ttu-id="4a062-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4a062-113">-AsJob</span></span>
<span data-ttu-id="4a062-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="4a062-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4a062-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a062-115">-DefaultProfile</span></span>
<span data-ttu-id="4a062-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4a062-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a062-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4a062-117">-Force</span></span>
<span data-ttu-id="4a062-118">Non chiedere conferma se si vuole sovrascrivere una risorsa.</span><span class="sxs-lookup"><span data-stu-id="4a062-118">Do not ask for confirmation if you want to overwrite a resource.</span></span>

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

### <span data-ttu-id="4a062-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="4a062-119">-Location</span></span>
<span data-ttu-id="4a062-120">La posizione.</span><span class="sxs-lookup"><span data-stu-id="4a062-120">The location.</span></span>

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

### <span data-ttu-id="4a062-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="4a062-121">-Name</span></span>
<span data-ttu-id="4a062-122">Nome del gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4a062-122">The name of the application security group.</span></span>

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

### <span data-ttu-id="4a062-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a062-123">-ResourceGroupName</span></span>
<span data-ttu-id="4a062-124">Il nome del gruppo di risorse del gruppo di sicurezza dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4a062-124">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="4a062-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="4a062-125">-Tag</span></span>
<span data-ttu-id="4a062-126">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="4a062-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="4a062-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4a062-127">-Confirm</span></span>
<span data-ttu-id="4a062-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a062-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a062-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a062-129">-WhatIf</span></span>
<span data-ttu-id="4a062-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a062-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a062-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4a062-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a062-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a062-132">CommonParameters</span></span>
<span data-ttu-id="4a062-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a062-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a062-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a062-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a062-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4a062-135">INPUTS</span></span>

### <span data-ttu-id="4a062-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4a062-136">System.String</span></span>

### <span data-ttu-id="4a062-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4a062-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4a062-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a062-138">OUTPUTS</span></span>

### <span data-ttu-id="4a062-139">Microsoft. Azure. Commands. Network. Models. PSApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4a062-139">Microsoft.Azure.Commands.Network.Models.PSApplicationSecurityGroup</span></span>

## <span data-ttu-id="4a062-140">Note</span><span class="sxs-lookup"><span data-stu-id="4a062-140">NOTES</span></span>

## <span data-ttu-id="4a062-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a062-141">RELATED LINKS</span></span>

[<span data-ttu-id="4a062-142">Get-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4a062-142">Get-AzureRmApplicationSecurityGroup</span></span>](./Get-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="4a062-143">Remove-AzureRmApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4a062-143">Remove-AzureRmApplicationSecurityGroup</span></span>](./Remove-AzureRmApplicationSecurityGroup.md)

[<span data-ttu-id="4a062-144">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4a062-144">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="4a062-145">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4a062-145">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="4a062-146">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4a062-146">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="4a062-147">New-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4a062-147">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="4a062-148">Add-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4a062-148">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="4a062-149">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="4a062-149">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)
