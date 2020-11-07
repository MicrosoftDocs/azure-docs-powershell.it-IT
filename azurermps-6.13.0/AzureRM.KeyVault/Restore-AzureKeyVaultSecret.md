---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultSecret.md
ms.openlocfilehash: ea2478225c3e5b3c0a3746a44aca13745e1af963
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685709"
---
# <span data-ttu-id="b5d85-101">Restore-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b5d85-101">Restore-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="b5d85-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b5d85-102">SYNOPSIS</span></span>
<span data-ttu-id="b5d85-103">Crea un segreto in un caveau chiave da un segreto di backup.</span><span class="sxs-lookup"><span data-stu-id="b5d85-103">Creates a secret in a key vault from a backed-up secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5d85-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5d85-104">SYNTAX</span></span>

### <span data-ttu-id="b5d85-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b5d85-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultSecret [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5d85-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b5d85-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5d85-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b5d85-107">ByResourceId</span></span>
```
Restore-AzureKeyVaultSecret [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5d85-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5d85-108">DESCRIPTION</span></span>
<span data-ttu-id="b5d85-109">Il cmdlet **Restore-AzureKeyVaultSecret** crea un segreto nell'archivio chiavi specificato.</span><span class="sxs-lookup"><span data-stu-id="b5d85-109">The **Restore-AzureKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="b5d85-110">Questo segreto è una copia del segreto di backup nel file di input e ha lo stesso nome del segreto originale.</span><span class="sxs-lookup"><span data-stu-id="b5d85-110">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="b5d85-111">Se il Vault chiave ha già un segreto con lo stesso nome, questo cmdlet non riesce invece di sovrascrivere il segreto originale.</span><span class="sxs-lookup"><span data-stu-id="b5d85-111">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="b5d85-112">Se il backup contiene più versioni di un segreto, tutte le versioni verranno ripristinate.</span><span class="sxs-lookup"><span data-stu-id="b5d85-112">If the backup contains multiple versions of a secret, all versions are restored.</span></span>
<span data-ttu-id="b5d85-113">Il Vault chiave in cui ripristinare il segreto può essere diverso da quello della chiave in cui è stato eseguito il backup del segreto.</span><span class="sxs-lookup"><span data-stu-id="b5d85-113">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="b5d85-114">Tuttavia, il Vault della chiave deve usare lo stesso abbonamento ed essere in un'area di Azure nella stessa geografia (ad esempio, Nord America).</span><span class="sxs-lookup"><span data-stu-id="b5d85-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="b5d85-115">Vedere il Centro protezione di Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) per il mapping delle aree di Azure alle geografie.</span><span class="sxs-lookup"><span data-stu-id="b5d85-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="b5d85-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5d85-116">EXAMPLES</span></span>

### <span data-ttu-id="b5d85-117">Esempio 1: ripristinare un segreto di backup</span><span class="sxs-lookup"><span data-stu-id="b5d85-117">Example 1: Restore a backed-up secret</span></span>
```powershell
PS C:\> Restore-AzureKeyVaultSecret -VaultName 'contoso' -InputFile "C:\Backup.blob"

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :
```

<span data-ttu-id="b5d85-118">Questo comando ripristina un segreto, incluse tutte le sue versioni, dal file di backup denominato backup. BLOB nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="b5d85-118">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named contoso.</span></span>

## <span data-ttu-id="b5d85-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b5d85-119">PARAMETERS</span></span>

### <span data-ttu-id="b5d85-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5d85-120">-DefaultProfile</span></span>
<span data-ttu-id="b5d85-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b5d85-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5d85-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="b5d85-122">-InputFile</span></span>
<span data-ttu-id="b5d85-123">Specifica il file di input che contiene il backup del segreto da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="b5d85-123">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="b5d85-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5d85-124">-InputObject</span></span>
<span data-ttu-id="b5d85-125">Oggetto Vault</span><span class="sxs-lookup"><span data-stu-id="b5d85-125">KeyVault object</span></span>

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

### <span data-ttu-id="b5d85-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5d85-126">-ResourceId</span></span>
<span data-ttu-id="b5d85-127">ID risorsa di un Vault</span><span class="sxs-lookup"><span data-stu-id="b5d85-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="b5d85-128">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="b5d85-128">-VaultName</span></span>
<span data-ttu-id="b5d85-129">Specifica il nome del Vault chiave in cui ripristinare il segreto.</span><span class="sxs-lookup"><span data-stu-id="b5d85-129">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="b5d85-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b5d85-130">-Confirm</span></span>
<span data-ttu-id="b5d85-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5d85-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5d85-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5d85-132">-WhatIf</span></span>
<span data-ttu-id="b5d85-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5d85-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5d85-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5d85-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5d85-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5d85-135">CommonParameters</span></span>
<span data-ttu-id="b5d85-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5d85-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5d85-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5d85-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5d85-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b5d85-138">INPUTS</span></span>

### <span data-ttu-id="b5d85-139">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="b5d85-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="b5d85-140">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b5d85-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="b5d85-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b5d85-141">System.String</span></span>

## <span data-ttu-id="b5d85-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5d85-142">OUTPUTS</span></span>

### <span data-ttu-id="b5d85-143">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b5d85-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="b5d85-144">Note</span><span class="sxs-lookup"><span data-stu-id="b5d85-144">NOTES</span></span>

## <span data-ttu-id="b5d85-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5d85-145">RELATED LINKS</span></span>

[<span data-ttu-id="b5d85-146">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b5d85-146">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="b5d85-147">Backup-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b5d85-147">Backup-AzureKeyVaultSecret</span></span>](./Backup-AzureKeyVaultSecret.md)

[<span data-ttu-id="b5d85-148">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b5d85-148">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="b5d85-149">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b5d85-149">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

