---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://go.microsoft.com/fwlink/?LinkId=690301
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Restore-AzureKeyVaultKey.md
ms.openlocfilehash: 1fb58d348af5f507e1bd3c8451f12918c69b309b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521618"
---
# <span data-ttu-id="679eb-101">Restore-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="679eb-101">Restore-AzureKeyVaultKey</span></span>

## <span data-ttu-id="679eb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="679eb-102">SYNOPSIS</span></span>
<span data-ttu-id="679eb-103">Crea una chiave in un Vault chiave da un tasto di backup.</span><span class="sxs-lookup"><span data-stu-id="679eb-103">Creates a key in a key vault from a backed-up key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="679eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="679eb-104">SYNTAX</span></span>

```
Restore-AzureKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="679eb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="679eb-105">DESCRIPTION</span></span>
<span data-ttu-id="679eb-106">Il cmdlet **Restore-AzureKeyVaultKey** crea una chiave nell'archivio chiavi specificato.</span><span class="sxs-lookup"><span data-stu-id="679eb-106">The **Restore-AzureKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="679eb-107">Questa chiave è una replica della chiave di backup nel file di input e ha lo stesso nome della chiave originale.</span><span class="sxs-lookup"><span data-stu-id="679eb-107">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="679eb-108">Se il Vault chiave ha già una chiave con lo stesso nome, questo cmdlet non riesce invece di sovrascrivere la chiave originale.</span><span class="sxs-lookup"><span data-stu-id="679eb-108">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="679eb-109">Se il backup contiene più versioni di una chiave, tutte le versioni verranno ripristinate.</span><span class="sxs-lookup"><span data-stu-id="679eb-109">If the backup contains multiple versions of a key, all versions are restored.</span></span>

<span data-ttu-id="679eb-110">Il Vault chiave in cui ripristinare la chiave può essere diverso da quello della chiave a cui è stato eseguito il backup della chiave.</span><span class="sxs-lookup"><span data-stu-id="679eb-110">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="679eb-111">Tuttavia, il Vault della chiave deve usare lo stesso abbonamento ed essere in un'area di Azure nella stessa geografia (ad esempio, Nord America).</span><span class="sxs-lookup"><span data-stu-id="679eb-111">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="679eb-112">Vedere il Centro protezione di Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) per il mapping delle aree di Azure alle geografie.</span><span class="sxs-lookup"><span data-stu-id="679eb-112">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="679eb-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="679eb-113">EXAMPLES</span></span>

### <span data-ttu-id="679eb-114">Esempio 1: ripristinare un tasto di backup</span><span class="sxs-lookup"><span data-stu-id="679eb-114">Example 1: Restore a backed-up key</span></span>
```
PS C:\>Restore-AzureKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"
```

<span data-ttu-id="679eb-115">Questo comando Ripristina una chiave, incluse tutte le relative versioni, dal file di backup denominato backup. BLOB nel caveau della chiave denominato MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="679eb-115">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="679eb-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="679eb-116">PARAMETERS</span></span>

### <span data-ttu-id="679eb-117">-InputFile</span><span class="sxs-lookup"><span data-stu-id="679eb-117">-InputFile</span></span>
<span data-ttu-id="679eb-118">Specifica il file di input che contiene il backup della chiave da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="679eb-118">Specifies the input file that contains the backup of the key to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="679eb-119">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="679eb-119">-VaultName</span></span>
<span data-ttu-id="679eb-120">Specifica il nome del Vault chiave in cui ripristinare la chiave.</span><span class="sxs-lookup"><span data-stu-id="679eb-120">Specifies the name of the key vault into which to restore the key.</span></span>

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

### <span data-ttu-id="679eb-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="679eb-121">-Confirm</span></span>
<span data-ttu-id="679eb-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="679eb-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="679eb-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="679eb-123">-WhatIf</span></span>
<span data-ttu-id="679eb-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="679eb-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="679eb-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="679eb-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="679eb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="679eb-126">-DefaultProfile</span></span>
<span data-ttu-id="679eb-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="679eb-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="679eb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="679eb-128">CommonParameters</span></span>
<span data-ttu-id="679eb-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="679eb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="679eb-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="679eb-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="679eb-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="679eb-131">INPUTS</span></span>

## <span data-ttu-id="679eb-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="679eb-132">OUTPUTS</span></span>

### <span data-ttu-id="679eb-133">Microsoft. Azure. Commands. Vault. Models. bundle</span><span class="sxs-lookup"><span data-stu-id="679eb-133">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="679eb-134">Note</span><span class="sxs-lookup"><span data-stu-id="679eb-134">NOTES</span></span>

## <span data-ttu-id="679eb-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="679eb-135">RELATED LINKS</span></span>

[<span data-ttu-id="679eb-136">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="679eb-136">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="679eb-137">Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="679eb-137">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="679eb-138">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="679eb-138">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="679eb-139">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="679eb-139">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

