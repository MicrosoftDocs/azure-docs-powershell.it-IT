---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedHsm.md
ms.openlocfilehash: ac778148f90d90caf52fdb3c029376daf4470069
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991114"
---
# <span data-ttu-id="a1d8f-101">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="a1d8f-101">Remove-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="a1d8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1d8f-102">SYNOPSIS</span></span>
<span data-ttu-id="a1d8f-103">Elimina un servizio HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="a1d8f-103">Deletes a managed HSM.</span></span>

## <span data-ttu-id="a1d8f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1d8f-104">SYNTAX</span></span>

### <span data-ttu-id="a1d8f-105">RemoveManagedHsmByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a1d8f-105">RemoveManagedHsmByName (Default)</span></span>
```
Remove-AzKeyVaultManagedHsm [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1d8f-106">RemoveManagedHsmByInputObject</span><span class="sxs-lookup"><span data-stu-id="a1d8f-106">RemoveManagedHsmByInputObject</span></span>
```
Remove-AzKeyVaultManagedHsm [-InputObject] <PSManagedHsm> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1d8f-107">RemoveManagedHsmByResourceId</span><span class="sxs-lookup"><span data-stu-id="a1d8f-107">RemoveManagedHsmByResourceId</span></span>
```
Remove-AzKeyVaultManagedHsm [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1d8f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a1d8f-108">DESCRIPTION</span></span>
<span data-ttu-id="a1d8f-109">Il cmdlet **Remove-AzKeyVaultManagedHsm** elimina il servizio HSM gestito specificato.</span><span class="sxs-lookup"><span data-stu-id="a1d8f-109">The **Remove-AzKeyVaultManagedHsm** cmdlet deletes the specified managed HSM.</span></span>
<span data-ttu-id="a1d8f-110">Elimina anche tutte le chiavi contenute nell'istanza.</span><span class="sxs-lookup"><span data-stu-id="a1d8f-110">It also deletes all keys contained in that instance.</span></span>
<span data-ttu-id="a1d8f-111">Anche se è facoltativo specificare il gruppo di risorse per questo cmdlet, è consigliabile farlo per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="a1d8f-111">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="a1d8f-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1d8f-112">EXAMPLES</span></span>

### <span data-ttu-id="a1d8f-113">Esempio 1: Rimuovere un servizio HSM gestito</span><span class="sxs-lookup"><span data-stu-id="a1d8f-113">Example 1: Remove a managed HSM</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedHsm -HsmName 'myhsm' -Force

True
```

<span data-ttu-id="a1d8f-114">Questo comando rimuove dall'abbonamento corrente l'hsm gestito denominato myhsm.</span><span class="sxs-lookup"><span data-stu-id="a1d8f-114">This command removes the managed hsm named myhsm from your current subscription.</span></span>

### <span data-ttu-id="a1d8f-115">Esempio 2: Rimuovere un'hsm gestita da un gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="a1d8f-115">Example 2: Remove a managed hsm from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedHsm -HsmName 'myhsm' -ResourceGroupName "myrg1" -PassThru

True
```

<span data-ttu-id="a1d8f-116">Questo comando rimuove l'hsm gestito denominato myhsm dal gruppo di risorse denominato myrg1.</span><span class="sxs-lookup"><span data-stu-id="a1d8f-116">This command removes the managed hsm named myhsm from the resource group named myrg1.</span></span>
<span data-ttu-id="a1d8f-117">Se non si specifica il nome del gruppo di risorse, il cmdlet cerca il servizio HSM gestito denominato per eliminarlo nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="a1d8f-117">If you do not specify the resource group name, the cmdlet searches for the named managed HSM to delete in your current subscription.</span></span>

## <span data-ttu-id="a1d8f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1d8f-118">PARAMETERS</span></span>

### <span data-ttu-id="a1d8f-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1d8f-119">-AsJob</span></span>
<span data-ttu-id="a1d8f-120">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a1d8f-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1d8f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1d8f-121">-DefaultProfile</span></span>
<span data-ttu-id="a1d8f-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a1d8f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1d8f-123">-Force</span><span class="sxs-lookup"><span data-stu-id="a1d8f-123">-Force</span></span>
<span data-ttu-id="a1d8f-124">Indica che il cmdlet non richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="a1d8f-124">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="a1d8f-125">Per impostazione predefinita, questo cmdlet chiede di confermare l'eliminazione dell'HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="a1d8f-125">By default, this cmdlet prompts you to confirm that you want to delete the managed HSM.</span></span>

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

### <span data-ttu-id="a1d8f-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1d8f-126">-InputObject</span></span>
<span data-ttu-id="a1d8f-127">Oggetto HSM gestito da eliminare.</span><span class="sxs-lookup"><span data-stu-id="a1d8f-127">Managed HSM object to be deleted.</span></span>

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

### <span data-ttu-id="a1d8f-128">-Name</span><span class="sxs-lookup"><span data-stu-id="a1d8f-128">-Name</span></span>
<span data-ttu-id="a1d8f-129">Specifica il nome dell'HSM gestito da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="a1d8f-129">Specifies the name of the managed HSM to remove.</span></span>

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

### <span data-ttu-id="a1d8f-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1d8f-130">-PassThru</span></span>
<span data-ttu-id="a1d8f-131">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a1d8f-131">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a1d8f-132">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="a1d8f-132">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a1d8f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1d8f-133">-ResourceGroupName</span></span>
<span data-ttu-id="a1d8f-134">Specifica il nome del gruppo di risorse da rimuovere per HSM gestito da Azure.</span><span class="sxs-lookup"><span data-stu-id="a1d8f-134">Specifies the name of resource group for Azure managed HSM to remove.</span></span>

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

### <span data-ttu-id="a1d8f-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1d8f-135">-ResourceId</span></span>
<span data-ttu-id="a1d8f-136">ID risorsa ManagedHsm.</span><span class="sxs-lookup"><span data-stu-id="a1d8f-136">ManagedHsm Resource Id.</span></span>

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

### <span data-ttu-id="a1d8f-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a1d8f-137">-Confirm</span></span>
<span data-ttu-id="a1d8f-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1d8f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1d8f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1d8f-139">-WhatIf</span></span>
<span data-ttu-id="a1d8f-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1d8f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1d8f-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1d8f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1d8f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1d8f-142">CommonParameters</span></span>
<span data-ttu-id="a1d8f-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1d8f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1d8f-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a1d8f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1d8f-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="a1d8f-145">INPUTS</span></span>

### <span data-ttu-id="a1d8f-146">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="a1d8f-146">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="a1d8f-147">System.String</span><span class="sxs-lookup"><span data-stu-id="a1d8f-147">System.String</span></span>

## <span data-ttu-id="a1d8f-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1d8f-148">OUTPUTS</span></span>

### <span data-ttu-id="a1d8f-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a1d8f-149">System.Boolean</span></span>

## <span data-ttu-id="a1d8f-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="a1d8f-150">NOTES</span></span>

## <span data-ttu-id="a1d8f-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1d8f-151">RELATED LINKS</span></span>

[<span data-ttu-id="a1d8f-152">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="a1d8f-152">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="a1d8f-153">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="a1d8f-153">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="a1d8f-154">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="a1d8f-154">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)