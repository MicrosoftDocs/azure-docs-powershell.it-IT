---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
ms.openlocfilehash: 04b4f6be3393eae0fba2f98c477b4174612d2b79
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001262"
---
# <span data-ttu-id="824c1-101">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="824c1-101">Remove-AzKeyVault</span></span>

## <span data-ttu-id="824c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="824c1-102">SYNOPSIS</span></span>
<span data-ttu-id="824c1-103">Elimina un vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="824c1-103">Deletes a key vault.</span></span>

## <span data-ttu-id="824c1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="824c1-104">SYNTAX</span></span>

### <span data-ttu-id="824c1-105">ByAvailableVault (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="824c1-105">ByAvailableVault (Default)</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="824c1-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="824c1-106">ByDeletedVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="824c1-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="824c1-107">InputObjectByAvailableVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="824c1-108">InputObjectByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="824c1-108">InputObjectByDeletedVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="824c1-109">ResourceIdByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="824c1-109">ResourceIdByAvailableVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [[-Location] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="824c1-110">ResourceIdByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="824c1-110">ResourceIdByDeletedVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="824c1-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="824c1-111">DESCRIPTION</span></span>
<span data-ttu-id="824c1-112">Il cmdlet **Remove-AzKeyVault** elimina il vault della chiave specificato.</span><span class="sxs-lookup"><span data-stu-id="824c1-112">The **Remove-AzKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="824c1-113">Elimina anche tutte le chiavi e i segreti contenuti in quell'istanza.</span><span class="sxs-lookup"><span data-stu-id="824c1-113">It also deletes all keys and secrets contained in that instance.</span></span>
<span data-ttu-id="824c1-114">Anche se è facoltativo specificare il gruppo di risorse per questo cmdlet, è consigliabile farlo per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="824c1-114">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="824c1-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="824c1-115">EXAMPLES</span></span>

### <span data-ttu-id="824c1-116">Esempio 1: Rimuovere un vault delle chiavi</span><span class="sxs-lookup"><span data-stu-id="824c1-116">Example 1: Remove a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVault -VaultName "Contoso03Vault" -PassThru

True
```

<span data-ttu-id="824c1-117">Questo comando rimuove la chiave vault denominata Contoso03Vault dall'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="824c1-117">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="824c1-118">Esempio 2: Rimuovere un vault chiave da un gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="824c1-118">Example 2: Remove a key vault from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVault -Name "Contoso03Vault" -ResourceGroupName "Group14" -PassThru

True
```

<span data-ttu-id="824c1-119">Questo comando rimuove la chiave vault denominata Contoso03Vault dal gruppo di risorse denominato.</span><span class="sxs-lookup"><span data-stu-id="824c1-119">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="824c1-120">Se non si specifica il nome del gruppo di risorse, il cmdlet cerca il vault con chiave denominata da eliminare nella sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="824c1-120">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

### <span data-ttu-id="824c1-121">Esempio 3: Rimuovere un'hsm gestita</span><span class="sxs-lookup"><span data-stu-id="824c1-121">Example 3: Remove a managed hsm</span></span>
```powershell
PS C:\>  Remove-AzKeyVault -Name "testManagedHsm" -Hsm -PassThru

True
```

<span data-ttu-id="824c1-122">Questo comando rimuove l'hsm gestito denominato testManagedHsm dalla sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="824c1-122">This command removes the managed hsm named testManagedHsm from your current subscription.</span></span>

## <span data-ttu-id="824c1-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="824c1-123">PARAMETERS</span></span>

### <span data-ttu-id="824c1-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="824c1-124">-AsJob</span></span>
<span data-ttu-id="824c1-125">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="824c1-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="824c1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="824c1-126">-DefaultProfile</span></span>
<span data-ttu-id="824c1-127">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="824c1-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="824c1-128">-Force</span><span class="sxs-lookup"><span data-stu-id="824c1-128">-Force</span></span>
<span data-ttu-id="824c1-129">Indica che il cmdlet non richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="824c1-129">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="824c1-130">Per impostazione predefinita, questo cmdlet chiede di confermare l'eliminazione del vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="824c1-130">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="824c1-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="824c1-131">-InputObject</span></span>
<span data-ttu-id="824c1-132">Oggetto Vault chiave da eliminare.</span><span class="sxs-lookup"><span data-stu-id="824c1-132">Key Vault object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectByAvailableVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="824c1-133">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="824c1-133">-InRemovedState</span></span>
<span data-ttu-id="824c1-134">Rimuovere definitivamente il vault eliminato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="824c1-134">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault, InputObjectByDeletedVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="824c1-135">-Location</span><span class="sxs-lookup"><span data-stu-id="824c1-135">-Location</span></span>
<span data-ttu-id="824c1-136">Posizione del vault eliminato.</span><span class="sxs-lookup"><span data-stu-id="824c1-136">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault, ResourceIdByAvailableVault
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="824c1-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="824c1-137">-PassThru</span></span>
<span data-ttu-id="824c1-138">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="824c1-138">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="824c1-139">Se questa opzione è specificata, restituisce true se ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="824c1-139">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="824c1-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="824c1-140">-ResourceGroupName</span></span>
<span data-ttu-id="824c1-141">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="824c1-141">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="824c1-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="824c1-142">-ResourceId</span></span>
<span data-ttu-id="824c1-143">ID risorsa KeyVault.</span><span class="sxs-lookup"><span data-stu-id="824c1-143">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByAvailableVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="824c1-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="824c1-144">-VaultName</span></span>
<span data-ttu-id="824c1-145">Specifica il nome del vault della chiave da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="824c1-145">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault, ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="824c1-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="824c1-146">-Confirm</span></span>
<span data-ttu-id="824c1-147">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="824c1-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="824c1-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="824c1-148">-WhatIf</span></span>
<span data-ttu-id="824c1-149">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="824c1-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="824c1-150">Il cmdlet non viene eseguito. Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="824c1-150">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="824c1-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="824c1-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="824c1-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="824c1-152">CommonParameters</span></span>
<span data-ttu-id="824c1-153">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="824c1-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="824c1-154">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="824c1-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="824c1-155">INPUT</span><span class="sxs-lookup"><span data-stu-id="824c1-155">INPUTS</span></span>

### <span data-ttu-id="824c1-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="824c1-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="824c1-157">System.String</span><span class="sxs-lookup"><span data-stu-id="824c1-157">System.String</span></span>

## <span data-ttu-id="824c1-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="824c1-158">OUTPUTS</span></span>

### <span data-ttu-id="824c1-159">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="824c1-159">System.Boolean</span></span>

## <span data-ttu-id="824c1-160">NOTE</span><span class="sxs-lookup"><span data-stu-id="824c1-160">NOTES</span></span>

## <span data-ttu-id="824c1-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="824c1-161">RELATED LINKS</span></span>

[<span data-ttu-id="824c1-162">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="824c1-162">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="824c1-163">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="824c1-163">New-AzKeyVault</span></span>](./New-AzKeyVault.md)
