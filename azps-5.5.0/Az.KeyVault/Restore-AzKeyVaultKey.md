---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
ms.openlocfilehash: 958aeb36ba047284085d471f73aadad78b756839
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185534"
---
# <span data-ttu-id="6739f-101">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6739f-101">Restore-AzKeyVaultKey</span></span>

## <span data-ttu-id="6739f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6739f-102">SYNOPSIS</span></span>
<span data-ttu-id="6739f-103">Crea una chiave in un vault delle chiavi da una chiave di cui è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="6739f-103">Creates a key in a key vault from a backed-up key.</span></span>

## <span data-ttu-id="6739f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6739f-104">SYNTAX</span></span>

### <span data-ttu-id="6739f-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6739f-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6739f-106">HsmByVaultName</span><span class="sxs-lookup"><span data-stu-id="6739f-106">HsmByVaultName</span></span>
```
Restore-AzKeyVaultKey -HsmName <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6739f-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6739f-107">ByInputObject</span></span>
```
Restore-AzKeyVaultKey [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6739f-108">HsmByInputObject</span><span class="sxs-lookup"><span data-stu-id="6739f-108">HsmByInputObject</span></span>
```
Restore-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6739f-109">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6739f-109">ByResourceId</span></span>
```
Restore-AzKeyVaultKey [-ResourceId] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6739f-110">HsmByResourceId</span><span class="sxs-lookup"><span data-stu-id="6739f-110">HsmByResourceId</span></span>
```
Restore-AzKeyVaultKey -HsmResourceId <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6739f-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6739f-111">DESCRIPTION</span></span>
<span data-ttu-id="6739f-112">Il cmdlet **Restore-AzKeyVaultKey** crea una chiave nel vault delle chiavi specificato.</span><span class="sxs-lookup"><span data-stu-id="6739f-112">The **Restore-AzKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="6739f-113">Questa chiave è una replica della chiave di cui è stato eseguito il backup nel file di input e ha lo stesso nome della chiave originale.</span><span class="sxs-lookup"><span data-stu-id="6739f-113">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="6739f-114">Se il vault delle chiavi ha già una chiave con lo stesso nome, questo cmdlet non riesce invece di sovrascrivere la chiave originale.</span><span class="sxs-lookup"><span data-stu-id="6739f-114">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="6739f-115">Se il backup contiene più versioni di una chiave, vengono ripristinate tutte le versioni.</span><span class="sxs-lookup"><span data-stu-id="6739f-115">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="6739f-116">Il vault delle chiavi in cui si ripristina la chiave può essere diverso da quello da cui è stato eseguito il backup della chiave.</span><span class="sxs-lookup"><span data-stu-id="6739f-116">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="6739f-117">Tuttavia, il vault chiave deve usare la stessa sottoscrizione ed essere in un'area geografica di Azure nella stessa area geografica, ad esempio Nord America.</span><span class="sxs-lookup"><span data-stu-id="6739f-117">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="6739f-118">Per il mapping tra le aree geografiche di Azure e le aree geografiche, vedere il Centro protezione di Microsoft https://azure.microsoft.com/support/trust-center/) Azure.</span><span class="sxs-lookup"><span data-stu-id="6739f-118">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="6739f-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6739f-119">EXAMPLES</span></span>

### <span data-ttu-id="6739f-120">Esempio 1: Ripristinare una chiave di cui è stato eseguito il backup</span><span class="sxs-lookup"><span data-stu-id="6739f-120">Example 1: Restore a backed-up key</span></span>
```powershell
PS C:\> Restore-AzKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

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

<span data-ttu-id="6739f-121">Questo comando ripristina una chiave, incluse tutte le relative versioni, dal file di backup denominato Backup.BLOB nel vault delle chiavi denominato MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="6739f-121">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="6739f-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6739f-122">PARAMETERS</span></span>

### <span data-ttu-id="6739f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6739f-123">-DefaultProfile</span></span>
<span data-ttu-id="6739f-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="6739f-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6739f-125">-HsmName</span><span class="sxs-lookup"><span data-stu-id="6739f-125">-HsmName</span></span>
<span data-ttu-id="6739f-126">Nome HSM.</span><span class="sxs-lookup"><span data-stu-id="6739f-126">HSM name.</span></span> <span data-ttu-id="6739f-127">Il cmdlet crea l'FQDN di un servizio HSM gestito in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="6739f-127">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6739f-128">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="6739f-128">-HsmObject</span></span>
<span data-ttu-id="6739f-129">Oggetto HSM</span><span class="sxs-lookup"><span data-stu-id="6739f-129">HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: HsmByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6739f-130">-HsmResourceId</span><span class="sxs-lookup"><span data-stu-id="6739f-130">-HsmResourceId</span></span>
<span data-ttu-id="6739f-131">ID risorsa Hsm</span><span class="sxs-lookup"><span data-stu-id="6739f-131">Hsm Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6739f-132">-InputFile</span><span class="sxs-lookup"><span data-stu-id="6739f-132">-InputFile</span></span>
<span data-ttu-id="6739f-133">Specifica il file di input che contiene il backup della chiave da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="6739f-133">Specifies the input file that contains the backup of the key to restore.</span></span>

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

### <span data-ttu-id="6739f-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6739f-134">-InputObject</span></span>
<span data-ttu-id="6739f-135">Oggetto KeyVault</span><span class="sxs-lookup"><span data-stu-id="6739f-135">KeyVault object</span></span>

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

### <span data-ttu-id="6739f-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6739f-136">-ResourceId</span></span>
<span data-ttu-id="6739f-137">ID risorsa KeyVault</span><span class="sxs-lookup"><span data-stu-id="6739f-137">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="6739f-138">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6739f-138">-VaultName</span></span>
<span data-ttu-id="6739f-139">Specifica il nome del vault della chiave in cui ripristinare la chiave.</span><span class="sxs-lookup"><span data-stu-id="6739f-139">Specifies the name of the key vault into which to restore the key.</span></span>

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

### <span data-ttu-id="6739f-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6739f-140">-Confirm</span></span>
<span data-ttu-id="6739f-141">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6739f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6739f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6739f-142">-WhatIf</span></span>
<span data-ttu-id="6739f-143">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6739f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6739f-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6739f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6739f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6739f-145">CommonParameters</span></span>
<span data-ttu-id="6739f-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6739f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6739f-147">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6739f-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6739f-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="6739f-148">INPUTS</span></span>

### <span data-ttu-id="6739f-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="6739f-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="6739f-150">System.String</span><span class="sxs-lookup"><span data-stu-id="6739f-150">System.String</span></span>

## <span data-ttu-id="6739f-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6739f-151">OUTPUTS</span></span>

### <span data-ttu-id="6739f-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6739f-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="6739f-153">NOTE</span><span class="sxs-lookup"><span data-stu-id="6739f-153">NOTES</span></span>

## <span data-ttu-id="6739f-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6739f-154">RELATED LINKS</span></span>

[<span data-ttu-id="6739f-155">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6739f-155">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="6739f-156">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6739f-156">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="6739f-157">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6739f-157">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="6739f-158">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="6739f-158">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

