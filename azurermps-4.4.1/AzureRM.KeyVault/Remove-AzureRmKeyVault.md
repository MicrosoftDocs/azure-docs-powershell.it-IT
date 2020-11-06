---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://go.microsoft.com/fwlink/?LinkId=690162
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVault.md
ms.openlocfilehash: 2a30a190fbf257142e1c1e4fb4329fd6c4f41e3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520510"
---
# <span data-ttu-id="b49b2-101">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="b49b2-101">Remove-AzureRmKeyVault</span></span>

## <span data-ttu-id="b49b2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b49b2-102">SYNOPSIS</span></span>
<span data-ttu-id="b49b2-103">Elimina un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="b49b2-103">Deletes a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b49b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b49b2-104">SYNTAX</span></span>

### <span data-ttu-id="b49b2-105">ByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="b49b2-105">ByAvailableVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b49b2-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="b49b2-106">ByDeletedVault</span></span>
```
Remove-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-Force] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b49b2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b49b2-107">DESCRIPTION</span></span>
<span data-ttu-id="b49b2-108">Il cmdlet **Remove-AzureRmKeyVault** Elimina il Vault Key specificato.</span><span class="sxs-lookup"><span data-stu-id="b49b2-108">The **Remove-AzureRmKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="b49b2-109">Elimina inoltre tutte le chiavi e i segreti contenuti in quell'istanza.</span><span class="sxs-lookup"><span data-stu-id="b49b2-109">It also deletes all keys and secrets contained in that instance.</span></span>

<span data-ttu-id="b49b2-110">Tieni presente che, anche se specificando il gruppo di risorse è facoltativo per questo cmdlet, dovresti migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="b49b2-110">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="b49b2-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b49b2-111">EXAMPLES</span></span>

### <span data-ttu-id="b49b2-112">Esempio 1: rimuovere un Vault chiave</span><span class="sxs-lookup"><span data-stu-id="b49b2-112">Example 1: Remove a key vault</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault"
```

<span data-ttu-id="b49b2-113">Questo comando rimuove il Vault della chiave denominato Contoso03Vault dall'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="b49b2-113">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="b49b2-114">Esempio 2: rimuovere un Vault chiave da un gruppo di risorse specificato</span><span class="sxs-lookup"><span data-stu-id="b49b2-114">Example 2: Remove a key vault from a specified resource group</span></span>
```
PS C:\>Remove-AzureRmKeyVault -VaultName "Contoso03Vault" -ResourceGroupName "Group14"
```

<span data-ttu-id="b49b2-115">Questo comando rimuove il Vault della chiave denominato Contoso03Vault dal gruppo di risorse denominato.</span><span class="sxs-lookup"><span data-stu-id="b49b2-115">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="b49b2-116">Se non specifichi il nome del gruppo di risorse, il cmdlet cerca il Vault della chiave denominata da eliminare nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="b49b2-116">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

## <span data-ttu-id="b49b2-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b49b2-117">PARAMETERS</span></span>

### <span data-ttu-id="b49b2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b49b2-118">-Force</span></span>
<span data-ttu-id="b49b2-119">Indica che il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="b49b2-119">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="b49b2-120">Per impostazione predefinita, questo cmdlet richiede di confermare che si vuole eliminare il Vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="b49b2-120">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="b49b2-121">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="b49b2-121">-InRemovedState</span></span>
<span data-ttu-id="b49b2-122">Rimuovere definitivamente il Vault eliminato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="b49b2-122">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b49b2-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b49b2-123">-Location</span></span>
<span data-ttu-id="b49b2-124">Posizione del Vault eliminato.</span><span class="sxs-lookup"><span data-stu-id="b49b2-124">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b49b2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b49b2-125">-ResourceGroupName</span></span>
<span data-ttu-id="b49b2-126">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b49b2-126">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b49b2-127">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="b49b2-127">-VaultName</span></span>
<span data-ttu-id="b49b2-128">Specifica il nome del Vault della chiave da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="b49b2-128">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b49b2-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b49b2-129">-Confirm</span></span>
<span data-ttu-id="b49b2-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b49b2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b49b2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b49b2-131">-WhatIf</span></span>
<span data-ttu-id="b49b2-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b49b2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b49b2-133">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b49b2-133">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b49b2-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b49b2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b49b2-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b49b2-135">-DefaultProfile</span></span>
<span data-ttu-id="b49b2-136">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b49b2-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b49b2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b49b2-137">CommonParameters</span></span>
<span data-ttu-id="b49b2-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b49b2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b49b2-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b49b2-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b49b2-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b49b2-140">INPUTS</span></span>

## <span data-ttu-id="b49b2-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b49b2-141">OUTPUTS</span></span>

## <span data-ttu-id="b49b2-142">Note</span><span class="sxs-lookup"><span data-stu-id="b49b2-142">NOTES</span></span>

## <span data-ttu-id="b49b2-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b49b2-143">RELATED LINKS</span></span>

[<span data-ttu-id="b49b2-144">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="b49b2-144">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="b49b2-145">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="b49b2-145">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)
