---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
ms.openlocfilehash: 231a4f9622aa9fecf0c6d832e5f7602da1bed1b1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187023"
---
# <span data-ttu-id="cd9c2-101">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="cd9c2-101">New-AzPublicIpPrefix</span></span>

## <span data-ttu-id="cd9c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd9c2-102">SYNOPSIS</span></span>
<span data-ttu-id="cd9c2-103">Crea un prefisso IP pubblico</span><span class="sxs-lookup"><span data-stu-id="cd9c2-103">Creates a Public IP Prefix</span></span>

## <span data-ttu-id="cd9c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd9c2-104">SYNTAX</span></span>

```
New-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 [-Tier <String>] -PrefixLength <UInt16> [-IpAddressVersion <String>] [-IpTag <PSPublicIpPrefixTag[]>]
 [-Zone <String[]>] [-CustomIpPrefix <PSCustomIpPrefix>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd9c2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cd9c2-105">DESCRIPTION</span></span>
<span data-ttu-id="cd9c2-106">Il cmdlet **New-AzPublicIpPrefix crea** un prefisso IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="cd9c2-106">The **New-AzPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="cd9c2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd9c2-107">EXAMPLES</span></span>

### <span data-ttu-id="cd9c2-108">Esempio 1: Creare un nuovo prefisso IP pubblico</span><span class="sxs-lookup"><span data-stu-id="cd9c2-108">Example 1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="cd9c2-109">Questo comando crea una nuova risorsa prefisso IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="cd9c2-109">This command creates a new public IP prefix resource.</span></span> 

### <span data-ttu-id="cd9c2-110">Esempio 2: Creare un nuovo prefisso IP pubblico globale</span><span class="sxs-lookup"><span data-stu-id="cd9c2-110">Example 2: Create a new global public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -ResourceGroupName $rgname -name $rname -location $location -Tier Global -PrefixLength 30
```

<span data-ttu-id="cd9c2-111">Questo comando crea una nuova risorsa prefisso IP pubblico globale.</span><span class="sxs-lookup"><span data-stu-id="cd9c2-111">This command creates a new global public IP prefix resource.</span></span> 

## <span data-ttu-id="cd9c2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd9c2-112">PARAMETERS</span></span>

### <span data-ttu-id="cd9c2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd9c2-113">-AsJob</span></span>
<span data-ttu-id="cd9c2-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="cd9c2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd9c2-115">-CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="cd9c2-115">-CustomIpPrefix</span></span>
<span data-ttu-id="cd9c2-116">Lo strumento CustomIpPrefix a cui verrà associato questo publicipPrefix</span><span class="sxs-lookup"><span data-stu-id="cd9c2-116">The CustomIpPrefix that this PublicIpPrefix will be associated with</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd9c2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd9c2-117">-DefaultProfile</span></span>
<span data-ttu-id="cd9c2-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cd9c2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd9c2-119">-Force</span><span class="sxs-lookup"><span data-stu-id="cd9c2-119">-Force</span></span>
<span data-ttu-id="cd9c2-120">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="cd9c2-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="cd9c2-121">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="cd9c2-121">-IpAddressVersion</span></span>
<span data-ttu-id="cd9c2-122">Versione dell'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="cd9c2-122">The public IP address version.</span></span>

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

### <span data-ttu-id="cd9c2-123">-IpTag</span><span class="sxs-lookup"><span data-stu-id="cd9c2-123">-IpTag</span></span>
<span data-ttu-id="cd9c2-124">Elenco IpTag.</span><span class="sxs-lookup"><span data-stu-id="cd9c2-124">IpTag List.</span></span>

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

### <span data-ttu-id="cd9c2-125">-Location</span><span class="sxs-lookup"><span data-stu-id="cd9c2-125">-Location</span></span>
<span data-ttu-id="cd9c2-126">Posizione del prefisso IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="cd9c2-126">The public IP prefix location.</span></span>

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

### <span data-ttu-id="cd9c2-127">-Name</span><span class="sxs-lookup"><span data-stu-id="cd9c2-127">-Name</span></span>
<span data-ttu-id="cd9c2-128">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="cd9c2-128">The resource name.</span></span>

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

### <span data-ttu-id="cd9c2-129">-PrefixLength</span><span class="sxs-lookup"><span data-stu-id="cd9c2-129">-PrefixLength</span></span>
<span data-ttu-id="cd9c2-130">Lunghezza di PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="cd9c2-130">The PublicIPPrefix length</span></span>

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

### <span data-ttu-id="cd9c2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd9c2-131">-ResourceGroupName</span></span>
<span data-ttu-id="cd9c2-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cd9c2-132">The resource group name.</span></span>

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

### <span data-ttu-id="cd9c2-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="cd9c2-133">-Sku</span></span>
<span data-ttu-id="cd9c2-134">Nome SKU prefisso IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="cd9c2-134">The public IP Prefix Sku name.</span></span>

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

### <span data-ttu-id="cd9c2-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="cd9c2-135">-Tag</span></span>
<span data-ttu-id="cd9c2-136">Tabella hash che rappresenta i tag di risorsa.</span><span class="sxs-lookup"><span data-stu-id="cd9c2-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="cd9c2-137">-Livello</span><span class="sxs-lookup"><span data-stu-id="cd9c2-137">-Tier</span></span>
<span data-ttu-id="cd9c2-138">Livello SKU prefisso IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="cd9c2-138">The public IP Prefix Sku tier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Regional, Global

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd9c2-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="cd9c2-139">-Zone</span></span>
<span data-ttu-id="cd9c2-140">Elenco di aree di disponibilità che denota l'indirizzo IP allocato per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="cd9c2-140">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="cd9c2-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd9c2-141">-Confirm</span></span>
<span data-ttu-id="cd9c2-142">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd9c2-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd9c2-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd9c2-143">-WhatIf</span></span>
<span data-ttu-id="cd9c2-144">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd9c2-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd9c2-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd9c2-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd9c2-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd9c2-146">CommonParameters</span></span>
<span data-ttu-id="cd9c2-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd9c2-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd9c2-148">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cd9c2-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd9c2-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="cd9c2-149">INPUTS</span></span>

### <span data-ttu-id="cd9c2-150">System.String</span><span class="sxs-lookup"><span data-stu-id="cd9c2-150">System.String</span></span>

### <span data-ttu-id="cd9c2-151">System.UInt16</span><span class="sxs-lookup"><span data-stu-id="cd9c2-151">System.UInt16</span></span>

### <span data-ttu-id="cd9c2-152">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span><span class="sxs-lookup"><span data-stu-id="cd9c2-152">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span></span>

### <span data-ttu-id="cd9c2-153">System.String[]</span><span class="sxs-lookup"><span data-stu-id="cd9c2-153">System.String[]</span></span>

### <span data-ttu-id="cd9c2-154">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="cd9c2-154">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cd9c2-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd9c2-155">OUTPUTS</span></span>

### <span data-ttu-id="cd9c2-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="cd9c2-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="cd9c2-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="cd9c2-157">NOTES</span></span>

## <span data-ttu-id="cd9c2-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd9c2-158">RELATED LINKS</span></span>

[<span data-ttu-id="cd9c2-159">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="cd9c2-159">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="cd9c2-160">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="cd9c2-160">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="cd9c2-161">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="cd9c2-161">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
