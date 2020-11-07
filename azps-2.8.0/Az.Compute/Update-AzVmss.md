---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: c8a482c4d3021e1dd5de30582d2dad501a20ed41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675108"
---
# <span data-ttu-id="2c2ea-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2c2ea-101">Update-AzVmss</span></span>

## <span data-ttu-id="2c2ea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2c2ea-102">SYNOPSIS</span></span>
<span data-ttu-id="2c2ea-103">Aggiorna lo stato di un VMSS.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="2c2ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2c2ea-104">SYNTAX</span></span>

### <span data-ttu-id="2c2ea-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2c2ea-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-BootDiagnosticsStorageUri <String>] [-CustomData <String>]
 [-DisableAutoRollback <Boolean>] [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticUpdate <Boolean>]
 [-ImageReferenceId <String>] [-ImageReferenceOffer <String>] [-ImageReferencePublisher <String>]
 [-ImageReferenceSku <String>] [-ImageReferenceVersion <String>] [-ImageUri <String>] [-LicenseType <String>]
 [-ManagedDiskStorageAccountType <String>] [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>]
 [-MaxUnhealthyInstancePercent <Int32>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-OsDiskCaching <CachingTypes>] [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>]
 [-PauseTimeBetweenBatches <String>] [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>] [-SinglePlacementGroup <Boolean>]
 [-SkuCapacity <Int32>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c2ea-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c2ea-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-AutomaticOSUpgrade <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-BootDiagnosticsStorageUri <String>] [-CustomData <String>]
 [-DisableAutoRollback <Boolean>] [-DisablePasswordAuthentication <Boolean>] [-EnableAutomaticUpdate <Boolean>]
 [-IdentityId <String[]>] -IdentityType <ResourceIdentityType> [-ImageReferenceId <String>]
 [-ImageReferenceOffer <String>] [-ImageReferencePublisher <String>] [-ImageReferenceSku <String>]
 [-ImageReferenceVersion <String>] [-ImageUri <String>] [-LicenseType <String>]
 [-ManagedDiskStorageAccountType <String>] [-MaxBatchInstancePercent <Int32>] [-MaxPrice <Double>]
 [-MaxUnhealthyInstancePercent <Int32>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-OsDiskCaching <CachingTypes>] [-OsDiskWriteAccelerator <Boolean>] [-Overprovision <Boolean>]
 [-PauseTimeBetweenBatches <String>] [-PlanName <String>] [-PlanProduct <String>] [-PlanPromotionCode <String>]
 [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>] [-SinglePlacementGroup <Boolean>]
 [-SkuCapacity <Int32>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TerminateScheduledEventNotBeforeTimeoutInMinutes <Int32>] [-TerminateScheduledEvents <Boolean>]
 [-TimeZone <String>] [-UltraSSDEnabled <Boolean>] [-UpgradePolicyMode <UpgradeMode>]
 [-VhdContainer <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c2ea-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c2ea-107">DESCRIPTION</span></span>
<span data-ttu-id="2c2ea-108">Il cmdlet **Update-AzVmss** aggiorna lo stato di un set di scale della macchina virtuale (VMSS) allo stato di un oggetto vmss locale.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="2c2ea-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2c2ea-109">EXAMPLES</span></span>

### <span data-ttu-id="2c2ea-110">Esempio 1: aggiornare lo stato di un VMSS allo stato di un oggetto VMSS locale.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="2c2ea-111">Questo comando Aggiorna lo stato del VMSS denominato VMSS001 che appartiene al gruppo di risorse denominato Group001 allo stato di un oggetto VMSS locale, $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="2c2ea-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2c2ea-112">PARAMETERS</span></span>

### <span data-ttu-id="2c2ea-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2c2ea-113">-AsJob</span></span>
<span data-ttu-id="2c2ea-114">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="2c2ea-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="2c2ea-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="2c2ea-116">Imposta se gli aggiornamenti del sistema operativo devono essere applicati automaticamente alle istanze del set di scala in modo scorrevole quando una versione più recente dell'immagine diventa disponibile.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c2ea-117">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="2c2ea-117">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="2c2ea-118">Se la diagnostica di avvio deve essere abilitata nel set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-118">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c2ea-119">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="2c2ea-119">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="2c2ea-120">URI dell'account di archiviazione da usare per posizionare l'output e la schermata della console.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-120">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="2c2ea-121">-CustomData</span><span class="sxs-lookup"><span data-stu-id="2c2ea-121">-CustomData</span></span>
<span data-ttu-id="2c2ea-122">Specifica una stringa codificata di base-64 di dati personalizzati.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-122">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="2c2ea-123">Questa operazione viene decodificata in una matrice binaria che viene salvata come file nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-123">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="2c2ea-124">La lunghezza massima della matrice binaria è di 65535 byte.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-124">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="2c2ea-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c2ea-125">-DefaultProfile</span></span>
<span data-ttu-id="2c2ea-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c2ea-127">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="2c2ea-127">-DisableAutoRollback</span></span>
<span data-ttu-id="2c2ea-128">Disabilitare il rollback automatico per i criteri di aggiornamento del sistema operativo automatico</span><span class="sxs-lookup"><span data-stu-id="2c2ea-128">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c2ea-129">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="2c2ea-129">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="2c2ea-130">Indica che questo cmdlet disabilita l'autenticazione tramite password per il sistema operativo Linux.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-130">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c2ea-131">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="2c2ea-131">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="2c2ea-132">Indica se le macchine virtuali Windows in VMSS sono abilitate per gli aggiornamenti automatici.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-132">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c2ea-133">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="2c2ea-133">-IdentityId</span></span>
<span data-ttu-id="2c2ea-134">Specifica l'elenco delle identità utente associate al set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-134">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="2c2ea-135">I riferimenti di identità utente saranno ID delle risorse ARM nella forma:'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="2c2ea-135">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c2ea-136">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="2c2ea-136">-IdentityType</span></span>
<span data-ttu-id="2c2ea-137">Specifica il tipo di identità usato per il set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-137">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="2c2ea-138">Il tipo ' SystemAssignedUserAssigned ' include sia un'identità creata in modo implicito che un set di identità assegnate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-138">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="2c2ea-139">Il tipo "None" rimuoverà le identità dal set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-139">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="2c2ea-140">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="2c2ea-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2c2ea-141">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="2c2ea-141">SystemAssigned</span></span>
- <span data-ttu-id="2c2ea-142">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="2c2ea-142">UserAssigned</span></span>
- <span data-ttu-id="2c2ea-143">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="2c2ea-143">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="2c2ea-144">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2c2ea-144">None</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: ExplicitIdentityParameterSet
Aliases:
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c2ea-145">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="2c2ea-145">-ImageReferenceId</span></span>
<span data-ttu-id="2c2ea-146">Specifica l'ID riferimento immagine.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-146">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="2c2ea-147">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="2c2ea-147">-ImageReferenceOffer</span></span>
<span data-ttu-id="2c2ea-148">Specifica il tipo di offerta VMImage (Virtual Machine Image).</span><span class="sxs-lookup"><span data-stu-id="2c2ea-148">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="2c2ea-149">Per ottenere un'offerta di immagine, usare il cmdlet Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-149">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="2c2ea-150">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="2c2ea-150">-ImageReferencePublisher</span></span>
<span data-ttu-id="2c2ea-151">Specifica il nome di un autore di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-151">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="2c2ea-152">Per ottenere un autore, usare il cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-152">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="2c2ea-153">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="2c2ea-153">-ImageReferenceSku</span></span>
<span data-ttu-id="2c2ea-154">Specifica la SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-154">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="2c2ea-155">Per ottenere SKU, usare il cmdlet Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-155">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="2c2ea-156">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="2c2ea-156">-ImageReferenceVersion</span></span>
<span data-ttu-id="2c2ea-157">Specifica la versione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-157">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="2c2ea-158">Per usare la versione più recente, specificare il valore più recente invece di una determinata versione.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-158">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="2c2ea-159">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="2c2ea-159">-ImageUri</span></span>
<span data-ttu-id="2c2ea-160">Specifica l'URI BLOB per l'immagine utente.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-160">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="2c2ea-161">VMSS crea un disco del sistema operativo nello stesso contenitore dell'immagine utente.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-161">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="2c2ea-162">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="2c2ea-162">-LicenseType</span></span>
<span data-ttu-id="2c2ea-163">Specificare il tipo di licenza, che è per portare il proprio scenario di licenza.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-163">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="2c2ea-164">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="2c2ea-164">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="2c2ea-165">Specifica il tipo di account di archiviazione per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-165">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="2c2ea-166">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="2c2ea-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2c2ea-167">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="2c2ea-167">StandardLRS</span></span>
- <span data-ttu-id="2c2ea-168">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="2c2ea-168">PremiumLRS</span></span>

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

### <span data-ttu-id="2c2ea-169">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="2c2ea-169">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="2c2ea-170">Percentuale massima delle istanze totali della macchina virtuale che verranno aggiornate simultaneamente dall'aggiornamento a rotazione in un unico batch.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-170">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="2c2ea-171">Poiché si tratta di un massimo, le istanze non sane nei batch precedenti o futuri possono causare una diminuzione della percentuale di istanze in un batch per garantire maggiore affidabilità.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-171">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="2c2ea-172">Se il valore non è specificato, viene impostato su 20.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-172">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="2c2ea-173">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="2c2ea-173">-MaxPrice</span></span>
<span data-ttu-id="2c2ea-174">Specifica il prezzo massimo che si vuole pagare per una VM/VMSS a priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-174">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="2c2ea-175">Questo prezzo è in dollari USA.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-175">This price is in US Dollars.</span></span> <span data-ttu-id="2c2ea-176">Questo prezzo verrà confrontato con il prezzo corrente con priorità bassa per le dimensioni della VM.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-176">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="2c2ea-177">Inoltre, i prezzi vengono confrontati al momento della creazione/aggiornamento della priorità bassa VM/VMSS e l'operazione avrà esito positivo solo se maxPrice è maggiore del prezzo corrente con priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-177">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="2c2ea-178">Il maxPrice verrà usato anche per rimuovere una VM/VMSS a priorità bassa se il prezzo corrente con priorità bassa supera il maxPrice dopo la creazione di VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-178">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="2c2ea-179">I valori possibili sono: qualsiasi valore decimale maggiore di zero.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-179">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="2c2ea-180">Esempio: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-180">Example: 0.01538.</span></span>  <span data-ttu-id="2c2ea-181">-1 indica che la priorità bassa VM/VMSS non deve essere sfrattata per motivi di prezzo.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-181">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="2c2ea-182">Inoltre, il prezzo massimo predefinito è-1 se non è fornito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-182">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c2ea-183">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="2c2ea-183">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="2c2ea-184">La percentuale massima delle istanze totali della macchina virtuale nel set di proporzioni che possono essere non sane contemporaneamente, come risultato dell'aggiornamento o per essere stati trovati in uno stato non sano dai controlli di integrità della macchina virtuale prima dell'interruzione dell'aggiornamento a rotazione.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-184">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="2c2ea-185">Questo vincolo verrà controllato prima di iniziare qualsiasi batch.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-185">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="2c2ea-186">Se il valore non è specificato, viene impostato su 20.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-186">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="2c2ea-187">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="2c2ea-187">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="2c2ea-188">La percentuale massima delle istanze di macchine virtuali aggiornate che possono essere trovate in uno stato non sano.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-188">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="2c2ea-189">Questo controllo avverrà dopo l'aggiornamento di ogni batch.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-189">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="2c2ea-190">Se questa percentuale viene mai superata, l'aggiornamento a rotazione viene interrotto.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-190">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="2c2ea-191">Se il valore non è specificato, viene impostato su 20.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-191">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="2c2ea-192">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="2c2ea-192">-OsDiskCaching</span></span>
<span data-ttu-id="2c2ea-193">Specifica la modalità di memorizzazione nella cache del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-193">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="2c2ea-194">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="2c2ea-194">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2c2ea-195">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2c2ea-195">None</span></span>
- <span data-ttu-id="2c2ea-196">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="2c2ea-196">ReadOnly</span></span>
- <span data-ttu-id="2c2ea-197">ReadWrite il valore predefinito è ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-197">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="2c2ea-198">Se si modifica il valore di memorizzazione nella cache, il cmdlet riavvia la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-198">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="2c2ea-199">Questa impostazione influenza la coerenza e le prestazioni del disco.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-199">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c2ea-200">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="2c2ea-200">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="2c2ea-201">Specifica se WriteAccelerator deve essere abilitato o disabilitato nel disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-201">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c2ea-202">-Provisioning</span><span class="sxs-lookup"><span data-stu-id="2c2ea-202">-Overprovision</span></span>
<span data-ttu-id="2c2ea-203">Indica se il cmdlet viene sovradisposto da VMSS.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-203">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c2ea-204">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="2c2ea-204">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="2c2ea-205">Il tempo di attesa tra il completamento dell'aggiornamento per tutte le macchine virtuali in un unico batch e l'avvio del batch successivo.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-205">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="2c2ea-206">La durata dell'ora deve essere specificata nel formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-206">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="2c2ea-207">Il valore predefinito è 0 secondi (PT0S).</span><span class="sxs-lookup"><span data-stu-id="2c2ea-207">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="2c2ea-208">-PlanName</span><span class="sxs-lookup"><span data-stu-id="2c2ea-208">-PlanName</span></span>
<span data-ttu-id="2c2ea-209">Specifica il nome del piano.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-209">Specifies the plan name.</span></span>

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

### <span data-ttu-id="2c2ea-210">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="2c2ea-210">-PlanProduct</span></span>
<span data-ttu-id="2c2ea-211">Specifica il prodotto piano.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-211">Specifies the plan product.</span></span>

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

### <span data-ttu-id="2c2ea-212">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="2c2ea-212">-PlanPromotionCode</span></span>
<span data-ttu-id="2c2ea-213">Specifica il codice promozionale per il piano.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-213">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="2c2ea-214">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="2c2ea-214">-PlanPublisher</span></span>
<span data-ttu-id="2c2ea-215">Specifica il piano Publisher.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-215">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="2c2ea-216">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="2c2ea-216">-ProvisionVMAgent</span></span>
<span data-ttu-id="2c2ea-217">Indica se l'agente macchina virtuale deve essere eseguito il provisioning nelle macchine virtuali di Windows in VMSS.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-217">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c2ea-218">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c2ea-218">-ResourceGroupName</span></span>
<span data-ttu-id="2c2ea-219">Specifica il nome del gruppo di risorse a cui appartiene VMSS.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-219">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c2ea-220">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="2c2ea-220">-SinglePlacementGroup</span></span>
<span data-ttu-id="2c2ea-221">Specifica il gruppo di posizionamento singolo.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-221">Specifies the single placement group.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c2ea-222">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="2c2ea-222">-SkuCapacity</span></span>
<span data-ttu-id="2c2ea-223">Specifica il numero di istanze in VMSS.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-223">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="2c2ea-224">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2c2ea-224">-SkuName</span></span>
<span data-ttu-id="2c2ea-225">Specifica le dimensioni di tutte le istanze di VMSS.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-225">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="2c2ea-226">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="2c2ea-226">-SkuTier</span></span>
<span data-ttu-id="2c2ea-227">Specifica il livello di VMSS.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-227">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="2c2ea-228">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="2c2ea-228">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2c2ea-229">Standard</span><span class="sxs-lookup"><span data-stu-id="2c2ea-229">Standard</span></span>
- <span data-ttu-id="2c2ea-230">Base</span><span class="sxs-lookup"><span data-stu-id="2c2ea-230">Basic</span></span>

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

### <span data-ttu-id="2c2ea-231">-Tag</span><span class="sxs-lookup"><span data-stu-id="2c2ea-231">-Tag</span></span>
<span data-ttu-id="2c2ea-232">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-232">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2c2ea-233">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="2c2ea-233">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2c2ea-234">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="2c2ea-234">-TerminateScheduledEventNotBeforeTimeoutInMinutes</span></span>
<span data-ttu-id="2c2ea-235">Intervallo di tempo configurabile (in minuti) una macchina virtuale che viene eliminata dovrà approvare l'evento di terminazione pianificata prima che l'evento venga approvato automaticamente (scaduta).</span><span class="sxs-lookup"><span data-stu-id="2c2ea-235">Configurable length of time (in minutes) a Virtual Machine being deleted will have to potentially approve the Terminate Scheduled Event before the event is auto approved (timed out).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c2ea-236">-TerminateScheduledEvents</span><span class="sxs-lookup"><span data-stu-id="2c2ea-236">-TerminateScheduledEvents</span></span>
<span data-ttu-id="2c2ea-237">Specifica se l'evento di terminazione pianificata è abilitato o disabilitato.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-237">Specifies whether the Terminate Scheduled event is enabled or disabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c2ea-238">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="2c2ea-238">-TimeZone</span></span>
<span data-ttu-id="2c2ea-239">Specifica il fuso orario per il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-239">Specifies the time zone for Windows OS.</span></span>

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

### <span data-ttu-id="2c2ea-240">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="2c2ea-240">-UltraSSDEnabled</span></span>
<span data-ttu-id="2c2ea-241">Il contrassegno che Abilita o Disabilita una funzionalità per avere uno o più dischi di dati gestiti con UltraSSD_LRS tipo di account di archiviazione nel set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-241">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="2c2ea-242">Dischi gestiti con tipo di account di archiviazione UltraSSD_LRS può essere aggiunto a un VMSS solo se questa proprietà è abilitata.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-242">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c2ea-243">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="2c2ea-243">-UpgradePolicyMode</span></span>
<span data-ttu-id="2c2ea-244">Specifica la modalità di aggiornamento delle macchine virtuali nel set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-244">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="2c2ea-245">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="2c2ea-245">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2c2ea-246">Automatico</span><span class="sxs-lookup"><span data-stu-id="2c2ea-246">Automatic</span></span>
- <span data-ttu-id="2c2ea-247">Manuale</span><span class="sxs-lookup"><span data-stu-id="2c2ea-247">Manual</span></span>
- <span data-ttu-id="2c2ea-248">Implementazione</span><span class="sxs-lookup"><span data-stu-id="2c2ea-248">Rolling</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.UpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c2ea-249">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="2c2ea-249">-VhdContainer</span></span>
<span data-ttu-id="2c2ea-250">Specifica gli URL del contenitore usati per archiviare i dischi del sistema operativo per VMSS.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-250">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="2c2ea-251">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2c2ea-251">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="2c2ea-252">Specifica un oggetto VMSS locale.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-252">Specifies a local VMSS object.</span></span>
<span data-ttu-id="2c2ea-253">Per ottenere un oggetto VMSS, usa il cmdlet Get-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-253">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="2c2ea-254">Questo oggetto macchina virtuale contiene lo stato aggiornato per VMSS.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-254">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c2ea-255">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="2c2ea-255">-VMScaleSetName</span></span>
<span data-ttu-id="2c2ea-256">Specifica il nome della VMSS creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-256">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c2ea-257">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2c2ea-257">-Confirm</span></span>
<span data-ttu-id="2c2ea-258">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-258">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c2ea-259">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c2ea-259">-WhatIf</span></span>
<span data-ttu-id="2c2ea-260">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-260">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c2ea-261">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-261">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c2ea-262">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c2ea-262">CommonParameters</span></span>
<span data-ttu-id="2c2ea-263">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c2ea-263">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c2ea-264">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c2ea-264">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c2ea-265">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2c2ea-265">INPUTS</span></span>

### <span data-ttu-id="2c2ea-266">System. String</span><span class="sxs-lookup"><span data-stu-id="2c2ea-266">System.String</span></span>

### <span data-ttu-id="2c2ea-267">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2c2ea-267">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="2c2ea-268">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2c2ea-268">System.Boolean</span></span>

## <span data-ttu-id="2c2ea-269">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2c2ea-269">OUTPUTS</span></span>

### <span data-ttu-id="2c2ea-270">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="2c2ea-270">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="2c2ea-271">Note</span><span class="sxs-lookup"><span data-stu-id="2c2ea-271">NOTES</span></span>

## <span data-ttu-id="2c2ea-272">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2c2ea-272">RELATED LINKS</span></span>

[<span data-ttu-id="2c2ea-273">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2c2ea-273">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="2c2ea-274">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2c2ea-274">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="2c2ea-275">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2c2ea-275">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="2c2ea-276">Riavviare-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2c2ea-276">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="2c2ea-277">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2c2ea-277">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="2c2ea-278">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2c2ea-278">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="2c2ea-279">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="2c2ea-279">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


