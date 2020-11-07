---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
ms.openlocfilehash: 8332f4a5b14668a767ddf77e974a25a14ac884ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674138"
---
# <span data-ttu-id="6d7df-101">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="6d7df-101">Remove-AzKeyVault</span></span>

## <span data-ttu-id="6d7df-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6d7df-102">SYNOPSIS</span></span>
<span data-ttu-id="6d7df-103">Elimina un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="6d7df-103">Deletes a key vault.</span></span>

## <span data-ttu-id="6d7df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6d7df-104">SYNTAX</span></span>

### <span data-ttu-id="6d7df-105">ByAvailableVault (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6d7df-105">ByAvailableVault (Default)</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d7df-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="6d7df-106">ByDeletedVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d7df-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="6d7df-107">InputObjectByAvailableVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d7df-108">InputObjectByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="6d7df-108">InputObjectByDeletedVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d7df-109">ResourceIdByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="6d7df-109">ResourceIdByAvailableVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [[-Location] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d7df-110">ResourceIdByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="6d7df-110">ResourceIdByDeletedVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d7df-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d7df-111">DESCRIPTION</span></span>
<span data-ttu-id="6d7df-112">Il cmdlet **Remove-AzKeyVault** Elimina il Vault Key specificato.</span><span class="sxs-lookup"><span data-stu-id="6d7df-112">The **Remove-AzKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="6d7df-113">Elimina inoltre tutte le chiavi e i segreti contenuti in quell'istanza.</span><span class="sxs-lookup"><span data-stu-id="6d7df-113">It also deletes all keys and secrets contained in that instance.</span></span>
<span data-ttu-id="6d7df-114">Tieni presente che, anche se specificando il gruppo di risorse è facoltativo per questo cmdlet, dovresti migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="6d7df-114">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="6d7df-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6d7df-115">EXAMPLES</span></span>

### <span data-ttu-id="6d7df-116">Esempio 1: rimuovere un Vault chiave</span><span class="sxs-lookup"><span data-stu-id="6d7df-116">Example 1: Remove a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVault -VaultName "Contoso03Vault" -PassThru

True
```

<span data-ttu-id="6d7df-117">Questo comando rimuove il Vault della chiave denominato Contoso03Vault dall'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="6d7df-117">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="6d7df-118">Esempio 2: rimuovere un Vault chiave da un gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="6d7df-118">Example 2: Remove a key vault from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14" -PassThru

True
```

<span data-ttu-id="6d7df-119">Questo comando rimuove il Vault della chiave denominato Contoso03Vault dal gruppo di risorse denominato.</span><span class="sxs-lookup"><span data-stu-id="6d7df-119">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="6d7df-120">Se non specifichi il nome del gruppo di risorse, il cmdlet cerca il Vault della chiave denominata da eliminare nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="6d7df-120">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="6d7df-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6d7df-121">PARAMETERS</span></span>

### <span data-ttu-id="6d7df-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d7df-122">-AsJob</span></span>
<span data-ttu-id="6d7df-123">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6d7df-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d7df-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d7df-124">-DefaultProfile</span></span>
<span data-ttu-id="6d7df-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6d7df-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d7df-126">-Force</span><span class="sxs-lookup"><span data-stu-id="6d7df-126">-Force</span></span>
<span data-ttu-id="6d7df-127">Indica che il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="6d7df-127">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="6d7df-128">Per impostazione predefinita, questo cmdlet richiede di confermare che si vuole eliminare il Vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="6d7df-128">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="6d7df-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d7df-129">-InputObject</span></span>
<span data-ttu-id="6d7df-130">Oggetto Vault chiave da eliminare.</span><span class="sxs-lookup"><span data-stu-id="6d7df-130">Key Vault object to be deleted.</span></span>

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

### <span data-ttu-id="6d7df-131">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="6d7df-131">-InRemovedState</span></span>
<span data-ttu-id="6d7df-132">Rimuovere definitivamente il Vault eliminato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="6d7df-132">Remove the previously deleted vault permanently.</span></span>

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

### <span data-ttu-id="6d7df-133">-Posizione</span><span class="sxs-lookup"><span data-stu-id="6d7df-133">-Location</span></span>
<span data-ttu-id="6d7df-134">Posizione del Vault eliminato.</span><span class="sxs-lookup"><span data-stu-id="6d7df-134">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="6d7df-135">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d7df-135">-PassThru</span></span>
<span data-ttu-id="6d7df-136">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="6d7df-136">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="6d7df-137">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="6d7df-137">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="6d7df-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d7df-138">-ResourceGroupName</span></span>
<span data-ttu-id="6d7df-139">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6d7df-139">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6d7df-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d7df-140">-ResourceId</span></span>
<span data-ttu-id="6d7df-141">ID risorsa di un Vault.</span><span class="sxs-lookup"><span data-stu-id="6d7df-141">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="6d7df-142">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="6d7df-142">-VaultName</span></span>
<span data-ttu-id="6d7df-143">Specifica il nome del Vault della chiave da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6d7df-143">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault, ByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d7df-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6d7df-144">-Confirm</span></span>
<span data-ttu-id="6d7df-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d7df-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d7df-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d7df-146">-WhatIf</span></span>
<span data-ttu-id="6d7df-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d7df-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d7df-148">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d7df-148">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d7df-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d7df-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d7df-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d7df-150">CommonParameters</span></span>
<span data-ttu-id="6d7df-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d7df-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d7df-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d7df-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d7df-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6d7df-153">INPUTS</span></span>

### <span data-ttu-id="6d7df-154">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="6d7df-154">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="6d7df-155">System. String</span><span class="sxs-lookup"><span data-stu-id="6d7df-155">System.String</span></span>

## <span data-ttu-id="6d7df-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6d7df-156">OUTPUTS</span></span>

### <span data-ttu-id="6d7df-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6d7df-157">System.Boolean</span></span>

## <span data-ttu-id="6d7df-158">Note</span><span class="sxs-lookup"><span data-stu-id="6d7df-158">NOTES</span></span>

## <span data-ttu-id="6d7df-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6d7df-159">RELATED LINKS</span></span>

[<span data-ttu-id="6d7df-160">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="6d7df-160">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="6d7df-161">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="6d7df-161">New-AzKeyVault</span></span>](./New-AzKeyVault.md)
