---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
ms.openlocfilehash: 17a39152c6e341773a2c3db7b701e0d37890f110
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193245"
---
# <span data-ttu-id="e8b72-101">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e8b72-101">Restore-AzKeyVaultKey</span></span>

## <span data-ttu-id="e8b72-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e8b72-102">SYNOPSIS</span></span>
<span data-ttu-id="e8b72-103">Crea una chiave in un Vault chiave da un tasto di backup.</span><span class="sxs-lookup"><span data-stu-id="e8b72-103">Creates a key in a key vault from a backed-up key.</span></span>

## <span data-ttu-id="e8b72-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8b72-104">SYNTAX</span></span>

### <span data-ttu-id="e8b72-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e8b72-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8b72-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e8b72-106">ByInputObject</span></span>
```
Restore-AzKeyVaultKey [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8b72-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e8b72-107">ByResourceId</span></span>
```
Restore-AzKeyVaultKey [-ResourceId] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8b72-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8b72-108">DESCRIPTION</span></span>
<span data-ttu-id="e8b72-109">Il cmdlet **Restore-AzKeyVaultKey** crea una chiave nell'archivio chiavi specificato.</span><span class="sxs-lookup"><span data-stu-id="e8b72-109">The **Restore-AzKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="e8b72-110">Questa chiave è una replica della chiave di backup nel file di input e ha lo stesso nome della chiave originale.</span><span class="sxs-lookup"><span data-stu-id="e8b72-110">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="e8b72-111">Se il Vault chiave ha già una chiave con lo stesso nome, questo cmdlet non riesce invece di sovrascrivere la chiave originale.</span><span class="sxs-lookup"><span data-stu-id="e8b72-111">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="e8b72-112">Se il backup contiene più versioni di una chiave, tutte le versioni verranno ripristinate.</span><span class="sxs-lookup"><span data-stu-id="e8b72-112">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="e8b72-113">Il Vault chiave in cui ripristinare la chiave può essere diverso da quello della chiave a cui è stato eseguito il backup della chiave.</span><span class="sxs-lookup"><span data-stu-id="e8b72-113">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="e8b72-114">Tuttavia, il Vault della chiave deve usare lo stesso abbonamento ed essere in un'area di Azure nella stessa geografia (ad esempio, Nord America).</span><span class="sxs-lookup"><span data-stu-id="e8b72-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="e8b72-115">Vedere il Centro protezione di Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) per il mapping delle aree di Azure alle geografie.</span><span class="sxs-lookup"><span data-stu-id="e8b72-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="e8b72-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8b72-116">EXAMPLES</span></span>

### <span data-ttu-id="e8b72-117">Esempio 1: ripristinare un tasto di backup</span><span class="sxs-lookup"><span data-stu-id="e8b72-117">Example 1: Restore a backed-up key</span></span>
```powershell
PS C:\> Restore-AzKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Vault Name     : MyKeyVault
Name           : key1
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://mykeyvault.vault.azure.net:443/keys/key1/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        :
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 4/6/2018 11:35:04 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="e8b72-118">Questo comando Ripristina una chiave, incluse tutte le relative versioni, dal file di backup denominato backup. BLOB nel caveau della chiave denominato MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="e8b72-118">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="e8b72-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e8b72-119">PARAMETERS</span></span>

### <span data-ttu-id="e8b72-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8b72-120">-DefaultProfile</span></span>
<span data-ttu-id="e8b72-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e8b72-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8b72-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="e8b72-122">-InputFile</span></span>
<span data-ttu-id="e8b72-123">Specifica il file di input che contiene il backup della chiave da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="e8b72-123">Specifies the input file that contains the backup of the key to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8b72-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8b72-124">-InputObject</span></span>
<span data-ttu-id="e8b72-125">Oggetto Vault</span><span class="sxs-lookup"><span data-stu-id="e8b72-125">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b72-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8b72-126">-ResourceId</span></span>
<span data-ttu-id="e8b72-127">ID risorsa di un Vault</span><span class="sxs-lookup"><span data-stu-id="e8b72-127">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8b72-128">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="e8b72-128">-VaultName</span></span>
<span data-ttu-id="e8b72-129">Specifica il nome del Vault chiave in cui ripristinare la chiave.</span><span class="sxs-lookup"><span data-stu-id="e8b72-129">Specifies the name of the key vault into which to restore the key.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8b72-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e8b72-130">-Confirm</span></span>
<span data-ttu-id="e8b72-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8b72-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8b72-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8b72-132">-WhatIf</span></span>
<span data-ttu-id="e8b72-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e8b72-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8b72-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e8b72-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8b72-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8b72-135">CommonParameters</span></span>
<span data-ttu-id="e8b72-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8b72-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8b72-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8b72-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8b72-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e8b72-138">INPUTS</span></span>

### <span data-ttu-id="e8b72-139">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="e8b72-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="e8b72-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e8b72-140">System.String</span></span>

## <span data-ttu-id="e8b72-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8b72-141">OUTPUTS</span></span>

### <span data-ttu-id="e8b72-142">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e8b72-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="e8b72-143">Note</span><span class="sxs-lookup"><span data-stu-id="e8b72-143">NOTES</span></span>

## <span data-ttu-id="e8b72-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8b72-144">RELATED LINKS</span></span>

[<span data-ttu-id="e8b72-145">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e8b72-145">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="e8b72-146">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e8b72-146">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="e8b72-147">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e8b72-147">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="e8b72-148">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e8b72-148">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

