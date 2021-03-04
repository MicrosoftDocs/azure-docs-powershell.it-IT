---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
ms.openlocfilehash: 168a1803781748eb81c3a2087876b2a7b18d9d39
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952173"
---
# <span data-ttu-id="f4e4b-101">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="f4e4b-101">New-AzNatGateway</span></span>

## <span data-ttu-id="f4e4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4e4b-102">SYNOPSIS</span></span>
<span data-ttu-id="f4e4b-103">Creare una nuova risorsa Gateway Nat con le proprietà Indirizzo IP pubblico/Prefisso IP pubblico, IdleTimeoutInMinutes e SKU.</span><span class="sxs-lookup"><span data-stu-id="f4e4b-103">Create new Nat Gateway resource with properties Public Ip Address/Public Ip Prefix, IdleTimeoutInMinutes and Sku.</span></span>

## <span data-ttu-id="f4e4b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4e4b-104">SYNTAX</span></span>

```
New-AzNatGateway -ResourceGroupName <String> -Name <String> [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>]
 [-Sku <String>] [-Location <String>] [-Tag <Hashtable>] [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4e4b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f4e4b-105">DESCRIPTION</span></span>
<span data-ttu-id="f4e4b-106">Il cmdlet **New-AzNatGateway** crea una risorsa gateway Nat.</span><span class="sxs-lookup"><span data-stu-id="f4e4b-106">The **New-AzNatGateway** cmdlet creates a Nat Gateway Resource.</span></span> <span data-ttu-id="f4e4b-107">Un natgateway richiede quanto segue:</span><span class="sxs-lookup"><span data-stu-id="f4e4b-107">A natgateway requires the following:</span></span> 
- <span data-ttu-id="f4e4b-108">Indirizzo IP pubblico e/o prefisso IP pubblico</span><span class="sxs-lookup"><span data-stu-id="f4e4b-108">Public Ip Address and/or Public Ip Prefix</span></span>
- <span data-ttu-id="f4e4b-109">IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="f4e4b-109">IdleTimeoutInMinutes</span></span> 
- <span data-ttu-id="f4e4b-110">SKU</span><span class="sxs-lookup"><span data-stu-id="f4e4b-110">Sku</span></span>
- <span data-ttu-id="f4e4b-111">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4e4b-111">ResourceGroupName</span></span>
- <span data-ttu-id="f4e4b-112">ResourceName</span><span class="sxs-lookup"><span data-stu-id="f4e4b-112">ResourceName</span></span>
- <span data-ttu-id="f4e4b-113">Posizione</span><span class="sxs-lookup"><span data-stu-id="f4e4b-113">Location</span></span>

## <span data-ttu-id="f4e4b-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4e4b-114">EXAMPLES</span></span>

### <span data-ttu-id="f4e4b-115">Esempio 1: Creare un gateway Nat con indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="f4e4b-115">Example 1: Create Nat Gateway with Public Ip Address</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip
```

### <span data-ttu-id="f4e4b-116">Esempio 2: Creare un gateway Nat con prefisso IP pubblico</span><span class="sxs-lookup"><span data-stu-id="f4e4b-116">Example 2: Create Nat Gateway with Public Ip Prefix</span></span>
```powershell
PS C:> $publicipprefix = New-AzPublicIpPrefix -Name "prefix2" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -PrefixLength "31"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpPrefix $publicipprefix
```

### <span data-ttu-id="f4e4b-117">Esempio 3: Creare un gateway Nat con indirizzo IP pubblico nell'area di disponibilità 1</span><span class="sxs-lookup"><span data-stu-id="f4e4b-117">Example 3: Create Nat Gateway with Public IP Address in Availability Zone 1</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip -Zone "1"
```

<span data-ttu-id="f4e4b-118">Il primo comando crea un indirizzo IP pubblico standard.</span><span class="sxs-lookup"><span data-stu-id="f4e4b-118">The first command creates standard Public IP Address.</span></span>
<span data-ttu-id="f4e4b-119">Il secondo comando crea un gateway NAT con indirizzo IP pubblico nell'area di disponibilità 1.</span><span class="sxs-lookup"><span data-stu-id="f4e4b-119">The second command creates NAT Gateway with Public IP Address in Availability Zone 1.</span></span>

## <span data-ttu-id="f4e4b-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4e4b-120">PARAMETERS</span></span>

### <span data-ttu-id="f4e4b-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4e4b-121">-AsJob</span></span>
<span data-ttu-id="f4e4b-122">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f4e4b-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f4e4b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4e4b-123">-DefaultProfile</span></span>
<span data-ttu-id="f4e4b-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f4e4b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4e4b-125">-Force</span><span class="sxs-lookup"><span data-stu-id="f4e4b-125">-Force</span></span>
<span data-ttu-id="f4e4b-126">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="f4e4b-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f4e4b-127">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="f4e4b-127">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="f4e4b-128">Timeout di inattività del gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="f4e4b-128">The idle timeout of the nat gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e4b-129">-Location</span><span class="sxs-lookup"><span data-stu-id="f4e4b-129">-Location</span></span>
<span data-ttu-id="f4e4b-130">Posizione.</span><span class="sxs-lookup"><span data-stu-id="f4e4b-130">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e4b-131">-Name</span><span class="sxs-lookup"><span data-stu-id="f4e4b-131">-Name</span></span>
<span data-ttu-id="f4e4b-132">Nome del gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="f4e4b-132">The name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e4b-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f4e4b-133">-PublicIpAddress</span></span>
<span data-ttu-id="f4e4b-134">Matrice di indirizzi IP pubblici associati alla risorsa gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="f4e4b-134">An array of public ip addresses associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e4b-135">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="f4e4b-135">-PublicIpPrefix</span></span>
<span data-ttu-id="f4e4b-136">Matrice di prefissi IP pubblici associati alla risorsa gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="f4e4b-136">An array of public ip prefixes associated with the nat gateway resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSResourceId[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e4b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4e4b-137">-ResourceGroupName</span></span>
<span data-ttu-id="f4e4b-138">Nome del gruppo di risorse del gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="f4e4b-138">The resource group name of the nat gateway.</span></span>

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

### <span data-ttu-id="f4e4b-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="f4e4b-139">-Sku</span></span>
<span data-ttu-id="f4e4b-140">Nome dello SKU di un gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="f4e4b-140">Name of a NAT gateway SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e4b-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="f4e4b-141">-Tag</span></span>
<span data-ttu-id="f4e4b-142">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="f4e4b-142">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e4b-143">-Zone</span><span class="sxs-lookup"><span data-stu-id="f4e4b-143">-Zone</span></span>
<span data-ttu-id="f4e4b-144">Elenco di aree di disponibilità che denota l'area in cui deve essere distribuito Gateway Nat.</span><span class="sxs-lookup"><span data-stu-id="f4e4b-144">A list of availability zones denoting the zone in which Nat Gateway should be deployed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4e4b-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4e4b-145">-Confirm</span></span>
<span data-ttu-id="f4e4b-146">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4e4b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4e4b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4e4b-147">-WhatIf</span></span>
<span data-ttu-id="f4e4b-148">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4e4b-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4e4b-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4e4b-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4e4b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4e4b-150">CommonParameters</span></span>
<span data-ttu-id="f4e4b-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4e4b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4e4b-152">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f4e4b-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4e4b-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="f4e4b-153">INPUTS</span></span>

### <span data-ttu-id="f4e4b-154">System.String</span><span class="sxs-lookup"><span data-stu-id="f4e4b-154">System.String</span></span>

### <span data-ttu-id="f4e4b-155">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f4e4b-155">System.Int32</span></span>

### <span data-ttu-id="f4e4b-156">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f4e4b-156">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f4e4b-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span><span class="sxs-lookup"><span data-stu-id="f4e4b-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

## <span data-ttu-id="f4e4b-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4e4b-158">OUTPUTS</span></span>

### <span data-ttu-id="f4e4b-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="f4e4b-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="f4e4b-160">NOTE</span><span class="sxs-lookup"><span data-stu-id="f4e4b-160">NOTES</span></span>

## <span data-ttu-id="f4e4b-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4e4b-161">RELATED LINKS</span></span>
