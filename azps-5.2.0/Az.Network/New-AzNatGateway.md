---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNatGateway.md
ms.openlocfilehash: 0855ba4e7e16503045d13c370838cd5d3fffb033
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344815"
---
# <span data-ttu-id="6b27c-101">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="6b27c-101">New-AzNatGateway</span></span>

## <span data-ttu-id="6b27c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6b27c-102">SYNOPSIS</span></span>
<span data-ttu-id="6b27c-103">Creare una nuova risorsa gateway NAT con le proprietà indirizzo IP pubblico/prefisso IP pubblico, IdleTimeoutInMinutes e SKU.</span><span class="sxs-lookup"><span data-stu-id="6b27c-103">Create new Nat Gateway resource with properties Public Ip Address/Public Ip Prefix, IdleTimeoutInMinutes and Sku.</span></span>

## <span data-ttu-id="6b27c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6b27c-104">SYNTAX</span></span>

```
New-AzNatGateway -ResourceGroupName <String> -Name <String> [-IdleTimeoutInMinutes <Int32>] [-Zone <String[]>]
 [-Sku <String>] [-Location <String>] [-Tag <Hashtable>] [-PublicIpAddress <PSResourceId[]>]
 [-PublicIpPrefix <PSResourceId[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b27c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b27c-105">DESCRIPTION</span></span>
<span data-ttu-id="6b27c-106">Il cmdlet **New-AzNatGateway** crea una risorsa gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="6b27c-106">The **New-AzNatGateway** cmdlet creates a Nat Gateway Resource.</span></span> <span data-ttu-id="6b27c-107">Un natgateway richiede le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="6b27c-107">A natgateway requires the following:</span></span> 
- <span data-ttu-id="6b27c-108">Indirizzo IP pubblico e/o prefisso IP pubblico</span><span class="sxs-lookup"><span data-stu-id="6b27c-108">Public Ip Address and/or Public Ip Prefix</span></span>
- <span data-ttu-id="6b27c-109">IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="6b27c-109">IdleTimeoutInMinutes</span></span> 
- <span data-ttu-id="6b27c-110">SKU</span><span class="sxs-lookup"><span data-stu-id="6b27c-110">Sku</span></span>
- <span data-ttu-id="6b27c-111">ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b27c-111">ResourceGroupName</span></span>
- <span data-ttu-id="6b27c-112">ResourceName</span><span class="sxs-lookup"><span data-stu-id="6b27c-112">ResourceName</span></span>
- <span data-ttu-id="6b27c-113">Posizione</span><span class="sxs-lookup"><span data-stu-id="6b27c-113">Location</span></span>

## <span data-ttu-id="6b27c-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6b27c-114">EXAMPLES</span></span>

### <span data-ttu-id="6b27c-115">Esempio 1: creare un gateway NAT con l'indirizzo IP pubblico</span><span class="sxs-lookup"><span data-stu-id="6b27c-115">Example 1: Create Nat Gateway with Public Ip Address</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip
```

### <span data-ttu-id="6b27c-116">Esempio 2: creare un gateway NAT con il prefisso IP pubblico</span><span class="sxs-lookup"><span data-stu-id="6b27c-116">Example 2: Create Nat Gateway with Public Ip Prefix</span></span>
```powershell
PS C:> $publicipprefix = New-AzPublicIpPrefix -Name "prefix2" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -PrefixLength "31"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpPrefix $publicipprefix
```

### <span data-ttu-id="6b27c-117">Esempio 3: creare un gateway NAT con l'indirizzo IP pubblico nella zona di disponibilità 1</span><span class="sxs-lookup"><span data-stu-id="6b27c-117">Example 3: Create Nat Gateway with Public IP Address in Availability Zone 1</span></span>
```powershell
PS C:> $pip = New-AzPublicIpAddress -Name "pip" -ResourceGroupName "natgateway_test" -Location "eastus2" -Sku "Standard" -IdleTimeoutInMinutes 4 -AllocationMethod "static"
PS C:> $natgateway = New-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway" -IdleTimeoutInMinutes 4 -Sku "Standard" -Location "eastus2" -PublicIpAddress $pip -Zone "1"
```

<span data-ttu-id="6b27c-118">Il primo comando crea l'indirizzo IP pubblico standard.</span><span class="sxs-lookup"><span data-stu-id="6b27c-118">The first command creates standard Public IP Address.</span></span>
<span data-ttu-id="6b27c-119">Il secondo comando crea il gateway NAT con l'indirizzo IP pubblico nella zona di disponibilità 1.</span><span class="sxs-lookup"><span data-stu-id="6b27c-119">The second command creates NAT Gateway with Public IP Address in Availability Zone 1.</span></span>

## <span data-ttu-id="6b27c-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6b27c-120">PARAMETERS</span></span>

### <span data-ttu-id="6b27c-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b27c-121">-AsJob</span></span>
<span data-ttu-id="6b27c-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6b27c-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6b27c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b27c-123">-DefaultProfile</span></span>
<span data-ttu-id="6b27c-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6b27c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b27c-125">-Force</span><span class="sxs-lookup"><span data-stu-id="6b27c-125">-Force</span></span>
<span data-ttu-id="6b27c-126">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="6b27c-126">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="6b27c-127">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="6b27c-127">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="6b27c-128">Timeout inattivo del gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="6b27c-128">The idle timeout of the nat gateway.</span></span>

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

### <span data-ttu-id="6b27c-129">-Posizione</span><span class="sxs-lookup"><span data-stu-id="6b27c-129">-Location</span></span>
<span data-ttu-id="6b27c-130">La posizione.</span><span class="sxs-lookup"><span data-stu-id="6b27c-130">The location.</span></span>

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

### <span data-ttu-id="6b27c-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="6b27c-131">-Name</span></span>
<span data-ttu-id="6b27c-132">Nome del gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="6b27c-132">The name of the nat gateway.</span></span>

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

### <span data-ttu-id="6b27c-133">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6b27c-133">-PublicIpAddress</span></span>
<span data-ttu-id="6b27c-134">Matrice di indirizzi IP pubblici associata alla risorsa gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="6b27c-134">An array of public ip addresses associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="6b27c-135">-PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="6b27c-135">-PublicIpPrefix</span></span>
<span data-ttu-id="6b27c-136">Matrice di prefissi IP pubblici associata alla risorsa gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="6b27c-136">An array of public ip prefixes associated with the nat gateway resource.</span></span>

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

### <span data-ttu-id="6b27c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b27c-137">-ResourceGroupName</span></span>
<span data-ttu-id="6b27c-138">Nome del gruppo di risorse del gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="6b27c-138">The resource group name of the nat gateway.</span></span>

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

### <span data-ttu-id="6b27c-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="6b27c-139">-Sku</span></span>
<span data-ttu-id="6b27c-140">Nome di un SKU del gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="6b27c-140">Name of a NAT gateway SKU.</span></span>

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

### <span data-ttu-id="6b27c-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="6b27c-141">-Tag</span></span>
<span data-ttu-id="6b27c-142">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="6b27c-142">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="6b27c-143">-Zona</span><span class="sxs-lookup"><span data-stu-id="6b27c-143">-Zone</span></span>
<span data-ttu-id="6b27c-144">Elenco di aree di disponibilità che indica la zona in cui deve essere distribuito il gateway NAT.</span><span class="sxs-lookup"><span data-stu-id="6b27c-144">A list of availability zones denoting the zone in which Nat Gateway should be deployed.</span></span>

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

### <span data-ttu-id="6b27c-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6b27c-145">-Confirm</span></span>
<span data-ttu-id="6b27c-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b27c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b27c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b27c-147">-WhatIf</span></span>
<span data-ttu-id="6b27c-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b27c-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b27c-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b27c-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b27c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b27c-150">CommonParameters</span></span>
<span data-ttu-id="6b27c-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b27c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b27c-152">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b27c-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b27c-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6b27c-153">INPUTS</span></span>

### <span data-ttu-id="6b27c-154">System. String</span><span class="sxs-lookup"><span data-stu-id="6b27c-154">System.String</span></span>

### <span data-ttu-id="6b27c-155">System. Int32</span><span class="sxs-lookup"><span data-stu-id="6b27c-155">System.Int32</span></span>

### <span data-ttu-id="6b27c-156">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6b27c-156">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6b27c-157">Microsoft. Azure. Commands. Network. Models. PSResourceId []</span><span class="sxs-lookup"><span data-stu-id="6b27c-157">Microsoft.Azure.Commands.Network.Models.PSResourceId[]</span></span>

## <span data-ttu-id="6b27c-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6b27c-158">OUTPUTS</span></span>

### <span data-ttu-id="6b27c-159">Microsoft. Azure. Commands. Network. Models. PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="6b27c-159">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="6b27c-160">Note</span><span class="sxs-lookup"><span data-stu-id="6b27c-160">NOTES</span></span>

## <span data-ttu-id="6b27c-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6b27c-161">RELATED LINKS</span></span>
