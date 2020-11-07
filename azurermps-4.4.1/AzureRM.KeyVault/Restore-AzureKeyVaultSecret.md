---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://go.microsoft.com/fwlink/?LinkId=690301
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultSecret.md
ms.openlocfilehash: bd619f6c4ec9891972d23738c1f2510cba0e2272
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686575"
---
# <span data-ttu-id="7649e-101">Restore-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7649e-101">Restore-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="7649e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7649e-102">SYNOPSIS</span></span>
<span data-ttu-id="7649e-103">Crea un segreto in un caveau chiave da un segreto di backup.</span><span class="sxs-lookup"><span data-stu-id="7649e-103">Creates a secret in a key vault from a backed-up secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7649e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7649e-104">SYNTAX</span></span>

```
Restore-AzureKeyVaultSecret [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7649e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7649e-105">DESCRIPTION</span></span>
<span data-ttu-id="7649e-106">Il cmdlet **Restore-AzureKeyVaultSecret** crea un segreto nell'archivio chiavi specificato.</span><span class="sxs-lookup"><span data-stu-id="7649e-106">The **Restore-AzureKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="7649e-107">Questo segreto è una copia del segreto di backup nel file di input e ha lo stesso nome del segreto originale.</span><span class="sxs-lookup"><span data-stu-id="7649e-107">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="7649e-108">Se il Vault chiave ha già un segreto con lo stesso nome, questo cmdlet non riesce invece di sovrascrivere il segreto originale.</span><span class="sxs-lookup"><span data-stu-id="7649e-108">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="7649e-109">Se il backup contiene più versioni di un segreto, tutte le versioni verranno ripristinate.</span><span class="sxs-lookup"><span data-stu-id="7649e-109">If the backup contains multiple versions of a secret, all versions are restored.</span></span>

<span data-ttu-id="7649e-110">Il Vault chiave in cui ripristinare il segreto può essere diverso da quello della chiave in cui è stato eseguito il backup del segreto.</span><span class="sxs-lookup"><span data-stu-id="7649e-110">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="7649e-111">Tuttavia, il Vault della chiave deve usare lo stesso abbonamento ed essere in un'area di Azure nella stessa geografia (ad esempio, Nord America).</span><span class="sxs-lookup"><span data-stu-id="7649e-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="7649e-112">Vedere il Centro protezione di Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) per il mapping delle aree di Azure alle geografie.</span><span class="sxs-lookup"><span data-stu-id="7649e-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="7649e-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7649e-113">EXAMPLES</span></span>

### <span data-ttu-id="7649e-114">Esempio 1: ripristinare un segreto di backup</span><span class="sxs-lookup"><span data-stu-id="7649e-114">Example 1: Restore a backed-up secret</span></span>
```
PS C:\>Restore-AzureKeyVaultSecret -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="7649e-115">Questo comando ripristina un segreto, incluse tutte le sue versioni, dal file di backup denominato backup. BLOB nel Vault Key denominato MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="7649e-115">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="7649e-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7649e-116">PARAMETERS</span></span>

### <span data-ttu-id="7649e-117">-InputFile</span><span class="sxs-lookup"><span data-stu-id="7649e-117">-InputFile</span></span>
<span data-ttu-id="7649e-118">Specifica il file di input che contiene il backup del segreto da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="7649e-118">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="7649e-119">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="7649e-119">-VaultName</span></span>
<span data-ttu-id="7649e-120">Specifica il nome del Vault chiave in cui ripristinare il segreto.</span><span class="sxs-lookup"><span data-stu-id="7649e-120">Specifies the name of the key vault into which to restore the secret.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7649e-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7649e-121">-Confirm</span></span>
<span data-ttu-id="7649e-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7649e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7649e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7649e-123">-WhatIf</span></span>
<span data-ttu-id="7649e-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7649e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7649e-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7649e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7649e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7649e-126">-DefaultProfile</span></span>
<span data-ttu-id="7649e-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7649e-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7649e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7649e-128">CommonParameters</span></span>
<span data-ttu-id="7649e-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7649e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7649e-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7649e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7649e-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7649e-131">INPUTS</span></span>

## <span data-ttu-id="7649e-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7649e-132">OUTPUTS</span></span>

### <span data-ttu-id="7649e-133">Microsoft. Azure. Commands. Vault. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="7649e-133">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="7649e-134">Note</span><span class="sxs-lookup"><span data-stu-id="7649e-134">NOTES</span></span>

## <span data-ttu-id="7649e-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7649e-135">RELATED LINKS</span></span>

[<span data-ttu-id="7649e-136">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7649e-136">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="7649e-137">Backup-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7649e-137">Backup-AzureKeyVaultSecret</span></span>](./Backup-AzureKeyVaultSecret.md)

[<span data-ttu-id="7649e-138">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7649e-138">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="7649e-139">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7649e-139">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

