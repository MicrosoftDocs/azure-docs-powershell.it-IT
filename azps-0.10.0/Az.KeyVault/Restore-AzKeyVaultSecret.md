---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/restore-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
ms.openlocfilehash: 4691d37532db3dd8e629bf1daad2654558a31de3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863030"
---
# <span data-ttu-id="e1f59-101">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e1f59-101">Restore-AzKeyVaultSecret</span></span>

## <span data-ttu-id="e1f59-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e1f59-102">SYNOPSIS</span></span>
<span data-ttu-id="e1f59-103">Crea un segreto in un caveau chiave da un segreto di backup.</span><span class="sxs-lookup"><span data-stu-id="e1f59-103">Creates a secret in a key vault from a backed-up secret.</span></span>

## <span data-ttu-id="e1f59-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e1f59-104">SYNTAX</span></span>

```
Restore-AzKeyVaultSecret [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1f59-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e1f59-105">DESCRIPTION</span></span>
<span data-ttu-id="e1f59-106">Il cmdlet **Restore-AzKeyVaultSecret** crea un segreto nell'archivio chiavi specificato.</span><span class="sxs-lookup"><span data-stu-id="e1f59-106">The **Restore-AzKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="e1f59-107">Questo segreto è una copia del segreto di backup nel file di input e ha lo stesso nome del segreto originale.</span><span class="sxs-lookup"><span data-stu-id="e1f59-107">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="e1f59-108">Se il Vault chiave ha già un segreto con lo stesso nome, questo cmdlet non riesce invece di sovrascrivere il segreto originale.</span><span class="sxs-lookup"><span data-stu-id="e1f59-108">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="e1f59-109">Se il backup contiene più versioni di un segreto, tutte le versioni verranno ripristinate.</span><span class="sxs-lookup"><span data-stu-id="e1f59-109">If the backup contains multiple versions of a secret, all versions are restored.</span></span>

<span data-ttu-id="e1f59-110">Il Vault chiave in cui ripristinare il segreto può essere diverso da quello della chiave in cui è stato eseguito il backup del segreto.</span><span class="sxs-lookup"><span data-stu-id="e1f59-110">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="e1f59-111">Tuttavia, il Vault della chiave deve usare lo stesso abbonamento ed essere in un'area di Azure nella stessa geografia (ad esempio, Nord America).</span><span class="sxs-lookup"><span data-stu-id="e1f59-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="e1f59-112">Vedere il Centro protezione di Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) per il mapping delle aree di Azure alle geografie.</span><span class="sxs-lookup"><span data-stu-id="e1f59-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="e1f59-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e1f59-113">EXAMPLES</span></span>

### <span data-ttu-id="e1f59-114">Esempio 1: ripristinare un segreto di backup</span><span class="sxs-lookup"><span data-stu-id="e1f59-114">Example 1: Restore a backed-up secret</span></span>
```
PS C:\>Restore-AzKeyVaultSecret -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="e1f59-115">Questo comando ripristina un segreto, incluse tutte le sue versioni, dal file di backup denominato backup. BLOB nel Vault Key denominato MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="e1f59-115">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="e1f59-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e1f59-116">PARAMETERS</span></span>

### <span data-ttu-id="e1f59-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1f59-117">-DefaultProfile</span></span>
<span data-ttu-id="e1f59-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e1f59-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1f59-119">-InputFile</span><span class="sxs-lookup"><span data-stu-id="e1f59-119">-InputFile</span></span>
<span data-ttu-id="e1f59-120">Specifica il file di input che contiene il backup del segreto da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="e1f59-120">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="e1f59-121">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="e1f59-121">-VaultName</span></span>
<span data-ttu-id="e1f59-122">Specifica il nome del Vault chiave in cui ripristinare il segreto.</span><span class="sxs-lookup"><span data-stu-id="e1f59-122">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="e1f59-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e1f59-123">-Confirm</span></span>
<span data-ttu-id="e1f59-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1f59-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1f59-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1f59-125">-WhatIf</span></span>
<span data-ttu-id="e1f59-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e1f59-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1f59-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e1f59-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1f59-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1f59-128">CommonParameters</span></span>
<span data-ttu-id="e1f59-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1f59-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1f59-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1f59-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1f59-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e1f59-131">INPUTS</span></span>

### <span data-ttu-id="e1f59-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e1f59-132">None</span></span>
<span data-ttu-id="e1f59-133">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="e1f59-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e1f59-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e1f59-134">OUTPUTS</span></span>

### <span data-ttu-id="e1f59-135">Microsoft. Azure. Commands. Vault. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="e1f59-135">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="e1f59-136">Note</span><span class="sxs-lookup"><span data-stu-id="e1f59-136">NOTES</span></span>

## <span data-ttu-id="e1f59-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e1f59-137">RELATED LINKS</span></span>

[<span data-ttu-id="e1f59-138">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e1f59-138">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="e1f59-139">Backup-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e1f59-139">Backup-AzKeyVaultSecret</span></span>](./Backup-AzKeyVaultSecret.md)

[<span data-ttu-id="e1f59-140">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e1f59-140">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="e1f59-141">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="e1f59-141">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

