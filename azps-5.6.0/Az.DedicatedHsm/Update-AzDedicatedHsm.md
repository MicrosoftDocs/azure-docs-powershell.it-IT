---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/powershell/module/az.dedicatedhsm/update-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
ms.openlocfilehash: ba005802294ef4fa1c890230230cbd44bc783216
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980749"
---
# <span data-ttu-id="de9cc-101">Update-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="de9cc-101">Update-AzDedicatedHsm</span></span>

## <span data-ttu-id="de9cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de9cc-102">SYNOPSIS</span></span>
<span data-ttu-id="de9cc-103">Aggiornare un HSM dedicato nella sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="de9cc-103">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="de9cc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de9cc-104">SYNTAX</span></span>

### <span data-ttu-id="de9cc-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="de9cc-105">UpdateExpanded (Default)</span></span>
```
Update-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="de9cc-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="de9cc-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="de9cc-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="de9cc-107">DESCRIPTION</span></span>
<span data-ttu-id="de9cc-108">Aggiornare un HSM dedicato nella sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="de9cc-108">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="de9cc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de9cc-109">EXAMPLES</span></span>

### <span data-ttu-id="de9cc-110">Esempio 1: Aggiornare il tag del parametro del servizio HSM dedicato in base al nome</span><span class="sxs-lookup"><span data-stu-id="de9cc-110">Example 1: Update the parameter tag of the Dedicated HSM by name</span></span>
```powershell
PS C:\> Update-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="de9cc-111">Questo comando aggiorna il tag del parametro del servizio HSM dedicato in base al nome</span><span class="sxs-lookup"><span data-stu-id="de9cc-111">This command updates the parameter tag of the Dedicated HSM by name</span></span>

### <span data-ttu-id="de9cc-112">Esempio 2: Aggiornare il tag del parametro del servizio HSM dedicato in base all'oggetto</span><span class="sxs-lookup"><span data-stu-id="de9cc-112">Example 2: Update the parameter tag of the Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz 
PS C:\> Update-AzDedicatedHsm -InputObject -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="de9cc-113">Questo comando aggiorna il tag di parametro di Dedicated HSM in base all'oggetto</span><span class="sxs-lookup"><span data-stu-id="de9cc-113">This command updates the parameter tag of the Dedicated HSM by object</span></span>

## <span data-ttu-id="de9cc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de9cc-114">PARAMETERS</span></span>

### <span data-ttu-id="de9cc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de9cc-115">-AsJob</span></span>
<span data-ttu-id="de9cc-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="de9cc-116">Run the command as a job</span></span>

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

### <span data-ttu-id="de9cc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de9cc-117">-DefaultProfile</span></span>
<span data-ttu-id="de9cc-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="de9cc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de9cc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de9cc-119">-InputObject</span></span>
<span data-ttu-id="de9cc-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="de9cc-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="de9cc-121">-Name</span><span class="sxs-lookup"><span data-stu-id="de9cc-121">-Name</span></span>
<span data-ttu-id="de9cc-122">Nome del servizio HSM dedicato</span><span class="sxs-lookup"><span data-stu-id="de9cc-122">Name of the dedicated HSM</span></span>

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

### <span data-ttu-id="de9cc-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="de9cc-123">-NoWait</span></span>
<span data-ttu-id="de9cc-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="de9cc-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="de9cc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de9cc-125">-ResourceGroupName</span></span>
<span data-ttu-id="de9cc-126">Nome del gruppo di risorse a cui appartiene il server.</span><span class="sxs-lookup"><span data-stu-id="de9cc-126">The name of the Resource Group to which the server belongs.</span></span>

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

### <span data-ttu-id="de9cc-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="de9cc-127">-SubscriptionId</span></span>
<span data-ttu-id="de9cc-128">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="de9cc-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="de9cc-129">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="de9cc-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="de9cc-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="de9cc-130">-Tag</span></span>
<span data-ttu-id="de9cc-131">Tag di risorse</span><span class="sxs-lookup"><span data-stu-id="de9cc-131">Resource tags</span></span>

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

### <span data-ttu-id="de9cc-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de9cc-132">-Confirm</span></span>
<span data-ttu-id="de9cc-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de9cc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de9cc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de9cc-134">-WhatIf</span></span>
<span data-ttu-id="de9cc-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de9cc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de9cc-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="de9cc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de9cc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de9cc-137">CommonParameters</span></span>
<span data-ttu-id="de9cc-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de9cc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de9cc-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="de9cc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de9cc-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="de9cc-140">INPUTS</span></span>

### <span data-ttu-id="de9cc-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="de9cc-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="de9cc-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de9cc-142">OUTPUTS</span></span>

### <span data-ttu-id="de9cc-143">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="de9cc-143">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="de9cc-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="de9cc-144">NOTES</span></span>

<span data-ttu-id="de9cc-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="de9cc-145">ALIASES</span></span>

<span data-ttu-id="de9cc-146">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="de9cc-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="de9cc-147">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="de9cc-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="de9cc-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="de9cc-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="de9cc-149">INPUTOBJECT <IDedicatedHsmIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="de9cc-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="de9cc-150">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="de9cc-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="de9cc-151">`[Name <String>]`: nome dell'Hsm dedicato</span><span class="sxs-lookup"><span data-stu-id="de9cc-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="de9cc-152">`[ResourceGroupName <String>]`: nome del gruppo di risorse a cui appartiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="de9cc-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="de9cc-153">`[SubscriptionId <String>]`: credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="de9cc-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="de9cc-154">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="de9cc-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="de9cc-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de9cc-155">RELATED LINKS</span></span>

