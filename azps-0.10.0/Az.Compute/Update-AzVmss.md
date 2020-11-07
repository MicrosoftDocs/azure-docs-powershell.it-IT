---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzVmss.md
ms.openlocfilehash: 5e3bafbc667cc0e26eb6469e681ca9355b4f307f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863318"
---
# <span data-ttu-id="e63f6-101">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e63f6-101">Update-AzVmss</span></span>

## <span data-ttu-id="e63f6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e63f6-102">SYNOPSIS</span></span>
<span data-ttu-id="e63f6-103">Aggiorna lo stato di un VMSS.</span><span class="sxs-lookup"><span data-stu-id="e63f6-103">Updates the state of a VMSS.</span></span>

## <span data-ttu-id="e63f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e63f6-104">SYNTAX</span></span>

### <span data-ttu-id="e63f6-105">DefaultParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e63f6-105">DefaultParameter (Default)</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>]
 [-ManagedDiskStorageAccountType <StorageAccountTypes>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-SinglePlacementGroup <Boolean>] [-CustomData <String>] [-UpgradePolicyMode <UpgradeMode>]
 [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>] [-Tag <Hashtable>]
 [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-ImageReferencePublisher <String>]
 [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>] [-SkuTier <String>]
 [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>] [-SkuName <String>] [-PlanPromotionCode <String>]
 [-MaxUnhealthyInstancePercent <Int32>] [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>]
 [-ImageReferenceOffer <String>] [-PauseTimeBetweenBatches <String>] [-OsDiskCaching <CachingTypes>]
 [-ImageReferenceVersion <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e63f6-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="e63f6-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>] [-ImageReferenceSku <String>] [-IdentityId <String[]>]
 [-ManagedDiskStorageAccountType <StorageAccountTypes>] [-PlanPublisher <String>] [-ProvisionVMAgent <Boolean>]
 [-BootDiagnosticsEnabled <Boolean>] [-Overprovision <Boolean>] [-MaxBatchInstancePercent <Int32>]
 [-TimeZone <String>] [-BootDiagnosticsStorageUri <String>] [-AutomaticOSUpgrade <Boolean>]
 [-SinglePlacementGroup <Boolean>] [-CustomData <String>] [-UpgradePolicyMode <UpgradeMode>]
 [-ImageReferenceId <String>] [-DisablePasswordAuthentication <Boolean>] [-Tag <Hashtable>]
 [-PlanName <String>] [-MaxUnhealthyUpgradedInstancePercent <Int32>] [-ImageReferencePublisher <String>]
 [-PlanProduct <String>] [-VhdContainer <String[]>] [-ImageUri <String>] [-SkuTier <String>]
 [-EnableAutomaticUpdate <Boolean>] [-LicenseType <String>] -IdentityType <ResourceIdentityType>
 [-SkuName <String>] [-PlanPromotionCode <String>] [-MaxUnhealthyInstancePercent <Int32>]
 [-SkuCapacity <Int32>] [-OsDiskWriteAccelerator <Boolean>] [-ImageReferenceOffer <String>]
 [-PauseTimeBetweenBatches <String>] [-OsDiskCaching <CachingTypes>] [-ImageReferenceVersion <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e63f6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e63f6-107">DESCRIPTION</span></span>
<span data-ttu-id="e63f6-108">Il cmdlet **Update-AzVmss** aggiorna lo stato di un set di scale della macchina virtuale (VMSS) allo stato di un oggetto vmss locale.</span><span class="sxs-lookup"><span data-stu-id="e63f6-108">The **Update-AzVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="e63f6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e63f6-109">EXAMPLES</span></span>

### <span data-ttu-id="e63f6-110">Esempio 1: aggiornare lo stato di un VMSS allo stato di un oggetto VMSS locale.</span><span class="sxs-lookup"><span data-stu-id="e63f6-110">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet $LocalVMSS
```

<span data-ttu-id="e63f6-111">Questo comando Aggiorna lo stato del VMSS denominato VMSS001 che appartiene al gruppo di risorse denominato Group001 allo stato di un oggetto VMSS locale, $LocalVMSS.</span><span class="sxs-lookup"><span data-stu-id="e63f6-111">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object, $LocalVMSS.</span></span>

## <span data-ttu-id="e63f6-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e63f6-112">PARAMETERS</span></span>

### <span data-ttu-id="e63f6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e63f6-113">-AsJob</span></span>
<span data-ttu-id="e63f6-114">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="e63f6-114">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-115">-AutomaticOSUpgrade</span><span class="sxs-lookup"><span data-stu-id="e63f6-115">-AutomaticOSUpgrade</span></span>
<span data-ttu-id="e63f6-116">Imposta se gli aggiornamenti del sistema operativo devono essere applicati automaticamente alle istanze del set di scala in modo scorrevole quando una versione più recente dell'immagine diventa disponibile.</span><span class="sxs-lookup"><span data-stu-id="e63f6-116">Sets whether OS upgrades should automatically be applied to scale set instances in a rolling fashion when a newer version of the image becomes available.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-117">-BootDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="e63f6-117">-BootDiagnosticsEnabled</span></span>
<span data-ttu-id="e63f6-118">Se la diagnostica di avvio deve essere abilitata nel set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e63f6-118">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-119">-BootDiagnosticsStorageUri</span><span class="sxs-lookup"><span data-stu-id="e63f6-119">-BootDiagnosticsStorageUri</span></span>
<span data-ttu-id="e63f6-120">URI dell'account di archiviazione da usare per posizionare l'output e la schermata della console.</span><span class="sxs-lookup"><span data-stu-id="e63f6-120">URI of the storage account to use for placing the console output and screenshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-121">-CustomData</span><span class="sxs-lookup"><span data-stu-id="e63f6-121">-CustomData</span></span>
<span data-ttu-id="e63f6-122">Specifica una stringa codificata di base-64 di dati personalizzati.</span><span class="sxs-lookup"><span data-stu-id="e63f6-122">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="e63f6-123">Questa operazione viene decodificata in una matrice binaria che viene salvata come file nella macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e63f6-123">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="e63f6-124">La lunghezza massima della matrice binaria è di 65535 byte.</span><span class="sxs-lookup"><span data-stu-id="e63f6-124">The maximum length of the binary array is 65535 bytes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e63f6-125">-DefaultProfile</span></span>
<span data-ttu-id="e63f6-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e63f6-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-127">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="e63f6-127">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="e63f6-128">Indica che questo cmdlet disabilita l'autenticazione tramite password per il sistema operativo Linux.</span><span class="sxs-lookup"><span data-stu-id="e63f6-128">Indicates that this cmdlet disables password authentication for Linux OS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-129">-EnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="e63f6-129">-EnableAutomaticUpdate</span></span>
<span data-ttu-id="e63f6-130">Indica se le macchine virtuali Windows in VMSS sono abilitate per gli aggiornamenti automatici.</span><span class="sxs-lookup"><span data-stu-id="e63f6-130">Indicates whether the Windows virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-131">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="e63f6-131">-IdentityId</span></span>
<span data-ttu-id="e63f6-132">Specifica l'elenco delle identità utente associate al set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e63f6-132">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="e63f6-133">I riferimenti di identità utente saranno ID delle risorse ARM nella forma:'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="e63f6-133">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: String[]
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-134">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="e63f6-134">-IdentityType</span></span>
<span data-ttu-id="e63f6-135">Specifica il tipo di identità usato per il set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e63f6-135">Specifies the type of identity used for the virtual machine scale set.</span></span>
<span data-ttu-id="e63f6-136">Il tipo ' SystemAssignedUserAssigned ' include sia un'identità creata in modo implicito che un set di identità assegnate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="e63f6-136">The type 'SystemAssignedUserAssigned' includes both an implicitly created identity and a set of user assigned identities.</span></span>
<span data-ttu-id="e63f6-137">Il tipo "None" rimuoverà le identità dal set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e63f6-137">The type 'None' will remove any identities from the virtual machine scale set.</span></span>
<span data-ttu-id="e63f6-138">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e63f6-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e63f6-139">SystemAssigned</span><span class="sxs-lookup"><span data-stu-id="e63f6-139">SystemAssigned</span></span>
- <span data-ttu-id="e63f6-140">UserAssigned</span><span class="sxs-lookup"><span data-stu-id="e63f6-140">UserAssigned</span></span>
- <span data-ttu-id="e63f6-141">SystemAssignedUserAssigned</span><span class="sxs-lookup"><span data-stu-id="e63f6-141">SystemAssignedUserAssigned</span></span>
- <span data-ttu-id="e63f6-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e63f6-142">None</span></span>

```yaml
Type: ResourceIdentityType
Parameter Sets: ExplicitIdentityParameterSet
Aliases: 
Accepted values: SystemAssigned, UserAssigned, SystemAssignedUserAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-143">-ImageReferenceId</span><span class="sxs-lookup"><span data-stu-id="e63f6-143">-ImageReferenceId</span></span>
<span data-ttu-id="e63f6-144">Specifica l'ID riferimento immagine.</span><span class="sxs-lookup"><span data-stu-id="e63f6-144">Specifies the image reference ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-145">-ImageReferenceOffer</span><span class="sxs-lookup"><span data-stu-id="e63f6-145">-ImageReferenceOffer</span></span>
<span data-ttu-id="e63f6-146">Specifica il tipo di offerta VMImage (Virtual Machine Image).</span><span class="sxs-lookup"><span data-stu-id="e63f6-146">Specifies the type of virtual machine image (VMImage) offer.</span></span>
<span data-ttu-id="e63f6-147">Per ottenere un'offerta di immagine, usare il cmdlet Get-AzVMImageOffer.</span><span class="sxs-lookup"><span data-stu-id="e63f6-147">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-148">-ImageReferencePublisher</span><span class="sxs-lookup"><span data-stu-id="e63f6-148">-ImageReferencePublisher</span></span>
<span data-ttu-id="e63f6-149">Specifica il nome di un autore di un VMImage.</span><span class="sxs-lookup"><span data-stu-id="e63f6-149">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="e63f6-150">Per ottenere un autore, usare il cmdlet Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="e63f6-150">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-151">-ImageReferenceSku</span><span class="sxs-lookup"><span data-stu-id="e63f6-151">-ImageReferenceSku</span></span>
<span data-ttu-id="e63f6-152">Specifica la SKU VMImage.</span><span class="sxs-lookup"><span data-stu-id="e63f6-152">Specifies the VMImage SKU.</span></span>
<span data-ttu-id="e63f6-153">Per ottenere SKU, usare il cmdlet Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="e63f6-153">To obtain SKUs, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-154">-ImageReferenceVersion</span><span class="sxs-lookup"><span data-stu-id="e63f6-154">-ImageReferenceVersion</span></span>
<span data-ttu-id="e63f6-155">Specifica la versione di VMImage.</span><span class="sxs-lookup"><span data-stu-id="e63f6-155">Specifies the version of the VMImage.</span></span>
<span data-ttu-id="e63f6-156">Per usare la versione più recente, specificare il valore più recente invece di una determinata versione.</span><span class="sxs-lookup"><span data-stu-id="e63f6-156">To use the latest version, specify a value of latest instead of a particular version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-157">-ImageUri</span><span class="sxs-lookup"><span data-stu-id="e63f6-157">-ImageUri</span></span>
<span data-ttu-id="e63f6-158">Specifica l'URI BLOB per l'immagine utente.</span><span class="sxs-lookup"><span data-stu-id="e63f6-158">Specifies the blob URI for the user image.</span></span>
<span data-ttu-id="e63f6-159">VMSS crea un disco del sistema operativo nello stesso contenitore dell'immagine utente.</span><span class="sxs-lookup"><span data-stu-id="e63f6-159">VMSS creates an operating system disk in the same container of the user image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-160">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="e63f6-160">-LicenseType</span></span>
<span data-ttu-id="e63f6-161">Specificare il tipo di licenza, che è per portare il proprio scenario di licenza.</span><span class="sxs-lookup"><span data-stu-id="e63f6-161">Specify the license type, which is for bringing your own license scenario.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-162">-ManagedDiskStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="e63f6-162">-ManagedDiskStorageAccountType</span></span>
<span data-ttu-id="e63f6-163">Specifica il tipo di account di archiviazione per il disco gestito.</span><span class="sxs-lookup"><span data-stu-id="e63f6-163">Specifies the storage account type for managed disk.</span></span>
<span data-ttu-id="e63f6-164">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e63f6-164">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e63f6-165">StandardLRS</span><span class="sxs-lookup"><span data-stu-id="e63f6-165">StandardLRS</span></span>
- <span data-ttu-id="e63f6-166">PremiumLRS</span><span class="sxs-lookup"><span data-stu-id="e63f6-166">PremiumLRS</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-167">-MaxBatchInstancePercent</span><span class="sxs-lookup"><span data-stu-id="e63f6-167">-MaxBatchInstancePercent</span></span>
<span data-ttu-id="e63f6-168">Percentuale massima delle istanze totali della macchina virtuale che verranno aggiornate simultaneamente dall'aggiornamento a rotazione in un unico batch.</span><span class="sxs-lookup"><span data-stu-id="e63f6-168">The maximum percent of total virtual machine instances that will be upgraded simultaneously by the rolling upgrade in one batch.</span></span>
<span data-ttu-id="e63f6-169">Poiché si tratta di un massimo, le istanze non sane nei batch precedenti o futuri possono causare una diminuzione della percentuale di istanze in un batch per garantire maggiore affidabilità.</span><span class="sxs-lookup"><span data-stu-id="e63f6-169">As this is a maximum, unhealthy instances in previous or future batches can cause the percentage of instances in a batch to decrease to ensure higher reliability.</span></span>
<span data-ttu-id="e63f6-170">Se il valore non è specificato, viene impostato su 20.</span><span class="sxs-lookup"><span data-stu-id="e63f6-170">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-171">-MaxUnhealthyInstancePercent</span><span class="sxs-lookup"><span data-stu-id="e63f6-171">-MaxUnhealthyInstancePercent</span></span>
<span data-ttu-id="e63f6-172">La percentuale massima delle istanze totali della macchina virtuale nel set di proporzioni che possono essere non sane contemporaneamente, come risultato dell'aggiornamento o per essere stati trovati in uno stato non sano dai controlli di integrità della macchina virtuale prima dell'interruzione dell'aggiornamento a rotazione.</span><span class="sxs-lookup"><span data-stu-id="e63f6-172">The maximum percentage of the total virtual machine instances in the scale set that can be simultaneously unhealthy, either as a result of being upgraded, or by being found in an unhealthy state by the virtual machine health checks before the rolling upgrade aborts.</span></span>
<span data-ttu-id="e63f6-173">Questo vincolo verrà controllato prima di iniziare qualsiasi batch.</span><span class="sxs-lookup"><span data-stu-id="e63f6-173">This constraint will be checked prior to starting any batch.</span></span>
<span data-ttu-id="e63f6-174">Se il valore non è specificato, viene impostato su 20.</span><span class="sxs-lookup"><span data-stu-id="e63f6-174">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-175">-MaxUnhealthyUpgradedInstancePercent</span><span class="sxs-lookup"><span data-stu-id="e63f6-175">-MaxUnhealthyUpgradedInstancePercent</span></span>
<span data-ttu-id="e63f6-176">La percentuale massima delle istanze di macchine virtuali aggiornate che possono essere trovate in uno stato non sano.</span><span class="sxs-lookup"><span data-stu-id="e63f6-176">The maximum percentage of upgraded virtual machine instances that can be found to be in an unhealthy state.</span></span>
<span data-ttu-id="e63f6-177">Questo controllo avverrà dopo l'aggiornamento di ogni batch.</span><span class="sxs-lookup"><span data-stu-id="e63f6-177">This check will happen after each batch is upgraded.</span></span>
<span data-ttu-id="e63f6-178">Se questa percentuale viene mai superata, l'aggiornamento a rotazione viene interrotto.</span><span class="sxs-lookup"><span data-stu-id="e63f6-178">If this percentage is ever exceeded, the rolling update aborts.</span></span>
<span data-ttu-id="e63f6-179">Se il valore non è specificato, viene impostato su 20.</span><span class="sxs-lookup"><span data-stu-id="e63f6-179">If the value is not specified, it is set to 20.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-180">-OsDiskCaching</span><span class="sxs-lookup"><span data-stu-id="e63f6-180">-OsDiskCaching</span></span>
<span data-ttu-id="e63f6-181">Specifica la modalità di memorizzazione nella cache del disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e63f6-181">Specifies the caching mode of the operating system disk.</span></span> <span data-ttu-id="e63f6-182">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e63f6-182">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e63f6-183">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e63f6-183">None</span></span>
- <span data-ttu-id="e63f6-184">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="e63f6-184">ReadOnly</span></span>
- <span data-ttu-id="e63f6-185">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e63f6-185">ReadWrite</span></span>

<span data-ttu-id="e63f6-186">Il valore predefinito è ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="e63f6-186">The default value is ReadWrite.</span></span>
<span data-ttu-id="e63f6-187">Se si modifica il valore di memorizzazione nella cache, il cmdlet riavvia la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="e63f6-187">If you change the caching value, the cmdlet will restart the virtual machine.</span></span>

<span data-ttu-id="e63f6-188">Questa impostazione influenza la coerenza e le prestazioni del disco.</span><span class="sxs-lookup"><span data-stu-id="e63f6-188">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-189">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="e63f6-189">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="e63f6-190">Specifica se WriteAccelerator deve essere abilitato o disabilitato nel disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e63f6-190">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-191">-Provisioning</span><span class="sxs-lookup"><span data-stu-id="e63f6-191">-Overprovision</span></span>
<span data-ttu-id="e63f6-192">Indica se il cmdlet viene sovradisposto da VMSS.</span><span class="sxs-lookup"><span data-stu-id="e63f6-192">Indicates whether the cmdlet overprovisions the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-193">-PauseTimeBetweenBatches</span><span class="sxs-lookup"><span data-stu-id="e63f6-193">-PauseTimeBetweenBatches</span></span>
<span data-ttu-id="e63f6-194">Il tempo di attesa tra il completamento dell'aggiornamento per tutte le macchine virtuali in un unico batch e l'avvio del batch successivo.</span><span class="sxs-lookup"><span data-stu-id="e63f6-194">The wait time between completing the update for all virtual machines in one batch and starting the next batch.</span></span>
<span data-ttu-id="e63f6-195">La durata dell'ora deve essere specificata nel formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="e63f6-195">The time duration should be specified in ISO 8601 format.</span></span>
<span data-ttu-id="e63f6-196">Il valore predefinito è 0 secondi (PT0S).</span><span class="sxs-lookup"><span data-stu-id="e63f6-196">The default value is 0 seconds (PT0S).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-197">-PlanName</span><span class="sxs-lookup"><span data-stu-id="e63f6-197">-PlanName</span></span>
<span data-ttu-id="e63f6-198">Specifica il nome del piano.</span><span class="sxs-lookup"><span data-stu-id="e63f6-198">Specifies the plan name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-199">-PlanProduct</span><span class="sxs-lookup"><span data-stu-id="e63f6-199">-PlanProduct</span></span>
<span data-ttu-id="e63f6-200">Specifica il prodotto piano.</span><span class="sxs-lookup"><span data-stu-id="e63f6-200">Specifies the plan product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-201">-PlanPromotionCode</span><span class="sxs-lookup"><span data-stu-id="e63f6-201">-PlanPromotionCode</span></span>
<span data-ttu-id="e63f6-202">Specifica il codice promozionale per il piano.</span><span class="sxs-lookup"><span data-stu-id="e63f6-202">Specifies the plan promotion code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-203">-PlanPublisher</span><span class="sxs-lookup"><span data-stu-id="e63f6-203">-PlanPublisher</span></span>
<span data-ttu-id="e63f6-204">Specifica il piano Publisher.</span><span class="sxs-lookup"><span data-stu-id="e63f6-204">Specifies the plan publisher.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-205">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="e63f6-205">-ProvisionVMAgent</span></span>
<span data-ttu-id="e63f6-206">Indica se l'agente macchina virtuale deve essere eseguito il provisioning nelle macchine virtuali di Windows in VMSS.</span><span class="sxs-lookup"><span data-stu-id="e63f6-206">Indicates whether virtual machine agent should be provisioned on the Windows virtual machines in the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-207">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e63f6-207">-ResourceGroupName</span></span>
<span data-ttu-id="e63f6-208">Specifica il nome del gruppo di risorse a cui appartiene VMSS.</span><span class="sxs-lookup"><span data-stu-id="e63f6-208">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-209">-SinglePlacementGroup</span><span class="sxs-lookup"><span data-stu-id="e63f6-209">-SinglePlacementGroup</span></span>
<span data-ttu-id="e63f6-210">Specifica il gruppo di posizionamento singolo.</span><span class="sxs-lookup"><span data-stu-id="e63f6-210">Specifies the single placement group.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-211">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="e63f6-211">-SkuCapacity</span></span>
<span data-ttu-id="e63f6-212">Specifica il numero di istanze in VMSS.</span><span class="sxs-lookup"><span data-stu-id="e63f6-212">Specifies the number of instances in the VMSS.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-213">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e63f6-213">-SkuName</span></span>
<span data-ttu-id="e63f6-214">Specifica le dimensioni di tutte le istanze di VMSS.</span><span class="sxs-lookup"><span data-stu-id="e63f6-214">Specifies the size of all the instances of VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-215">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="e63f6-215">-SkuTier</span></span>
<span data-ttu-id="e63f6-216">Specifica il livello di VMSS.</span><span class="sxs-lookup"><span data-stu-id="e63f6-216">Specifies the tier of VMSS.</span></span>
<span data-ttu-id="e63f6-217">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e63f6-217">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e63f6-218">Standard</span><span class="sxs-lookup"><span data-stu-id="e63f6-218">Standard</span></span>
- <span data-ttu-id="e63f6-219">Base</span><span class="sxs-lookup"><span data-stu-id="e63f6-219">Basic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-220">-Tag</span><span class="sxs-lookup"><span data-stu-id="e63f6-220">-Tag</span></span>
<span data-ttu-id="e63f6-221">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e63f6-221">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e63f6-222">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="e63f6-222">For example:</span></span>

<span data-ttu-id="e63f6-223">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="e63f6-223">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-224">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="e63f6-224">-TimeZone</span></span>
<span data-ttu-id="e63f6-225">Specifica il fuso orario per il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="e63f6-225">Specifies the time zone for Windows OS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-226">-UpgradePolicyMode</span><span class="sxs-lookup"><span data-stu-id="e63f6-226">-UpgradePolicyMode</span></span>
<span data-ttu-id="e63f6-227">Specifica la modalità di aggiornamento delle macchine virtuali nel set di proporzioni.</span><span class="sxs-lookup"><span data-stu-id="e63f6-227">Specified the mode of an upgrade to virtual machines in the scale set.</span></span>
<span data-ttu-id="e63f6-228">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e63f6-228">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e63f6-229">Automatico</span><span class="sxs-lookup"><span data-stu-id="e63f6-229">Automatic</span></span>
- <span data-ttu-id="e63f6-230">Manuale</span><span class="sxs-lookup"><span data-stu-id="e63f6-230">Manual</span></span>
- <span data-ttu-id="e63f6-231">Implementazione</span><span class="sxs-lookup"><span data-stu-id="e63f6-231">Rolling</span></span>

```yaml
Type: UpgradeMode
Parameter Sets: (All)
Aliases: 
Accepted values: Automatic, Manual, Rolling

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-232">-VhdContainer</span><span class="sxs-lookup"><span data-stu-id="e63f6-232">-VhdContainer</span></span>
<span data-ttu-id="e63f6-233">Specifica gli URL del contenitore usati per archiviare i dischi del sistema operativo per VMSS.</span><span class="sxs-lookup"><span data-stu-id="e63f6-233">Specifies the container URLs that are used to store operating system disks for the VMSS.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-234">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e63f6-234">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="e63f6-235">Specifica un oggetto VMSS locale.</span><span class="sxs-lookup"><span data-stu-id="e63f6-235">Specifies a local VMSS object.</span></span>
<span data-ttu-id="e63f6-236">Per ottenere un oggetto VMSS, usa il cmdlet Get-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="e63f6-236">To obtain a VMSS object, use the Get-AzVmss cmdlet.</span></span>
<span data-ttu-id="e63f6-237">Questo oggetto macchina virtuale contiene lo stato aggiornato per VMSS.</span><span class="sxs-lookup"><span data-stu-id="e63f6-237">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-238">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e63f6-238">-VMScaleSetName</span></span>
<span data-ttu-id="e63f6-239">Specifica il nome della VMSS creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e63f6-239">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-240">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e63f6-240">-Confirm</span></span>
<span data-ttu-id="e63f6-241">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e63f6-241">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-242">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e63f6-242">-WhatIf</span></span>
<span data-ttu-id="e63f6-243">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e63f6-243">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="e63f6-244">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e63f6-244">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e63f6-245">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e63f6-245">CommonParameters</span></span>
<span data-ttu-id="e63f6-246">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e63f6-246">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e63f6-247">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e63f6-247">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e63f6-248">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e63f6-248">INPUTS</span></span>

### <span data-ttu-id="e63f6-249">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e63f6-249">VirtualMachineScaleSet</span></span>
<span data-ttu-id="e63f6-250">Il parametro ' VirtualMachineScaleSet ' accetta il valore di tipo ' VirtualMachineScaleSet ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="e63f6-250">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="e63f6-251">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e63f6-251">OUTPUTS</span></span>

### <span data-ttu-id="e63f6-252">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e63f6-252">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="e63f6-253">Note</span><span class="sxs-lookup"><span data-stu-id="e63f6-253">NOTES</span></span>

## <span data-ttu-id="e63f6-254">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e63f6-254">RELATED LINKS</span></span>

[<span data-ttu-id="e63f6-255">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e63f6-255">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="e63f6-256">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e63f6-256">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="e63f6-257">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e63f6-257">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="e63f6-258">Riavviare-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e63f6-258">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="e63f6-259">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e63f6-259">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="e63f6-260">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e63f6-260">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="e63f6-261">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="e63f6-261">Stop-AzVmss</span></span>](./Stop-AzVmss.md)


