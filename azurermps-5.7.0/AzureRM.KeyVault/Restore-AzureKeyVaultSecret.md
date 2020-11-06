---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultSecret.md
ms.openlocfilehash: 1ba12a18c88004dcc1c6761d71fdc1983a5ba0c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518091"
---
# <span data-ttu-id="58f0e-101">Restore-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="58f0e-101">Restore-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="58f0e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="58f0e-102">SYNOPSIS</span></span>
<span data-ttu-id="58f0e-103">Crea un segreto in un caveau chiave da un segreto di backup.</span><span class="sxs-lookup"><span data-stu-id="58f0e-103">Creates a secret in a key vault from a backed-up secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58f0e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58f0e-104">SYNTAX</span></span>

### <span data-ttu-id="58f0e-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="58f0e-105">ByVaultName (Default)</span></span>
```
Restore-AzureKeyVaultSecret [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58f0e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="58f0e-106">ByInputObject</span></span>
```
Restore-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58f0e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58f0e-107">DESCRIPTION</span></span>
<span data-ttu-id="58f0e-108">Il cmdlet **Restore-AzureKeyVaultSecret** crea un segreto nell'archivio chiavi specificato.</span><span class="sxs-lookup"><span data-stu-id="58f0e-108">The **Restore-AzureKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="58f0e-109">Questo segreto è una copia del segreto di backup nel file di input e ha lo stesso nome del segreto originale.</span><span class="sxs-lookup"><span data-stu-id="58f0e-109">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="58f0e-110">Se il Vault chiave ha già un segreto con lo stesso nome, questo cmdlet non riesce invece di sovrascrivere il segreto originale.</span><span class="sxs-lookup"><span data-stu-id="58f0e-110">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="58f0e-111">Se il backup contiene più versioni di un segreto, tutte le versioni verranno ripristinate.</span><span class="sxs-lookup"><span data-stu-id="58f0e-111">If the backup contains multiple versions of a secret, all versions are restored.</span></span>

<span data-ttu-id="58f0e-112">Il Vault chiave in cui ripristinare il segreto può essere diverso da quello della chiave in cui è stato eseguito il backup del segreto.</span><span class="sxs-lookup"><span data-stu-id="58f0e-112">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="58f0e-113">Tuttavia, il Vault della chiave deve usare lo stesso abbonamento ed essere in un'area di Azure nella stessa geografia (ad esempio, Nord America).</span><span class="sxs-lookup"><span data-stu-id="58f0e-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="58f0e-114">Vedere il Centro protezione di Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) per il mapping delle aree di Azure alle geografie.</span><span class="sxs-lookup"><span data-stu-id="58f0e-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="58f0e-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58f0e-115">EXAMPLES</span></span>

### <span data-ttu-id="58f0e-116">Esempio 1: ripristinare un segreto di backup</span><span class="sxs-lookup"><span data-stu-id="58f0e-116">Example 1: Restore a backed-up secret</span></span>
```
PS C:\>Restore-AzureKeyVaultSecret -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="58f0e-117">Questo comando ripristina un segreto, incluse tutte le sue versioni, dal file di backup denominato backup. BLOB nel Vault Key denominato MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="58f0e-117">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="58f0e-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="58f0e-118">PARAMETERS</span></span>

### <span data-ttu-id="58f0e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58f0e-119">-DefaultProfile</span></span>
<span data-ttu-id="58f0e-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="58f0e-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58f0e-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="58f0e-121">-InputFile</span></span>
<span data-ttu-id="58f0e-122">Specifica il file di input che contiene il backup del segreto da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="58f0e-122">Specifies the input file that contains the backup of the secret to restore.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58f0e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58f0e-123">-InputObject</span></span>
<span data-ttu-id="58f0e-124">Oggetto Vault</span><span class="sxs-lookup"><span data-stu-id="58f0e-124">KeyVault object</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58f0e-125">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="58f0e-125">-VaultName</span></span>
<span data-ttu-id="58f0e-126">Specifica il nome del Vault chiave in cui ripristinare il segreto.</span><span class="sxs-lookup"><span data-stu-id="58f0e-126">Specifies the name of the key vault into which to restore the secret.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58f0e-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="58f0e-127">-Confirm</span></span>
<span data-ttu-id="58f0e-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58f0e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58f0e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58f0e-129">-WhatIf</span></span>
<span data-ttu-id="58f0e-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="58f0e-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58f0e-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="58f0e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58f0e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58f0e-132">CommonParameters</span></span>
<span data-ttu-id="58f0e-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58f0e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58f0e-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58f0e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58f0e-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="58f0e-135">INPUTS</span></span>

### <span data-ttu-id="58f0e-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="58f0e-136">None</span></span>
<span data-ttu-id="58f0e-137">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="58f0e-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="58f0e-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58f0e-138">OUTPUTS</span></span>

### <span data-ttu-id="58f0e-139">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="58f0e-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="58f0e-140">Note</span><span class="sxs-lookup"><span data-stu-id="58f0e-140">NOTES</span></span>

## <span data-ttu-id="58f0e-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58f0e-141">RELATED LINKS</span></span>

[<span data-ttu-id="58f0e-142">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="58f0e-142">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="58f0e-143">Backup-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="58f0e-143">Backup-AzureKeyVaultSecret</span></span>](./Backup-AzureKeyVaultSecret.md)

[<span data-ttu-id="58f0e-144">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="58f0e-144">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="58f0e-145">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="58f0e-145">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

