---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/update-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
ms.openlocfilehash: 5aa286eeedb08e6f582210d98a1d29bcd0074031
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324293"
---
# <span data-ttu-id="c74a0-101">Update-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="c74a0-101">Update-AzDedicatedHsm</span></span>

## <span data-ttu-id="c74a0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c74a0-102">SYNOPSIS</span></span>
<span data-ttu-id="c74a0-103">Aggiornare un HSM dedicato nell'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="c74a0-103">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="c74a0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c74a0-104">SYNTAX</span></span>

### <span data-ttu-id="c74a0-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c74a0-105">UpdateExpanded (Default)</span></span>
```
Update-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c74a0-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c74a0-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c74a0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c74a0-107">DESCRIPTION</span></span>
<span data-ttu-id="c74a0-108">Aggiornare un HSM dedicato nell'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="c74a0-108">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="c74a0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c74a0-109">EXAMPLES</span></span>

### <span data-ttu-id="c74a0-110">Esempio 1: aggiornare il tag Parameter del HSM dedicato per nome</span><span class="sxs-lookup"><span data-stu-id="c74a0-110">Example 1: Update the parameter tag of the Dedicated HSM by name</span></span>
```powershell
PS C:\> Update-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="c74a0-111">Questo comando Aggiorna il tag di parametro del HSM dedicato per nome</span><span class="sxs-lookup"><span data-stu-id="c74a0-111">This command updates the parameter tag of the Dedicated HSM by name</span></span>

### <span data-ttu-id="c74a0-112">Esempio 2: aggiornare il tag Parameter del HSM dedicato per oggetto</span><span class="sxs-lookup"><span data-stu-id="c74a0-112">Example 2: Update the parameter tag of the Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz 
PS C:\> Update-AzDedicatedHsm -InputObject -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="c74a0-113">Questo comando Aggiorna il tag di parametro del HSM dedicato per oggetto</span><span class="sxs-lookup"><span data-stu-id="c74a0-113">This command updates the parameter tag of the Dedicated HSM by object</span></span>

## <span data-ttu-id="c74a0-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c74a0-114">PARAMETERS</span></span>

### <span data-ttu-id="c74a0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c74a0-115">-AsJob</span></span>
<span data-ttu-id="c74a0-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="c74a0-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c74a0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c74a0-117">-DefaultProfile</span></span>
<span data-ttu-id="c74a0-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c74a0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c74a0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c74a0-119">-InputObject</span></span>
<span data-ttu-id="c74a0-120">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="c74a0-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c74a0-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c74a0-121">-Name</span></span>
<span data-ttu-id="c74a0-122">Nome dell'HSM dedicato</span><span class="sxs-lookup"><span data-stu-id="c74a0-122">Name of the dedicated HSM</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c74a0-123">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="c74a0-123">-NoWait</span></span>
<span data-ttu-id="c74a0-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="c74a0-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c74a0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c74a0-125">-ResourceGroupName</span></span>
<span data-ttu-id="c74a0-126">Nome del gruppo di risorse a cui appartiene il server.</span><span class="sxs-lookup"><span data-stu-id="c74a0-126">The name of the Resource Group to which the server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c74a0-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c74a0-127">-SubscriptionId</span></span>
<span data-ttu-id="c74a0-128">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c74a0-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c74a0-129">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="c74a0-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c74a0-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="c74a0-130">-Tag</span></span>
<span data-ttu-id="c74a0-131">Tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="c74a0-131">Resource tags</span></span>

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

### <span data-ttu-id="c74a0-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c74a0-132">-Confirm</span></span>
<span data-ttu-id="c74a0-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c74a0-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c74a0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c74a0-134">-WhatIf</span></span>
<span data-ttu-id="c74a0-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c74a0-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c74a0-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c74a0-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c74a0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c74a0-137">CommonParameters</span></span>
<span data-ttu-id="c74a0-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c74a0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c74a0-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c74a0-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c74a0-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c74a0-140">INPUTS</span></span>

### <span data-ttu-id="c74a0-141">Microsoft. Azure. PowerShell. Cmdlets. DedicatedHsm. Models. IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="c74a0-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="c74a0-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c74a0-142">OUTPUTS</span></span>

### <span data-ttu-id="c74a0-143">Microsoft. Azure. PowerShell. Cmdlets. DedicatedHsm. Models. Api20181031. IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="c74a0-143">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="c74a0-144">Note</span><span class="sxs-lookup"><span data-stu-id="c74a0-144">NOTES</span></span>

<span data-ttu-id="c74a0-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c74a0-145">ALIASES</span></span>

<span data-ttu-id="c74a0-146">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c74a0-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c74a0-147">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="c74a0-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c74a0-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c74a0-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c74a0-149">INPUTOBJECT <IDedicatedHsmIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="c74a0-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c74a0-150">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="c74a0-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c74a0-151">`[Name <String>]`: Nome dell'HSM dedicato</span><span class="sxs-lookup"><span data-stu-id="c74a0-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="c74a0-152">`[ResourceGroupName <String>]`: Nome del gruppo di risorse a cui appartiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="c74a0-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="c74a0-153">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c74a0-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c74a0-154">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="c74a0-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c74a0-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c74a0-155">RELATED LINKS</span></span>

