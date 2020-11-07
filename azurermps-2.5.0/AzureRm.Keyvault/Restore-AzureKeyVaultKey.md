---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/restore-azurekeyvaultkey
schema: 2.0.0
ms.openlocfilehash: 7bad1311d463b8372d07a33c549682a2cade4041
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865784"
---
# <span data-ttu-id="500c6-101">Restore-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="500c6-101">Restore-AzureKeyVaultKey</span></span>

## <span data-ttu-id="500c6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="500c6-102">SYNOPSIS</span></span>
<span data-ttu-id="500c6-103">Crea una chiave in un Vault chiave da un tasto di backup.</span><span class="sxs-lookup"><span data-stu-id="500c6-103">Creates a key in a key vault from a backed-up key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="500c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="500c6-104">SYNTAX</span></span>

```
Restore-AzureKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="500c6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="500c6-105">DESCRIPTION</span></span>
<span data-ttu-id="500c6-106">Il cmdlet **Restore-AzureKeyVaultKey** crea una chiave nell'archivio chiavi specificato.</span><span class="sxs-lookup"><span data-stu-id="500c6-106">The **Restore-AzureKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="500c6-107">Questa chiave è una replica della chiave di backup nel file di input e ha lo stesso nome della chiave originale.</span><span class="sxs-lookup"><span data-stu-id="500c6-107">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="500c6-108">Se il Vault chiave ha già una chiave con lo stesso nome, questo cmdlet non riesce invece di sovrascrivere la chiave originale.</span><span class="sxs-lookup"><span data-stu-id="500c6-108">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="500c6-109">Se il backup contiene più versioni di una chiave, tutte le versioni verranno ripristinate.</span><span class="sxs-lookup"><span data-stu-id="500c6-109">If the backup contains multiple versions of a key, all versions are restored.</span></span>

<span data-ttu-id="500c6-110">Il Vault chiave in cui ripristinare la chiave può essere diverso da quello della chiave a cui è stato eseguito il backup della chiave.</span><span class="sxs-lookup"><span data-stu-id="500c6-110">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="500c6-111">Tuttavia, il Vault della chiave deve usare lo stesso abbonamento ed essere in un'area di Azure nella stessa geografia (ad esempio, Nord America).</span><span class="sxs-lookup"><span data-stu-id="500c6-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="500c6-112">Vedere il Centro protezione di Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) per il mapping delle aree di Azure alle geografie.</span><span class="sxs-lookup"><span data-stu-id="500c6-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="500c6-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="500c6-113">EXAMPLES</span></span>

### <span data-ttu-id="500c6-114">Esempio 1: ripristinare un tasto di backup</span><span class="sxs-lookup"><span data-stu-id="500c6-114">Example 1: Restore a backed-up key</span></span>
```
PS C:\>Restore-AzureKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="500c6-115">Questo comando Ripristina una chiave, incluse tutte le relative versioni, dal file di backup denominato backup. BLOB nel caveau della chiave denominato MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="500c6-115">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="500c6-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="500c6-116">PARAMETERS</span></span>

### <span data-ttu-id="500c6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="500c6-117">-DefaultProfile</span></span>
<span data-ttu-id="500c6-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="500c6-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="500c6-119">-InputFile</span><span class="sxs-lookup"><span data-stu-id="500c6-119">-InputFile</span></span>
<span data-ttu-id="500c6-120">Specifica il file di input che contiene il backup della chiave da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="500c6-120">Specifies the input file that contains the backup of the key to restore.</span></span>

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

### <span data-ttu-id="500c6-121">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="500c6-121">-VaultName</span></span>
<span data-ttu-id="500c6-122">Specifica il nome del Vault chiave in cui ripristinare la chiave.</span><span class="sxs-lookup"><span data-stu-id="500c6-122">Specifies the name of the key vault into which to restore the key.</span></span>

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

### <span data-ttu-id="500c6-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="500c6-123">-Confirm</span></span>
<span data-ttu-id="500c6-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="500c6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="500c6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="500c6-125">-WhatIf</span></span>
<span data-ttu-id="500c6-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="500c6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="500c6-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="500c6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="500c6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="500c6-128">CommonParameters</span></span>
<span data-ttu-id="500c6-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="500c6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="500c6-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="500c6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="500c6-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="500c6-131">INPUTS</span></span>

## <span data-ttu-id="500c6-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="500c6-132">OUTPUTS</span></span>

### <span data-ttu-id="500c6-133">Microsoft. Azure. Commands. Vault. Models. bundle</span><span class="sxs-lookup"><span data-stu-id="500c6-133">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="500c6-134">Note</span><span class="sxs-lookup"><span data-stu-id="500c6-134">NOTES</span></span>

## <span data-ttu-id="500c6-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="500c6-135">RELATED LINKS</span></span>

[<span data-ttu-id="500c6-136">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="500c6-136">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="500c6-137">Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="500c6-137">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="500c6-138">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="500c6-138">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="500c6-139">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="500c6-139">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

