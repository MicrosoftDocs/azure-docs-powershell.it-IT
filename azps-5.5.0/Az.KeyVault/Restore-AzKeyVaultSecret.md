---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
ms.openlocfilehash: 5a00bab81cad7b77873459ab58615a2836970b09
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185526"
---
# <span data-ttu-id="ad132-101">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ad132-101">Restore-AzKeyVaultSecret</span></span>

## <span data-ttu-id="ad132-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad132-102">SYNOPSIS</span></span>
<span data-ttu-id="ad132-103">Crea un segreto in un vault della chiave da un segreto di cui è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="ad132-103">Creates a secret in a key vault from a backed-up secret.</span></span>

## <span data-ttu-id="ad132-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad132-104">SYNTAX</span></span>

### <span data-ttu-id="ad132-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ad132-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultSecret [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad132-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ad132-106">ByInputObject</span></span>
```
Restore-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad132-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ad132-107">ByResourceId</span></span>
```
Restore-AzKeyVaultSecret [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad132-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ad132-108">DESCRIPTION</span></span>
<span data-ttu-id="ad132-109">Il cmdlet **Restore-AzKeyVaultSecret** crea un segreto nel vault delle chiavi specificato.</span><span class="sxs-lookup"><span data-stu-id="ad132-109">The **Restore-AzKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="ad132-110">Questo segreto è una replica del segreto di cui è stato eseguito il backup nel file di input e ha lo stesso nome del segreto originale.</span><span class="sxs-lookup"><span data-stu-id="ad132-110">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="ad132-111">Se il vault della chiave ha già un segreto con lo stesso nome, questo cmdlet non riesce invece di sovrascrivere il segreto originale.</span><span class="sxs-lookup"><span data-stu-id="ad132-111">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="ad132-112">Se il backup contiene più versioni di un segreto, vengono ripristinate tutte le versioni.</span><span class="sxs-lookup"><span data-stu-id="ad132-112">If the backup contains multiple versions of a secret, all versions are restored.</span></span>
<span data-ttu-id="ad132-113">Il vault delle chiavi in cui si ripristina il segreto può essere diverso da quello da cui è stato eseguito il backup del segreto.</span><span class="sxs-lookup"><span data-stu-id="ad132-113">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="ad132-114">Tuttavia, il vault chiave deve usare la stessa sottoscrizione ed essere in un'area geografica di Azure nella stessa area geografica, ad esempio Nord America.</span><span class="sxs-lookup"><span data-stu-id="ad132-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="ad132-115">Per il mapping tra le aree geografiche di Azure e le aree geografiche, vedere il Centro protezione di Microsoft https://azure.microsoft.com/support/trust-center/) Azure.</span><span class="sxs-lookup"><span data-stu-id="ad132-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="ad132-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad132-116">EXAMPLES</span></span>

### <span data-ttu-id="ad132-117">Esempio 1: Ripristinare un segreto di cui è stato eseguito il backup</span><span class="sxs-lookup"><span data-stu-id="ad132-117">Example 1: Restore a backed-up secret</span></span>
```powershell
PS C:\> Restore-AzKeyVaultSecret -VaultName 'contoso' -InputFile "C:\Backup.blob"

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

<span data-ttu-id="ad132-118">Questo comando ripristina un segreto, incluse tutte le relative versioni, dal file di backup denominato Backup.BLOB nella chiave vault denominata contoso.</span><span class="sxs-lookup"><span data-stu-id="ad132-118">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named contoso.</span></span>

## <span data-ttu-id="ad132-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad132-119">PARAMETERS</span></span>

### <span data-ttu-id="ad132-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad132-120">-DefaultProfile</span></span>
<span data-ttu-id="ad132-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="ad132-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad132-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="ad132-122">-InputFile</span></span>
<span data-ttu-id="ad132-123">Specifica il file di input che contiene il backup del segreto da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="ad132-123">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="ad132-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ad132-124">-InputObject</span></span>
<span data-ttu-id="ad132-125">Oggetto KeyVault</span><span class="sxs-lookup"><span data-stu-id="ad132-125">KeyVault object</span></span>

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

### <span data-ttu-id="ad132-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad132-126">-ResourceId</span></span>
<span data-ttu-id="ad132-127">ID risorsa KeyVault</span><span class="sxs-lookup"><span data-stu-id="ad132-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="ad132-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ad132-128">-VaultName</span></span>
<span data-ttu-id="ad132-129">Specifica il nome del vault della chiave in cui ripristinare il segreto.</span><span class="sxs-lookup"><span data-stu-id="ad132-129">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="ad132-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad132-130">-Confirm</span></span>
<span data-ttu-id="ad132-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad132-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad132-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad132-132">-WhatIf</span></span>
<span data-ttu-id="ad132-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad132-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad132-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ad132-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad132-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad132-135">CommonParameters</span></span>
<span data-ttu-id="ad132-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad132-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad132-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ad132-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad132-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="ad132-138">INPUTS</span></span>

### <span data-ttu-id="ad132-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="ad132-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="ad132-140">System.String</span><span class="sxs-lookup"><span data-stu-id="ad132-140">System.String</span></span>

## <span data-ttu-id="ad132-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad132-141">OUTPUTS</span></span>

### <span data-ttu-id="ad132-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ad132-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="ad132-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="ad132-143">NOTES</span></span>

## <span data-ttu-id="ad132-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad132-144">RELATED LINKS</span></span>

[<span data-ttu-id="ad132-145">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ad132-145">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="ad132-146">Backup-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ad132-146">Backup-AzKeyVaultSecret</span></span>](./Backup-AzKeyVaultSecret.md)

[<span data-ttu-id="ad132-147">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ad132-147">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="ad132-148">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ad132-148">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

