---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/new-azsippool
schema: 2.0.0
ms.openlocfilehash: 2b04c5c1eb4d0a2b79543bf81bbfc02d1f0fb4ad
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023261"
---
# <span data-ttu-id="2dec0-101">New-AzsIPPool</span><span class="sxs-lookup"><span data-stu-id="2dec0-101">New-AzsIPPool</span></span>

## <span data-ttu-id="2dec0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2dec0-102">SYNOPSIS</span></span>
<span data-ttu-id="2dec0-103">Creare un pool IP.</span><span class="sxs-lookup"><span data-stu-id="2dec0-103">Create an IP pool.</span></span>
<span data-ttu-id="2dec0-104">Non è possibile eliminare una volta creato un pool IP.</span><span class="sxs-lookup"><span data-stu-id="2dec0-104">Once created an IP pool cannot be deleted.</span></span>

## <span data-ttu-id="2dec0-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2dec0-105">SYNTAX</span></span>

### <span data-ttu-id="2dec0-106">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2dec0-106">CreateExpanded (Default)</span></span>
```
New-AzsIPPool -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-AddressPrefix <String>] [-EndIPAddress <String>]
 [-NumberOfAllocatedIPAddress <Int64>] [-NumberOfIPAddress <Int64>] [-NumberOfIPAddressesInTransition <Int64>]
 [-StartIPAddress <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2dec0-107">Creare</span><span class="sxs-lookup"><span data-stu-id="2dec0-107">Create</span></span>
```
New-AzsIPPool -Name <String> -Pool <IIPPool> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="2dec0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2dec0-108">DESCRIPTION</span></span>
<span data-ttu-id="2dec0-109">Creare un pool IP.</span><span class="sxs-lookup"><span data-stu-id="2dec0-109">Create an IP pool.</span></span>
<span data-ttu-id="2dec0-110">Non è possibile eliminare una volta creato un pool IP.</span><span class="sxs-lookup"><span data-stu-id="2dec0-110">Once created an IP pool cannot be deleted.</span></span>

## <span data-ttu-id="2dec0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2dec0-111">EXAMPLES</span></span>

### <span data-ttu-id="2dec0-112">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="2dec0-112">Example 1:</span></span>
```powershell
PS C:\> New-AzsIpPool -Name IpPool4 -StartIpAddress ***.***.***.*** -EndIpAddress ***.***.***.*** -AddressPrefix ***.***.***.***/24

```

<span data-ttu-id="2dec0-113">Creare un nuovo pool IP.</span><span class="sxs-lookup"><span data-stu-id="2dec0-113">Create a new IP pool.</span></span>



## <span data-ttu-id="2dec0-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2dec0-114">PARAMETERS</span></span>

### <span data-ttu-id="2dec0-115">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="2dec0-115">-AddressPrefix</span></span>
<span data-ttu-id="2dec0-116">Prefisso dell'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="2dec0-116">The address prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2dec0-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2dec0-117">-AsJob</span></span>
<span data-ttu-id="2dec0-118">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="2dec0-118">Run the command as a job</span></span>

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

### <span data-ttu-id="2dec0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dec0-119">-DefaultProfile</span></span>
<span data-ttu-id="2dec0-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2dec0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2dec0-121">-EndIPAddress</span><span class="sxs-lookup"><span data-stu-id="2dec0-121">-EndIPAddress</span></span>
<span data-ttu-id="2dec0-122">Indirizzo IP finale.</span><span class="sxs-lookup"><span data-stu-id="2dec0-122">The ending IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2dec0-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="2dec0-123">-Location</span></span>
<span data-ttu-id="2dec0-124">Area geografica in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="2dec0-124">The region where the resource is located.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2dec0-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="2dec0-125">-Name</span></span>
<span data-ttu-id="2dec0-126">Nome del pool IP.</span><span class="sxs-lookup"><span data-stu-id="2dec0-126">IP pool name.</span></span>

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

### <span data-ttu-id="2dec0-127">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="2dec0-127">-NoWait</span></span>
<span data-ttu-id="2dec0-128">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="2dec0-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2dec0-129">-NumberOfAllocatedIPAddress</span><span class="sxs-lookup"><span data-stu-id="2dec0-129">-NumberOfAllocatedIPAddress</span></span>
<span data-ttu-id="2dec0-130">Numero di indirizzi IP attualmente assegnati.</span><span class="sxs-lookup"><span data-stu-id="2dec0-130">The number of currently allocated IP addresses.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2dec0-131">-NumberOfIPAddress</span><span class="sxs-lookup"><span data-stu-id="2dec0-131">-NumberOfIPAddress</span></span>
<span data-ttu-id="2dec0-132">Numero totale di indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="2dec0-132">The total number of IP addresses.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2dec0-133">-NumberOfIPAddressesInTransition</span><span class="sxs-lookup"><span data-stu-id="2dec0-133">-NumberOfIPAddressesInTransition</span></span>
<span data-ttu-id="2dec0-134">Numero corrente di indirizzi IP in Transition.</span><span class="sxs-lookup"><span data-stu-id="2dec0-134">The current number of IP addresses in transition.</span></span>

```yaml
Type: System.Int64
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2dec0-135">-Pool</span><span class="sxs-lookup"><span data-stu-id="2dec0-135">-Pool</span></span>
<span data-ttu-id="2dec0-136">Questa risorsa definisce l'intervallo di indirizzi IP da cui vengono assegnati gli indirizzi per i nodi all'interno di una subnet.</span><span class="sxs-lookup"><span data-stu-id="2dec0-136">This resource defines the range of IP addresses from which addresses are allocated for nodes within a subnet.</span></span>
<span data-ttu-id="2dec0-137">Per costruire, vedere la sezione Note per le proprietà del POOL e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="2dec0-137">To construct, see NOTES section for POOL properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="2dec0-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dec0-138">-ResourceGroupName</span></span>
<span data-ttu-id="2dec0-139">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2dec0-139">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2dec0-140">-StartIPAddress</span><span class="sxs-lookup"><span data-stu-id="2dec0-140">-StartIPAddress</span></span>
<span data-ttu-id="2dec0-141">Indirizzo IP iniziale.</span><span class="sxs-lookup"><span data-stu-id="2dec0-141">The starting IP address.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2dec0-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2dec0-142">-SubscriptionId</span></span>
<span data-ttu-id="2dec0-143">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2dec0-143">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2dec0-144">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="2dec0-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2dec0-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="2dec0-145">-Tag</span></span>
<span data-ttu-id="2dec0-146">Elenco di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="2dec0-146">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2dec0-147">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2dec0-147">-Confirm</span></span>
<span data-ttu-id="2dec0-148">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dec0-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dec0-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dec0-149">-WhatIf</span></span>
<span data-ttu-id="2dec0-150">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2dec0-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dec0-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2dec0-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dec0-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dec0-152">CommonParameters</span></span>
<span data-ttu-id="2dec0-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dec0-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dec0-154">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2dec0-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dec0-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2dec0-155">INPUTS</span></span>

### <span data-ttu-id="2dec0-156">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20160501. IIPPool</span><span class="sxs-lookup"><span data-stu-id="2dec0-156">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool</span></span>

## <span data-ttu-id="2dec0-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2dec0-157">OUTPUTS</span></span>

### <span data-ttu-id="2dec0-158">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20160501. IIPPool</span><span class="sxs-lookup"><span data-stu-id="2dec0-158">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool</span></span>



## <span data-ttu-id="2dec0-159">Note</span><span class="sxs-lookup"><span data-stu-id="2dec0-159">NOTES</span></span>

<span data-ttu-id="2dec0-160">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="2dec0-160">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2dec0-161">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2dec0-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="2dec0-162">POOL <IIPPool> : questa risorsa definisce l'intervallo di indirizzi IP da cui vengono assegnati gli indirizzi per i nodi all'interno di una subnet.</span><span class="sxs-lookup"><span data-stu-id="2dec0-162">POOL <IIPPool>: This resource defines the range of IP addresses from which addresses are allocated for nodes within a subnet.</span></span>
  - <span data-ttu-id="2dec0-163">`[Location <String>]`: Area geografica in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="2dec0-163">`[Location <String>]`: The region where the resource is located.</span></span>
  - <span data-ttu-id="2dec0-164">`[Tag <IResourceTags>]`: Elenco di coppie chiave-valore.</span><span class="sxs-lookup"><span data-stu-id="2dec0-164">`[Tag <IResourceTags>]`: List of key-value pairs.</span></span>
    - <span data-ttu-id="2dec0-165">`[(Any) <String>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="2dec0-165">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="2dec0-166">`[AddressPrefix <String>]`: Il prefisso dell'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="2dec0-166">`[AddressPrefix <String>]`: The address prefix.</span></span>
  - <span data-ttu-id="2dec0-167">`[EndIPAddress <String>]`: L'indirizzo IP finale.</span><span class="sxs-lookup"><span data-stu-id="2dec0-167">`[EndIPAddress <String>]`: The ending IP address.</span></span>
  - <span data-ttu-id="2dec0-168">`[NumberOfAllocatedIPAddresses <Int64?>]`: Numero di indirizzi IP attualmente assegnati.</span><span class="sxs-lookup"><span data-stu-id="2dec0-168">`[NumberOfAllocatedIPAddresses <Int64?>]`: The number of currently allocated IP addresses.</span></span>
  - <span data-ttu-id="2dec0-169">`[NumberOfIPAddresses <Int64?>]`: Numero totale di indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="2dec0-169">`[NumberOfIPAddresses <Int64?>]`: The total number of IP addresses.</span></span>
  - <span data-ttu-id="2dec0-170">`[NumberOfIPAddressesInTransition <Int64?>]`: Numero corrente di indirizzi IP in transizione.</span><span class="sxs-lookup"><span data-stu-id="2dec0-170">`[NumberOfIPAddressesInTransition <Int64?>]`: The current number of IP addresses in transition.</span></span>
  - <span data-ttu-id="2dec0-171">`[StartIPAddress <String>]`: L'indirizzo IP iniziale.</span><span class="sxs-lookup"><span data-stu-id="2dec0-171">`[StartIPAddress <String>]`: The starting IP address.</span></span>

## <span data-ttu-id="2dec0-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2dec0-172">RELATED LINKS</span></span>

