---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpAllocation.md
ms.openlocfilehash: 9a6c84c0ff5d22a4f6c6038266598c6adfe19b29
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379105"
---
# <span data-ttu-id="984ed-101">New-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="984ed-101">New-AzIpAllocation</span></span>

## <span data-ttu-id="984ed-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="984ed-102">SYNOPSIS</span></span>
<span data-ttu-id="984ed-103">Crea un IpAllocation di Azure.</span><span class="sxs-lookup"><span data-stu-id="984ed-103">Creates an Azure IpAllocation.</span></span>

## <span data-ttu-id="984ed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="984ed-104">SYNTAX</span></span>

```
New-AzIpAllocation -Name <String> -ResourceGroupName <String> -Location <String>
 -IpAllocationType <String> [-Prefix <String>] [-PrefixLength <Int32>] [-PrefixType <String>]
 [-IpamAllocationId <String>] [-IpAllocationTag <Hashtable>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="984ed-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="984ed-105">DESCRIPTION</span></span>
<span data-ttu-id="984ed-106">Il cmdlet **New-AzIpAllocation** crea un IpAllocation di Azure</span><span class="sxs-lookup"><span data-stu-id="984ed-106">The **New-AzIpAllocation** cmdlet creates an Azure IpAllocation</span></span>

## <span data-ttu-id="984ed-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="984ed-107">EXAMPLES</span></span>

### <span data-ttu-id="984ed-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="984ed-108">Example 1</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -Prefix '1.2.3.4/32' -IpAllocationTag @{"VnetId"="vnet1"}
```

### <span data-ttu-id="984ed-109">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="984ed-109">Example 2</span></span>
```powershell
New-AzIpAllocation -ResourceName 'TestIpAllocation'  -ResourceGroupName 'TestResourcegroupName' -Location 'eastus' -IpAllocationType 'Hypernet' -PrefixLength 32 -PrefixType 'ipv4' -IpAllocationTag @{"VnetId"="vnet1"}
```

## <span data-ttu-id="984ed-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="984ed-110">PARAMETERS</span></span>

### <span data-ttu-id="984ed-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="984ed-111">-AsJob</span></span>
<span data-ttu-id="984ed-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="984ed-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="984ed-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="984ed-113">-DefaultProfile</span></span>
<span data-ttu-id="984ed-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="984ed-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="984ed-115">-Force</span><span class="sxs-lookup"><span data-stu-id="984ed-115">-Force</span></span>
<span data-ttu-id="984ed-116">Non chiedere conferma se si vuole eseguire l'override di una risorsa</span><span class="sxs-lookup"><span data-stu-id="984ed-116">Do not ask for confirmation if you want to override a resource</span></span>

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

### <span data-ttu-id="984ed-117">-IpAllocationTag</span><span class="sxs-lookup"><span data-stu-id="984ed-117">-IpAllocationTag</span></span>
<span data-ttu-id="984ed-118">Tag di allocazione dell'allocazione IP</span><span class="sxs-lookup"><span data-stu-id="984ed-118">The allocation tags of the IP allocation</span></span>

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

### <span data-ttu-id="984ed-119">-IpAllocationType</span><span class="sxs-lookup"><span data-stu-id="984ed-119">-IpAllocationType</span></span>
<span data-ttu-id="984ed-120">Tipo di allocazione IP</span><span class="sxs-lookup"><span data-stu-id="984ed-120">The type of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hypernet, Undefined

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="984ed-121">-IpamAllocationId</span><span class="sxs-lookup"><span data-stu-id="984ed-121">-IpamAllocationId</span></span>
<span data-ttu-id="984ed-122">ID di allocazione IPAM dell'allocazione IP</span><span class="sxs-lookup"><span data-stu-id="984ed-122">The ipam allocation ID of the IP allocation</span></span>

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

### <span data-ttu-id="984ed-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="984ed-123">-Location</span></span>
<span data-ttu-id="984ed-124">posizione.</span><span class="sxs-lookup"><span data-stu-id="984ed-124">location.</span></span>

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

### <span data-ttu-id="984ed-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="984ed-125">-Name</span></span>
<span data-ttu-id="984ed-126">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="984ed-126">The resource name.</span></span>

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

### <span data-ttu-id="984ed-127">-Prefisso</span><span class="sxs-lookup"><span data-stu-id="984ed-127">-Prefix</span></span>
<span data-ttu-id="984ed-128">Prefisso dell'allocazione IP</span><span class="sxs-lookup"><span data-stu-id="984ed-128">The prefix of the IP allocation</span></span>

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

### <span data-ttu-id="984ed-129">-LunghezzaPrefisso</span><span class="sxs-lookup"><span data-stu-id="984ed-129">-PrefixLength</span></span>
<span data-ttu-id="984ed-130">Lunghezza del prefisso dell'allocazione IP</span><span class="sxs-lookup"><span data-stu-id="984ed-130">The prefix length of the IP allocation</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="984ed-131">-PrefixType</span><span class="sxs-lookup"><span data-stu-id="984ed-131">-PrefixType</span></span>
<span data-ttu-id="984ed-132">Tipo di prefisso dell'allocazione IP</span><span class="sxs-lookup"><span data-stu-id="984ed-132">The prefix type of the IP allocation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPV4, IPV6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="984ed-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="984ed-133">-ResourceGroupName</span></span>
<span data-ttu-id="984ed-134">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="984ed-134">The resource group name.</span></span>

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

### <span data-ttu-id="984ed-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="984ed-135">-Tag</span></span>
<span data-ttu-id="984ed-136">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="984ed-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="984ed-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="984ed-137">-Confirm</span></span>
<span data-ttu-id="984ed-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="984ed-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="984ed-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="984ed-139">-WhatIf</span></span>
<span data-ttu-id="984ed-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="984ed-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="984ed-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="984ed-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="984ed-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="984ed-142">CommonParameters</span></span>
<span data-ttu-id="984ed-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="984ed-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="984ed-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="984ed-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="984ed-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="984ed-145">INPUTS</span></span>

### <span data-ttu-id="984ed-146">System. String</span><span class="sxs-lookup"><span data-stu-id="984ed-146">System.String</span></span>

### <span data-ttu-id="984ed-147">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="984ed-147">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="984ed-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="984ed-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="984ed-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="984ed-149">OUTPUTS</span></span>

### <span data-ttu-id="984ed-150">Microsoft. Azure. Commands. Network. Models. PSIpAllocation</span><span class="sxs-lookup"><span data-stu-id="984ed-150">Microsoft.Azure.Commands.Network.Models.PSIpAllocation</span></span>

## <span data-ttu-id="984ed-151">Note</span><span class="sxs-lookup"><span data-stu-id="984ed-151">NOTES</span></span>

## <span data-ttu-id="984ed-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="984ed-152">RELATED LINKS</span></span>
