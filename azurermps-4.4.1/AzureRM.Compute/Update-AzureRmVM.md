---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 38917534-49C6-47EA-B815-240F794EE655
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVM.md
ms.openlocfilehash: ad337c07f22b2805002347758f91bf0ea781adad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518331"
---
# <span data-ttu-id="0987e-101">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0987e-101">Update-AzureRmVM</span></span>

## <span data-ttu-id="0987e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0987e-102">SYNOPSIS</span></span>
<span data-ttu-id="0987e-103">Aggiorna lo stato di una macchina virtuale di Azure.</span><span class="sxs-lookup"><span data-stu-id="0987e-103">Updates the state of an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0987e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0987e-104">SYNTAX</span></span>

### <span data-ttu-id="0987e-105">ResourceGroupNameParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0987e-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Update-AzureRmVM -VM <PSVirtualMachine> [-Tags <Hashtable>] [-IdentityType <ResourceIdentityType>]
 [-AssignIdentity] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0987e-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="0987e-106">IdParameterSetName</span></span>
```
Update-AzureRmVM -VM <PSVirtualMachine> [-Tags <Hashtable>] [-IdentityType <ResourceIdentityType>]
 [-AssignIdentity] [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0987e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0987e-107">DESCRIPTION</span></span>
<span data-ttu-id="0987e-108">Il cmdlet **Update-AzureRmVM** aggiorna lo stato di una macchina virtuale di Azure allo stato di un oggetto macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0987e-108">The **Update-AzureRmVM** cmdlet updates the state of an Azure virtual machine to the state of a virtual machine object.</span></span>

## <span data-ttu-id="0987e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0987e-109">EXAMPLES</span></span>

### <span data-ttu-id="0987e-110">Esempio 1: aggiornare una macchina virtuale</span><span class="sxs-lookup"><span data-stu-id="0987e-110">Example 1: Update a virtual machine</span></span>
```
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="0987e-111">Questo comando Aggiorna la macchina virtuale, $VirtualMachine, in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="0987e-111">This command updates the virtual machine, $VirtualMachine, in ResourceGroup11.</span></span>
<span data-ttu-id="0987e-112">Il comando lo aggiorna usando l'oggetto macchina virtuale archiviato nella variabile $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="0987e-112">The command updates it by using the virtual machine object stored in the $VirtualMachine variable.</span></span>
<span data-ttu-id="0987e-113">Per ottenere un oggetto macchina virtuale, usare il cmdlet **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="0987e-113">To obtain a virtual machine object, use the **Get-AzureRmVM** cmdlet.</span></span>

## <span data-ttu-id="0987e-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0987e-114">PARAMETERS</span></span>

### <span data-ttu-id="0987e-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="0987e-115">-AssignIdentity</span></span>
<span data-ttu-id="0987e-116">Specificare l'identità di sistema assegnata per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0987e-116">Specify the system assigned identity for the virtual machine.</span></span>

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

### <span data-ttu-id="0987e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0987e-117">-DefaultProfile</span></span>
<span data-ttu-id="0987e-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0987e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0987e-119">-ID</span><span class="sxs-lookup"><span data-stu-id="0987e-119">-Id</span></span>
<span data-ttu-id="0987e-120">Specifica l'ID risorsa della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0987e-120">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="0987e-121">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="0987e-121">-IdentityType</span></span>
<span data-ttu-id="0987e-122">Tipo di identità utilizzata per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0987e-122">The type of identity used for the virtual machine.</span></span> <span data-ttu-id="0987e-123">Attualmente, l'unico tipo supportato è "SystemAssigned", che crea in modo implicito un'identità.</span><span class="sxs-lookup"><span data-stu-id="0987e-123">Currently, the only supported type is 'SystemAssigned', which implicitly creates an identity.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ResourceIdentityType]
Parameter Sets: (All)
Aliases: 
Accepted values: SystemAssigned

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0987e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0987e-124">-ResourceGroupName</span></span>
<span data-ttu-id="0987e-125">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0987e-125">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0987e-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="0987e-126">-Tags</span></span>
<span data-ttu-id="0987e-127">Specifica che le risorse e i gruppi di risorse possono essere contrassegnati con un set di coppie nome/valore.</span><span class="sxs-lookup"><span data-stu-id="0987e-127">Specifies the resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="0987e-128">L'aggiunta di tag alle risorse consente di raggruppare le risorse tra gruppi di risorse e di creare visualizzazioni personalizzate.</span><span class="sxs-lookup"><span data-stu-id="0987e-128">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="0987e-129">Ogni risorsa o gruppo di risorse può avere un massimo di 15 contrassegni.</span><span class="sxs-lookup"><span data-stu-id="0987e-129">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="0987e-130">-VM</span><span class="sxs-lookup"><span data-stu-id="0987e-130">-VM</span></span>
<span data-ttu-id="0987e-131">Specifica un oggetto macchina virtuale locale.</span><span class="sxs-lookup"><span data-stu-id="0987e-131">Specifies a local virtual machine object.</span></span>
<span data-ttu-id="0987e-132">Per ottenere un oggetto macchina virtuale, usare il cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="0987e-132">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="0987e-133">Questo oggetto macchina virtuale contiene lo stato aggiornato per la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="0987e-133">This virtual machine object contains the updated state for the virtual machine.</span></span>

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

### <span data-ttu-id="0987e-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0987e-134">-Confirm</span></span>
<span data-ttu-id="0987e-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0987e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0987e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0987e-136">-WhatIf</span></span>
<span data-ttu-id="0987e-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0987e-137">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="0987e-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0987e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0987e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0987e-139">CommonParameters</span></span>
<span data-ttu-id="0987e-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0987e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0987e-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0987e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0987e-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0987e-142">INPUTS</span></span>

## <span data-ttu-id="0987e-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0987e-143">OUTPUTS</span></span>

## <span data-ttu-id="0987e-144">Note</span><span class="sxs-lookup"><span data-stu-id="0987e-144">NOTES</span></span>

## <span data-ttu-id="0987e-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0987e-145">RELATED LINKS</span></span>

[<span data-ttu-id="0987e-146">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0987e-146">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="0987e-147">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0987e-147">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="0987e-148">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0987e-148">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="0987e-149">Riavviare-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0987e-149">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="0987e-150">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0987e-150">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="0987e-151">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0987e-151">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="0987e-152">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="0987e-152">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


