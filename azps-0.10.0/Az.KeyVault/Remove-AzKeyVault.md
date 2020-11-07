---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-Azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
ms.openlocfilehash: 20187e2d7a844b472217fd30acbac9805e85ad40
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863033"
---
# <span data-ttu-id="7a4fe-101">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="7a4fe-101">Remove-AzKeyVault</span></span>

## <span data-ttu-id="7a4fe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7a4fe-102">SYNOPSIS</span></span>
<span data-ttu-id="7a4fe-103">Elimina un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="7a4fe-103">Deletes a key vault.</span></span>

## <span data-ttu-id="7a4fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a4fe-104">SYNTAX</span></span>

### <span data-ttu-id="7a4fe-105">ByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="7a4fe-105">ByAvailableVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a4fe-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="7a4fe-106">ByDeletedVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [-Location] <String> [-Force] [-InRemovedState] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a4fe-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a4fe-107">DESCRIPTION</span></span>
<span data-ttu-id="7a4fe-108">Il cmdlet **Remove-AzKeyVault** Elimina il Vault Key specificato.</span><span class="sxs-lookup"><span data-stu-id="7a4fe-108">The **Remove-AzKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="7a4fe-109">Elimina inoltre tutte le chiavi e i segreti contenuti in quell'istanza.</span><span class="sxs-lookup"><span data-stu-id="7a4fe-109">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="7a4fe-110">Tieni presente che, anche se specificando il gruppo di risorse è facoltativo per questo cmdlet, dovresti migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="7a4fe-110">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="7a4fe-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a4fe-111">EXAMPLES</span></span>

### <span data-ttu-id="7a4fe-112">Esempio 1: rimuovere un Vault chiave</span><span class="sxs-lookup"><span data-stu-id="7a4fe-112">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="7a4fe-113">Questo comando rimuove il Vault della chiave denominato Contoso03Vault dall'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="7a4fe-113">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="7a4fe-114">Esempio 2: rimuovere un Vault chiave da un gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="7a4fe-114">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="7a4fe-115">Questo comando rimuove il Vault della chiave denominato Contoso03Vault dal gruppo di risorse denominato.</span><span class="sxs-lookup"><span data-stu-id="7a4fe-115">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="7a4fe-116">Se non specifichi il nome del gruppo di risorse, il cmdlet cerca il Vault della chiave denominata da eliminare nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="7a4fe-116">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="7a4fe-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7a4fe-117">PARAMETERS</span></span>

### <span data-ttu-id="7a4fe-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a4fe-118">-AsJob</span></span>
<span data-ttu-id="7a4fe-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7a4fe-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a4fe-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a4fe-120">-DefaultProfile</span></span>
<span data-ttu-id="7a4fe-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7a4fe-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a4fe-122">-Force</span><span class="sxs-lookup"><span data-stu-id="7a4fe-122">-Force</span></span>
<span data-ttu-id="7a4fe-123">Indica che il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="7a4fe-123">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="7a4fe-124">Per impostazione predefinita, questo cmdlet richiede di confermare che si vuole eliminare il Vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="7a4fe-124">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="7a4fe-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="7a4fe-125">-InRemovedState</span></span>
<span data-ttu-id="7a4fe-126">Rimuovere definitivamente il Vault eliminato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="7a4fe-126">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a4fe-127">-Posizione</span><span class="sxs-lookup"><span data-stu-id="7a4fe-127">-Location</span></span>
<span data-ttu-id="7a4fe-128">Posizione del Vault eliminato.</span><span class="sxs-lookup"><span data-stu-id="7a4fe-128">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="7a4fe-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a4fe-129">-ResourceGroupName</span></span>
<span data-ttu-id="7a4fe-130">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7a4fe-130">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7a4fe-131">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="7a4fe-131">-VaultName</span></span>
<span data-ttu-id="7a4fe-132">Specifica il nome del Vault della chiave da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="7a4fe-132">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a4fe-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7a4fe-133">-Confirm</span></span>
<span data-ttu-id="7a4fe-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a4fe-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a4fe-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a4fe-135">-WhatIf</span></span>
<span data-ttu-id="7a4fe-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a4fe-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a4fe-137">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a4fe-137">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a4fe-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a4fe-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a4fe-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a4fe-139">CommonParameters</span></span>
<span data-ttu-id="7a4fe-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a4fe-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a4fe-141">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a4fe-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a4fe-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7a4fe-142">INPUTS</span></span>

### <span data-ttu-id="7a4fe-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7a4fe-143">None</span></span>
<span data-ttu-id="7a4fe-144">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="7a4fe-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7a4fe-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a4fe-145">OUTPUTS</span></span>

## <span data-ttu-id="7a4fe-146">Note</span><span class="sxs-lookup"><span data-stu-id="7a4fe-146">NOTES</span></span>

## <span data-ttu-id="7a4fe-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a4fe-147">RELATED LINKS</span></span>

[<span data-ttu-id="7a4fe-148">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="7a4fe-148">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="7a4fe-149">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="7a4fe-149">New-AzKeyVault</span></span>](./New-AzKeyVault.md)
