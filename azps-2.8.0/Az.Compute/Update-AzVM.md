---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: 339d63fe02c8286dc5867428269dc2e2afe342d3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675111"
---
# <span data-ttu-id="947ee-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="947ee-101">Update-AzVM</span></span>

## <span data-ttu-id="947ee-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="947ee-102">SYNOPSIS</span></span>
<span data-ttu-id="947ee-103">Aggiorna lo stato di una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="947ee-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="947ee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="947ee-104">SYNTAX</span></span>

### <span data-ttu-id="947ee-105">ResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="947ee-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="947ee-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="947ee-106">AssignIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="947ee-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="947ee-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="947ee-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="947ee-108">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-MaxPrice <Double>] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="947ee-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="947ee-109">DESCRIPTION</span></span>
<span data-ttu-id="947ee-110">Il cmdlet **Update-AzVM** aggiorna lo stato di una macchina virtuale di Azure allo stato di un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="947ee-110">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="947ee-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="947ee-111">EXAMPLES</span></span>

### <span data-ttu-id="947ee-112">Esempio 1: aggiornare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="947ee-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="947ee-113">Questo comando Aggiorna la macchina virtuale, $VirtualMachine, in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="947ee-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="947ee-114">Il comando lo aggiorna usando l'oggetto macchina virtuale archiviato nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="947ee-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="947ee-115">Per ottenere un oggetto macchina virtuale, usare il cmdlet **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="947ee-115">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="947ee-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="947ee-116">PARAMETERS</span></span>

### <span data-ttu-id="947ee-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="947ee-117">-AsJob</span></span>
<span data-ttu-id="947ee-118">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="947ee-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="947ee-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="947ee-119">-AssignIdentity</span></span>
<span data-ttu-id="947ee-120">Specifica l'identità assegnata dal sistema per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="947ee-120">Specify the system-assigned identity for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="947ee-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="947ee-121">-DefaultProfile</span></span>
<span data-ttu-id="947ee-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="947ee-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="947ee-123">-ID</span><span class="sxs-lookup"><span data-stu-id="947ee-123">-Id</span></span>
<span data-ttu-id="947ee-124">Specifica l'ID risorsa della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="947ee-124">Specifies the resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="947ee-125">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="947ee-125">-IdentityId</span></span>
<span data-ttu-id="947ee-126">Specifica l'elenco delle identità utente associate alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="947ee-126">Specifies the list of user identities associated with the virtual machine.</span></span>
<span data-ttu-id="947ee-127">I riferimenti di identità utente saranno ID delle risorse ARM nella forma:'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="947ee-127">The user identity references will be ARM resource IDs in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="947ee-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="947ee-128">-IdentityType</span></span>
<span data-ttu-id="947ee-129">Tipo di identità utilizzata per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="947ee-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="947ee-130">I valori validi sono SystemAssigned, UserAssigned, SystemAssignedUserAssigned e None.</span><span class="sxs-lookup"><span data-stu-id="947ee-130">Valid values are SystemAssigned, UserAssigned, SystemAssignedUserAssigned, and None.</span></span>

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

### <span data-ttu-id="947ee-131">-MaxPrice</span><span class="sxs-lookup"><span data-stu-id="947ee-131">-MaxPrice</span></span>
<span data-ttu-id="947ee-132">Specifica il prezzo massimo che si vuole pagare per una VM/VMSS a priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="947ee-132">Specifies the maximum price you are willing to pay for a low priority VM/VMSS.</span></span> <span data-ttu-id="947ee-133">Questo prezzo è in dollari USA.</span><span class="sxs-lookup"><span data-stu-id="947ee-133">This price is in US Dollars.</span></span> <span data-ttu-id="947ee-134">Questo prezzo verrà confrontato con il prezzo corrente con priorità bassa per le dimensioni della VM.</span><span class="sxs-lookup"><span data-stu-id="947ee-134">This price will be compared with the current low priority price for the VM size.</span></span> <span data-ttu-id="947ee-135">Inoltre, i prezzi vengono confrontati al momento della creazione/aggiornamento della priorità bassa VM/VMSS e l'operazione avrà esito positivo solo se maxPrice è maggiore del prezzo corrente con priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="947ee-135">Also, the prices are compared at the time of create/update of low priority VM/VMSS and the operation will only succeed if the maxPrice is greater than the current low priority price.</span></span> <span data-ttu-id="947ee-136">Il maxPrice verrà usato anche per rimuovere una VM/VMSS a priorità bassa se il prezzo corrente con priorità bassa supera il maxPrice dopo la creazione di VM/VMSS.</span><span class="sxs-lookup"><span data-stu-id="947ee-136">The maxPrice will also be used for evicting a low priority VM/VMSS if the current low priority price goes beyond the maxPrice after creation of VM/VMSS.</span></span> <span data-ttu-id="947ee-137">I valori possibili sono: qualsiasi valore decimale maggiore di zero.</span><span class="sxs-lookup"><span data-stu-id="947ee-137">Possible values are: any decimal value greater than zero.</span></span> <span data-ttu-id="947ee-138">Esempio: 0,01538.</span><span class="sxs-lookup"><span data-stu-id="947ee-138">Example: 0.01538.</span></span>  <span data-ttu-id="947ee-139">-1 indica che la priorità bassa VM/VMSS non deve essere sfrattata per motivi di prezzo.</span><span class="sxs-lookup"><span data-stu-id="947ee-139">-1 indicates that the low priority VM/VMSS should not be evicted for price reasons.</span></span> <span data-ttu-id="947ee-140">Inoltre, il prezzo massimo predefinito è-1 se non è fornito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="947ee-140">Also, the default max price is -1 if it is not provided by you.</span></span>

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

### <span data-ttu-id="947ee-141">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="947ee-141">-NoWait</span></span>
<span data-ttu-id="947ee-142">Avvia l'operazione e restituisce immediatamente, prima del completamento dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="947ee-142">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="947ee-143">Per determinare se l'operazione è stata completata correttamente, usare un altro meccanismo.</span><span class="sxs-lookup"><span data-stu-id="947ee-143">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="947ee-144">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="947ee-144">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="947ee-145">Specifica se WriteAccelerator deve essere abilitato o disabilitato nel disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="947ee-145">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="947ee-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="947ee-146">-ResourceGroupName</span></span>
<span data-ttu-id="947ee-147">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="947ee-147">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName, AssignIdentityParameterSet, ExplicitIdentityParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="947ee-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="947ee-148">-Tag</span></span>
<span data-ttu-id="947ee-149">Specifica che le risorse e i gruppi di risorse possono essere contrassegnati con un set di coppie nome/valore.</span><span class="sxs-lookup"><span data-stu-id="947ee-149">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="947ee-150">L'aggiunta di tag alle risorse consente di raggruppare le risorse tra gruppi di risorse e di creare visualizzazioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="947ee-150">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="947ee-151">Ogni risorsa o gruppo di risorse può avere un massimo di 15 contrassegni.</span><span class="sxs-lookup"><span data-stu-id="947ee-151">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="947ee-152">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="947ee-152">-UltraSSDEnabled</span></span>
<span data-ttu-id="947ee-153">Il contrassegno che consente o Disabilita una funzionalità per avere uno o più dischi di dati gestiti con il tipo di account di archiviazione UltraSSD_LRS nella VM.</span><span class="sxs-lookup"><span data-stu-id="947ee-153">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="947ee-154">Dischi gestiti con tipo di account di archiviazione UltraSSD_LRS possono essere aggiunti a una macchina virtuale solo se questa proprietà è abilitata.</span><span class="sxs-lookup"><span data-stu-id="947ee-154">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

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

### <span data-ttu-id="947ee-155">-VM</span><span class="sxs-lookup"><span data-stu-id="947ee-155">-VM</span></span>
<span data-ttu-id="947ee-156">Specifica un oggetto macchina virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="947ee-156">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="947ee-157">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="947ee-157">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="947ee-158">Questo oggetto macchina virtuale contiene lo stato aggiornato per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="947ee-158">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="947ee-159">-Confermare</span><span class="sxs-lookup"><span data-stu-id="947ee-159">-Confirm</span></span>
<span data-ttu-id="947ee-160">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="947ee-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="947ee-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="947ee-161">-WhatIf</span></span>
<span data-ttu-id="947ee-162">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="947ee-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="947ee-163">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="947ee-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="947ee-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="947ee-164">CommonParameters</span></span>
<span data-ttu-id="947ee-165">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="947ee-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="947ee-166">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="947ee-166">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="947ee-167">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="947ee-167">INPUTS</span></span>

### <span data-ttu-id="947ee-168">System. String</span><span class="sxs-lookup"><span data-stu-id="947ee-168">System.String</span></span>

### <span data-ttu-id="947ee-169">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="947ee-169">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="947ee-170">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="947ee-170">System.Boolean</span></span>

## <span data-ttu-id="947ee-171">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="947ee-171">OUTPUTS</span></span>

### <span data-ttu-id="947ee-172">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="947ee-172">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="947ee-173">Note</span><span class="sxs-lookup"><span data-stu-id="947ee-173">NOTES</span></span>

## <span data-ttu-id="947ee-174">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="947ee-174">RELATED LINKS</span></span>

[<span data-ttu-id="947ee-175">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="947ee-175">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="947ee-176">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="947ee-176">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="947ee-177">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="947ee-177">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="947ee-178">Riavviare-AzVM</span><span class="sxs-lookup"><span data-stu-id="947ee-178">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="947ee-179">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="947ee-179">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="947ee-180">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="947ee-180">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="947ee-181">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="947ee-181">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


