---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
ms.openlocfilehash: 32060f2d9d468669f963f653f335729ca6c25761
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022838"
---
# <span data-ttu-id="90ff8-101">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="90ff8-101">Remove-AzKeyVault</span></span>

## <span data-ttu-id="90ff8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="90ff8-102">SYNOPSIS</span></span>
<span data-ttu-id="90ff8-103">Elimina un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="90ff8-103">Deletes a key vault.</span></span>

## <span data-ttu-id="90ff8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="90ff8-104">SYNTAX</span></span>

### <span data-ttu-id="90ff8-105">ByAvailableVault (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="90ff8-105">ByAvailableVault (Default)</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90ff8-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="90ff8-106">ByDeletedVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90ff8-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="90ff8-107">InputObjectByAvailableVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90ff8-108">InputObjectByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="90ff8-108">InputObjectByDeletedVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90ff8-109">ResourceIdByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="90ff8-109">ResourceIdByAvailableVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [[-Location] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90ff8-110">ResourceIdByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="90ff8-110">ResourceIdByDeletedVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90ff8-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="90ff8-111">DESCRIPTION</span></span>
<span data-ttu-id="90ff8-112">Il cmdlet **Remove-AzKeyVault** Elimina il Vault Key specificato.</span><span class="sxs-lookup"><span data-stu-id="90ff8-112">The **Remove-AzKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="90ff8-113">Elimina inoltre tutte le chiavi e i segreti contenuti in quell'istanza.</span><span class="sxs-lookup"><span data-stu-id="90ff8-113">It also deletes all keys and secrets contained in that instance.</span></span>
<span data-ttu-id="90ff8-114">Tieni presente che, anche se specificando il gruppo di risorse è facoltativo per questo cmdlet, dovresti migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="90ff8-114">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="90ff8-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="90ff8-115">EXAMPLES</span></span>

### <span data-ttu-id="90ff8-116">Esempio 1: rimuovere un Vault chiave</span><span class="sxs-lookup"><span data-stu-id="90ff8-116">Example 1: Remove a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVault -VaultName "Contoso03Vault" -PassThru

True
```

<span data-ttu-id="90ff8-117">Questo comando rimuove il Vault della chiave denominato Contoso03Vault dall'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="90ff8-117">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="90ff8-118">Esempio 2: rimuovere un Vault chiave da un gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="90ff8-118">Example 2: Remove a key vault from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVault -Name "Contoso03Vault" -ResourceGroupName "Group14" -PassThru

True
```

<span data-ttu-id="90ff8-119">Questo comando rimuove il Vault della chiave denominato Contoso03Vault dal gruppo di risorse denominato.</span><span class="sxs-lookup"><span data-stu-id="90ff8-119">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="90ff8-120">Se non specifichi il nome del gruppo di risorse, il cmdlet cerca il Vault della chiave denominata da eliminare nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="90ff8-120">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="90ff8-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="90ff8-121">PARAMETERS</span></span>

### <span data-ttu-id="90ff8-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90ff8-122">-AsJob</span></span>
<span data-ttu-id="90ff8-123">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="90ff8-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="90ff8-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90ff8-124">-DefaultProfile</span></span>
<span data-ttu-id="90ff8-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="90ff8-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90ff8-126">-Force</span><span class="sxs-lookup"><span data-stu-id="90ff8-126">-Force</span></span>
<span data-ttu-id="90ff8-127">Indica che il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="90ff8-127">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="90ff8-128">Per impostazione predefinita, questo cmdlet richiede di confermare che si vuole eliminare il Vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="90ff8-128">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="90ff8-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90ff8-129">-InputObject</span></span>
<span data-ttu-id="90ff8-130">Oggetto Vault chiave da eliminare.</span><span class="sxs-lookup"><span data-stu-id="90ff8-130">Key Vault object to be deleted.</span></span>

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

### <span data-ttu-id="90ff8-131">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="90ff8-131">-InRemovedState</span></span>
<span data-ttu-id="90ff8-132">Rimuovere definitivamente il Vault eliminato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="90ff8-132">Remove the previously deleted vault permanently.</span></span>

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

### <span data-ttu-id="90ff8-133">-Posizione</span><span class="sxs-lookup"><span data-stu-id="90ff8-133">-Location</span></span>
<span data-ttu-id="90ff8-134">Posizione del Vault eliminato.</span><span class="sxs-lookup"><span data-stu-id="90ff8-134">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="90ff8-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90ff8-135">-PassThru</span></span>
<span data-ttu-id="90ff8-136">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="90ff8-136">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="90ff8-137">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="90ff8-137">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="90ff8-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90ff8-138">-ResourceGroupName</span></span>
<span data-ttu-id="90ff8-139">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="90ff8-139">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="90ff8-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90ff8-140">-ResourceId</span></span>
<span data-ttu-id="90ff8-141">ID risorsa di un Vault.</span><span class="sxs-lookup"><span data-stu-id="90ff8-141">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="90ff8-142">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="90ff8-142">-VaultName</span></span>
<span data-ttu-id="90ff8-143">Specifica il nome del Vault della chiave da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="90ff8-143">Specifies the name of the key vault to remove.</span></span>

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

### <span data-ttu-id="90ff8-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="90ff8-144">-Confirm</span></span>
<span data-ttu-id="90ff8-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90ff8-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90ff8-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90ff8-146">-WhatIf</span></span>
<span data-ttu-id="90ff8-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="90ff8-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90ff8-148">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="90ff8-148">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90ff8-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="90ff8-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90ff8-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90ff8-150">CommonParameters</span></span>
<span data-ttu-id="90ff8-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90ff8-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90ff8-152">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90ff8-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90ff8-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="90ff8-153">INPUTS</span></span>

### <span data-ttu-id="90ff8-154">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="90ff8-154">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="90ff8-155">System. String</span><span class="sxs-lookup"><span data-stu-id="90ff8-155">System.String</span></span>

## <span data-ttu-id="90ff8-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="90ff8-156">OUTPUTS</span></span>

### <span data-ttu-id="90ff8-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="90ff8-157">System.Boolean</span></span>

## <span data-ttu-id="90ff8-158">Note</span><span class="sxs-lookup"><span data-stu-id="90ff8-158">NOTES</span></span>

## <span data-ttu-id="90ff8-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="90ff8-159">RELATED LINKS</span></span>

[<span data-ttu-id="90ff8-160">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="90ff8-160">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="90ff8-161">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="90ff8-161">New-AzKeyVault</span></span>](./New-AzKeyVault.md)
