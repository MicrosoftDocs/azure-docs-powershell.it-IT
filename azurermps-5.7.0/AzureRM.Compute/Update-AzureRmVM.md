---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermvm
schema: 2.0.0
ms.openlocfilehash: 55f7b56f57bf18c4a3bf3198e8335cff08caae97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508280"
---
# <span data-ttu-id="7f734-101">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7f734-101">Update-AzureRmVM</span></span>

## <span data-ttu-id="7f734-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f734-102">SYNOPSIS</span></span>
<span data-ttu-id="7f734-103">Aggiorna lo stato di una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="7f734-103">Updates the state of an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f734-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f734-104">SYNTAX</span></span>

### <span data-ttu-id="7f734-105">ResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7f734-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 [-OsDiskWriteAccelerator <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f734-106">AssignIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f734-106">AssignIdentityParameterSet</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-AssignIdentity]
 [-OsDiskWriteAccelerator <Boolean>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f734-107">ExplicitIdentityParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f734-107">ExplicitIdentityParameterSet</span></span>
```
Update-AzureRmVM [-ResourceGroupName] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>]
 -IdentityType <ResourceIdentityType> [-IdentityId <String[]>] [-OsDiskWriteAccelerator <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f734-108">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="7f734-108">IdParameterSetName</span></span>
```
Update-AzureRmVM [-Id] <String> -VM <PSVirtualMachine> [-Tag <Hashtable>] [-OsDiskWriteAccelerator <Boolean>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f734-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f734-109">DESCRIPTION</span></span>
<span data-ttu-id="7f734-110">Il cmdlet **Update-AzureRmVM** aggiorna lo stato di una macchina virtuale di Azure allo stato di un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f734-110">The **Update-AzureRmVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="7f734-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f734-111">EXAMPLES</span></span>

### <span data-ttu-id="7f734-112">Esempio 1: aggiornare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="7f734-112">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="7f734-113">Questo comando Aggiorna la macchina virtuale, $VirtualMachine, in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="7f734-113">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="7f734-114">Il comando lo aggiorna usando l'oggetto macchina virtuale archiviato nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="7f734-114">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="7f734-115">Per ottenere un oggetto macchina virtuale, usare il cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="7f734-115">To obtain a virtual machine object, use the **Get-AzureRmVM** cmdlet.</span></span>

## <span data-ttu-id="7f734-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f734-116">PARAMETERS</span></span>

### <span data-ttu-id="7f734-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f734-117">-AsJob</span></span>
<span data-ttu-id="7f734-118">Esegui cmdlet in background e restituisci un processo per tenere traccia dello stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="7f734-118">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7f734-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="7f734-119">-AssignIdentity</span></span>
<span data-ttu-id="7f734-120">Specificare l'identità di sistema assegnata per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f734-120">Specify the system assigned identity for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AssignIdentityParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f734-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f734-121">-DefaultProfile</span></span>
<span data-ttu-id="7f734-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7f734-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f734-123">-ID</span><span class="sxs-lookup"><span data-stu-id="7f734-123">-Id</span></span>
<span data-ttu-id="7f734-124">Specifica l'ID risorsa della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f734-124">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f734-125">-IdentityId</span><span class="sxs-lookup"><span data-stu-id="7f734-125">-IdentityId</span></span>
<span data-ttu-id="7f734-126">Specifica l'elenco delle identità utente associate al set di scale della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f734-126">Specifies the list of user identities associated with the virtual machine scale set.</span></span>
<span data-ttu-id="7f734-127">I riferimenti di identità utente saranno ID delle risorse ARM nella forma:'/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span><span class="sxs-lookup"><span data-stu-id="7f734-127">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="7f734-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="7f734-128">-IdentityType</span></span>
<span data-ttu-id="7f734-129">Tipo di identità utilizzata per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f734-129">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="7f734-130">Attualmente, l'unico tipo supportato è "SystemAssigned", che crea in modo implicito un'identità.</span><span class="sxs-lookup"><span data-stu-id="7f734-130">Currently, the only supported type is 'SystemAssigned', which implicitly creates an identity.</span></span>

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

### <span data-ttu-id="7f734-131">-OsDiskWriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="7f734-131">-OsDiskWriteAccelerator</span></span>
<span data-ttu-id="7f734-132">Specifica se WriteAccelerator deve essere abilitato o disabilitato nel disco del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7f734-132">Specifies whether WriteAccelerator should be enabled or disabled on the OS disk.</span></span>

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

### <span data-ttu-id="7f734-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f734-133">-ResourceGroupName</span></span>
<span data-ttu-id="7f734-134">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f734-134">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName, AssignIdentityParameterSet, ExplicitIdentityParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f734-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="7f734-135">-Tag</span></span>
<span data-ttu-id="7f734-136">Specifica che le risorse e i gruppi di risorse possono essere contrassegnati con un set di coppie nome/valore.</span><span class="sxs-lookup"><span data-stu-id="7f734-136">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="7f734-137">L'aggiunta di tag alle risorse consente di raggruppare le risorse tra gruppi di risorse e di creare visualizzazioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="7f734-137">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="7f734-138">Ogni risorsa o gruppo di risorse può avere un massimo di 15 contrassegni.</span><span class="sxs-lookup"><span data-stu-id="7f734-138">Each resource or resource group can have a maximum of 15 tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f734-139">-VM</span><span class="sxs-lookup"><span data-stu-id="7f734-139">-VM</span></span>
<span data-ttu-id="7f734-140">Specifica un oggetto macchina virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="7f734-140">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="7f734-141">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="7f734-141">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="7f734-142">Questo oggetto macchina virtuale contiene lo stato aggiornato per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="7f734-142">This virtual machine object contains the updated state for the virtual machine.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f734-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7f734-143">-Confirm</span></span>
<span data-ttu-id="7f734-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f734-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f734-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f734-145">-WhatIf</span></span>
<span data-ttu-id="7f734-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7f734-146">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="7f734-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7f734-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f734-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f734-148">CommonParameters</span></span>
<span data-ttu-id="7f734-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f734-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f734-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f734-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f734-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f734-151">INPUTS</span></span>

### <span data-ttu-id="7f734-152">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7f734-152">PSVirtualMachine</span></span>
<span data-ttu-id="7f734-153">Il parametro ' VM ' accetta il valore di tipo ' PSVirtualMachine ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7f734-153">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="7f734-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f734-154">OUTPUTS</span></span>

### <span data-ttu-id="7f734-155">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="7f734-155">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="7f734-156">Note</span><span class="sxs-lookup"><span data-stu-id="7f734-156">NOTES</span></span>

## <span data-ttu-id="7f734-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f734-157">RELATED LINKS</span></span>

[<span data-ttu-id="7f734-158">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7f734-158">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="7f734-159">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7f734-159">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="7f734-160">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7f734-160">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="7f734-161">Riavviare-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7f734-161">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="7f734-162">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7f734-162">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="7f734-163">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7f734-163">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="7f734-164">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="7f734-164">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


