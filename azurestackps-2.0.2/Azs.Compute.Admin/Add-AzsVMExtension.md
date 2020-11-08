---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/add-azsvmextension
schema: 2.0.0
ms.openlocfilehash: a9c5a207d478fe40181150206990cb47ad4e45d5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030391"
---
# <span data-ttu-id="e59e9-101">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="e59e9-101">Add-AzsVMExtension</span></span>

## <span data-ttu-id="e59e9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e59e9-102">SYNOPSIS</span></span>
<span data-ttu-id="e59e9-103">Creare un'immagine di estensione della macchina virtuale con Publisher, versione.</span><span class="sxs-lookup"><span data-stu-id="e59e9-103">Create a Virtual Machine Extension Image with publisher, version.</span></span>

## <span data-ttu-id="e59e9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e59e9-104">SYNTAX</span></span>

### <span data-ttu-id="e59e9-105">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e59e9-105">CreateExpanded (Default)</span></span>
```
Add-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String>] [-ComputeRole <String>] [-IsSystemExtension] [-PropertiesPublisher <String>]
 [-ProvisioningState <ProvisioningState>] [-SourceBlob <String>] [-SupportMultipleExtensions]
 [-VmOsType <OSType>] [-VMScaleSetEnabled] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e59e9-106">Creare</span><span class="sxs-lookup"><span data-stu-id="e59e9-106">Create</span></span>
```
Add-AzsVMExtension -Publisher <String> -Type <String> -Version <String> -Extension <IVMExtensionParameters>
 [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="e59e9-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e59e9-107">CreateViaIdentity</span></span>
```
Add-AzsVMExtension -InputObject <IComputeAdminIdentity> -Extension <IVMExtensionParameters>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e59e9-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e59e9-108">CreateViaIdentityExpanded</span></span>
```
Add-AzsVMExtension -InputObject <IComputeAdminIdentity> [-Publisher <String>] [-ComputeRole <String>]
 [-IsSystemExtension] [-ProvisioningState <ProvisioningState>] [-SourceBlob <String>]
 [-SupportMultipleExtensions] [-VmOsType <OSType>] [-VMScaleSetEnabled] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e59e9-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e59e9-109">DESCRIPTION</span></span>
<span data-ttu-id="e59e9-110">Creare un'immagine di estensione della macchina virtuale con Publisher, versione.</span><span class="sxs-lookup"><span data-stu-id="e59e9-110">Create a Virtual Machine Extension Image with publisher, version.</span></span>

## <span data-ttu-id="e59e9-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e59e9-111">EXAMPLES</span></span>

### <span data-ttu-id="e59e9-112">Esempio 1: Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="e59e9-112">Example 1: Add-AzsVMExtension</span></span>
```powershell
PS C:\> Add-AzsVMExtension -Location "local" -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0" -ComputeRole "IaaS" -SourceBlob "https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip" -SupportMultipleExtensions -VmOsType "Linux"

ExtensionType            : MicroExtension
TypeHandlerVersion       : 0.1.0
ComputeRole              : IaaS
Id                       : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locati
                           ons/local/artifactTypes/VMExtension/publishers/Microsoft/types/MicroExtension/versions/0.1.0
IsSystemExtension        : False
Location                 : local
Name                     :
ProvisioningState        : Creating
Publisher                : Microsoft
SourceBlobUri            : https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip
SupportMultipleExtension : True
Type                     : Microsoft.Compute.Admin/locations/artifactTypes/publishers/types/versions
VMScaleSetEnabled        : False
VmosType                 : Linux
```

<span data-ttu-id="e59e9-113">Usa un collegamento accessibile pubblicamente per specificare la posizione dell'estensione oppure l'URI in un BLOB di Azure usando SasUri.</span><span class="sxs-lookup"><span data-stu-id="e59e9-113">Use a publicly accessible link to provide the location of the extension, or the URI to an Azure Blob using the SasUri.</span></span>

## <span data-ttu-id="e59e9-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e59e9-114">PARAMETERS</span></span>

### <span data-ttu-id="e59e9-115">-ComputeRole</span><span class="sxs-lookup"><span data-stu-id="e59e9-115">-ComputeRole</span></span>
<span data-ttu-id="e59e9-116">Ruolo di calcolo</span><span class="sxs-lookup"><span data-stu-id="e59e9-116">Compute role</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e59e9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e59e9-117">-DefaultProfile</span></span>
<span data-ttu-id="e59e9-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e59e9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e59e9-119">-Extension</span><span class="sxs-lookup"><span data-stu-id="e59e9-119">-Extension</span></span>
<span data-ttu-id="e59e9-120">Parametri usati per creare una nuova immagine di estensione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e59e9-120">Parameters used to create a new Virtual Machine Extension Image.</span></span>
<span data-ttu-id="e59e9-121">Per costruire, vedere la sezione Note per le proprietà di estensione e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e59e9-121">To construct, see NOTES section for EXTENSION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtensionParameters
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="e59e9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e59e9-122">-InputObject</span></span>
<span data-ttu-id="e59e9-123">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e59e9-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="e59e9-124">-IsSystemExtension</span><span class="sxs-lookup"><span data-stu-id="e59e9-124">-IsSystemExtension</span></span>
<span data-ttu-id="e59e9-125">Indica se l'estensione è per il sistema.</span><span class="sxs-lookup"><span data-stu-id="e59e9-125">Indicates if the extension is for the system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e59e9-126">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e59e9-126">-Location</span></span>
<span data-ttu-id="e59e9-127">Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e59e9-127">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e59e9-128">-PropertiesPublisher</span><span class="sxs-lookup"><span data-stu-id="e59e9-128">-PropertiesPublisher</span></span>
<span data-ttu-id="e59e9-129">L'editore dell'estensione VM</span><span class="sxs-lookup"><span data-stu-id="e59e9-129">The publisher of the VM Extension</span></span>

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

### <span data-ttu-id="e59e9-130">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="e59e9-130">-ProvisioningState</span></span>
<span data-ttu-id="e59e9-131">Stato di provisioning dell'estensione.</span><span class="sxs-lookup"><span data-stu-id="e59e9-131">Provisioning state of extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Support.ProvisioningState
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e59e9-132">-Publisher</span><span class="sxs-lookup"><span data-stu-id="e59e9-132">-Publisher</span></span>
<span data-ttu-id="e59e9-133">Nome dell'autore.</span><span class="sxs-lookup"><span data-stu-id="e59e9-133">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e59e9-134">-SourceBlob</span><span class="sxs-lookup"><span data-stu-id="e59e9-134">-SourceBlob</span></span>
<span data-ttu-id="e59e9-135">URI in Azure o BLOB AzureStack.</span><span class="sxs-lookup"><span data-stu-id="e59e9-135">URI to Azure or AzureStack blob.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e59e9-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e59e9-136">-SubscriptionId</span></span>
<span data-ttu-id="e59e9-137">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e59e9-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e59e9-138">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="e59e9-138">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e59e9-139">-SupportMultipleExtensions</span><span class="sxs-lookup"><span data-stu-id="e59e9-139">-SupportMultipleExtensions</span></span>
<span data-ttu-id="e59e9-140">True se supporta più estensioni.</span><span class="sxs-lookup"><span data-stu-id="e59e9-140">True if supports multiple extensions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e59e9-141">-Digitare</span><span class="sxs-lookup"><span data-stu-id="e59e9-141">-Type</span></span>
<span data-ttu-id="e59e9-142">Tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="e59e9-142">Type of extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e59e9-143">-Versione</span><span class="sxs-lookup"><span data-stu-id="e59e9-143">-Version</span></span>
<span data-ttu-id="e59e9-144">La versione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e59e9-144">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e59e9-145">-VmOsType</span><span class="sxs-lookup"><span data-stu-id="e59e9-145">-VmOsType</span></span>
<span data-ttu-id="e59e9-146">Tipo di sistema operativo della macchina virtuale di destinazione necessario per la distribuzione del gestore di estensione.</span><span class="sxs-lookup"><span data-stu-id="e59e9-146">Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Support.OSType
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e59e9-147">-VMScaleSetEnabled</span><span class="sxs-lookup"><span data-stu-id="e59e9-147">-VMScaleSetEnabled</span></span>
<span data-ttu-id="e59e9-148">Valore che indica se l'estensione è abilitata per il supporto del set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e59e9-148">Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e59e9-149">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e59e9-149">-Confirm</span></span>
<span data-ttu-id="e59e9-150">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e59e9-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e59e9-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e59e9-151">-WhatIf</span></span>
<span data-ttu-id="e59e9-152">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e59e9-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e59e9-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e59e9-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e59e9-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e59e9-154">CommonParameters</span></span>
<span data-ttu-id="e59e9-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e59e9-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e59e9-156">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e59e9-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e59e9-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e59e9-157">INPUTS</span></span>

### <span data-ttu-id="e59e9-158">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20151201Preview. IVMExtensionParameters</span><span class="sxs-lookup"><span data-stu-id="e59e9-158">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtensionParameters</span></span>

### <span data-ttu-id="e59e9-159">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="e59e9-159">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="e59e9-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e59e9-160">OUTPUTS</span></span>

### <span data-ttu-id="e59e9-161">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20151201Preview. IVMExtension</span><span class="sxs-lookup"><span data-stu-id="e59e9-161">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtension</span></span>



## <span data-ttu-id="e59e9-162">Note</span><span class="sxs-lookup"><span data-stu-id="e59e9-162">NOTES</span></span>

<span data-ttu-id="e59e9-163">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="e59e9-163">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e59e9-164">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e59e9-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e59e9-165">ESTENSIONE <IVMExtensionParameters> : parametri usati per creare una nuova immagine di estensione della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e59e9-165">EXTENSION <IVMExtensionParameters>: Parameters used to create a new Virtual Machine Extension Image.</span></span>
  - <span data-ttu-id="e59e9-166">`[ComputeRole <String>]`: COMPUTE Role</span><span class="sxs-lookup"><span data-stu-id="e59e9-166">`[ComputeRole <String>]`: Compute role</span></span>
  - <span data-ttu-id="e59e9-167">`[IsSystemExtension <Boolean?>]`: Indica se l'estensione è per il sistema.</span><span class="sxs-lookup"><span data-stu-id="e59e9-167">`[IsSystemExtension <Boolean?>]`: Indicates if the extension is for the system.</span></span>
  - <span data-ttu-id="e59e9-168">`[ProvisioningState <ProvisioningState?>]`: Provisioning dello stato di estensione.</span><span class="sxs-lookup"><span data-stu-id="e59e9-168">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of extension.</span></span>
  - <span data-ttu-id="e59e9-169">`[Publisher <String>]`: L'editore dell'estensione VM</span><span class="sxs-lookup"><span data-stu-id="e59e9-169">`[Publisher <String>]`: The publisher of the VM Extension</span></span>
  - <span data-ttu-id="e59e9-170">`[SourceBlobUri <String>]`: URI in Azure o BLOB AzureStack.</span><span class="sxs-lookup"><span data-stu-id="e59e9-170">`[SourceBlobUri <String>]`: URI to Azure or AzureStack blob.</span></span>
  - <span data-ttu-id="e59e9-171">`[SupportMultipleExtension <Boolean?>]`: True se supporta più estensioni.</span><span class="sxs-lookup"><span data-stu-id="e59e9-171">`[SupportMultipleExtension <Boolean?>]`: True if supports multiple extensions.</span></span>
  - <span data-ttu-id="e59e9-172">`[VMScaleSetEnabled <Boolean?>]`: Valore che indica se l'estensione è abilitata per il supporto del set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e59e9-172">`[VMScaleSetEnabled <Boolean?>]`: Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>
  - <span data-ttu-id="e59e9-173">`[VmosType <OSType?>]`: Tipo di sistema operativo della macchina virtuale di destinazione necessario per la distribuzione del gestore di estensione.</span><span class="sxs-lookup"><span data-stu-id="e59e9-173">`[VmosType <OSType?>]`: Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

<span data-ttu-id="e59e9-174">INPUTOBJECT <IComputeAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="e59e9-174">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e59e9-175">`[DiskId <String>]`: GUID del disco come identità.</span><span class="sxs-lookup"><span data-stu-id="e59e9-175">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="e59e9-176">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="e59e9-176">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e59e9-177">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e59e9-177">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="e59e9-178">`[MigrationId <String>]`: Nome GUID processo di migrazione.</span><span class="sxs-lookup"><span data-stu-id="e59e9-178">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="e59e9-179">`[Offer <String>]`: Nome dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="e59e9-179">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="e59e9-180">`[Publisher <String>]`: Nome del server di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="e59e9-180">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="e59e9-181">`[QuotaName <String>]`: Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="e59e9-181">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="e59e9-182">`[Sku <String>]`: Nome dell'USK.</span><span class="sxs-lookup"><span data-stu-id="e59e9-182">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="e59e9-183">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e59e9-183">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e59e9-184">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="e59e9-184">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="e59e9-185">`[Type <String>]`: Tipo di estensione.</span><span class="sxs-lookup"><span data-stu-id="e59e9-185">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="e59e9-186">`[Version <String>]`: La versione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e59e9-186">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="e59e9-187">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e59e9-187">RELATED LINKS</span></span>

