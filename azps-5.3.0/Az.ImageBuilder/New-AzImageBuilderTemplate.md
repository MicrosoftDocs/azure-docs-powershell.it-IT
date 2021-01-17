---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/New-AzImageBuilderTemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/New-AzImageBuilderTemplate.md
ms.openlocfilehash: 337584fb7f960f64ee94c5206f9bf60b0cc6c21a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386791"
---
# <span data-ttu-id="0e704-101">New-AzImageBuilderTemplate</span><span class="sxs-lookup"><span data-stu-id="0e704-101">New-AzImageBuilderTemplate</span></span>

## <span data-ttu-id="0e704-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0e704-102">SYNOPSIS</span></span>
<span data-ttu-id="0e704-103">Creare un modello di immagine della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="0e704-103">Create a virtual machine image template</span></span>

## <span data-ttu-id="0e704-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0e704-104">SYNTAX</span></span>

```
New-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 -Distribute <IImageTemplateDistributor[]> -Source <IImageTemplateSource> -UserAssignedIdentityId <String>
 [-SubscriptionId <String>] [-BuildTimeoutInMinute <Int32>] [-Customize <IImageTemplateCustomizer[]>]
 [-LastRunStatusEndTime <DateTime>] [-LastRunStatusMessage <String>] [-LastRunStatusRunState <RunState>]
 [-LastRunStatusRunSubState <RunSubState>] [-LastRunStatusStartTime <DateTime>] [-Location <String>]
 [-ProvisioningErrorCode <ProvisioningErrorCode>] [-ProvisioningErrorMessage <String>] [-Tag <Hashtable>]
 [-VMProfileOsdiskSizeInGb <Int32>] [-VMProfileVmSize <String>] [-VnetConfigSubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0e704-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e704-105">DESCRIPTION</span></span>
<span data-ttu-id="0e704-106">Creare un modello di immagine della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="0e704-106">Create a virtual machine image template</span></span>

## <span data-ttu-id="0e704-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0e704-107">EXAMPLES</span></span>

### <span data-ttu-id="0e704-108">Esempio 1: creare un modello di immagine della macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="0e704-108">Example 1: Create a virtual machine image template</span></span>
```powershell
PS C:\> $srcPlatform = New-AzImageBuilderSourceObject -SourceTypePlatformImage -Publisher 'Canonical'  -Offer 'UbuntuServer' -Sku '18.04-LTS' -Version 'latest'
PS C:\> $disSharedImg = New-AzImageBuilderDistributorObject -SharedImageDistributor -ArtifactTag @{tag='dis-share'} -GalleryImageId '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/wyunchi-imagebuilder/providers/Microsoft.Compute/galleries/testsharedgallery/images/imagedefinition-linux/versions/1.0.0' -ReplicationRegion 'eastus2' -RunOutputName 'runoutput-01'  -ExcludeFromLatest $false
PS C:\> $customizer = New-AzImageBuilderCustomizerObject -ShellCustomizer -CustomizerName 'CheckSumCompareShellScript' -ScriptUri 'https://raw.githubusercontent.com/danielsollondon/azvmimagebuilder/master/quickquickstarts/customizeScript2.sh' -Sha256Checksum 'ade4c5214c3c675e92c66e2d067a870c5b81b9844b3de3cc72c49ff36425fc93'
PS C:\> $userAssignedIdentity = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/wyunchi-imagebuilder/providers/Microsoft.ManagedIdentity/userAssignedIdentities/image-builder-user-assign-identity'
PS C:\> New-AzImageBuilderTemplate -ImageTemplateName platform-shared-img -ResourceGroupName wyunchi-imagebuilder -Source $srcPlatform -Distribute $disSharedImg -Customize $customizer -Location eastus  -UserAssignedIdentityId $userAssignedIdentity

Location Name                Type
-------- ----                ----
PlanInfoPlanName      :
PlanInfoPlanPublisher :
Sku                   : 18.04-LTS
Version               : latest
PlanInfo              : Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.PlatformImagePurchasePlan
```

<span data-ttu-id="0e704-109">Questo comando crea un modello di immagine della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0e704-109">This commands creates a virtual machine image template.</span></span>

## <span data-ttu-id="0e704-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0e704-110">PARAMETERS</span></span>

### <span data-ttu-id="0e704-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e704-111">-AsJob</span></span>
<span data-ttu-id="0e704-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="0e704-112">Run the command as a job</span></span>

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

### <span data-ttu-id="0e704-113">-BuildTimeoutInMinute</span><span class="sxs-lookup"><span data-stu-id="0e704-113">-BuildTimeoutInMinute</span></span>
<span data-ttu-id="0e704-114">Durata massima da attendere durante la creazione del modello di immagine.</span><span class="sxs-lookup"><span data-stu-id="0e704-114">Maximum duration to wait while building the image template.</span></span>
<span data-ttu-id="0e704-115">Omettere o specificare 0 per usare il valore predefinito (4 ore).</span><span class="sxs-lookup"><span data-stu-id="0e704-115">Omit or specify 0 to use the default (4 hours).</span></span>

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

### <span data-ttu-id="0e704-116">-Personalizza</span><span class="sxs-lookup"><span data-stu-id="0e704-116">-Customize</span></span>
<span data-ttu-id="0e704-117">Specifica le proprietà usate per descrivere i passaggi di personalizzazione dell'immagine, come l'origine dell'immagine e così via. Per costruire, vedere la sezione Note per personalizzare le proprietà e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="0e704-117">Specifies the properties used to describe the customization steps of the image, like Image source etc. To construct, see NOTES section for CUSTOMIZE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateCustomizer[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e704-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e704-118">-DefaultProfile</span></span>
<span data-ttu-id="0e704-119">Region HideParameter le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0e704-119">region HideParameter The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e704-120">-Distribuire</span><span class="sxs-lookup"><span data-stu-id="0e704-120">-Distribute</span></span>
<span data-ttu-id="0e704-121">Le destinazioni di distribuzione in cui deve andare l'output dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="0e704-121">The distribution targets where the image output needs to go to.</span></span>
<span data-ttu-id="0e704-122">Per costruire, vedere la sezione Note per distribuire le proprietà e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="0e704-122">To construct, see NOTES section for DISTRIBUTE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateDistributor[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e704-123">-ImageTemplateName</span><span class="sxs-lookup"><span data-stu-id="0e704-123">-ImageTemplateName</span></span>
<span data-ttu-id="0e704-124">Nome del modello di immagine.</span><span class="sxs-lookup"><span data-stu-id="0e704-124">The name of the image Template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e704-125">-LastRunStatusEndTime</span><span class="sxs-lookup"><span data-stu-id="0e704-125">-LastRunStatusEndTime</span></span>
<span data-ttu-id="0e704-126">Ora di fine dell'ultima esecuzione (UTC).</span><span class="sxs-lookup"><span data-stu-id="0e704-126">End time of the last run (UTC).</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e704-127">-LastRunStatusMessage</span><span class="sxs-lookup"><span data-stu-id="0e704-127">-LastRunStatusMessage</span></span>
<span data-ttu-id="0e704-128">Informazioni dettagliate sull'ultimo stato di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="0e704-128">Verbose information about the last run state.</span></span>

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

### <span data-ttu-id="0e704-129">-LastRunStatusRunState</span><span class="sxs-lookup"><span data-stu-id="0e704-129">-LastRunStatusRunState</span></span>
<span data-ttu-id="0e704-130">Stato dell'ultima esecuzione.</span><span class="sxs-lookup"><span data-stu-id="0e704-130">State of the last run.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.RunState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e704-131">-LastRunStatusRunSubState</span><span class="sxs-lookup"><span data-stu-id="0e704-131">-LastRunStatusRunSubState</span></span>
<span data-ttu-id="0e704-132">Stato secondario dell'ultima esecuzione.</span><span class="sxs-lookup"><span data-stu-id="0e704-132">Sub-state of the last run.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.RunSubState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e704-133">-LastRunStatusStartTime</span><span class="sxs-lookup"><span data-stu-id="0e704-133">-LastRunStatusStartTime</span></span>
<span data-ttu-id="0e704-134">Ora di inizio dell'ultima esecuzione (UTC).</span><span class="sxs-lookup"><span data-stu-id="0e704-134">Start time of the last run (UTC).</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e704-135">-Posizione</span><span class="sxs-lookup"><span data-stu-id="0e704-135">-Location</span></span>
<span data-ttu-id="0e704-136">Posizione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="0e704-136">Resource location.</span></span>

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

### <span data-ttu-id="0e704-137">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="0e704-137">-NoWait</span></span>
<span data-ttu-id="0e704-138">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="0e704-138">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0e704-139">-ProvisioningErrorCode</span><span class="sxs-lookup"><span data-stu-id="0e704-139">-ProvisioningErrorCode</span></span>
<span data-ttu-id="0e704-140">Codice di errore dell'errore di provisioning.</span><span class="sxs-lookup"><span data-stu-id="0e704-140">Error code of the provisioning failure.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Support.ProvisioningErrorCode
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e704-141">-ProvisioningErrorMessage</span><span class="sxs-lookup"><span data-stu-id="0e704-141">-ProvisioningErrorMessage</span></span>
<span data-ttu-id="0e704-142">Messaggio di errore dettagliato relativo all'errore di provisioning.</span><span class="sxs-lookup"><span data-stu-id="0e704-142">Verbose error message about the provisioning failure.</span></span>

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

### <span data-ttu-id="0e704-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e704-143">-ResourceGroupName</span></span>
<span data-ttu-id="0e704-144">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0e704-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="0e704-145">-Origine</span><span class="sxs-lookup"><span data-stu-id="0e704-145">-Source</span></span>
<span data-ttu-id="0e704-146">Descrive un'origine di immagine della macchina virtuale per la creazione, la personalizzazione e la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="0e704-146">Describes a virtual machine image source for building, customizing and distributing.</span></span>
<span data-ttu-id="0e704-147">Per costruire, vedere la sezione Note per le proprietà di origine e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="0e704-147">To construct, see NOTES section for SOURCE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplateSource
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e704-148">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0e704-148">-SubscriptionId</span></span>
<span data-ttu-id="0e704-149">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0e704-149">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>

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

### <span data-ttu-id="0e704-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="0e704-150">-Tag</span></span>
<span data-ttu-id="0e704-151">Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="0e704-151">Resource tags.</span></span>

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

### <span data-ttu-id="0e704-152">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="0e704-152">-UserAssignedIdentityId</span></span>
<span data-ttu-id="0e704-153">ID dell'identità assegnata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="0e704-153">The id of user assigned identity.</span></span>

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

### <span data-ttu-id="0e704-154">-VMProfileOsdiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="0e704-154">-VMProfileOsdiskSizeInGb</span></span>
<span data-ttu-id="0e704-155">Dimensioni del disco del sistema operativo in GB.</span><span class="sxs-lookup"><span data-stu-id="0e704-155">Size of the OS disk in GB.</span></span>
<span data-ttu-id="0e704-156">Omettere o specificare 0 per usare le dimensioni del disco operativo predefinite di Azure.</span><span class="sxs-lookup"><span data-stu-id="0e704-156">Omit or specify 0 to use Azure's default OS disk size.</span></span>

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

### <span data-ttu-id="0e704-157">-VMProfileVmSize</span><span class="sxs-lookup"><span data-stu-id="0e704-157">-VMProfileVmSize</span></span>
<span data-ttu-id="0e704-158">Dimensioni della macchina virtuale usata per creare, personalizzare e acquisire immagini.</span><span class="sxs-lookup"><span data-stu-id="0e704-158">Size of the virtual machine used to build, customize and capture images.</span></span>
<span data-ttu-id="0e704-159">Omettere o specificare una stringa vuota per usare il valore predefinito (Standard_D1_v2).</span><span class="sxs-lookup"><span data-stu-id="0e704-159">Omit or specify empty string to use the default (Standard_D1_v2).</span></span>

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

### <span data-ttu-id="0e704-160">-VnetConfigSubnetId</span><span class="sxs-lookup"><span data-stu-id="0e704-160">-VnetConfigSubnetId</span></span>
<span data-ttu-id="0e704-161">ID risorsa di una subnet preesistente.</span><span class="sxs-lookup"><span data-stu-id="0e704-161">Resource id of a pre-existing subnet.</span></span>

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

### <span data-ttu-id="0e704-162">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0e704-162">-Confirm</span></span>
<span data-ttu-id="0e704-163">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e704-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e704-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e704-164">-WhatIf</span></span>
<span data-ttu-id="0e704-165">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0e704-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e704-166">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0e704-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e704-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e704-167">CommonParameters</span></span>
<span data-ttu-id="0e704-168">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e704-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e704-169">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e704-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e704-170">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0e704-170">INPUTS</span></span>

## <span data-ttu-id="0e704-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0e704-171">OUTPUTS</span></span>

### <span data-ttu-id="0e704-172">Microsoft. Azure. PowerShell. Cmdlets. ImageBuilder. Models. Api20200214. IImageTemplate</span><span class="sxs-lookup"><span data-stu-id="0e704-172">Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.Api20200214.IImageTemplate</span></span>

## <span data-ttu-id="0e704-173">Note</span><span class="sxs-lookup"><span data-stu-id="0e704-173">NOTES</span></span>

<span data-ttu-id="0e704-174">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0e704-174">ALIASES</span></span>

<span data-ttu-id="0e704-175">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0e704-175">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0e704-176">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="0e704-176">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0e704-177">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0e704-177">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0e704-178">CUSTOMIZe <IImageTemplateCustomizer [] >: specifica le proprietà usate per descrivere i passaggi di personalizzazione dell'immagine, come l'origine dell'immagine e così via.</span><span class="sxs-lookup"><span data-stu-id="0e704-178">CUSTOMIZE <IImageTemplateCustomizer[]>: Specifies the properties used to describe the customization steps of the image, like Image source etc.</span></span>
  - <span data-ttu-id="0e704-179">`Type <String>`: Il tipo di strumento di personalizzazione che si vuole usare nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="0e704-179">`Type <String>`: The type of customization tool you want to use on the Image.</span></span> <span data-ttu-id="0e704-180">Ad esempio, "Shell" può essere Shell Customizer</span><span class="sxs-lookup"><span data-stu-id="0e704-180">For example, "Shell" can be shell customizer</span></span>
  - <span data-ttu-id="0e704-181">`[Name <String>]`: Nome descrittivo per specificare il contesto per il passaggio di personalizzazione</span><span class="sxs-lookup"><span data-stu-id="0e704-181">`[Name <String>]`: Friendly Name to provide context on what this customization step does</span></span>

<span data-ttu-id="0e704-182">DISTRIBUIRE <IImageTemplateDistributor [] >: le destinazioni di distribuzione in cui deve andare l'output dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="0e704-182">DISTRIBUTE <IImageTemplateDistributor[]>: The distribution targets where the image output needs to go to.</span></span>
  - <span data-ttu-id="0e704-183">`RunOutputName <String>`: Nome da usare per il RunOutput associato.</span><span class="sxs-lookup"><span data-stu-id="0e704-183">`RunOutputName <String>`: The name to be used for the associated RunOutput.</span></span>
  - <span data-ttu-id="0e704-184">`Type <String>`: Tipo di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="0e704-184">`Type <String>`: Type of distribution.</span></span>
  - <span data-ttu-id="0e704-185">`[ArtifactTag <IImageTemplateDistributorArtifactTags>]`: Tag che verranno applicati all'elemento dopo la creazione/aggiornamento da parte del server di distribuzione.</span><span class="sxs-lookup"><span data-stu-id="0e704-185">`[ArtifactTag <IImageTemplateDistributorArtifactTags>]`: Tags that will be applied to the artifact once it has been created/updated by the distributor.</span></span>
    - <span data-ttu-id="0e704-186">`[(Any) <String>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="0e704-186">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>

<span data-ttu-id="0e704-187">ORIGINE <IImageTemplateSource> : descrive un'origine delle immagini di una macchina virtuale per la creazione, la personalizzazione e la distribuzione.</span><span class="sxs-lookup"><span data-stu-id="0e704-187">SOURCE <IImageTemplateSource>: Describes a virtual machine image source for building, customizing and distributing.</span></span>
  - <span data-ttu-id="0e704-188">`Type <String>`: Specifica il tipo di immagine di origine con cui si vuole iniziare.</span><span class="sxs-lookup"><span data-stu-id="0e704-188">`Type <String>`: Specifies the type of source image you want to start with.</span></span>

## <span data-ttu-id="0e704-189">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0e704-189">RELATED LINKS</span></span>

