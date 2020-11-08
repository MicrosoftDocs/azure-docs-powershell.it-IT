---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareauthorization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareAuthorization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWareAuthorization.md
ms.openlocfilehash: 13f5e76a7fbb101e9fa6b1247f233c0f85aba8bf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190425"
---
# <span data-ttu-id="cd580-101">Remove-AzVMWareAuthorization</span><span class="sxs-lookup"><span data-stu-id="cd580-101">Remove-AzVMWareAuthorization</span></span>

## <span data-ttu-id="cd580-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cd580-102">SYNOPSIS</span></span>
<span data-ttu-id="cd580-103">Eliminare un'autorizzazione del circuito ExpressRoute in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="cd580-103">Delete an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="cd580-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd580-104">SYNTAX</span></span>

### <span data-ttu-id="cd580-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cd580-105">Delete (Default)</span></span>
```
Remove-AzVMWareAuthorization -Name <String> -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="cd580-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cd580-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWareAuthorization -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cd580-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd580-107">DESCRIPTION</span></span>
<span data-ttu-id="cd580-108">Eliminare un'autorizzazione del circuito ExpressRoute in un cloud privato</span><span class="sxs-lookup"><span data-stu-id="cd580-108">Delete an ExpressRoute Circuit Authorization in a private cloud</span></span>

## <span data-ttu-id="cd580-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd580-109">EXAMPLES</span></span>

### <span data-ttu-id="cd580-110">Esempio 1: eliminare l'autorizzazione per il cloud privato</span><span class="sxs-lookup"><span data-stu-id="cd580-110">Example 1: Delete authorization for private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWareAuthorization -Name azps-test-auth -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

```

<span data-ttu-id="cd580-111">Eliminare l'autorizzazione per il cloud privato</span><span class="sxs-lookup"><span data-stu-id="cd580-111">Delete authorization for private cloud</span></span>

## <span data-ttu-id="cd580-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cd580-112">PARAMETERS</span></span>

### <span data-ttu-id="cd580-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd580-113">-AsJob</span></span>
<span data-ttu-id="cd580-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="cd580-114">Run the command as a job</span></span>

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

### <span data-ttu-id="cd580-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd580-115">-DefaultProfile</span></span>
<span data-ttu-id="cd580-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cd580-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd580-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd580-117">-InputObject</span></span>
<span data-ttu-id="cd580-118">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="cd580-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd580-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="cd580-119">-Name</span></span>
<span data-ttu-id="cd580-120">Nome dell'autorizzazione del circuito ExpressRoute nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="cd580-120">Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: AuthorizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd580-121">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="cd580-121">-NoWait</span></span>
<span data-ttu-id="cd580-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="cd580-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cd580-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd580-123">-PassThru</span></span>
<span data-ttu-id="cd580-124">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="cd580-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cd580-125">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="cd580-125">-PrivateCloudName</span></span>
<span data-ttu-id="cd580-126">Nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="cd580-126">Name of the private cloud</span></span>

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

### <span data-ttu-id="cd580-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd580-127">-ResourceGroupName</span></span>
<span data-ttu-id="cd580-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cd580-128">The name of the resource group.</span></span>
<span data-ttu-id="cd580-129">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="cd580-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="cd580-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd580-130">-SubscriptionId</span></span>
<span data-ttu-id="cd580-131">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cd580-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="cd580-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cd580-132">-Confirm</span></span>
<span data-ttu-id="cd580-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd580-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd580-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd580-134">-WhatIf</span></span>
<span data-ttu-id="cd580-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd580-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd580-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd580-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd580-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd580-137">CommonParameters</span></span>
<span data-ttu-id="cd580-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd580-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd580-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd580-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd580-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cd580-140">INPUTS</span></span>

### <span data-ttu-id="cd580-141">Microsoft. Azure. PowerShell. Cmdlets. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="cd580-141">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="cd580-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd580-142">OUTPUTS</span></span>

### <span data-ttu-id="cd580-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cd580-143">System.Boolean</span></span>

## <span data-ttu-id="cd580-144">Note</span><span class="sxs-lookup"><span data-stu-id="cd580-144">NOTES</span></span>

<span data-ttu-id="cd580-145">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cd580-145">ALIASES</span></span>

<span data-ttu-id="cd580-146">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cd580-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cd580-147">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="cd580-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cd580-148">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cd580-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cd580-149">INPUTOBJECT <IVMWareIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="cd580-149">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cd580-150">`[AuthorizationName <String>]`: Nome dell'autorizzazione del circuito ExpressRoute nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="cd580-150">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="cd580-151">`[ClusterName <String>]`: Nome del cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="cd580-151">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="cd580-152">`[HcxEnterpriseSiteName <String>]`: Nome del sito aziendale di HCX nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="cd580-152">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="cd580-153">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="cd580-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cd580-154">`[Location <String>]`: Area di Azure</span><span class="sxs-lookup"><span data-stu-id="cd580-154">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="cd580-155">`[PrivateCloudName <String>]`: Nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="cd580-155">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="cd580-156">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cd580-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="cd580-157">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="cd580-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="cd580-158">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cd580-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="cd580-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd580-159">RELATED LINKS</span></span>
