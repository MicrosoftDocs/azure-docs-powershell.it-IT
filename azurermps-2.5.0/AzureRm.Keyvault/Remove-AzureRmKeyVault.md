---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvault
schema: 2.0.0
ms.openlocfilehash: 2365a58093be3193c7ac285d6dd38fbaf769ccd4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865789"
---
# <span data-ttu-id="609c4-101">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="609c4-101">Remove-AzureRmKeyVault</span></span>

## <span data-ttu-id="609c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="609c4-102">SYNOPSIS</span></span>
<span data-ttu-id="609c4-103">Elimina un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="609c4-103">Deletes a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="609c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="609c4-104">SYNTAX</span></span>

### <span data-ttu-id="609c4-105">ByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="609c4-105">ByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="609c4-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="609c4-106">ByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-Force] [-InRemovedState] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="609c4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="609c4-107">DESCRIPTION</span></span>
<span data-ttu-id="609c4-108">Il cmdlet **Remove-AzureRmKeyVault** Elimina il Vault Key specificato.</span><span class="sxs-lookup"><span data-stu-id="609c4-108">The **Remove-AzureRmKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="609c4-109">Elimina inoltre tutte le chiavi e i segreti contenuti in quell'istanza.</span><span class="sxs-lookup"><span data-stu-id="609c4-109">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="609c4-110">Tieni presente che, anche se specificando il gruppo di risorse è facoltativo per questo cmdlet, dovresti migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="609c4-110">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="609c4-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="609c4-111">EXAMPLES</span></span>

### <span data-ttu-id="609c4-112">Esempio 1: rimuovere un Vault chiave</span><span class="sxs-lookup"><span data-stu-id="609c4-112">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="609c4-113">Questo comando rimuove il Vault della chiave denominato Contoso03Vault dall'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="609c4-113">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="609c4-114">Esempio 2: rimuovere un Vault chiave da un gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="609c4-114">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="609c4-115">Questo comando rimuove il Vault della chiave denominato Contoso03Vault dal gruppo di risorse denominato.</span><span class="sxs-lookup"><span data-stu-id="609c4-115">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="609c4-116">Se non specifichi il nome del gruppo di risorse, il cmdlet cerca il Vault della chiave denominata da eliminare nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="609c4-116">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="609c4-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="609c4-117">PARAMETERS</span></span>

### <span data-ttu-id="609c4-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="609c4-118">-AsJob</span></span>
<span data-ttu-id="609c4-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="609c4-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="609c4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="609c4-120">-DefaultProfile</span></span>
<span data-ttu-id="609c4-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="609c4-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="609c4-122">-Force</span><span class="sxs-lookup"><span data-stu-id="609c4-122">-Force</span></span>
<span data-ttu-id="609c4-123">Indica che il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="609c4-123">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="609c4-124">Per impostazione predefinita, questo cmdlet richiede di confermare che si vuole eliminare il Vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="609c4-124">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="609c4-125">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="609c4-125">-InRemovedState</span></span>
<span data-ttu-id="609c4-126">Rimuovere definitivamente il Vault eliminato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="609c4-126">Remove the previously deleted vault permanently.</span></span>

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

### <span data-ttu-id="609c4-127">-Posizione</span><span class="sxs-lookup"><span data-stu-id="609c4-127">-Location</span></span>
<span data-ttu-id="609c4-128">Posizione del Vault eliminato.</span><span class="sxs-lookup"><span data-stu-id="609c4-128">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="609c4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="609c4-129">-ResourceGroupName</span></span>
<span data-ttu-id="609c4-130">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="609c4-130">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="609c4-131">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="609c4-131">-VaultName</span></span>
<span data-ttu-id="609c4-132">Specifica il nome del Vault della chiave da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="609c4-132">Specifies the name of the key vault to remove.</span></span>

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

### <span data-ttu-id="609c4-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="609c4-133">-Confirm</span></span>
<span data-ttu-id="609c4-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="609c4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="609c4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="609c4-135">-WhatIf</span></span>
<span data-ttu-id="609c4-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="609c4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="609c4-137">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="609c4-137">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="609c4-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="609c4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="609c4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="609c4-139">CommonParameters</span></span>
<span data-ttu-id="609c4-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="609c4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="609c4-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="609c4-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="609c4-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="609c4-142">INPUTS</span></span>

## <span data-ttu-id="609c4-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="609c4-143">OUTPUTS</span></span>

## <span data-ttu-id="609c4-144">Note</span><span class="sxs-lookup"><span data-stu-id="609c4-144">NOTES</span></span>

## <span data-ttu-id="609c4-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="609c4-145">RELATED LINKS</span></span>

[<span data-ttu-id="609c4-146">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="609c4-146">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="609c4-147">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="609c4-147">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)
