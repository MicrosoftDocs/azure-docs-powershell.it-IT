---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/restore-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: 136469819a43dbb918aefebd8134b38ef4a943c7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952477"
---
# <span data-ttu-id="fd14f-101">Restore-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fd14f-101">Restore-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="fd14f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd14f-102">SYNOPSIS</span></span>
<span data-ttu-id="fd14f-103">Ripristina un account di archiviazione gestito in un vault della chiave da un file di backup.</span><span class="sxs-lookup"><span data-stu-id="fd14f-103">Restores a managed storage account in a key vault from a backup file.</span></span>

## <span data-ttu-id="fd14f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fd14f-104">SYNTAX</span></span>

### <span data-ttu-id="fd14f-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fd14f-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd14f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fd14f-106">ByInputObject</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd14f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fd14f-107">ByResourceId</span></span>
```
Restore-AzKeyVaultManagedStorageAccount [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd14f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fd14f-108">DESCRIPTION</span></span>
<span data-ttu-id="fd14f-109">Il cmdlet **Restore-AzKeyVaultManagedStorageAccount** crea un account di archiviazione gestito nella chiave vault specificata da un file di backup.</span><span class="sxs-lookup"><span data-stu-id="fd14f-109">The **Restore-AzKeyVaultManagedStorageAccount** cmdlet creates a managed storage account in the specified key vault from a backup file.</span></span>
<span data-ttu-id="fd14f-110">Questo account di archiviazione gestito è una replica dell'account di archiviazione gestito di cui è stato eseguito il backup nel file di input e ha lo stesso nome dell'originale.</span><span class="sxs-lookup"><span data-stu-id="fd14f-110">This managed storage account is a replica of the backed-up managed storage account in the input file and has the same name as the original.</span></span>
<span data-ttu-id="fd14f-111">Se il vault della chiave contiene già un account di archiviazione gestito con lo stesso nome, questo cmdlet non riesce invece di sovrascrivere l'originale.</span><span class="sxs-lookup"><span data-stu-id="fd14f-111">If the key vault already contains a managed storage account by the same name, this cmdlet fails instead of overwriting the original.</span></span>
<span data-ttu-id="fd14f-112">Il vault delle chiavi in cui si ripristina l'account di archiviazione gestito può essere diverso da quello da cui è stato eseguito il backup dell'account di archiviazione gestito.</span><span class="sxs-lookup"><span data-stu-id="fd14f-112">The key vault that you restore the managed storage account into can be different from the key vault that you backed up the managed storage account from.</span></span>
<span data-ttu-id="fd14f-113">Tuttavia, il vault chiave deve usare la stessa sottoscrizione ed essere in un'area geografica di Azure nella stessa area geografica, ad esempio Nord America.</span><span class="sxs-lookup"><span data-stu-id="fd14f-113">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="fd14f-114">Per il mapping tra le aree geografiche di Azure e le aree geografiche, vedere il Centro protezione di Microsoft https://azure.microsoft.com/support/trust-center/) Azure.</span><span class="sxs-lookup"><span data-stu-id="fd14f-114">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="fd14f-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fd14f-115">EXAMPLES</span></span>

### <span data-ttu-id="fd14f-116">Esempio 1: Ripristinare un account di archiviazione gestito di cui è stato eseguito il backup</span><span class="sxs-lookup"><span data-stu-id="fd14f-116">Example 1: Restore a backed-up managed storage account</span></span>
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

<span data-ttu-id="fd14f-117">Questo comando ripristina un account di archiviazione gestito, incluse tutte le relative versioni, dal file di backup denominato Backup.BLOB nella chiave vault denominata MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="fd14f-117">This command restores a managed storage account, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="fd14f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd14f-118">PARAMETERS</span></span>

### <span data-ttu-id="fd14f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd14f-119">-DefaultProfile</span></span>
<span data-ttu-id="fd14f-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fd14f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd14f-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="fd14f-121">-InputFile</span></span>
<span data-ttu-id="fd14f-122">File di input.</span><span class="sxs-lookup"><span data-stu-id="fd14f-122">Input file.</span></span>
<span data-ttu-id="fd14f-123">File di input che contiene il BLOB di cui è stato eseguito il backup</span><span class="sxs-lookup"><span data-stu-id="fd14f-123">The input file containing the backed-up blob</span></span>

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

### <span data-ttu-id="fd14f-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd14f-124">-InputObject</span></span>
<span data-ttu-id="fd14f-125">Oggetto KeyVault</span><span class="sxs-lookup"><span data-stu-id="fd14f-125">KeyVault object</span></span>

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

### <span data-ttu-id="fd14f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd14f-126">-ResourceId</span></span>
<span data-ttu-id="fd14f-127">ID risorsa KeyVault</span><span class="sxs-lookup"><span data-stu-id="fd14f-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="fd14f-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fd14f-128">-VaultName</span></span>
<span data-ttu-id="fd14f-129">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="fd14f-129">Vault name.</span></span>
<span data-ttu-id="fd14f-130">Il cmdlet crea l'FQDN di un vault in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="fd14f-130">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="fd14f-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd14f-131">-Confirm</span></span>
<span data-ttu-id="fd14f-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd14f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd14f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd14f-133">-WhatIf</span></span>
<span data-ttu-id="fd14f-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd14f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd14f-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd14f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd14f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd14f-136">CommonParameters</span></span>
<span data-ttu-id="fd14f-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd14f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd14f-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fd14f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd14f-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="fd14f-139">INPUTS</span></span>

### <span data-ttu-id="fd14f-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="fd14f-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="fd14f-141">System.String</span><span class="sxs-lookup"><span data-stu-id="fd14f-141">System.String</span></span>

## <span data-ttu-id="fd14f-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fd14f-142">OUTPUTS</span></span>

### <span data-ttu-id="fd14f-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fd14f-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="fd14f-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="fd14f-144">NOTES</span></span>

## <span data-ttu-id="fd14f-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fd14f-145">RELATED LINKS</span></span>
