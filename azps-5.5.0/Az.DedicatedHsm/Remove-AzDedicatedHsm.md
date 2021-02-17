---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/remove-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Remove-AzDedicatedHsm.md
ms.openlocfilehash: aeb8eddcc094e951c78cfe778182cece70448111
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177014"
---
# <span data-ttu-id="5e86c-101">Remove-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="5e86c-101">Remove-AzDedicatedHsm</span></span>

## <span data-ttu-id="5e86c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e86c-102">SYNOPSIS</span></span>
<span data-ttu-id="5e86c-103">Elimina il servizio HSM dedicato di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="5e86c-103">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="5e86c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e86c-104">SYNTAX</span></span>

### <span data-ttu-id="5e86c-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5e86c-105">Delete (Default)</span></span>
```
Remove-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5e86c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5e86c-106">DeleteViaIdentity</span></span>
```
Remove-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5e86c-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5e86c-107">DESCRIPTION</span></span>
<span data-ttu-id="5e86c-108">Elimina il servizio HSM dedicato di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="5e86c-108">Deletes the specified Azure Dedicated HSM.</span></span>

## <span data-ttu-id="5e86c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e86c-109">EXAMPLES</span></span>

### <span data-ttu-id="5e86c-110">Esempio 1: Rimuovere un servizio HSM dedicato in base al nome</span><span class="sxs-lookup"><span data-stu-id="5e86c-110">Example 1: Remove a Dedicated HSM by name</span></span>
```powershell
PS C:\> Remove-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="5e86c-111">Questo commnad rimuove un modulo di sicurezza hardware (HSM) in base al nome.</span><span class="sxs-lookup"><span data-stu-id="5e86c-111">This commnad removes a hardware security module(HSM) by name.</span></span>

### <span data-ttu-id="5e86c-112">Esempio 2: Rimuovere un HSM dedicato in base all'oggetto</span><span class="sxs-lookup"><span data-stu-id="5e86c-112">Example 2: Remove a Dedicated HSM  by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz
PS C:\> Remove-AzDedicatedHsm -InputObject  $hsm

```

<span data-ttu-id="5e86c-113">Questo commnad rimuove un HSM dedicato in base all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5e86c-113">This commnad removes a Dedicated HSM by object.</span></span>

## <span data-ttu-id="5e86c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e86c-114">PARAMETERS</span></span>

### <span data-ttu-id="5e86c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e86c-115">-AsJob</span></span>
<span data-ttu-id="5e86c-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="5e86c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="5e86c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e86c-117">-DefaultProfile</span></span>
<span data-ttu-id="5e86c-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5e86c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e86c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e86c-119">-InputObject</span></span>
<span data-ttu-id="5e86c-120">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="5e86c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e86c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5e86c-121">-Name</span></span>
<span data-ttu-id="5e86c-122">Il nome del servizio HSM dedicato da eliminare</span><span class="sxs-lookup"><span data-stu-id="5e86c-122">The name of the dedicated HSM to delete</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e86c-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5e86c-123">-NoWait</span></span>
<span data-ttu-id="5e86c-124">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="5e86c-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5e86c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e86c-125">-PassThru</span></span>
<span data-ttu-id="5e86c-126">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="5e86c-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5e86c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e86c-127">-ResourceGroupName</span></span>
<span data-ttu-id="5e86c-128">Nome del gruppo di risorse a cui appartiene il servizio HSM dedicato.</span><span class="sxs-lookup"><span data-stu-id="5e86c-128">The name of the Resource Group to which the dedicated HSM belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e86c-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5e86c-129">-SubscriptionId</span></span>
<span data-ttu-id="5e86c-130">Credenziali di abbonamento che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5e86c-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5e86c-131">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="5e86c-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e86c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e86c-132">-Confirm</span></span>
<span data-ttu-id="5e86c-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e86c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e86c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e86c-134">-WhatIf</span></span>
<span data-ttu-id="5e86c-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e86c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e86c-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e86c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e86c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e86c-137">CommonParameters</span></span>
<span data-ttu-id="5e86c-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e86c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e86c-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5e86c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e86c-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="5e86c-140">INPUTS</span></span>

### <span data-ttu-id="5e86c-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="5e86c-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="5e86c-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e86c-142">OUTPUTS</span></span>

### <span data-ttu-id="5e86c-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5e86c-143">System.Boolean</span></span>

## <span data-ttu-id="5e86c-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="5e86c-144">NOTES</span></span>

<span data-ttu-id="5e86c-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="5e86c-145">ALIASES</span></span>

<span data-ttu-id="5e86c-146">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="5e86c-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5e86c-147">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="5e86c-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5e86c-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5e86c-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5e86c-149">INPUTOBJECT <IDedicatedHsmIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="5e86c-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5e86c-150">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="5e86c-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5e86c-151">`[Name <String>]`: nome dell'Hsm dedicato</span><span class="sxs-lookup"><span data-stu-id="5e86c-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="5e86c-152">`[ResourceGroupName <String>]`: nome del gruppo di risorse a cui appartiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="5e86c-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="5e86c-153">`[SubscriptionId <String>]`: credenziali di sottoscrizione che identificano in modo univoco la sottoscrizione di Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5e86c-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5e86c-154">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="5e86c-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="5e86c-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e86c-155">RELATED LINKS</span></span>

