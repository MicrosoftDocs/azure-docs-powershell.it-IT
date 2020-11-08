---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsm.md
ms.openlocfilehash: 6555299726d8dcf443382f72c2aba6324b6b377d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193252"
---
# <span data-ttu-id="e1723-101">Remove-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="e1723-101">Remove-AzManagedHsm</span></span>

## <span data-ttu-id="e1723-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e1723-102">SYNOPSIS</span></span>
<span data-ttu-id="e1723-103">Elimina un HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="e1723-103">Deletes a managed HSM.</span></span>

## <span data-ttu-id="e1723-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e1723-104">SYNTAX</span></span>

### <span data-ttu-id="e1723-105">RemoveManagedHsmByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e1723-105">RemoveManagedHsmByName (Default)</span></span>
```
Remove-AzManagedHsm [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1723-106">RemoveManagedHsmByInputObject</span><span class="sxs-lookup"><span data-stu-id="e1723-106">RemoveManagedHsmByInputObject</span></span>
```
Remove-AzManagedHsm [-InputObject] <PSManagedHsm> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1723-107">RemoveManagedHsmByResourceId</span><span class="sxs-lookup"><span data-stu-id="e1723-107">RemoveManagedHsmByResourceId</span></span>
```
Remove-AzManagedHsm [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1723-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1723-108">DESCRIPTION</span></span>
<span data-ttu-id="e1723-109">Il cmdlet **Remove-AzManagedHsm** Elimina l'HSM gestito specificato.</span><span class="sxs-lookup"><span data-stu-id="e1723-109">The **Remove-AzManagedHsm** cmdlet deletes the specified managed HSM.</span></span>
<span data-ttu-id="e1723-110">Elimina inoltre tutte le chiavi contenute in quell'istanza.</span><span class="sxs-lookup"><span data-stu-id="e1723-110">It also deletes all keys contained in that instance.</span></span>
<span data-ttu-id="e1723-111">Tieni presente che, anche se specificando il gruppo di risorse è facoltativo per questo cmdlet, dovresti migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="e1723-111">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="e1723-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e1723-112">EXAMPLES</span></span>

### <span data-ttu-id="e1723-113">Esempio 1: rimuovere un HSM gestito</span><span class="sxs-lookup"><span data-stu-id="e1723-113">Example 1: Remove a managed HSM</span></span>
```powershell
PS C:\> Remove-AzManagedHsm -HsmName 'myhsm' -Force

True
```

<span data-ttu-id="e1723-114">Questo comando rimuove l'HSM gestito denominato myhsm dall'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="e1723-114">This command removes the managed hsm named myhsm from your current subscription.</span></span>

### <span data-ttu-id="e1723-115">Esempio 2: rimuovere un HSM gestito da un gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="e1723-115">Example 2: Remove a managed hsm from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzManagedHsm -HsmName 'myhsm' -ResourceGroupName "myrg1" -PassThru

True
```

<span data-ttu-id="e1723-116">Questo comando rimuove l'HSM gestito denominato myhsm dal gruppo di risorse denominato myrg1.</span><span class="sxs-lookup"><span data-stu-id="e1723-116">This command removes the managed hsm named myhsm from the resource group named myrg1.</span></span>
<span data-ttu-id="e1723-117">Se non specifichi il nome del gruppo di risorse, il cmdlet cerca l'HSM gestito con nome da eliminare nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="e1723-117">If you do not specify the resource group name, the cmdlet searches for the named managed HSM to delete in your current subscription.</span></span>

## <span data-ttu-id="e1723-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e1723-118">PARAMETERS</span></span>

### <span data-ttu-id="e1723-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1723-119">-AsJob</span></span>
<span data-ttu-id="e1723-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e1723-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e1723-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1723-121">-DefaultProfile</span></span>
<span data-ttu-id="e1723-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e1723-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1723-123">-Force</span><span class="sxs-lookup"><span data-stu-id="e1723-123">-Force</span></span>
<span data-ttu-id="e1723-124">Indica che il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="e1723-124">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="e1723-125">Per impostazione predefinita, questo cmdlet richiede di confermare che si vuole eliminare l'HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="e1723-125">By default, this cmdlet prompts you to confirm that you want to delete the managed HSM.</span></span>

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

### <span data-ttu-id="e1723-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1723-126">-InputObject</span></span>
<span data-ttu-id="e1723-127">Oggetto HSM gestito da eliminare.</span><span class="sxs-lookup"><span data-stu-id="e1723-127">Managed HSM object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: RemoveManagedHsmByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1723-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="e1723-128">-Name</span></span>
<span data-ttu-id="e1723-129">Specifica il nome dell'HSM gestito da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="e1723-129">Specifies the name of the managed HSM to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByName
Aliases: HsmName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1723-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1723-130">-PassThru</span></span>
<span data-ttu-id="e1723-131">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="e1723-131">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="e1723-132">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="e1723-132">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="e1723-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1723-133">-ResourceGroupName</span></span>
<span data-ttu-id="e1723-134">Specifica il nome del gruppo di risorse per l'HSM gestito da Azure da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="e1723-134">Specifies the name of resource group for Azure managed HSM to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1723-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e1723-135">-ResourceId</span></span>
<span data-ttu-id="e1723-136">ID risorsa ManagedHsm.</span><span class="sxs-lookup"><span data-stu-id="e1723-136">ManagedHsm Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1723-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e1723-137">-Confirm</span></span>
<span data-ttu-id="e1723-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1723-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1723-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1723-139">-WhatIf</span></span>
<span data-ttu-id="e1723-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e1723-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1723-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e1723-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1723-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1723-142">CommonParameters</span></span>
<span data-ttu-id="e1723-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1723-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1723-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1723-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1723-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e1723-145">INPUTS</span></span>

### <span data-ttu-id="e1723-146">Microsoft. Azure. Commands. Vault. Models. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="e1723-146">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="e1723-147">System. String</span><span class="sxs-lookup"><span data-stu-id="e1723-147">System.String</span></span>

## <span data-ttu-id="e1723-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e1723-148">OUTPUTS</span></span>

### <span data-ttu-id="e1723-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e1723-149">System.Boolean</span></span>

## <span data-ttu-id="e1723-150">Note</span><span class="sxs-lookup"><span data-stu-id="e1723-150">NOTES</span></span>

## <span data-ttu-id="e1723-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e1723-151">RELATED LINKS</span></span>

[<span data-ttu-id="e1723-152">Get-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="e1723-152">Get-AzManagedHsm</span></span>](./Get-AzManagedHsm.md)

[<span data-ttu-id="e1723-153">New-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="e1723-153">New-AzManagedHsm</span></span>](./New-AzManagedHsm.md)

[<span data-ttu-id="e1723-154">Update-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="e1723-154">Update-AzManagedHsm</span></span>](./Update-AzManagedHsm.md)