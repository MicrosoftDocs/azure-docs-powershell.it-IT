---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: e9ec68d7c3991d7a3eded2566d8e299ddcc36c85
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192169"
---
# <span data-ttu-id="9e98f-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="9e98f-101">Update-AzVM</span></span>

## <span data-ttu-id="9e98f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9e98f-102">SYNOPSIS</span></span>
<span data-ttu-id="9e98f-103">Aggiorna lo stato di una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="9e98f-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="9e98f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e98f-104">SYNTAX</span></span>

### <span data-ttu-id="9e98f-105">ResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9e98f-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>]
 [-ProximityPlacementGroupId <String>] [-HostId <String>] [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e98f-106">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="9e98f-106">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e98f-107">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9e98f-107">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-ProximityPlacementGroupId <String>] [-HostId <String>]
 [-EncryptionAtHost <Boolean>] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e98f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e98f-108">DESCRIPTION</span></span>
<span data-ttu-id="9e98f-109">Il cmdlet **Update-AzVM** aggiorna lo stato di una macchina virtuale di Azure allo stato di un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9e98f-109">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="9e98f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e98f-110">EXAMPLES</span></span>

### <span data-ttu-id="9e98f-111">Esempio 1: aggiornare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="9e98f-111">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="9e98f-112">Questo comando Aggiorna la macchina virtuale, $VirtualMachine, in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="9e98f-112">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="9e98f-113">Il comando lo aggiorna usando l'oggetto macchina virtuale archiviato nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="9e98f-113">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="9e98f-114">Per ottenere un oggetto macchina virtuale, usare il cmdlet **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="9e98f-114">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="9e98f-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9e98f-115">PARAMETERS</span></span>

### <span data-ttu-id="9e98f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e98f-116">-AsJob</span></span>
<span data-ttu-id="9e98f-117">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="9e98f-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="9e98f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e98f-118">-DefaultProfile</span></span>
<span data-ttu-id="9e98f-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9e98f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e98f-120">-HostId</span><span class="sxs-lookup"><span data-stu-id="9e98f-120">-HostId</span></span>
<span data-ttu-id="9e98f-121">ID dell'host</span><span class="sxs-lookup"><span data-stu-id="9e98f-121">The Id of Host</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e98f-122">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="9e98f-122">-EncryptionAtHost</span></span>
<span data-ttu-id="9e98f-123">La proprietà EncryptionAtHost può essere usata dall'utente nella richiesta per abilitare o disabilitare la crittografia host per la macchina virtuale o il set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9e98f-123">EncryptionAtHost property can be used by user in the request to enable or disable the Host Encryption for the virtual machine or virtual machine scale set.</span></span> <span data-ttu-id="9e98f-124">Ciò consentirà la crittografia per tutti i dischi, incluso il disco Resource/Temp all'host stesso.</span><span class="sxs-lookup"><span data-stu-id="9e98f-124">This will enable the encryption for all the disks including Resource/Temp disk at host itself.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e98f-125">-ID</span><span class="sxs-lookup"><span data-stu-id="9e98f-125">-Id</span></span>
<span data-ttu-id="9e98f-126">Specifica l'ID risorsa della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9e98f-126">Specifies the resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e98f-127">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="9e98f-127">-IdentityId</span></span>
<span data-ttu-id="9e98f-128">Specifica l'elenco delle identità utente associate alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9e98f-128">Specifies the list of user identities associated with the virtual machine.</span></span>
<span data-ttu-id="9e98f-129">I riferimenti di identità utente saranno ID delle risorse ARM nella forma:'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="9e98f-129">The user identity references will be ARM resource IDs in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="9e98f-130">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="9e98f-130">-IdentityType</span></span>
<span data-ttu-id="9e98f-131">Tipo di identità utilizzata per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9e98f-131">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="9e98f-132">I valori validi sono SystemAssigned, UserAssigned, SystemAssignedUserAssigned e None.</span><span class="sxs-lookup"><span data-stu-id="9e98f-132">Valid values are SystemAssigned, UserAssigned, SystemAssignedUserAssigned, and None.</span></span>

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

### <span data-ttu-id="9e98f-133">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="9e98f-133">-MaxPrice</span></span>
<span data-ttu-id="9e98f-134">Specifica il prezzo massimo che si vuole pagare per una VM/VMSS a priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="9e98f-134">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="9e98f-135">Questo prezzo è in dollari USA.</span><span class="sxs-lookup"><span data-stu-id="9e98f-135">This price is in US Dollars.</span></span> <span data-ttu-id="9e98f-136">Questo prezzo verrà confrontato con il prezzo corrente con priorità bassa per le dimensioni della VM.</span><span class="sxs-lookup"><span data-stu-id="9e98f-136">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="9e98f-137">Inoltre, i prezzi vengono confrontati al momento della creazione/aggiornamento della priorità bassa VM/VMSS e l'operazione avrà esito positivo solo se maxPrice è maggiore del prezzo corrente con priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="9e98f-137">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="9e98f-138">Il maxPrice verrà usato anche per rimuovere una VM/VMSS a priorità bassa se il prezzo corrente con priorità bassa supera il maxPrice dopo la creazione di VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="9e98f-138">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="9e98f-139">I valori possibili sono: qualsiasi valore decimale maggiore di zero.</span><span class="sxs-lookup"><span data-stu-id="9e98f-139">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="9e98f-140">Esempio: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="9e98f-140">Example: 0.01538.</span></span>  <span data-ttu-id="9e98f-141">-1 indica che la priorità bassa VM/VMSS non deve essere sfrattata per motivi di prezzo.</span><span class="sxs-lookup"><span data-stu-id="9e98f-141">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="9e98f-142">Inoltre, il prezzo massimo predefinito è-1 se non è fornito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="9e98f-142">Also, the default max price is -1 if it is not provided by you.</span></span>

```yaml
Type: System.Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e98f-143">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="9e98f-143">-NoWait</span></span>
<span data-ttu-id="9e98f-144">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="9e98f-144">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="9e98f-145">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="9e98f-145">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="9e98f-146">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="9e98f-146">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="9e98f-147">Specifica se WriteAccelerator deve essere abilitato o disabilitato nel disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9e98f-147">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="9e98f-148">-ProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="9e98f-148">-ProximityPlacementGroupId</span></span>
<span data-ttu-id="9e98f-149">ID risorsa del gruppo di posizionamento di prossimità da usare con questa macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9e98f-149">The resource id of the Proximity Placement Group to use with this virtual machine.</span></span>

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

### <span data-ttu-id="9e98f-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e98f-150">-ResourceGroupName</span></span>
<span data-ttu-id="9e98f-151">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9e98f-151">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName, ExplicitIdentityParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e98f-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="9e98f-152">-Tag</span></span>
<span data-ttu-id="9e98f-153">Specifica che le risorse e i gruppi di risorse possono essere contrassegnati con un set di coppie nome/valore.</span><span class="sxs-lookup"><span data-stu-id="9e98f-153">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="9e98f-154">L'aggiunta di tag alle risorse consente di raggruppare le risorse tra gruppi di risorse e di creare visualizzazioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="9e98f-154">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="9e98f-155">Ogni risorsa o gruppo di risorse può avere un massimo di 15 contrassegni.</span><span class="sxs-lookup"><span data-stu-id="9e98f-155">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="9e98f-156">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="9e98f-156">-UltraSSDEnabled</span></span>
<span data-ttu-id="9e98f-157">Il contrassegno che consente o Disabilita una funzionalità per avere uno o più dischi di dati gestiti con il tipo di account di archiviazione UltraSSD_LRS nella VM.</span><span class="sxs-lookup"><span data-stu-id="9e98f-157">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="9e98f-158">Dischi gestiti con tipo di account di archiviazione UltraSSD_LRS possono essere aggiunti a una macchina virtuale solo se questa proprietà è abilitata.</span><span class="sxs-lookup"><span data-stu-id="9e98f-158">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

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

### <span data-ttu-id="9e98f-159">-VM</span><span class="sxs-lookup"><span data-stu-id="9e98f-159">-VM</span></span>
<span data-ttu-id="9e98f-160">Specifica un oggetto macchina virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="9e98f-160">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="9e98f-161">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="9e98f-161">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="9e98f-162">Questo oggetto macchina virtuale contiene lo stato aggiornato per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9e98f-162">This virtual machine object contains the updated state for the virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e98f-163">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9e98f-163">-Confirm</span></span>
<span data-ttu-id="9e98f-164">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e98f-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e98f-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e98f-165">-WhatIf</span></span>
<span data-ttu-id="9e98f-166">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e98f-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e98f-167">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e98f-167">The cmdlet is not run.</span></span>

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


### <span data-ttu-id="9e98f-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e98f-168">CommonParameters</span></span>
<span data-ttu-id="9e98f-169">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e98f-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e98f-170">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9e98f-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e98f-171">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9e98f-171">INPUTS</span></span>

### <span data-ttu-id="9e98f-172">System. String</span><span class="sxs-lookup"><span data-stu-id="9e98f-172">System.String</span></span>

### <span data-ttu-id="9e98f-173">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9e98f-173">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="9e98f-174">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9e98f-174">System.Boolean</span></span>

## <span data-ttu-id="9e98f-175">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e98f-175">OUTPUTS</span></span>

### <span data-ttu-id="9e98f-176">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9e98f-176">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9e98f-177">Note</span><span class="sxs-lookup"><span data-stu-id="9e98f-177">NOTES</span></span>

## <span data-ttu-id="9e98f-178">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e98f-178">RELATED LINKS</span></span>

[<span data-ttu-id="9e98f-179">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="9e98f-179">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="9e98f-180">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="9e98f-180">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="9e98f-181">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="9e98f-181">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="9e98f-182">Riavviare-AzVM</span><span class="sxs-lookup"><span data-stu-id="9e98f-182">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="9e98f-183">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="9e98f-183">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="9e98f-184">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="9e98f-184">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="9e98f-185">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="9e98f-185">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


