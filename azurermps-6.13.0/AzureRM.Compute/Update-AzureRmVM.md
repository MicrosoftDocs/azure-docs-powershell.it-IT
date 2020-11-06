---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmVM.md
ms.openlocfilehash: e29eb849dfd7ec3417daaea1b0cae447d20f1322
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518808"
---
# <span data-ttu-id="9cf6a-101">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9cf6a-101">Update-AzureRmVM</span></span>

## <span data-ttu-id="9cf6a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9cf6a-102">SYNOPSIS</span></span>
<span data-ttu-id="9cf6a-103">Aggiorna lo stato di una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="9cf6a-103">Updates the state of an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cf6a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9cf6a-104">SYNTAX</span></span>

### <span data-ttu-id="9cf6a-105">ResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9cf6a-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cf6a-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cf6a-106">AssignIdentityParameterSet</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-UltraSSDEnabled <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cf6a-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="9cf6a-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9cf6a-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9cf6a-108">IdParameterSetName</span></span>
```
Update-AzureRmVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-UltraSSDEnabled <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9cf6a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9cf6a-109">DESCRIPTION</span></span>
<span data-ttu-id="9cf6a-110">Il cmdlet **Update-AzureRmVM** aggiorna lo stato di una macchina virtuale di Azure allo stato di un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9cf6a-110">The **Update-AzureRmVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="9cf6a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9cf6a-111">EXAMPLES</span></span>

### <span data-ttu-id="9cf6a-112">Esempio 1: aggiornare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="9cf6a-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="9cf6a-113">Questo comando Aggiorna la macchina virtuale, $VirtualMachine, in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="9cf6a-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="9cf6a-114">Il comando lo aggiorna usando l'oggetto macchina virtuale archiviato nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="9cf6a-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="9cf6a-115">Per ottenere un oggetto macchina virtuale, usare il cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="9cf6a-115">To obtain a virtual machine object, use the **Get-AzureRmVM** cmdlet.</span></span>

## <span data-ttu-id="9cf6a-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9cf6a-116">PARAMETERS</span></span>

### <span data-ttu-id="9cf6a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9cf6a-117">-AsJob</span></span>
<span data-ttu-id="9cf6a-118">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="9cf6a-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="9cf6a-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="9cf6a-119">-AssignIdentity</span></span>
<span data-ttu-id="9cf6a-120">Specificare l'identità di sistema assegnata per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9cf6a-120">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="9cf6a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cf6a-121">-DefaultProfile</span></span>
<span data-ttu-id="9cf6a-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9cf6a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9cf6a-123">-ID</span><span class="sxs-lookup"><span data-stu-id="9cf6a-123">-Id</span></span>
<span data-ttu-id="9cf6a-124">Specifica l'ID risorsa della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9cf6a-124">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="9cf6a-125">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="9cf6a-125">-IdentityId</span></span>
<span data-ttu-id="9cf6a-126">Specifica l'elenco delle identità utente associate al set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9cf6a-126">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="9cf6a-127">I riferimenti di identità utente saranno ID delle risorse ARM nella forma:'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="9cf6a-127">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="9cf6a-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="9cf6a-128">-IdentityType</span></span>
<span data-ttu-id="9cf6a-129">Tipo di identità utilizzata per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9cf6a-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="9cf6a-130">Attualmente, l'unico tipo supportato è "SystemAssigned", che crea in modo implicito un'identità.</span><span class="sxs-lookup"><span data-stu-id="9cf6a-130">Currently, the only supported type is 'SystemAssigned', which implicitly creates an identity.</span></span>

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

### <span data-ttu-id="9cf6a-131">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="9cf6a-131">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="9cf6a-132">Specifica se WriteAccelerator deve essere abilitato o disabilitato nel disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="9cf6a-132">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="9cf6a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cf6a-133">-ResourceGroupName</span></span>
<span data-ttu-id="9cf6a-134">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9cf6a-134">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9cf6a-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="9cf6a-135">-Tag</span></span>
<span data-ttu-id="9cf6a-136">Specifica che le risorse e i gruppi di risorse possono essere contrassegnati con un set di coppie nome/valore.</span><span class="sxs-lookup"><span data-stu-id="9cf6a-136">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="9cf6a-137">L'aggiunta di tag alle risorse consente di raggruppare le risorse tra gruppi di risorse e di creare visualizzazioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="9cf6a-137">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="9cf6a-138">Ogni risorsa o gruppo di risorse può avere un massimo di 15 contrassegni.</span><span class="sxs-lookup"><span data-stu-id="9cf6a-138">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="9cf6a-139">-UltraSSDEnabled</span><span class="sxs-lookup"><span data-stu-id="9cf6a-139">-UltraSSDEnabled</span></span>
<span data-ttu-id="9cf6a-140">Il contrassegno che consente o Disabilita una funzionalità per avere uno o più dischi di dati gestiti con il tipo di account di archiviazione UltraSSD_LRS nella VM.</span><span class="sxs-lookup"><span data-stu-id="9cf6a-140">The flag that enables or disables a capability to have one or more managed data disks with UltraSSD_LRS storage account type on the VM.</span></span>
<span data-ttu-id="9cf6a-141">Dischi gestiti con tipo di account di archiviazione UltraSSD_LRS possono essere aggiunti a una macchina virtuale solo se questa proprietà è abilitata.</span><span class="sxs-lookup"><span data-stu-id="9cf6a-141">Managed disks with storage account type UltraSSD_LRS can be added to a virtual machine only if this property is enabled.</span></span>

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

### <span data-ttu-id="9cf6a-142">-VM</span><span class="sxs-lookup"><span data-stu-id="9cf6a-142">-VM</span></span>
<span data-ttu-id="9cf6a-143">Specifica un oggetto macchina virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="9cf6a-143">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="9cf6a-144">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="9cf6a-144">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="9cf6a-145">Questo oggetto macchina virtuale contiene lo stato aggiornato per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9cf6a-145">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="9cf6a-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9cf6a-146">-Confirm</span></span>
<span data-ttu-id="9cf6a-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9cf6a-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cf6a-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cf6a-148">-WhatIf</span></span>
<span data-ttu-id="9cf6a-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9cf6a-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cf6a-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9cf6a-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cf6a-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cf6a-151">CommonParameters</span></span>
<span data-ttu-id="9cf6a-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cf6a-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cf6a-153">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cf6a-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cf6a-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9cf6a-154">INPUTS</span></span>

### <span data-ttu-id="9cf6a-155">System. String</span><span class="sxs-lookup"><span data-stu-id="9cf6a-155">System.String</span></span>

### <span data-ttu-id="9cf6a-156">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9cf6a-156">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="9cf6a-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9cf6a-157">OUTPUTS</span></span>

### <span data-ttu-id="9cf6a-158">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9cf6a-158">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9cf6a-159">Note</span><span class="sxs-lookup"><span data-stu-id="9cf6a-159">NOTES</span></span>

## <span data-ttu-id="9cf6a-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9cf6a-160">RELATED LINKS</span></span>

[<span data-ttu-id="9cf6a-161">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9cf6a-161">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="9cf6a-162">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9cf6a-162">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="9cf6a-163">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9cf6a-163">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="9cf6a-164">Riavviare-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9cf6a-164">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="9cf6a-165">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9cf6a-165">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="9cf6a-166">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="9cf6a-166">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="9cf6a-167">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="9cf6a-167">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


