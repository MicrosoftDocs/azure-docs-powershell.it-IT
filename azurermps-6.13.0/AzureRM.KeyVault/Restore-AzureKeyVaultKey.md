---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
ms.openlocfilehash: 70c56aaee4bf6547ad932965a190d3ecb2d93f6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510967"
---
# <span data-ttu-id="ed721-101">Restore-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ed721-101">Restore-AzureKeyVaultKey</span></span>

## <span data-ttu-id="ed721-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ed721-102">SYNOPSIS</span></span>
<span data-ttu-id="ed721-103">Crea una chiave in un Vault chiave da un tasto di backup.</span><span class="sxs-lookup"><span data-stu-id="ed721-103">Creates a key in a key vault from a backed-up key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed721-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed721-104">SYNTAX</span></span>

### <span data-ttu-id="ed721-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ed721-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed721-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ed721-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed721-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ed721-107">ByResourceId</span></span>
```
Restore-AzureKeyVaultKey [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed721-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed721-108">DESCRIPTION</span></span>
<span data-ttu-id="ed721-109">Il cmdlet **Restore-AzureKeyVaultKey** crea una chiave nell'archivio chiavi specificato.</span><span class="sxs-lookup"><span data-stu-id="ed721-109">The **Restore-AzureKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="ed721-110">Questa chiave è una replica della chiave di backup nel file di input e ha lo stesso nome della chiave originale.</span><span class="sxs-lookup"><span data-stu-id="ed721-110">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="ed721-111">Se il Vault chiave ha già una chiave con lo stesso nome, questo cmdlet non riesce invece di sovrascrivere la chiave originale.</span><span class="sxs-lookup"><span data-stu-id="ed721-111">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="ed721-112">Se il backup contiene più versioni di una chiave, tutte le versioni verranno ripristinate.</span><span class="sxs-lookup"><span data-stu-id="ed721-112">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="ed721-113">Il Vault chiave in cui ripristinare la chiave può essere diverso da quello della chiave a cui è stato eseguito il backup della chiave.</span><span class="sxs-lookup"><span data-stu-id="ed721-113">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="ed721-114">Tuttavia, il Vault della chiave deve usare lo stesso abbonamento ed essere in un'area di Azure nella stessa geografia (ad esempio, Nord America).</span><span class="sxs-lookup"><span data-stu-id="ed721-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="ed721-115">Vedere il Centro protezione di Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) per il mapping delle aree di Azure alle geografie.</span><span class="sxs-lookup"><span data-stu-id="ed721-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="ed721-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed721-116">EXAMPLES</span></span>

### <span data-ttu-id="ed721-117">Esempio 1: ripristinare un tasto di backup</span><span class="sxs-lookup"><span data-stu-id="ed721-117">Example 1: Restore a backed-up key</span></span>
```powershell
PS C:\> Restore-AzureKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

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

<span data-ttu-id="ed721-118">Questo comando Ripristina una chiave, incluse tutte le relative versioni, dal file di backup denominato backup. BLOB nel caveau della chiave denominato MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="ed721-118">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="ed721-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ed721-119">PARAMETERS</span></span>

### <span data-ttu-id="ed721-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed721-120">-DefaultProfile</span></span>
<span data-ttu-id="ed721-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ed721-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed721-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="ed721-122">-InputFile</span></span>
<span data-ttu-id="ed721-123">Specifica il file di input che contiene il backup della chiave da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="ed721-123">Specifies the input file that contains the backup of the key to restore.</span></span>

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

### <span data-ttu-id="ed721-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed721-124">-InputObject</span></span>
<span data-ttu-id="ed721-125">Oggetto Vault</span><span class="sxs-lookup"><span data-stu-id="ed721-125">KeyVault object</span></span>

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

### <span data-ttu-id="ed721-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed721-126">-ResourceId</span></span>
<span data-ttu-id="ed721-127">ID risorsa di un Vault</span><span class="sxs-lookup"><span data-stu-id="ed721-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="ed721-128">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="ed721-128">-VaultName</span></span>
<span data-ttu-id="ed721-129">Specifica il nome del Vault chiave in cui ripristinare la chiave.</span><span class="sxs-lookup"><span data-stu-id="ed721-129">Specifies the name of the key vault into which to restore the key.</span></span>

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

### <span data-ttu-id="ed721-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ed721-130">-Confirm</span></span>
<span data-ttu-id="ed721-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed721-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed721-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed721-132">-WhatIf</span></span>
<span data-ttu-id="ed721-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed721-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed721-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed721-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed721-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed721-135">CommonParameters</span></span>
<span data-ttu-id="ed721-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed721-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed721-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed721-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed721-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ed721-138">INPUTS</span></span>

### <span data-ttu-id="ed721-139">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="ed721-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="ed721-140">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ed721-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="ed721-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ed721-141">System.String</span></span>

## <span data-ttu-id="ed721-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed721-142">OUTPUTS</span></span>

### <span data-ttu-id="ed721-143">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ed721-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="ed721-144">Note</span><span class="sxs-lookup"><span data-stu-id="ed721-144">NOTES</span></span>

## <span data-ttu-id="ed721-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed721-145">RELATED LINKS</span></span>

[<span data-ttu-id="ed721-146">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ed721-146">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="ed721-147">Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ed721-147">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="ed721-148">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ed721-148">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="ed721-149">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ed721-149">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

