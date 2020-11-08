---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/new-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
ms.openlocfilehash: ff1fc53d7fec9a56564bbf536469ea9f745f9265
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190232"
---
# <span data-ttu-id="a0d4f-101">New-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="a0d4f-101">New-AzDedicatedHsm</span></span>

## <span data-ttu-id="a0d4f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a0d4f-102">SYNOPSIS</span></span>
<span data-ttu-id="a0d4f-103">Creare o aggiornare un HSM dedicato nell'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="a0d4f-103">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="a0d4f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a0d4f-104">SYNTAX</span></span>

```
New-AzDedicatedHsm -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-NetworkInterface <INetworkInterface[]>] [-Sku <String>] [-StampId <String>] [-SubnetId <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="a0d4f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0d4f-105">DESCRIPTION</span></span>
<span data-ttu-id="a0d4f-106">Creare o aggiornare un HSM dedicato nell'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="a0d4f-106">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="a0d4f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a0d4f-107">EXAMPLES</span></span>

### <span data-ttu-id="a0d4f-108">Esempio 1: creare un HSM dedicato in una rete virtuale esistente</span><span class="sxs-lookup"><span data-stu-id="a0d4f-108">Example 1: Create a Dedicated HSM into an existing virtual network</span></span>
```powershell
PS C:\> New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="a0d4f-109">Questo comando crea un HSM dedicato in una rete virtuale esistente.</span><span class="sxs-lookup"><span data-stu-id="a0d4f-109">This command creates a Dedicated HSM into an existing virtual network.</span></span>

<span data-ttu-id="a0d4f-110">**Nota:** Attualmente `New-AzDedicatedHsm` ha una limitazione che restituisce prima che l'HSM sia completamente provisioning in Azure.</span><span class="sxs-lookup"><span data-stu-id="a0d4f-110">**NOTE:** Currently `New-AzDedicatedHsm` has a limitation that it returns before the HSM is fully provisioned on Azure.</span></span>
<span data-ttu-id="a0d4f-111">Quindi, dopo la creazione di un nuovo HSM, eseguire una query sul relativo stato per verificare che `Get-AzDedicatedHsm` `Provisioning State` sia `Succeeded` prima di usarlo.</span><span class="sxs-lookup"><span data-stu-id="a0d4f-111">Therefore after creating a new HSM, please query its state by `Get-AzDedicatedHsm` and make sure its `Provisioning State` is `Succeeded` before using it.</span></span>

## <span data-ttu-id="a0d4f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a0d4f-112">PARAMETERS</span></span>

### <span data-ttu-id="a0d4f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0d4f-113">-AsJob</span></span>
<span data-ttu-id="a0d4f-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="a0d4f-114">Run the command as a job</span></span>

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

### <span data-ttu-id="a0d4f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0d4f-115">-DefaultProfile</span></span>
<span data-ttu-id="a0d4f-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a0d4f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0d4f-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a0d4f-117">-Location</span></span>
<span data-ttu-id="a0d4f-118">Il percorso di Azure supportato in cui deve essere creato l'HSM dedicato.</span><span class="sxs-lookup"><span data-stu-id="a0d4f-118">The supported Azure location where the dedicated HSM should be created.</span></span>

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

### <span data-ttu-id="a0d4f-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="a0d4f-119">-Name</span></span>
<span data-ttu-id="a0d4f-120">Nome dell'HSM dedicato</span><span class="sxs-lookup"><span data-stu-id="a0d4f-120">Name of the dedicated Hsm</span></span>

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

### <span data-ttu-id="a0d4f-121">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a0d4f-121">-NetworkInterface</span></span>
<span data-ttu-id="a0d4f-122">Specifica l'elenco di ID delle risorse per le interfacce di rete associate all'HSM dedicato.</span><span class="sxs-lookup"><span data-stu-id="a0d4f-122">Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
<span data-ttu-id="a0d4f-123">Per costruire, vedere la sezione Note per le proprietà di NETWORKINTERFACE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a0d4f-123">To construct, see NOTES section for NETWORKINTERFACE properties and create a hash table.</span></span>

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

### <span data-ttu-id="a0d4f-124">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="a0d4f-124">-NoWait</span></span>
<span data-ttu-id="a0d4f-125">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="a0d4f-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a0d4f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0d4f-126">-ResourceGroupName</span></span>
<span data-ttu-id="a0d4f-127">Nome del gruppo di risorse a cui appartiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="a0d4f-127">The name of the Resource Group to which the resource belongs.</span></span>

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

### <span data-ttu-id="a0d4f-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="a0d4f-128">-Sku</span></span>
<span data-ttu-id="a0d4f-129">SKU dell'HSM dedicato</span><span class="sxs-lookup"><span data-stu-id="a0d4f-129">SKU of the dedicated HSM</span></span>

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

### <span data-ttu-id="a0d4f-130">-StampId</span><span class="sxs-lookup"><span data-stu-id="a0d4f-130">-StampId</span></span>
<span data-ttu-id="a0d4f-131">Questo campo verrà usato quando RP non supporta le aree di disponibilità.</span><span class="sxs-lookup"><span data-stu-id="a0d4f-131">This field will be used when RP does not support Availability zones.</span></span>

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

### <span data-ttu-id="a0d4f-132">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="a0d4f-132">-SubnetId</span></span>
<span data-ttu-id="a0d4f-133">ID risorsa ARM in forma di/subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span><span class="sxs-lookup"><span data-stu-id="a0d4f-133">The ARM resource id in the form of /subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span></span>

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

### <span data-ttu-id="a0d4f-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a0d4f-134">-SubscriptionId</span></span>
<span data-ttu-id="a0d4f-135">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a0d4f-135">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a0d4f-136">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="a0d4f-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a0d4f-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="a0d4f-137">-Tag</span></span>
<span data-ttu-id="a0d4f-138">Tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="a0d4f-138">Resource tags</span></span>

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

### <span data-ttu-id="a0d4f-139">-Zona</span><span class="sxs-lookup"><span data-stu-id="a0d4f-139">-Zone</span></span>
<span data-ttu-id="a0d4f-140">Aree HSM dedicate.</span><span class="sxs-lookup"><span data-stu-id="a0d4f-140">The Dedicated Hsm zones.</span></span>

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

### <span data-ttu-id="a0d4f-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a0d4f-141">-Confirm</span></span>
<span data-ttu-id="a0d4f-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0d4f-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0d4f-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0d4f-143">-WhatIf</span></span>
<span data-ttu-id="a0d4f-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0d4f-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0d4f-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0d4f-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0d4f-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0d4f-146">CommonParameters</span></span>
<span data-ttu-id="a0d4f-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0d4f-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0d4f-148">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0d4f-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0d4f-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a0d4f-149">INPUTS</span></span>

## <span data-ttu-id="a0d4f-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a0d4f-150">OUTPUTS</span></span>

### <span data-ttu-id="a0d4f-151">Microsoft. Azure. PowerShell. Cmdlets. DedicatedHsm. Models. Api20181031. IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="a0d4f-151">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="a0d4f-152">Note</span><span class="sxs-lookup"><span data-stu-id="a0d4f-152">NOTES</span></span>

<span data-ttu-id="a0d4f-153">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a0d4f-153">ALIASES</span></span>

<span data-ttu-id="a0d4f-154">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a0d4f-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a0d4f-155">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="a0d4f-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a0d4f-156">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a0d4f-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a0d4f-157">NETWORKINTERFACE <INetworkInterface [] >: specifica l'elenco di ID delle risorse per le interfacce di rete associate all'HSM dedicato.</span><span class="sxs-lookup"><span data-stu-id="a0d4f-157">NETWORKINTERFACE <INetworkInterface[]>: Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
  - <span data-ttu-id="a0d4f-158">`[PrivateIPAddress <String>]`: Indirizzo IP privato dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="a0d4f-158">`[PrivateIPAddress <String>]`: Private Ip address of the interface</span></span>

## <span data-ttu-id="a0d4f-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a0d4f-159">RELATED LINKS</span></span>

