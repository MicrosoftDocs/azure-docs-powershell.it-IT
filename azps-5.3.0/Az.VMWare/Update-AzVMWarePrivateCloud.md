---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWarePrivateCloud.md
ms.openlocfilehash: e47cf4fe3eef11664640e947b7093dc302f90ea3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474794"
---
# <span data-ttu-id="469ef-101">Update-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="469ef-101">Update-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="469ef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="469ef-102">SYNOPSIS</span></span>
<span data-ttu-id="469ef-103">Aggiornare un cloud privato</span><span class="sxs-lookup"><span data-stu-id="469ef-103">Update a private cloud</span></span>

## <span data-ttu-id="469ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="469ef-104">SYNTAX</span></span>

### <span data-ttu-id="469ef-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="469ef-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentitySource <IIdentitySource[]>] [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="469ef-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="469ef-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-IdentitySource <IIdentitySource[]>]
 [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="469ef-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="469ef-107">DESCRIPTION</span></span>
<span data-ttu-id="469ef-108">Aggiornare un cloud privato</span><span class="sxs-lookup"><span data-stu-id="469ef-108">Update a private cloud</span></span>

## <span data-ttu-id="469ef-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="469ef-109">EXAMPLES</span></span>

### <span data-ttu-id="469ef-110">Esempio 1: aggiornare le dimensioni del cloud privato per nome</span><span class="sxs-lookup"><span data-stu-id="469ef-110">Example 1: Update size of private cloud by name</span></span>
```powershell
PS C:\> Update-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="469ef-111">Aggiornare le dimensioni del cloud privato per nome</span><span class="sxs-lookup"><span data-stu-id="469ef-111">Update size of private cloud by name</span></span>

### <span data-ttu-id="469ef-112">Esempio 2: aggiornare le dimensioni dell'oggetto cloud privato per input</span><span class="sxs-lookup"><span data-stu-id="469ef-112">Example 2: Update size of private cloud by input object</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud | Update-AzVMWarePrivateCloud -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="469ef-113">Aggiornare le dimensioni dell'oggetto cloud privato per input</span><span class="sxs-lookup"><span data-stu-id="469ef-113">Update size of private cloud by input object</span></span>

## <span data-ttu-id="469ef-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="469ef-114">PARAMETERS</span></span>

### <span data-ttu-id="469ef-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="469ef-115">-AsJob</span></span>
<span data-ttu-id="469ef-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="469ef-116">Run the command as a job</span></span>

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

### <span data-ttu-id="469ef-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="469ef-117">-DefaultProfile</span></span>
<span data-ttu-id="469ef-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="469ef-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="469ef-119">-IdentitySource</span><span class="sxs-lookup"><span data-stu-id="469ef-119">-IdentitySource</span></span>
<span data-ttu-id="469ef-120">vCenter Single Sign-on-source per la creazione, vedere la sezione Note per le proprietà di IDENTITYSOURCE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="469ef-120">vCenter Single Sign On Identity Sources To construct, see NOTES section for IDENTITYSOURCE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IIdentitySource[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="469ef-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="469ef-121">-InputObject</span></span>
<span data-ttu-id="469ef-122">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="469ef-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="469ef-123">-Internet</span><span class="sxs-lookup"><span data-stu-id="469ef-123">-Internet</span></span>
<span data-ttu-id="469ef-124">La connettività a Internet è abilitata o disabilitata</span><span class="sxs-lookup"><span data-stu-id="469ef-124">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="469ef-125">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="469ef-125">-ManagementClusterSize</span></span>
<span data-ttu-id="469ef-126">Dimensioni del cluster</span><span class="sxs-lookup"><span data-stu-id="469ef-126">The cluster size</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="469ef-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="469ef-127">-Name</span></span>
<span data-ttu-id="469ef-128">Nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="469ef-128">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="469ef-129">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="469ef-129">-NoWait</span></span>
<span data-ttu-id="469ef-130">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="469ef-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="469ef-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="469ef-131">-ResourceGroupName</span></span>
<span data-ttu-id="469ef-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="469ef-132">The name of the resource group.</span></span>
<span data-ttu-id="469ef-133">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="469ef-133">The name is case insensitive.</span></span>

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

### <span data-ttu-id="469ef-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="469ef-134">-SubscriptionId</span></span>
<span data-ttu-id="469ef-135">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="469ef-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="469ef-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="469ef-136">-Tag</span></span>
<span data-ttu-id="469ef-137">Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="469ef-137">Resource tags.</span></span>

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

### <span data-ttu-id="469ef-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="469ef-138">-Confirm</span></span>
<span data-ttu-id="469ef-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="469ef-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="469ef-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="469ef-140">-WhatIf</span></span>
<span data-ttu-id="469ef-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="469ef-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="469ef-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="469ef-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="469ef-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="469ef-143">CommonParameters</span></span>
<span data-ttu-id="469ef-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="469ef-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="469ef-145">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="469ef-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="469ef-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="469ef-146">INPUTS</span></span>

### <span data-ttu-id="469ef-147">Microsoft. Azure. PowerShell. Cmdlets. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="469ef-147">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="469ef-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="469ef-148">OUTPUTS</span></span>

### <span data-ttu-id="469ef-149">Microsoft. Azure. PowerShell. Cmdlets. VMWare. Models. Api20200320. IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="469ef-149">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="469ef-150">Note</span><span class="sxs-lookup"><span data-stu-id="469ef-150">NOTES</span></span>

<span data-ttu-id="469ef-151">ALIAS</span><span class="sxs-lookup"><span data-stu-id="469ef-151">ALIASES</span></span>

<span data-ttu-id="469ef-152">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="469ef-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="469ef-153">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="469ef-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="469ef-154">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="469ef-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="469ef-155">IDENTITYSOURCE <IIdentitySource [] >: Single Sign-on per le origini delle identità</span><span class="sxs-lookup"><span data-stu-id="469ef-155">IDENTITYSOURCE <IIdentitySource[]>: vCenter Single Sign On Identity Sources</span></span>
  - <span data-ttu-id="469ef-156">`[Alias <String>]`: Nome NetBIOS del dominio</span><span class="sxs-lookup"><span data-stu-id="469ef-156">`[Alias <String>]`: The domain's NetBIOS name</span></span>
  - <span data-ttu-id="469ef-157">`[BaseGroupDn <String>]`: Nome distinto di base per i gruppi</span><span class="sxs-lookup"><span data-stu-id="469ef-157">`[BaseGroupDn <String>]`: The base distinguished name for groups</span></span>
  - <span data-ttu-id="469ef-158">`[BaseUserDn <String>]`: Nome distinto di base per gli utenti</span><span class="sxs-lookup"><span data-stu-id="469ef-158">`[BaseUserDn <String>]`: The base distinguished name for users</span></span>
  - <span data-ttu-id="469ef-159">`[Domain <String>]`: Nome DNS del dominio</span><span class="sxs-lookup"><span data-stu-id="469ef-159">`[Domain <String>]`: The domain's dns name</span></span>
  - <span data-ttu-id="469ef-160">`[Name <String>]`: Nome dell'origine di identità</span><span class="sxs-lookup"><span data-stu-id="469ef-160">`[Name <String>]`: The name of the identity source</span></span>
  - <span data-ttu-id="469ef-161">`[Password <String>]`: La password dell'utente di Active Directory con un minimo di accesso di sola lettura a base DN per utenti e gruppi.</span><span class="sxs-lookup"><span data-stu-id="469ef-161">`[Password <String>]`: The password of the Active Directory user with a minimum of read-only access to Base DN for users and groups.</span></span>
  - <span data-ttu-id="469ef-162">`[PrimaryServer <String>]`: URL del server primario</span><span class="sxs-lookup"><span data-stu-id="469ef-162">`[PrimaryServer <String>]`: Primary server URL</span></span>
  - <span data-ttu-id="469ef-163">`[SecondaryServer <String>]`: URL del server secondario</span><span class="sxs-lookup"><span data-stu-id="469ef-163">`[SecondaryServer <String>]`: Secondary server URL</span></span>
  - <span data-ttu-id="469ef-164">`[Ssl <SslEnum?>]`: Proteggere le comunicazioni LDAP con il certificato SSL (LDAPs)</span><span class="sxs-lookup"><span data-stu-id="469ef-164">`[Ssl <SslEnum?>]`: Protect LDAP communication using SSL certificate (LDAPS)</span></span>
  - <span data-ttu-id="469ef-165">`[Username <String>]`: ID di un utente di Active Directory con un minimo di accesso di sola lettura a base DN per utenti e gruppi</span><span class="sxs-lookup"><span data-stu-id="469ef-165">`[Username <String>]`: The ID of an Active Directory user with a minimum of read-only access to Base DN for users and group</span></span>

<span data-ttu-id="469ef-166">INPUTOBJECT <IVMWareIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="469ef-166">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="469ef-167">`[AuthorizationName <String>]`: Nome dell'autorizzazione del circuito ExpressRoute nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="469ef-167">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="469ef-168">`[ClusterName <String>]`: Nome del cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="469ef-168">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="469ef-169">`[HcxEnterpriseSiteName <String>]`: Nome del sito aziendale di HCX nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="469ef-169">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="469ef-170">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="469ef-170">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="469ef-171">`[Location <String>]`: Area di Azure</span><span class="sxs-lookup"><span data-stu-id="469ef-171">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="469ef-172">`[PrivateCloudName <String>]`: Nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="469ef-172">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="469ef-173">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="469ef-173">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="469ef-174">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="469ef-174">The name is case insensitive.</span></span>
  - <span data-ttu-id="469ef-175">`[SubscriptionId <String>]`: ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="469ef-175">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="469ef-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="469ef-176">RELATED LINKS</span></span>

