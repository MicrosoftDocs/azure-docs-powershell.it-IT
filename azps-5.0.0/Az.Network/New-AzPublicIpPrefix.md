---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpPrefix.md
ms.openlocfilehash: cc00afb5dcdd4cc11c61cf96f2ae8ac3bb201bb5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193931"
---
# <span data-ttu-id="99e8f-101">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="99e8f-101">New-AzPublicIpPrefix</span></span>

## <span data-ttu-id="99e8f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="99e8f-102">SYNOPSIS</span></span>
<span data-ttu-id="99e8f-103">Crea un prefisso IP pubblico</span><span class="sxs-lookup"><span data-stu-id="99e8f-103">Creates a Public IP Prefix</span></span>

## <span data-ttu-id="99e8f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99e8f-104">SYNTAX</span></span>

```
New-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Location <String>] [-Sku <String>]
 -PrefixLength <UInt16> [-IpAddressVersion <String>] [-IpTag <PSPublicIpPrefixTag[]>] [-Zone <String[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="99e8f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99e8f-105">DESCRIPTION</span></span>
<span data-ttu-id="99e8f-106">Il cmdlet **New-AzPublicIpPrefix** crea un prefisso IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="99e8f-106">The **New-AzPublicIpPrefix** cmdlet creates a public IP prefix.</span></span>

## <span data-ttu-id="99e8f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99e8f-107">EXAMPLES</span></span>

### <span data-ttu-id="99e8f-108">Esempio 1: creare un nuovo prefisso IP pubblico</span><span class="sxs-lookup"><span data-stu-id="99e8f-108">Example 1: Create a new public Ip prefix</span></span>
```powershell
PS C:\> $publicIpPrefix = New-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName -PrefixLength 30
```

<span data-ttu-id="99e8f-109">Questo comando crea una nuova risorsa di prefisso IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="99e8f-109">This command creates a new public IP prefix resource.</span></span> 

## <span data-ttu-id="99e8f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="99e8f-110">PARAMETERS</span></span>

### <span data-ttu-id="99e8f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="99e8f-111">-AsJob</span></span>
<span data-ttu-id="99e8f-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="99e8f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="99e8f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99e8f-113">-DefaultProfile</span></span>
<span data-ttu-id="99e8f-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="99e8f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99e8f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="99e8f-115">-Force</span></span>
<span data-ttu-id="99e8f-116">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="99e8f-116">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="99e8f-117">-IpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="99e8f-117">-IpAddressVersion</span></span>
<span data-ttu-id="99e8f-118">Versione dell'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="99e8f-118">The public IP address version.</span></span>

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

### <span data-ttu-id="99e8f-119">-IpTag</span><span class="sxs-lookup"><span data-stu-id="99e8f-119">-IpTag</span></span>
<span data-ttu-id="99e8f-120">Elenco IpTag.</span><span class="sxs-lookup"><span data-stu-id="99e8f-120">IpTag List.</span></span>

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

### <span data-ttu-id="99e8f-121">-Posizione</span><span class="sxs-lookup"><span data-stu-id="99e8f-121">-Location</span></span>
<span data-ttu-id="99e8f-122">Posizione del prefisso IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="99e8f-122">The public IP prefix location.</span></span>

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

### <span data-ttu-id="99e8f-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="99e8f-123">-Name</span></span>
<span data-ttu-id="99e8f-124">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="99e8f-124">The resource name.</span></span>

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

### <span data-ttu-id="99e8f-125">-LunghezzaPrefisso</span><span class="sxs-lookup"><span data-stu-id="99e8f-125">-PrefixLength</span></span>
<span data-ttu-id="99e8f-126">La lunghezza di PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="99e8f-126">The PublicIPPrefix length</span></span>

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

### <span data-ttu-id="99e8f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99e8f-127">-ResourceGroupName</span></span>
<span data-ttu-id="99e8f-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="99e8f-128">The resource group name.</span></span>

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

### <span data-ttu-id="99e8f-129">-SKU</span><span class="sxs-lookup"><span data-stu-id="99e8f-129">-Sku</span></span>
<span data-ttu-id="99e8f-130">Nome USK del prefisso IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="99e8f-130">The public IP Prefix Sku name.</span></span>

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

### <span data-ttu-id="99e8f-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="99e8f-131">-Tag</span></span>
<span data-ttu-id="99e8f-132">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="99e8f-132">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="99e8f-133">-Zona</span><span class="sxs-lookup"><span data-stu-id="99e8f-133">-Zone</span></span>
<span data-ttu-id="99e8f-134">Elenco delle aree di disponibilità che indicano che l'IP allocato per la risorsa deve provenire.</span><span class="sxs-lookup"><span data-stu-id="99e8f-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="99e8f-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="99e8f-135">-Confirm</span></span>
<span data-ttu-id="99e8f-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99e8f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99e8f-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99e8f-137">-WhatIf</span></span>
<span data-ttu-id="99e8f-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99e8f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99e8f-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99e8f-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99e8f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99e8f-140">CommonParameters</span></span>
<span data-ttu-id="99e8f-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99e8f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99e8f-142">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99e8f-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99e8f-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="99e8f-143">INPUTS</span></span>

### <span data-ttu-id="99e8f-144">System. String</span><span class="sxs-lookup"><span data-stu-id="99e8f-144">System.String</span></span>

### <span data-ttu-id="99e8f-145">System. UInt16</span><span class="sxs-lookup"><span data-stu-id="99e8f-145">System.UInt16</span></span>

### <span data-ttu-id="99e8f-146">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefixTag []</span><span class="sxs-lookup"><span data-stu-id="99e8f-146">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefixTag[]</span></span>

### <span data-ttu-id="99e8f-147">System. String []</span><span class="sxs-lookup"><span data-stu-id="99e8f-147">System.String[]</span></span>

### <span data-ttu-id="99e8f-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="99e8f-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="99e8f-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99e8f-149">OUTPUTS</span></span>

### <span data-ttu-id="99e8f-150">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="99e8f-150">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="99e8f-151">Note</span><span class="sxs-lookup"><span data-stu-id="99e8f-151">NOTES</span></span>

## <span data-ttu-id="99e8f-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99e8f-152">RELATED LINKS</span></span>

[<span data-ttu-id="99e8f-153">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="99e8f-153">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="99e8f-154">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="99e8f-154">Remove-AzPublicIpPrefix</span></span>](./Remove-AzPublicIpPrefix.md)

[<span data-ttu-id="99e8f-155">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="99e8f-155">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
