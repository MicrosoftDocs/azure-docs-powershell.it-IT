---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
ms.openlocfilehash: 0c9e37433d28a16a28ca56daf4a726347b7a9533
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686317"
---
# <span data-ttu-id="62ca8-101">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="62ca8-101">Remove-AzureRmKeyVault</span></span>

## <span data-ttu-id="62ca8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="62ca8-102">SYNOPSIS</span></span>
<span data-ttu-id="62ca8-103">Elimina un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="62ca8-103">Deletes a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62ca8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62ca8-104">SYNTAX</span></span>

### <span data-ttu-id="62ca8-105">ByAvailableVault (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="62ca8-105">ByAvailableVault (Default)</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62ca8-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="62ca8-106">ByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62ca8-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="62ca8-107">InputObjectByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62ca8-108">InputObjectByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="62ca8-108">InputObjectByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62ca8-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62ca8-109">DESCRIPTION</span></span>
<span data-ttu-id="62ca8-110">Il cmdlet **Remove-AzureRmKeyVault** Elimina il Vault Key specificato.</span><span class="sxs-lookup"><span data-stu-id="62ca8-110">The **Remove-AzureRmKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="62ca8-111">Elimina inoltre tutte le chiavi e i segreti contenuti in quell'istanza.</span><span class="sxs-lookup"><span data-stu-id="62ca8-111">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="62ca8-112">Tieni presente che, anche se specificando il gruppo di risorse è facoltativo per questo cmdlet, dovresti migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="62ca8-112">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="62ca8-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62ca8-113">EXAMPLES</span></span>

### <span data-ttu-id="62ca8-114">Esempio 1: rimuovere un Vault chiave</span><span class="sxs-lookup"><span data-stu-id="62ca8-114">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="62ca8-115">Questo comando rimuove il Vault della chiave denominato Contoso03Vault dall'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="62ca8-115">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="62ca8-116">Esempio 2: rimuovere un Vault chiave da un gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="62ca8-116">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="62ca8-117">Questo comando rimuove il Vault della chiave denominato Contoso03Vault dal gruppo di risorse denominato.</span><span class="sxs-lookup"><span data-stu-id="62ca8-117">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="62ca8-118">Se non specifichi il nome del gruppo di risorse, il cmdlet cerca il Vault della chiave denominata da eliminare nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="62ca8-118">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="62ca8-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="62ca8-119">PARAMETERS</span></span>

### <span data-ttu-id="62ca8-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62ca8-120">-AsJob</span></span>
<span data-ttu-id="62ca8-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="62ca8-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="62ca8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62ca8-122">-DefaultProfile</span></span>
<span data-ttu-id="62ca8-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="62ca8-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62ca8-124">-Force</span><span class="sxs-lookup"><span data-stu-id="62ca8-124">-Force</span></span>
<span data-ttu-id="62ca8-125">Indica che il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="62ca8-125">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="62ca8-126">Per impostazione predefinita, questo cmdlet richiede di confermare che si vuole eliminare il Vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="62ca8-126">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="62ca8-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62ca8-127">-InputObject</span></span>
<span data-ttu-id="62ca8-128">Oggetto Vault chiave da eliminare.</span><span class="sxs-lookup"><span data-stu-id="62ca8-128">Key Vault object to be deleted.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectByAvailableVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62ca8-129">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="62ca8-129">-InRemovedState</span></span>
<span data-ttu-id="62ca8-130">Rimuovere definitivamente il Vault eliminato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="62ca8-130">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62ca8-131">-Posizione</span><span class="sxs-lookup"><span data-stu-id="62ca8-131">-Location</span></span>
<span data-ttu-id="62ca8-132">Posizione del Vault eliminato.</span><span class="sxs-lookup"><span data-stu-id="62ca8-132">The location of the deleted vault.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62ca8-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62ca8-133">-PassThru</span></span>
<span data-ttu-id="62ca8-134">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="62ca8-134">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="62ca8-135">Se questo parametro è specificato, restituisce vero se riuscito.</span><span class="sxs-lookup"><span data-stu-id="62ca8-135">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="62ca8-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62ca8-136">-ResourceGroupName</span></span>
<span data-ttu-id="62ca8-137">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="62ca8-137">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62ca8-138">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="62ca8-138">-VaultName</span></span>
<span data-ttu-id="62ca8-139">Specifica il nome del Vault della chiave da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="62ca8-139">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableVault, ByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62ca8-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="62ca8-140">-Confirm</span></span>
<span data-ttu-id="62ca8-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62ca8-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62ca8-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62ca8-142">-WhatIf</span></span>
<span data-ttu-id="62ca8-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62ca8-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62ca8-144">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62ca8-144">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62ca8-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62ca8-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62ca8-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62ca8-146">CommonParameters</span></span>
<span data-ttu-id="62ca8-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62ca8-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62ca8-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62ca8-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62ca8-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="62ca8-149">INPUTS</span></span>

### <span data-ttu-id="62ca8-150">Nessuno</span><span class="sxs-lookup"><span data-stu-id="62ca8-150">None</span></span>
<span data-ttu-id="62ca8-151">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="62ca8-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="62ca8-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62ca8-152">OUTPUTS</span></span>

### <span data-ttu-id="62ca8-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="62ca8-153">System.Boolean</span></span>

## <span data-ttu-id="62ca8-154">Note</span><span class="sxs-lookup"><span data-stu-id="62ca8-154">NOTES</span></span>

## <span data-ttu-id="62ca8-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62ca8-155">RELATED LINKS</span></span>

[<span data-ttu-id="62ca8-156">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="62ca8-156">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="62ca8-157">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="62ca8-157">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)
