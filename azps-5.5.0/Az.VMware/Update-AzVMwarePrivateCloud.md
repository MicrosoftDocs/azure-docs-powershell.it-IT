---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwarePrivateCloud.md
ms.openlocfilehash: dbea608c24d8da8fa292316653b3e16953aed8b6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208891"
---
# <span data-ttu-id="71142-101">Update-AzVMwarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="71142-101">Update-AzVMwarePrivateCloud</span></span>

## <span data-ttu-id="71142-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71142-102">SYNOPSIS</span></span>
<span data-ttu-id="71142-103">Aggiornare un cloud privato</span><span class="sxs-lookup"><span data-stu-id="71142-103">Update a private cloud</span></span>

## <span data-ttu-id="71142-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71142-104">SYNTAX</span></span>

### <span data-ttu-id="71142-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="71142-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMwarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentitySource <IIdentitySource[]>] [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="71142-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="71142-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMwarePrivateCloud -InputObject <IVMwareIdentity> [-IdentitySource <IIdentitySource[]>]
 [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="71142-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="71142-107">DESCRIPTION</span></span>
<span data-ttu-id="71142-108">Aggiornare un cloud privato</span><span class="sxs-lookup"><span data-stu-id="71142-108">Update a private cloud</span></span>

## <span data-ttu-id="71142-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71142-109">EXAMPLES</span></span>

### <span data-ttu-id="71142-110">Esempio 1: Aggiornare le dimensioni del cloud privato in base al nome</span><span class="sxs-lookup"><span data-stu-id="71142-110">Example 1: Update size of private cloud by name</span></span>
```powershell
PS C:\> Update-AzVMwarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="71142-111">Aggiornare le dimensioni del cloud privato in base al nome</span><span class="sxs-lookup"><span data-stu-id="71142-111">Update size of private cloud by name</span></span>

### <span data-ttu-id="71142-112">Esempio 2: Aggiornare le dimensioni del cloud privato in base all'oggetto di input</span><span class="sxs-lookup"><span data-stu-id="71142-112">Example 2: Update size of private cloud by input object</span></span>
```powershell
PS C:\> Get-AzVMwarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud | Update-AzVMwarePrivateCloud -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="71142-113">Aggiornare le dimensioni del cloud privato in base all'oggetto di input</span><span class="sxs-lookup"><span data-stu-id="71142-113">Update size of private cloud by input object</span></span>

## <span data-ttu-id="71142-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71142-114">PARAMETERS</span></span>

### <span data-ttu-id="71142-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71142-115">-AsJob</span></span>
<span data-ttu-id="71142-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="71142-116">Run the command as a job</span></span>

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

### <span data-ttu-id="71142-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71142-117">-DefaultProfile</span></span>
<span data-ttu-id="71142-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="71142-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71142-119">-IdentitySource</span><span class="sxs-lookup"><span data-stu-id="71142-119">-IdentitySource</span></span>
<span data-ttu-id="71142-120">vCenter Single Sign On Identity Sources To construct, vedere la sezione NOTES per le proprietà IDENTITYSOURCE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="71142-120">vCenter Single Sign On Identity Sources To construct, see NOTES section for IDENTITYSOURCE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IIdentitySource[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71142-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71142-121">-InputObject</span></span>
<span data-ttu-id="71142-122">Creazione di un parametro Identity To, vedere la sezione NOTES per le proprietà INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="71142-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71142-123">-Internet</span><span class="sxs-lookup"><span data-stu-id="71142-123">-Internet</span></span>
<span data-ttu-id="71142-124">La connettività a Internet è abilitata o disabilitata</span><span class="sxs-lookup"><span data-stu-id="71142-124">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71142-125">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="71142-125">-ManagementClusterSize</span></span>
<span data-ttu-id="71142-126">Le dimensioni del cluster</span><span class="sxs-lookup"><span data-stu-id="71142-126">The cluster size</span></span>

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

### <span data-ttu-id="71142-127">-Name</span><span class="sxs-lookup"><span data-stu-id="71142-127">-Name</span></span>
<span data-ttu-id="71142-128">Nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="71142-128">Name of the private cloud</span></span>

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

### <span data-ttu-id="71142-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="71142-129">-NoWait</span></span>
<span data-ttu-id="71142-130">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="71142-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="71142-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71142-131">-ResourceGroupName</span></span>
<span data-ttu-id="71142-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="71142-132">The name of the resource group.</span></span>
<span data-ttu-id="71142-133">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="71142-133">The name is case insensitive.</span></span>

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

### <span data-ttu-id="71142-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="71142-134">-SubscriptionId</span></span>
<span data-ttu-id="71142-135">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="71142-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="71142-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="71142-136">-Tag</span></span>
<span data-ttu-id="71142-137">Tag di risorse.</span><span class="sxs-lookup"><span data-stu-id="71142-137">Resource tags.</span></span>

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

### <span data-ttu-id="71142-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71142-138">-Confirm</span></span>
<span data-ttu-id="71142-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71142-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71142-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71142-140">-WhatIf</span></span>
<span data-ttu-id="71142-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71142-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71142-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71142-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71142-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71142-143">CommonParameters</span></span>
<span data-ttu-id="71142-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71142-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71142-145">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="71142-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71142-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="71142-146">INPUTS</span></span>

### <span data-ttu-id="71142-147">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span><span class="sxs-lookup"><span data-stu-id="71142-147">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="71142-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71142-148">OUTPUTS</span></span>

### <span data-ttu-id="71142-149">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="71142-149">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="71142-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="71142-150">NOTES</span></span>

<span data-ttu-id="71142-151">ALIAS</span><span class="sxs-lookup"><span data-stu-id="71142-151">ALIASES</span></span>

<span data-ttu-id="71142-152">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="71142-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="71142-153">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="71142-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="71142-154">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="71142-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="71142-155">IDENTITYSOURCE <IIdentitySource[]>: origini identità Single #A0 vCenter</span><span class="sxs-lookup"><span data-stu-id="71142-155">IDENTITYSOURCE <IIdentitySource[]>: vCenter Single Sign On Identity Sources</span></span>
  - <span data-ttu-id="71142-156">`[Alias <String>]`: nome Net PIÙ.SEE del dominio</span><span class="sxs-lookup"><span data-stu-id="71142-156">`[Alias <String>]`: The domain's NetBIOS name</span></span>
  - <span data-ttu-id="71142-157">`[BaseGroupDn <String>]`: nome distinto di base per i gruppi</span><span class="sxs-lookup"><span data-stu-id="71142-157">`[BaseGroupDn <String>]`: The base distinguished name for groups</span></span>
  - <span data-ttu-id="71142-158">`[BaseUserDn <String>]`: nome distinto di base per gli utenti</span><span class="sxs-lookup"><span data-stu-id="71142-158">`[BaseUserDn <String>]`: The base distinguished name for users</span></span>
  - <span data-ttu-id="71142-159">`[Domain <String>]`: nome dns del dominio</span><span class="sxs-lookup"><span data-stu-id="71142-159">`[Domain <String>]`: The domain's dns name</span></span>
  - <span data-ttu-id="71142-160">`[Name <String>]`: nome dell'origine dell'identità</span><span class="sxs-lookup"><span data-stu-id="71142-160">`[Name <String>]`: The name of the identity source</span></span>
  - <span data-ttu-id="71142-161">`[Password <String>]`: la password dell'utente di Active Directory con almeno l'accesso in sola lettura al DN di base per utenti e gruppi.</span><span class="sxs-lookup"><span data-stu-id="71142-161">`[Password <String>]`: The password of the Active Directory user with a minimum of read-only access to Base DN for users and groups.</span></span>
  - <span data-ttu-id="71142-162">`[PrimaryServer <String>]`: URL server principale</span><span class="sxs-lookup"><span data-stu-id="71142-162">`[PrimaryServer <String>]`: Primary server URL</span></span>
  - <span data-ttu-id="71142-163">`[SecondaryServer <String>]`: URL server secondario</span><span class="sxs-lookup"><span data-stu-id="71142-163">`[SecondaryServer <String>]`: Secondary server URL</span></span>
  - <span data-ttu-id="71142-164">`[Ssl <SslEnum?>]`: per proteggere le comunicazioni LDAP con un certificato SSL (LDAPS)</span><span class="sxs-lookup"><span data-stu-id="71142-164">`[Ssl <SslEnum?>]`: Protect LDAP communication using SSL certificate (LDAPS)</span></span>
  - <span data-ttu-id="71142-165">`[Username <String>]`: ID di un utente di Active Directory con almeno l'accesso in sola lettura al DN di base per utenti e gruppi</span><span class="sxs-lookup"><span data-stu-id="71142-165">`[Username <String>]`: The ID of an Active Directory user with a minimum of read-only access to Base DN for users and group</span></span>

<span data-ttu-id="71142-166">INPUTOBJECT <IVMwareIdentity> : parametro identity</span><span class="sxs-lookup"><span data-stu-id="71142-166">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="71142-167">`[AuthorizationName <String>]`: nome dell'autorizzazione del circuito ExpressRoute nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="71142-167">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="71142-168">`[ClusterName <String>]`: nome del cluster nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="71142-168">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="71142-169">`[HcxEnterpriseSiteName <String>]`: nome del sito HCX Enterprise nel cloud privato</span><span class="sxs-lookup"><span data-stu-id="71142-169">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="71142-170">`[Id <String>]`: percorso di identità della risorsa</span><span class="sxs-lookup"><span data-stu-id="71142-170">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="71142-171">`[Location <String>]`: Area geografica Azure</span><span class="sxs-lookup"><span data-stu-id="71142-171">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="71142-172">`[PrivateCloudName <String>]`: nome del cloud privato</span><span class="sxs-lookup"><span data-stu-id="71142-172">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="71142-173">`[ResourceGroupName <String>]`: nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="71142-173">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="71142-174">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="71142-174">The name is case insensitive.</span></span>
  - <span data-ttu-id="71142-175">`[SubscriptionId <String>]`: ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="71142-175">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="71142-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71142-176">RELATED LINKS</span></span>

