---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/powershell/module/az.dedicatedhsm/new-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
ms.openlocfilehash: 9d2d1ee1dd17b9d1783ba267b2f656be6adce05b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966381"
---
# <span data-ttu-id="1fbdc-101">New-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="1fbdc-101">New-AzDedicatedHsm</span></span>

## <span data-ttu-id="1fbdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fbdc-102">SYNOPSIS</span></span>
<span data-ttu-id="1fbdc-103">Creare o aggiornare un HSM dedicato nell'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="1fbdc-103">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="1fbdc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1fbdc-104">SYNTAX</span></span>

```
New-AzDedicatedHsm -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-NetworkInterface <INetworkInterface[]>] [-Sku <String>] [-StampId <String>] [-SubnetId <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="1fbdc-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1fbdc-105">DESCRIPTION</span></span>
<span data-ttu-id="1fbdc-106">Creare o aggiornare un HSM dedicato nell'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="1fbdc-106">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="1fbdc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1fbdc-107">EXAMPLES</span></span>

### <span data-ttu-id="1fbdc-108">Esempio 1: Creare un servizio HSM dedicato in una rete virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="1fbdc-108">Example 1: Create a Dedicated HSM into an existing virtual network</span></span>
```powershell
PS C:\> New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="1fbdc-109">Questo comando crea un servizio HSM dedicato in una rete virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="1fbdc-109">This command creates a Dedicated HSM into an existing virtual network.</span></span>

<span data-ttu-id="1fbdc-110">**NOTA:** Attualmente `New-AzDedicatedHsm` esiste una limitazione che restituisce prima del provisioning completo di HSM in Azure.</span><span class="sxs-lookup"><span data-stu-id="1fbdc-110">**NOTE:** Currently `New-AzDedicatedHsm` has a limitation that it returns before the HSM is fully provisioned on Azure.</span></span>
<span data-ttu-id="1fbdc-111">Pertanto, dopo aver creato un nuovo HSM, verificarne lo stato e assicurarsi che `Get-AzDedicatedHsm` lo sia prima di `Provisioning State` `Succeeded` usarlo.</span><span class="sxs-lookup"><span data-stu-id="1fbdc-111">Therefore after creating a new HSM, please query its state by `Get-AzDedicatedHsm` and make sure its `Provisioning State` is `Succeeded` before using it.</span></span>

## <span data-ttu-id="1fbdc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1fbdc-112">PARAMETERS</span></span>

### <span data-ttu-id="1fbdc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1fbdc-113">-AsJob</span></span>
<span data-ttu-id="1fbdc-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="1fbdc-114">Run the command as a job</span></span>

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

### <span data-ttu-id="1fbdc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fbdc-115">-DefaultProfile</span></span>
<span data-ttu-id="1fbdc-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1fbdc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fbdc-117">-Location</span><span class="sxs-lookup"><span data-stu-id="1fbdc-117">-Location</span></span>
<span data-ttu-id="1fbdc-118">Posizione di Azure supportata in cui deve essere creato il servizio HSM dedicato.</span><span class="sxs-lookup"><span data-stu-id="1fbdc-118">The supported Azure location where the dedicated HSM should be created.</span></span>

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

### <span data-ttu-id="1fbdc-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1fbdc-119">-Name</span></span>
<span data-ttu-id="1fbdc-120">Nome dell'Hsm dedicato</span><span class="sxs-lookup"><span data-stu-id="1fbdc-120">Name of the dedicated Hsm</span></span>

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

### <span data-ttu-id="1fbdc-121">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="1fbdc-121">-NetworkInterface</span></span>
<span data-ttu-id="1fbdc-122">Specifica l'elenco degli ID di risorsa per le interfacce di rete associate all'HSM dedicato.</span><span class="sxs-lookup"><span data-stu-id="1fbdc-122">Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
<span data-ttu-id="1fbdc-123">Per creare, vedere la sezione NOTE per le proprietà NETWORKINTERFACE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="1fbdc-123">To construct, see NOTES section for NETWORKINTERFACE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.INetworkInterface[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fbdc-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1fbdc-124">-NoWait</span></span>
<span data-ttu-id="1fbdc-125">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="1fbdc-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1fbdc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fbdc-126">-ResourceGroupName</span></span>
<span data-ttu-id="1fbdc-127">Nome del gruppo di risorse a cui appartiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="1fbdc-127">The name of the Resource Group to which the resource belongs.</span></span>

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

### <span data-ttu-id="1fbdc-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="1fbdc-128">-Sku</span></span>
<span data-ttu-id="1fbdc-129">SKU dell'HSM dedicato</span><span class="sxs-lookup"><span data-stu-id="1fbdc-129">SKU of the dedicated HSM</span></span>

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

### <span data-ttu-id="1fbdc-130">-StampId</span><span class="sxs-lookup"><span data-stu-id="1fbdc-130">-StampId</span></span>
<span data-ttu-id="1fbdc-131">Questo campo verrà usato quando il componente predefinito non supporta le aree di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="1fbdc-131">This field will be used when RP does not support Availability zones.</span></span>

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

### <span data-ttu-id="1fbdc-132">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="1fbdc-132">-SubnetId</span></span>
<span data-ttu-id="1fbdc-133">Id ARM risorsa nel formato /subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span><span class="sxs-lookup"><span data-stu-id="1fbdc-133">The ARM resource id in the form of /subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span></span>

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

### <span data-ttu-id="1fbdc-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1fbdc-134">-SubscriptionId</span></span>
<span data-ttu-id="1fbdc-135">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1fbdc-135">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1fbdc-136">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="1fbdc-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1fbdc-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="1fbdc-137">-Tag</span></span>
<span data-ttu-id="1fbdc-138">Tag di risorse</span><span class="sxs-lookup"><span data-stu-id="1fbdc-138">Resource tags</span></span>

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

### <span data-ttu-id="1fbdc-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="1fbdc-139">-Zone</span></span>
<span data-ttu-id="1fbdc-140">Le aree Hsm dedicated.</span><span class="sxs-lookup"><span data-stu-id="1fbdc-140">The Dedicated Hsm zones.</span></span>

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

### <span data-ttu-id="1fbdc-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1fbdc-141">-Confirm</span></span>
<span data-ttu-id="1fbdc-142">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fbdc-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fbdc-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fbdc-143">-WhatIf</span></span>
<span data-ttu-id="1fbdc-144">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1fbdc-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fbdc-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1fbdc-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fbdc-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fbdc-146">CommonParameters</span></span>
<span data-ttu-id="1fbdc-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fbdc-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fbdc-148">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1fbdc-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fbdc-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="1fbdc-149">INPUTS</span></span>

## <span data-ttu-id="1fbdc-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1fbdc-150">OUTPUTS</span></span>

### <span data-ttu-id="1fbdc-151">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="1fbdc-151">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="1fbdc-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="1fbdc-152">NOTES</span></span>

<span data-ttu-id="1fbdc-153">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1fbdc-153">ALIASES</span></span>

<span data-ttu-id="1fbdc-154">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="1fbdc-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1fbdc-155">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="1fbdc-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1fbdc-156">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1fbdc-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1fbdc-157">NETWORKINTERFACE <INetworkInterface[]>: specifica l'elenco di ID risorsa per le interfacce di rete associate all'HSM dedicato.</span><span class="sxs-lookup"><span data-stu-id="1fbdc-157">NETWORKINTERFACE <INetworkInterface[]>: Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
  - <span data-ttu-id="1fbdc-158">`[PrivateIPAddress <String>]`: indirizzo IP privato dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="1fbdc-158">`[PrivateIPAddress <String>]`: Private Ip address of the interface</span></span>

## <span data-ttu-id="1fbdc-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1fbdc-159">RELATED LINKS</span></span>

