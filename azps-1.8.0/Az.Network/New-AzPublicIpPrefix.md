---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
ms.openlocfilehash: 6ee4f046281a36f0d0da798f1954a29f8d98d9c5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678245"
---
# <span data-ttu-id="47248-101">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="47248-101">New-AzPublicIpPrefix</span></span>

## <span data-ttu-id="47248-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="47248-102">SYNOPSIS</span></span>
<span data-ttu-id="47248-103">Crea un prefisso IP pubblico</span><span class="sxs-lookup"><span data-stu-id="47248-103">Creates a Public IP Prefix</span></span>

## <span data-ttu-id="47248-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="47248-104">SYNTAX</span></span>

```
New-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -PrefixLength <UInt16> [-IpAddressVersion <String>] [-IpTag <PSPublicIpPrefixTag[]>] [-Zone <String[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="47248-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47248-105">DESCRIPTION</span></span>
<span data-ttu-id="47248-106">Il cmdlet **New-AzPublicIpPrefix** crea un prefisso IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="47248-106">The **New-AzPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="47248-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="47248-107">EXAMPLES</span></span>

### <span data-ttu-id="47248-108">1: creare un nuovo prefisso IP pubblico</span><span class="sxs-lookup"><span data-stu-id="47248-108">1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="47248-109">Questo comando crea una nuova risorsa di prefisso IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="47248-109">This command creates a new public IP prefix resource.</span></span> 

## <span data-ttu-id="47248-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="47248-110">PARAMETERS</span></span>

### <span data-ttu-id="47248-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47248-111">-AsJob</span></span>
<span data-ttu-id="47248-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="47248-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47248-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47248-113">-DefaultProfile</span></span>
<span data-ttu-id="47248-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="47248-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47248-115">-Force</span><span class="sxs-lookup"><span data-stu-id="47248-115">-Force</span></span>
<span data-ttu-id="47248-116">Non chiedere conferma se si vuole usare una risorsa per un sovrarito</span><span class="sxs-lookup"><span data-stu-id="47248-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="47248-117">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="47248-117">-IpAddressVersion</span></span>
<span data-ttu-id="47248-118">Versione dell'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="47248-118">The public IP address version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47248-119">-IpTag</span><span class="sxs-lookup"><span data-stu-id="47248-119">-IpTag</span></span>
<span data-ttu-id="47248-120">Elenco IpTag.</span><span class="sxs-lookup"><span data-stu-id="47248-120">IpTag List.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47248-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="47248-121">-Location</span></span>
<span data-ttu-id="47248-122">Posizione del prefisso IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="47248-122">The public IP prefix location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47248-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="47248-123">-Name</span></span>
<span data-ttu-id="47248-124">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="47248-124">The resource name.</span></span>

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

### <span data-ttu-id="47248-125">-LunghezzaPrefisso</span><span class="sxs-lookup"><span data-stu-id="47248-125">-PrefixLength</span></span>
<span data-ttu-id="47248-126">La lunghezza di PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="47248-126">The PublicIPPrefix length</span></span>

```yaml
Type: System.UInt16
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47248-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47248-127">-ResourceGroupName</span></span>
<span data-ttu-id="47248-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="47248-128">The resource group name.</span></span>

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

### <span data-ttu-id="47248-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="47248-129">-Sku</span></span>
<span data-ttu-id="47248-130">Nome USK del prefisso IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="47248-130">The public IP Prefix Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47248-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="47248-131">-Tag</span></span>
<span data-ttu-id="47248-132">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="47248-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="47248-133">-Zona</span><span class="sxs-lookup"><span data-stu-id="47248-133">-Zone</span></span>
<span data-ttu-id="47248-134">Elenco delle aree di disponibilità che indicano che l'IP allocato per la risorsa deve provenire.</span><span class="sxs-lookup"><span data-stu-id="47248-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47248-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="47248-135">-Confirm</span></span>
<span data-ttu-id="47248-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47248-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47248-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47248-137">-WhatIf</span></span>
<span data-ttu-id="47248-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47248-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47248-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47248-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47248-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47248-140">CommonParameters</span></span>
<span data-ttu-id="47248-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47248-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47248-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47248-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47248-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="47248-143">INPUTS</span></span>

### <span data-ttu-id="47248-144">System. String</span><span class="sxs-lookup"><span data-stu-id="47248-144">System.String</span></span>

### <span data-ttu-id="47248-145">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="47248-145">System.UInt16</span></span>

### <span data-ttu-id="47248-146">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefixTag []</span><span class="sxs-lookup"><span data-stu-id="47248-146">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span></span>

### <span data-ttu-id="47248-147">System. String []</span><span class="sxs-lookup"><span data-stu-id="47248-147">System.String[]</span></span>

### <span data-ttu-id="47248-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="47248-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="47248-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="47248-149">OUTPUTS</span></span>

### <span data-ttu-id="47248-150">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="47248-150">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="47248-151">Note</span><span class="sxs-lookup"><span data-stu-id="47248-151">NOTES</span></span>

## <span data-ttu-id="47248-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="47248-152">RELATED LINKS</span></span>

[<span data-ttu-id="47248-153">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="47248-153">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="47248-154">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="47248-154">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="47248-155">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="47248-155">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
