---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/remove-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Remove-AzVMWarePrivateCloud.md
ms.openlocfilehash: accf225acfb05fdcaf49eb5dde4d1bae0332d300
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190417"
---
# <span data-ttu-id="e3982-101">Remove-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="e3982-101">Remove-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="e3982-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e3982-102">SYNOPSIS</span></span>
<span data-ttu-id="e3982-103">Eliminare un cloud privato</span><span class="sxs-lookup"><span data-stu-id="e3982-103">Delete a private cloud</span></span>

## <span data-ttu-id="e3982-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3982-104">SYNTAX</span></span>

### <span data-ttu-id="e3982-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e3982-105">Delete (Default)</span></span>
```
Remove-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e3982-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e3982-106">DeleteViaIdentity</span></span>
```
Remove-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e3982-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3982-107">DESCRIPTION</span></span>
<span data-ttu-id="e3982-108">Eliminare un cloud privato</span><span class="sxs-lookup"><span data-stu-id="e3982-108">Delete a private cloud</span></span>

## <span data-ttu-id="e3982-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3982-109">EXAMPLES</span></span>

### <span data-ttu-id="e3982-110">Esempio 1: eliminare il cloud privato</span><span class="sxs-lookup"><span data-stu-id="e3982-110">Example 1: Delete private cloud</span></span>
```powershell
PS C:\> Remove-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud

```

<span data-ttu-id="e3982-111">Eliminare il cloud privato</span><span class="sxs-lookup"><span data-stu-id="e3982-111">Delete private cloud</span></span>

## <span data-ttu-id="e3982-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e3982-112">PARAMETERS</span></span>

### <span data-ttu-id="e3982-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3982-113">-AsJob</span></span>
<span data-ttu-id="e3982-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="e3982-114">Run the command as a job</span></span>

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

### <span data-ttu-id="e3982-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3982-115">-DefaultProfile</span></span>
<span data-ttu-id="e3982-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3982-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3982-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3982-117">-InputObject</span></span>
<span data-ttu-id="e3982-118">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e3982-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e3982-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3982-119">-Name</span></span>
<span data-ttu-id="e3982-120">Nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="e3982-120">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3982-121">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="e3982-121">-NoWait</span></span>
<span data-ttu-id="e3982-122">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="e3982-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e3982-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3982-123">-PassThru</span></span>
<span data-ttu-id="e3982-124">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="e3982-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e3982-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3982-125">-ResourceGroupName</span></span>
<span data-ttu-id="e3982-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e3982-126">The name of the resource group.</span></span>
<span data-ttu-id="e3982-127">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e3982-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e3982-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e3982-128">-SubscriptionId</span></span>
<span data-ttu-id="e3982-129">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e3982-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e3982-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e3982-130">-Confirm</span></span>
<span data-ttu-id="e3982-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3982-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3982-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3982-132">-WhatIf</span></span>
<span data-ttu-id="e3982-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3982-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3982-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3982-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3982-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3982-135">CommonParameters</span></span>
<span data-ttu-id="e3982-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3982-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3982-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3982-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3982-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e3982-138">INPUTS</span></span>

### <span data-ttu-id="e3982-139">Microsoft. Azure. PowerShell. Cmdlets. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="e3982-139">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="e3982-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3982-140">OUTPUTS</span></span>

### <span data-ttu-id="e3982-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e3982-141">System.Boolean</span></span>

## <span data-ttu-id="e3982-142">Note</span><span class="sxs-lookup"><span data-stu-id="e3982-142">NOTES</span></span>

<span data-ttu-id="e3982-143">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e3982-143">ALIASES</span></span>

<span data-ttu-id="e3982-144">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e3982-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e3982-145">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="e3982-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e3982-146">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e3982-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e3982-147">INPUTOBJECT <IVMWareIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="e3982-147">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e3982-148">`[AuthorizationName <String>]`: Nome dell'autorizzazione del circuito ExpressRoute nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="e3982-148">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="e3982-149">`[ClusterName <String>]`: Nome del cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="e3982-149">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="e3982-150">`[HcxEnterpriseSiteName <String>]`: Nome del sito aziendale di HCX nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="e3982-150">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="e3982-151">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="e3982-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e3982-152">`[Location <String>]`: Area di Azure</span><span class="sxs-lookup"><span data-stu-id="e3982-152">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="e3982-153">`[PrivateCloudName <String>]`: Nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="e3982-153">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="e3982-154">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e3982-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="e3982-155">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="e3982-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="e3982-156">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e3982-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="e3982-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3982-157">RELATED LINKS</span></span>

