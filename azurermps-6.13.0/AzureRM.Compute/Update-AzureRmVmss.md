---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVmss.md
ms.openlocfilehash: d2ecc5799319dcbc9b2e3710c186ffd7ebc09c64
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518804"
---
# <span data-ttu-id="ff9e9-101">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ff9e9-101">Update-AzureRmVmss</span></span>

## <span data-ttu-id="ff9e9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ff9e9-102">SYNOPSIS</span></span>
<span data-ttu-id="ff9e9-103">Aggiorna lo stato di un VMSS.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-103">Updates the state of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff9e9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ff9e9-104">SYNTAX</span></span>

### <span data-ttu-id="ff9e9-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ff9e9-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>]
 [-ManagedDiskStorageAccountType <String>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-DisableAutoRollback <Boolean>] [-SinglePlacementGroup <Boolean>] [-CustomData <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>]
 [-Tag <Hashtable>] [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-ImageReferencePublisher <String>] [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>]
 [-SkuTier <String>] [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>] [-SkuName <String>]
 [-PlanPromotionCode <String>] [-MaxUnhealthyInstancePercent <Int32>] [-SkuCapacity <Int32>]
 [-OsDiskWriteAccelerator <Boolean>] [-ImageReferenceOffer <String>] [-PauseTimeBetweenBatches <String>]
 [-OsDiskCaching <CachingTypes>] [-ImageReferenceVersion <String>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff9e9-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff9e9-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>] [-IdentityId <String[]>]
 [-ManagedDiskStorageAccountType <String>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-DisableAutoRollback <Boolean>] [-SinglePlacementGroup <Boolean>] [-CustomData <String>]
 [-UpgradePolicyMode <UpgradeMode>] [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>]
 [-Tag <Hashtable>] [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>]
 [-ImageReferencePublisher <String>] [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>]
 [-SkuTier <String>] [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>]
 -IdentityType <ResourceIdentityType> [-SkuName <String>] [-PlanPromotionCode <String>]
 [-MaxUnhealthyInstancePercent <Int32>] [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>]
 [-ImageReferenceOffer <String>] [-PauseTimeBetweenBatches <String>] [-OsDiskCaching <CachingTypes>]
 [-ImageReferenceVersion <String>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff9e9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff9e9-107">DESCRIPTION</span></span>
<span data-ttu-id="ff9e9-108">Il cmdlet **Update-AzureRmVmss** aggiorna lo stato di un set di scale della macchina virtuale (VMSS) allo stato di un oggetto vmss locale.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-108">The **Update-AzureRmVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="ff9e9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ff9e9-109">EXAMPLES</span></span>

### <span data-ttu-id="ff9e9-110">Esempio 1: aggiornare lo stato di un VMSS allo stato di un oggetto VMSS locale.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzureRmVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="ff9e9-111">Questo comando Aggiorna lo stato del VMSS denominato VMSS001 che appartiene al gruppo di risorse denominato Group001 allo stato di un oggetto VMSS locale, $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="ff9e9-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ff9e9-112">PARAMETERS</span></span>

### <span data-ttu-id="ff9e9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff9e9-113">-AsJob</span></span>
<span data-ttu-id="ff9e9-114">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ff9e9-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="ff9e9-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="ff9e9-116">Imposta se gli aggiornamenti del sistema operativo devono essere applicati automaticamente alle istanze del set di scala in modo scorrevole quando una versione più recente dell'immagine diventa disponibile.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

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

### <span data-ttu-id="ff9e9-117">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="ff9e9-117">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="ff9e9-118">Se la diagnostica di avvio deve essere abilitata nel set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-118">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

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

### <span data-ttu-id="ff9e9-119">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="ff9e9-119">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="ff9e9-120">URI dell'account di archiviazione da usare per posizionare l'output e la schermata della console.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-120">URI of the storage account to use for placing the console output and screenshot.</span></span>

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

### <span data-ttu-id="ff9e9-121">-CustomData</span><span class="sxs-lookup"><span data-stu-id="ff9e9-121">-CustomData</span></span>
<span data-ttu-id="ff9e9-122">Specifica una stringa codificata di base-64 di dati personalizzati.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-122">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="ff9e9-123">Questa operazione viene decodificata in una matrice binaria che viene salvata come file nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-123">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="ff9e9-124">La lunghezza massima della matrice binaria è di 65535 byte.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-124">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="ff9e9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff9e9-125">-DefaultProfile</span></span>
<span data-ttu-id="ff9e9-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff9e9-127">-DisableAutoRollback</span><span class="sxs-lookup"><span data-stu-id="ff9e9-127">-DisableAutoRollback</span></span>
<span data-ttu-id="ff9e9-128">Disabilitare il rollback automatico per i criteri di aggiornamento del sistema operativo automatico</span><span class="sxs-lookup"><span data-stu-id="ff9e9-128">Disable Auto Rollback for Auto OS Upgrade Policy</span></span>

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

### <span data-ttu-id="ff9e9-129">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="ff9e9-129">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="ff9e9-130">Indica che questo cmdlet disabilita l'autenticazione tramite password per il sistema operativo Linux.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-130">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

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

### <span data-ttu-id="ff9e9-131">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="ff9e9-131">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="ff9e9-132">Indica se le macchine virtuali Windows in VMSS sono abilitate per gli aggiornamenti automatici.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-132">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="ff9e9-133">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="ff9e9-133">-IdentityId</span></span>
<span data-ttu-id="ff9e9-134">Specifica l'elenco delle identità utente associate al set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-134">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="ff9e9-135">I riferimenti di identità utente saranno ID delle risorse ARM nella forma:'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="ff9e9-135">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="ff9e9-136">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="ff9e9-136">-IdentityType</span></span>
<span data-ttu-id="ff9e9-137">Specifica il tipo di identità usato per il set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-137">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="ff9e9-138">Il tipo ' SystemAssignedUserAssigned ' include sia un'identità creata in modo implicito che un set di identità assegnate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-138">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="ff9e9-139">Il tipo "None" rimuoverà le identità dal set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-139">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="ff9e9-140">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ff9e9-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ff9e9-141">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="ff9e9-141">SystemAssigned</span></span>
- <span data-ttu-id="ff9e9-142">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="ff9e9-142">UserAssigned</span></span>
- <span data-ttu-id="ff9e9-143">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="ff9e9-143">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="ff9e9-144">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ff9e9-144">None</span></span>

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

### <span data-ttu-id="ff9e9-145">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="ff9e9-145">-ImageReferenceId</span></span>
<span data-ttu-id="ff9e9-146">Specifica l'ID riferimento immagine.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-146">Specifies the image reference ID.</span></span>

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

### <span data-ttu-id="ff9e9-147">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="ff9e9-147">-ImageReferenceOffer</span></span>
<span data-ttu-id="ff9e9-148">Specifica il tipo di offerta VMImage (Virtual Machine Image).</span><span class="sxs-lookup"><span data-stu-id="ff9e9-148">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="ff9e9-149">Per ottenere un'offerta di immagine, usare il cmdlet Get-AzureRmVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-149">To obtain an image offer, use the Get-AzureRmVMImageOffer cmdlet.</span></span>

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

### <span data-ttu-id="ff9e9-150">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="ff9e9-150">-ImageReferencePublisher</span></span>
<span data-ttu-id="ff9e9-151">Specifica il nome di un autore di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-151">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="ff9e9-152">Per ottenere un autore, usare il cmdlet Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-152">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="ff9e9-153">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="ff9e9-153">-ImageReferenceSku</span></span>
<span data-ttu-id="ff9e9-154">Specifica la SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-154">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="ff9e9-155">Per ottenere SKU, usare il cmdlet Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-155">To obtain SKUs, use the Get-AzureRmVMImageSku cmdlet.</span></span>

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

### <span data-ttu-id="ff9e9-156">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="ff9e9-156">-ImageReferenceVersion</span></span>
<span data-ttu-id="ff9e9-157">Specifica la versione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-157">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="ff9e9-158">Per usare la versione più recente, specificare il valore più recente invece di una determinata versione.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-158">To use the latest version, specify a value of latest instead of a particular version.</span></span>

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

### <span data-ttu-id="ff9e9-159">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="ff9e9-159">-ImageUri</span></span>
<span data-ttu-id="ff9e9-160">Specifica l'URI BLOB per l'immagine utente.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-160">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="ff9e9-161">VMSS crea un disco del sistema operativo nello stesso contenitore dell'immagine utente.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-161">VMSS creates an operating system disk in the same container of the user image.</span></span>

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

### <span data-ttu-id="ff9e9-162">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ff9e9-162">-LicenseType</span></span>
<span data-ttu-id="ff9e9-163">Specificare il tipo di licenza, che è per portare il proprio scenario di licenza.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-163">Specify the license type, which is for bringing your own license scenario.</span></span>

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

### <span data-ttu-id="ff9e9-164">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="ff9e9-164">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="ff9e9-165">Specifica il tipo di account di archiviazione per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-165">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="ff9e9-166">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ff9e9-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ff9e9-167">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="ff9e9-167">StandardLRS</span></span>
- <span data-ttu-id="ff9e9-168">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="ff9e9-168">PremiumLRS</span></span>

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

### <span data-ttu-id="ff9e9-169">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="ff9e9-169">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="ff9e9-170">Percentuale massima delle istanze totali della macchina virtuale che verranno aggiornate simultaneamente dall'aggiornamento a rotazione in un unico batch.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-170">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="ff9e9-171">Poiché si tratta di un massimo, le istanze non sane nei batch precedenti o futuri possono causare una diminuzione della percentuale di istanze in un batch per garantire maggiore affidabilità.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-171">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="ff9e9-172">Se il valore non è specificato, viene impostato su 20.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-172">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="ff9e9-173">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="ff9e9-173">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="ff9e9-174">La percentuale massima delle istanze totali della macchina virtuale nel set di proporzioni che possono essere non sane contemporaneamente, come risultato dell'aggiornamento o per essere stati trovati in uno stato non sano dai controlli di integrità della macchina virtuale prima dell'interruzione dell'aggiornamento a rotazione.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-174">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="ff9e9-175">Questo vincolo verrà controllato prima di iniziare qualsiasi batch.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-175">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="ff9e9-176">Se il valore non è specificato, viene impostato su 20.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-176">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="ff9e9-177">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="ff9e9-177">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="ff9e9-178">La percentuale massima delle istanze di macchine virtuali aggiornate che possono essere trovate in uno stato non sano.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-178">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="ff9e9-179">Questo controllo avverrà dopo l'aggiornamento di ogni batch.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-179">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="ff9e9-180">Se questa percentuale viene mai superata, l'aggiornamento a rotazione viene interrotto.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-180">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="ff9e9-181">Se il valore non è specificato, viene impostato su 20.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-181">If the value is not specified, it is set to 20.</span></span>

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

### <span data-ttu-id="ff9e9-182">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="ff9e9-182">-OsDiskCaching</span></span>
<span data-ttu-id="ff9e9-183">Specifica la modalità di memorizzazione nella cache del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-183">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="ff9e9-184">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ff9e9-184">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ff9e9-185">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ff9e9-185">None</span></span>
- <span data-ttu-id="ff9e9-186">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ff9e9-186">ReadOnly</span></span>
- <span data-ttu-id="ff9e9-187">ReadWrite il valore predefinito è ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-187">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="ff9e9-188">Se si modifica il valore di memorizzazione nella cache, il cmdlet riavvia la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-188">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>
<span data-ttu-id="ff9e9-189">Questa impostazione influenza la coerenza e le prestazioni del disco.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-189">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="ff9e9-190">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="ff9e9-190">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="ff9e9-191">Specifica se WriteAccelerator deve essere abilitato o disabilitato nel disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-191">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="ff9e9-192">-Provisioning</span><span class="sxs-lookup"><span data-stu-id="ff9e9-192">-Overprovision</span></span>
<span data-ttu-id="ff9e9-193">Indica se il cmdlet viene sovradisposto da VMSS.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-193">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

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

### <span data-ttu-id="ff9e9-194">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="ff9e9-194">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="ff9e9-195">Il tempo di attesa tra il completamento dell'aggiornamento per tutte le macchine virtuali in un unico batch e l'avvio del batch successivo.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-195">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="ff9e9-196">La durata dell'ora deve essere specificata nel formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-196">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="ff9e9-197">Il valore predefinito è 0 secondi (PT0S).</span><span class="sxs-lookup"><span data-stu-id="ff9e9-197">The default value is 0 seconds (PT0S).</span></span>

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

### <span data-ttu-id="ff9e9-198">-PlanName</span><span class="sxs-lookup"><span data-stu-id="ff9e9-198">-PlanName</span></span>
<span data-ttu-id="ff9e9-199">Specifica il nome del piano.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-199">Specifies the plan name.</span></span>

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

### <span data-ttu-id="ff9e9-200">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="ff9e9-200">-PlanProduct</span></span>
<span data-ttu-id="ff9e9-201">Specifica il prodotto piano.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-201">Specifies the plan product.</span></span>

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

### <span data-ttu-id="ff9e9-202">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="ff9e9-202">-PlanPromotionCode</span></span>
<span data-ttu-id="ff9e9-203">Specifica il codice promozionale per il piano.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-203">Specifies the plan promotion code.</span></span>

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

### <span data-ttu-id="ff9e9-204">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="ff9e9-204">-PlanPublisher</span></span>
<span data-ttu-id="ff9e9-205">Specifica il piano Publisher.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-205">Specifies the plan publisher.</span></span>

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

### <span data-ttu-id="ff9e9-206">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="ff9e9-206">-ProvisionVMAgent</span></span>
<span data-ttu-id="ff9e9-207">Indica se l'agente macchina virtuale deve essere eseguito il provisioning nelle macchine virtuali di Windows in VMSS.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-207">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="ff9e9-208">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff9e9-208">-ResourceGroupName</span></span>
<span data-ttu-id="ff9e9-209">Specifica il nome del gruppo di risorse a cui appartiene VMSS.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-209">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff9e9-210">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="ff9e9-210">-SinglePlacementGroup</span></span>
<span data-ttu-id="ff9e9-211">Specifica il gruppo di posizionamento singolo.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-211">Specifies the single placement group.</span></span>

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

### <span data-ttu-id="ff9e9-212">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="ff9e9-212">-SkuCapacity</span></span>
<span data-ttu-id="ff9e9-213">Specifica il numero di istanze in VMSS.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-213">Specifies the number of instances in the VMSS.</span></span>

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

### <span data-ttu-id="ff9e9-214">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ff9e9-214">-SkuName</span></span>
<span data-ttu-id="ff9e9-215">Specifica le dimensioni di tutte le istanze di VMSS.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-215">Specifies the size of all the instances of VMSS.</span></span>

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

### <span data-ttu-id="ff9e9-216">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="ff9e9-216">-SkuTier</span></span>
<span data-ttu-id="ff9e9-217">Specifica il livello di VMSS.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-217">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="ff9e9-218">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ff9e9-218">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ff9e9-219">Standard</span><span class="sxs-lookup"><span data-stu-id="ff9e9-219">Standard</span></span>
- <span data-ttu-id="ff9e9-220">Base</span><span class="sxs-lookup"><span data-stu-id="ff9e9-220">Basic</span></span>

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

### <span data-ttu-id="ff9e9-221">-Tag</span><span class="sxs-lookup"><span data-stu-id="ff9e9-221">-Tag</span></span>
<span data-ttu-id="ff9e9-222">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-222">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ff9e9-223">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ff9e9-223">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ff9e9-224">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="ff9e9-224">-TimeZone</span></span>
<span data-ttu-id="ff9e9-225">Specifica il fuso orario per il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-225">Specifies the time zone for Windows OS.</span></span>

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

### <span data-ttu-id="ff9e9-226">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="ff9e9-226">-UltraSSDEnabled</span></span>
<span data-ttu-id="ff9e9-227">Il contrassegno che Abilita o Disabilita una funzionalità per avere uno o più dischi di dati gestiti con UltraSSD_LRS tipo di account di archiviazione nel set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-227">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the virtual machine scale set.</span></span>
<span data-ttu-id="ff9e9-228">Dischi gestiti con tipo di account di archiviazione UltraSSD_LRS può essere aggiunto a un VMSS solo se questa proprietà è abilitata.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-228">Managed disks with storage account type UltraSSD_LRS can be added to a VMSS only if this property is enabled.</span></span>

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

### <span data-ttu-id="ff9e9-229">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="ff9e9-229">-UpgradePolicyMode</span></span>
<span data-ttu-id="ff9e9-230">Specifica la modalità di aggiornamento delle macchine virtuali nel set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-230">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="ff9e9-231">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ff9e9-231">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ff9e9-232">Automatico</span><span class="sxs-lookup"><span data-stu-id="ff9e9-232">Automatic</span></span>
- <span data-ttu-id="ff9e9-233">Manuale</span><span class="sxs-lookup"><span data-stu-id="ff9e9-233">Manual</span></span>
- <span data-ttu-id="ff9e9-234">Implementazione</span><span class="sxs-lookup"><span data-stu-id="ff9e9-234">Rolling</span></span>

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

### <span data-ttu-id="ff9e9-235">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="ff9e9-235">-VhdContainer</span></span>
<span data-ttu-id="ff9e9-236">Specifica gli URL del contenitore usati per archiviare i dischi del sistema operativo per VMSS.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-236">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

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

### <span data-ttu-id="ff9e9-237">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ff9e9-237">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="ff9e9-238">Specifica un oggetto VMSS locale.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-238">Specifies a local VMSS object.</span></span>
<span data-ttu-id="ff9e9-239">Per ottenere un oggetto VMSS, usa il cmdlet Get-AzureRmVmss.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-239">To obtain a VMSS object, use the Get-AzureRmVmss cmdlet.</span></span>
<span data-ttu-id="ff9e9-240">Questo oggetto macchina virtuale contiene lo stato aggiornato per VMSS.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-240">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff9e9-241">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ff9e9-241">-VMScaleSetName</span></span>
<span data-ttu-id="ff9e9-242">Specifica il nome della VMSS creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-242">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff9e9-243">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ff9e9-243">-Confirm</span></span>
<span data-ttu-id="ff9e9-244">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-244">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff9e9-245">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff9e9-245">-WhatIf</span></span>
<span data-ttu-id="ff9e9-246">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-246">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff9e9-247">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-247">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff9e9-248">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff9e9-248">CommonParameters</span></span>
<span data-ttu-id="ff9e9-249">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff9e9-249">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff9e9-250">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff9e9-250">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff9e9-251">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ff9e9-251">INPUTS</span></span>

### <span data-ttu-id="ff9e9-252">System. String</span><span class="sxs-lookup"><span data-stu-id="ff9e9-252">System.String</span></span>

### <span data-ttu-id="ff9e9-253">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ff9e9-253">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>
<span data-ttu-id="ff9e9-254">Parametri: VirtualMachineScaleSet (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ff9e9-254">Parameters: VirtualMachineScaleSet (ByValue)</span></span>

## <span data-ttu-id="ff9e9-255">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ff9e9-255">OUTPUTS</span></span>

### <span data-ttu-id="ff9e9-256">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ff9e9-256">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="ff9e9-257">Note</span><span class="sxs-lookup"><span data-stu-id="ff9e9-257">NOTES</span></span>

## <span data-ttu-id="ff9e9-258">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ff9e9-258">RELATED LINKS</span></span>

[<span data-ttu-id="ff9e9-259">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ff9e9-259">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="ff9e9-260">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ff9e9-260">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="ff9e9-261">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ff9e9-261">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="ff9e9-262">Riavviare-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ff9e9-262">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="ff9e9-263">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ff9e9-263">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="ff9e9-264">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ff9e9-264">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="ff9e9-265">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ff9e9-265">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)


