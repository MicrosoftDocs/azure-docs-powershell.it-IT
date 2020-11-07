---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVM.md
ms.openlocfilehash: e87536a524766ac86b80d790ee1372336fedba17
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93836596"
---
# <span data-ttu-id="26162-101">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="26162-101">Update-AzVM</span></span>

## <span data-ttu-id="26162-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="26162-102">SYNOPSIS</span></span>
<span data-ttu-id="26162-103">Aggiorna lo stato di una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="26162-103">Updates the state of an Azure virtual machine.</span></span>

## <span data-ttu-id="26162-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26162-104">SYNTAX</span></span>

### <span data-ttu-id="26162-105">ResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="26162-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26162-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="26162-106">AssignIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26162-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="26162-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26162-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="26162-108">IdParameterSetName</span></span>
```
Update-AzVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26162-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26162-109">DESCRIPTION</span></span>
<span data-ttu-id="26162-110">Il cmdlet **Update-AzVM** aggiorna lo stato di una macchina virtuale di Azure allo stato di un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="26162-110">The **Update-AzVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="26162-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26162-111">EXAMPLES</span></span>

### <span data-ttu-id="26162-112">Esempio 1: aggiornare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="26162-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="26162-113">Questo comando Aggiorna la macchina virtuale, $VirtualMachine, in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="26162-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="26162-114">Il comando lo aggiorna usando l'oggetto macchina virtuale archiviato nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="26162-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="26162-115">Per ottenere un oggetto macchina virtuale, usare il cmdlet **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="26162-115">To obtain a virtual machine object, use the **Get-AzVM** cmdlet.</span></span>

## <span data-ttu-id="26162-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26162-116">PARAMETERS</span></span>

### <span data-ttu-id="26162-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26162-117">-AsJob</span></span>
<span data-ttu-id="26162-118">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="26162-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="26162-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="26162-119">-AssignIdentity</span></span>
<span data-ttu-id="26162-120">Specifica l'identità assegnata dal sistema per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="26162-120">Specify the system-assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="26162-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26162-121">-DefaultProfile</span></span>
<span data-ttu-id="26162-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="26162-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26162-123">-ID</span><span class="sxs-lookup"><span data-stu-id="26162-123">-Id</span></span>
<span data-ttu-id="26162-124">Specifica l'ID risorsa della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="26162-124">Specifies the resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="26162-125">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="26162-125">-IdentityId</span></span>
<span data-ttu-id="26162-126">Specifica l'elenco delle identità utente associate alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="26162-126">Specifies the list of user identities associated with the virtual machine.</span></span>
<span data-ttu-id="26162-127">I riferimenti di identità utente saranno ID delle risorse ARM nella forma:'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="26162-127">The user identity references will be ARM resource IDs in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="26162-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="26162-128">-IdentityType</span></span>
<span data-ttu-id="26162-129">Tipo di identità utilizzata per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="26162-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="26162-130">I valori validi sono SystemAssigned, UserAssigned, SystemAssignedUserAssigned e None.</span><span class="sxs-lookup"><span data-stu-id="26162-130">Valid values are SystemAssigned, UserAssigned, SystemAssignedUserAssigned, and None.</span></span>

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

### <span data-ttu-id="26162-131">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="26162-131">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="26162-132">Specifica se WriteAccelerator deve essere abilitato o disabilitato nel disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="26162-132">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="26162-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26162-133">-ResourceGroupName</span></span>
<span data-ttu-id="26162-134">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="26162-134">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="26162-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="26162-135">-Tag</span></span>
<span data-ttu-id="26162-136">Specifica che le risorse e i gruppi di risorse possono essere contrassegnati con un set di coppie nome/valore.</span><span class="sxs-lookup"><span data-stu-id="26162-136">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="26162-137">L'aggiunta di tag alle risorse consente di raggruppare le risorse tra gruppi di risorse e di creare visualizzazioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="26162-137">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="26162-138">Ogni risorsa o gruppo di risorse può avere un massimo di 15 contrassegni.</span><span class="sxs-lookup"><span data-stu-id="26162-138">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="26162-139">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="26162-139">-UltraSSDEnabled</span></span>
<span data-ttu-id="26162-140">Il contrassegno che consente o Disabilita una funzionalità per avere uno o più dischi di dati gestiti con il tipo di account di archiviazione UltraSSD_LRS nella VM.</span><span class="sxs-lookup"><span data-stu-id="26162-140">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="26162-141">Dischi gestiti con tipo di account di archiviazione UltraSSD_LRS possono essere aggiunti a una macchina virtuale solo se questa proprietà è abilitata.</span><span class="sxs-lookup"><span data-stu-id="26162-141">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

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

### <span data-ttu-id="26162-142">-VM</span><span class="sxs-lookup"><span data-stu-id="26162-142">-VM</span></span>
<span data-ttu-id="26162-143">Specifica un oggetto macchina virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="26162-143">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="26162-144">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="26162-144">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="26162-145">Questo oggetto macchina virtuale contiene lo stato aggiornato per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="26162-145">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="26162-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="26162-146">-Confirm</span></span>
<span data-ttu-id="26162-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26162-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26162-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26162-148">-WhatIf</span></span>
<span data-ttu-id="26162-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26162-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26162-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26162-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26162-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26162-151">CommonParameters</span></span>
<span data-ttu-id="26162-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26162-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26162-153">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26162-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26162-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="26162-154">INPUTS</span></span>

### <span data-ttu-id="26162-155">System. String</span><span class="sxs-lookup"><span data-stu-id="26162-155">System.String</span></span>

### <span data-ttu-id="26162-156">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="26162-156">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="26162-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="26162-157">System.Boolean</span></span>

## <span data-ttu-id="26162-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26162-158">OUTPUTS</span></span>

### <span data-ttu-id="26162-159">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="26162-159">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="26162-160">Note</span><span class="sxs-lookup"><span data-stu-id="26162-160">NOTES</span></span>

## <span data-ttu-id="26162-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26162-161">RELATED LINKS</span></span>

[<span data-ttu-id="26162-162">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="26162-162">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="26162-163">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="26162-163">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="26162-164">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="26162-164">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="26162-165">Riavviare-AzVM</span><span class="sxs-lookup"><span data-stu-id="26162-165">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="26162-166">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="26162-166">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="26162-167">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="26162-167">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="26162-168">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="26162-168">New-AzVMConfig</span></span>](./New-AzVMConfig.md)


