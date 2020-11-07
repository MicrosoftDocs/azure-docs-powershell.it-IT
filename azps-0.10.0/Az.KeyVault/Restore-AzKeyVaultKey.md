---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/restore-AzKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
ms.openlocfilehash: 5d090bae05e3d931fbf41b656ea66409d1297e8f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863037"
---
# <span data-ttu-id="0c989-101">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0c989-101">Restore-AzKeyVaultKey</span></span>

## <span data-ttu-id="0c989-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c989-102">SYNOPSIS</span></span>
<span data-ttu-id="0c989-103">Crea una chiave in un Vault chiave da un tasto di backup.</span><span class="sxs-lookup"><span data-stu-id="0c989-103">Creates a key in a key vault from a backed-up key.</span></span>

## <span data-ttu-id="0c989-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c989-104">SYNTAX</span></span>

```
Restore-AzKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c989-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c989-105">DESCRIPTION</span></span>
<span data-ttu-id="0c989-106">Il cmdlet **Restore-AzKeyVaultKey** crea una chiave nell'archivio chiavi specificato.</span><span class="sxs-lookup"><span data-stu-id="0c989-106">The **Restore-AzKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="0c989-107">Questa chiave è una replica della chiave di backup nel file di input e ha lo stesso nome della chiave originale.</span><span class="sxs-lookup"><span data-stu-id="0c989-107">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="0c989-108">Se il Vault chiave ha già una chiave con lo stesso nome, questo cmdlet non riesce invece di sovrascrivere la chiave originale.</span><span class="sxs-lookup"><span data-stu-id="0c989-108">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="0c989-109">Se il backup contiene più versioni di una chiave, tutte le versioni verranno ripristinate.</span><span class="sxs-lookup"><span data-stu-id="0c989-109">If the backup contains multiple versions of a key, all versions are restored.</span></span>

<span data-ttu-id="0c989-110">Il Vault chiave in cui ripristinare la chiave può essere diverso da quello della chiave a cui è stato eseguito il backup della chiave.</span><span class="sxs-lookup"><span data-stu-id="0c989-110">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="0c989-111">Tuttavia, il Vault della chiave deve usare lo stesso abbonamento ed essere in un'area di Azure nella stessa geografia (ad esempio, Nord America).</span><span class="sxs-lookup"><span data-stu-id="0c989-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="0c989-112">Vedere il Centro protezione di Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) per il mapping delle aree di Azure alle geografie.</span><span class="sxs-lookup"><span data-stu-id="0c989-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="0c989-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c989-113">EXAMPLES</span></span>

### <span data-ttu-id="0c989-114">Esempio 1: ripristinare un tasto di backup</span><span class="sxs-lookup"><span data-stu-id="0c989-114">Example 1: Restore a backed-up key</span></span>
```
PS C:\>Restore-AzKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="0c989-115">Questo comando Ripristina una chiave, incluse tutte le relative versioni, dal file di backup denominato backup. BLOB nel caveau della chiave denominato MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="0c989-115">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="0c989-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c989-116">PARAMETERS</span></span>

### <span data-ttu-id="0c989-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c989-117">-DefaultProfile</span></span>
<span data-ttu-id="0c989-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0c989-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c989-119">-InputFile</span><span class="sxs-lookup"><span data-stu-id="0c989-119">-InputFile</span></span>
<span data-ttu-id="0c989-120">Specifica il file di input che contiene il backup della chiave da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="0c989-120">Specifies the input file that contains the backup of the key to restore.</span></span>

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

### <span data-ttu-id="0c989-121">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="0c989-121">-VaultName</span></span>
<span data-ttu-id="0c989-122">Specifica il nome del Vault chiave in cui ripristinare la chiave.</span><span class="sxs-lookup"><span data-stu-id="0c989-122">Specifies the name of the key vault into which to restore the key.</span></span>

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

### <span data-ttu-id="0c989-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0c989-123">-Confirm</span></span>
<span data-ttu-id="0c989-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c989-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c989-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c989-125">-WhatIf</span></span>
<span data-ttu-id="0c989-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c989-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c989-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c989-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c989-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c989-128">CommonParameters</span></span>
<span data-ttu-id="0c989-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c989-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c989-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c989-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c989-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c989-131">INPUTS</span></span>

### <span data-ttu-id="0c989-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0c989-132">None</span></span>
<span data-ttu-id="0c989-133">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="0c989-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0c989-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c989-134">OUTPUTS</span></span>

### <span data-ttu-id="0c989-135">Microsoft. Azure. Commands. Vault. Models. bundle</span><span class="sxs-lookup"><span data-stu-id="0c989-135">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="0c989-136">Note</span><span class="sxs-lookup"><span data-stu-id="0c989-136">NOTES</span></span>

## <span data-ttu-id="0c989-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c989-137">RELATED LINKS</span></span>

[<span data-ttu-id="0c989-138">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0c989-138">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="0c989-139">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0c989-139">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="0c989-140">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0c989-140">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="0c989-141">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0c989-141">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

