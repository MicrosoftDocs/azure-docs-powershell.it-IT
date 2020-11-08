---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 4750561aed6643c17fed6e42d13551be76635d72
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019589"
---
# <span data-ttu-id="0088c-101">Restore-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0088c-101">Restore-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="0088c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0088c-102">SYNOPSIS</span></span>
<span data-ttu-id="0088c-103">Ripristina un account di archiviazione gestita in un Vault chiave da un file di backup.</span><span class="sxs-lookup"><span data-stu-id="0088c-103">Restores a managed storage account in a key vault from a backup file.</span></span>

## <span data-ttu-id="0088c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0088c-104">SYNTAX</span></span>

### <span data-ttu-id="0088c-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0088c-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0088c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0088c-106">ByInputObject</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0088c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0088c-107">ByResourceId</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0088c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0088c-108">DESCRIPTION</span></span>
<span data-ttu-id="0088c-109">Il cmdlet **Restore-AzKeyVaultManagedStorageAccount** crea un account di archiviazione gestita nell'archivio chiavi specificato da un file di backup.</span><span class="sxs-lookup"><span data-stu-id="0088c-109">The **Restore-AzKeyVaultManagedStorageAccount** cmdlet creates a managed storage account in the specified key vault from a backup file.</span></span>
<span data-ttu-id="0088c-110">Questo account di archiviazione gestita è una replica dell'account di archiviazione gestita di cui è stato eseguito il backup nel file di input e ha lo stesso nome dell'originale.</span><span class="sxs-lookup"><span data-stu-id="0088c-110">This managed storage account is a replica of the backed-up managed storage account in the input file and has the same name as the original.</span></span>
<span data-ttu-id="0088c-111">Se il Vault chiave contiene già un account di archiviazione gestita con lo stesso nome, questo cmdlet non riesce invece di sovrascrivere l'originale.</span><span class="sxs-lookup"><span data-stu-id="0088c-111">If the key vault already contains a managed storage account by the same name, this cmdlet fails instead of overwriting the original.</span></span>
<span data-ttu-id="0088c-112">Il Vault chiave in cui ripristinare l'account di archiviazione gestita può essere diverso da quello della chiave che è stato eseguito il backup dell'account di archiviazione gestita.</span><span class="sxs-lookup"><span data-stu-id="0088c-112">The key vault that you restore the managed storage account into can be different from the key vault that you backed up the managed storage account from.</span></span>
<span data-ttu-id="0088c-113">Tuttavia, il Vault della chiave deve usare lo stesso abbonamento ed essere in un'area di Azure nella stessa geografia (ad esempio, Nord America).</span><span class="sxs-lookup"><span data-stu-id="0088c-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="0088c-114">Vedere il Centro protezione di Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) per il mapping delle aree di Azure alle geografie.</span><span class="sxs-lookup"><span data-stu-id="0088c-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="0088c-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0088c-115">EXAMPLES</span></span>

### <span data-ttu-id="0088c-116">Esempio 1: ripristinare un account di archiviazione gestita di cui è stato eseguito il backup</span><span class="sxs-lookup"><span data-stu-id="0088c-116">Example 1: Restore a backed-up managed storage account</span></span>
```powershell
PS C:\> Restore-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Id                  : https://mykeyvault.vault.azure.net:443/storage/mystorageaccount
Vault Name          : MyKeyVault
AccountName         : mystorageaccount
Account Resource Id : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.St
                      orage/storageAccounts/mystorageaccount
Active Key Name     : key1
Auto Regenerate Key : True
Regeneration Period : 90.00:00:00
Enabled             : True
Created             : 5/21/2018 11:55:58 PM
Updated             : 5/21/2018 11:55:58 PM
Tags                :
```

<span data-ttu-id="0088c-117">Questo comando ripristina un account di archiviazione gestita, incluse tutte le relative versioni, dal file di backup denominato backup. BLOB nel caveau della chiave denominato MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="0088c-117">This command restores a managed storage account, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="0088c-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0088c-118">PARAMETERS</span></span>

### <span data-ttu-id="0088c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0088c-119">-DefaultProfile</span></span>
<span data-ttu-id="0088c-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0088c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0088c-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="0088c-121">-InputFile</span></span>
<span data-ttu-id="0088c-122">File di input.</span><span class="sxs-lookup"><span data-stu-id="0088c-122">Input file.</span></span>
<span data-ttu-id="0088c-123">File di input contenente il BLOB di cui è stato eseguito il backup</span><span class="sxs-lookup"><span data-stu-id="0088c-123">The input file containing the backed-up blob</span></span>

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

### <span data-ttu-id="0088c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0088c-124">-InputObject</span></span>
<span data-ttu-id="0088c-125">Oggetto Vault</span><span class="sxs-lookup"><span data-stu-id="0088c-125">KeyVault object</span></span>

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

### <span data-ttu-id="0088c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0088c-126">-ResourceId</span></span>
<span data-ttu-id="0088c-127">ID risorsa di un Vault</span><span class="sxs-lookup"><span data-stu-id="0088c-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="0088c-128">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="0088c-128">-VaultName</span></span>
<span data-ttu-id="0088c-129">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="0088c-129">Vault name.</span></span>
<span data-ttu-id="0088c-130">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="0088c-130">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="0088c-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0088c-131">-Confirm</span></span>
<span data-ttu-id="0088c-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0088c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0088c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0088c-133">-WhatIf</span></span>
<span data-ttu-id="0088c-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0088c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0088c-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0088c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0088c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0088c-136">CommonParameters</span></span>
<span data-ttu-id="0088c-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0088c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0088c-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0088c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0088c-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0088c-139">INPUTS</span></span>

### <span data-ttu-id="0088c-140">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="0088c-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="0088c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0088c-141">System.String</span></span>

## <span data-ttu-id="0088c-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0088c-142">OUTPUTS</span></span>

### <span data-ttu-id="0088c-143">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0088c-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="0088c-144">Note</span><span class="sxs-lookup"><span data-stu-id="0088c-144">NOTES</span></span>

## <span data-ttu-id="0088c-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0088c-145">RELATED LINKS</span></span>
