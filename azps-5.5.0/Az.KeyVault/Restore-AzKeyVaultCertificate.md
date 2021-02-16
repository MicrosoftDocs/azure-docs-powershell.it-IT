---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultCertificate.md
ms.openlocfilehash: 298d6bac6b2c1b37cff47a22a1647caafdb3e843
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199975"
---
# <span data-ttu-id="3793c-101">Restore-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3793c-101">Restore-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="3793c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3793c-102">SYNOPSIS</span></span>
<span data-ttu-id="3793c-103">Ripristina un certificato in un vault delle chiavi da un file di backup.</span><span class="sxs-lookup"><span data-stu-id="3793c-103">Restores a certificate in a key vault from a backup file.</span></span>

## <span data-ttu-id="3793c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3793c-104">SYNTAX</span></span>

### <span data-ttu-id="3793c-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3793c-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultCertificate [-VaultName] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3793c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3793c-106">ByInputObject</span></span>
```
Restore-AzKeyVaultCertificate [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3793c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3793c-107">ByResourceId</span></span>
```
Restore-AzKeyVaultCertificate [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3793c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3793c-108">DESCRIPTION</span></span>
<span data-ttu-id="3793c-109">Il cmdlet **Restore-AzKeyVaultCertificate** crea un certificato nella chiave vault specificata da un file di backup.</span><span class="sxs-lookup"><span data-stu-id="3793c-109">The **Restore-AzKeyVaultCertificate** cmdlet creates a certificate in the specified key vault from a backup file.</span></span>
<span data-ttu-id="3793c-110">Questo certificato è una replica del certificato di cui è stato eseguito il backup nel file di input e ha lo stesso nome del certificato originale.</span><span class="sxs-lookup"><span data-stu-id="3793c-110">This certificate is a replica of the backed-up certificate in the input file and has the same name as the original certificate.</span></span>
<span data-ttu-id="3793c-111">Se il vault della chiave contiene già un certificato con lo stesso nome, questo cmdlet non riesce invece di sovrascrivere il certificato originale.</span><span class="sxs-lookup"><span data-stu-id="3793c-111">If the key vault already contains a certificate by the same name, this cmdlet fails instead of overwriting the original certificate.</span></span>
<span data-ttu-id="3793c-112">Se il backup contiene più versioni di un certificato, vengono ripristinate tutte le versioni.</span><span class="sxs-lookup"><span data-stu-id="3793c-112">If the backup contains multiple versions of a certificate, all versions are restored.</span></span>
<span data-ttu-id="3793c-113">Il vault delle chiavi in cui si ripristina il certificato può essere diverso da quello da cui è stato eseguito il backup del certificato.</span><span class="sxs-lookup"><span data-stu-id="3793c-113">The key vault that you restore the certificate into can be different from the key vault that you backed up the certificate from.</span></span>
<span data-ttu-id="3793c-114">Tuttavia, il vault chiave deve usare la stessa sottoscrizione ed essere in un'area geografica di Azure nella stessa area geografica, ad esempio Nord America.</span><span class="sxs-lookup"><span data-stu-id="3793c-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="3793c-115">Per il mapping tra le aree geografiche di Azure e le aree geografiche, vedere il Centro protezione di Microsoft https://azure.microsoft.com/support/trust-center/) Azure.</span><span class="sxs-lookup"><span data-stu-id="3793c-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="3793c-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3793c-116">EXAMPLES</span></span>

### <span data-ttu-id="3793c-117">Esempio 1: Ripristinare un certificato di cui è stato eseguito il backup</span><span class="sxs-lookup"><span data-stu-id="3793c-117">Example 1: Restore a backed-up certificate</span></span>
```powershell
PS C:\> Restore-AzKeyVaultCertificate -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Certificate   : [Subject]
                  CN=contoso.com

                [Issuer]
                  CN=contoso.com

                [Serial Number]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                [Not Before]
                  5/25/2018 3:47:41 AM

                [Not After]
                  11/25/2018 2:57:41 AM

                [Thumbprint]
                  XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId         : https://mykeyvault.vault.azure.net:443/keys/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
SecretId      : https://mykeyvault.vault.azure.net:443/secrets/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
Thumbprint    : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel : Purgeable
Enabled       : True
Expires       : 11/25/2018 10:57:41 AM
NotBefore     : 5/25/2018 10:47:41 AM
Created       : 5/25/2018 10:57:41 AM
Updated       : 5/25/2018 10:57:41 AM
Tags          : 
VaultName     : MyKeyVault
Name          : cert1
Version       : bd406f6d6b3a41a1a1c633494d8c3c3a
Id            : https://mykeyvault.vault.azure.net:443/certificates/cert1/bd406f6d6b3a41a1a1c633494d8c3c3a
```

<span data-ttu-id="3793c-118">Questo comando ripristina un certificato, incluse tutte le relative versioni, dal file di backup denominato Backup.BLOB nella chiave vault denominata MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="3793c-118">This command restores a certificate, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="3793c-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3793c-119">PARAMETERS</span></span>

### <span data-ttu-id="3793c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3793c-120">-DefaultProfile</span></span>
<span data-ttu-id="3793c-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3793c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3793c-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="3793c-122">-InputFile</span></span>
<span data-ttu-id="3793c-123">File di input.</span><span class="sxs-lookup"><span data-stu-id="3793c-123">Input file.</span></span>
<span data-ttu-id="3793c-124">File di input che contiene il BLOB di cui è stato eseguito il backup</span><span class="sxs-lookup"><span data-stu-id="3793c-124">The input file containing the backed-up blob</span></span>

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

### <span data-ttu-id="3793c-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3793c-125">-InputObject</span></span>
<span data-ttu-id="3793c-126">Oggetto KeyVault</span><span class="sxs-lookup"><span data-stu-id="3793c-126">KeyVault object</span></span>

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

### <span data-ttu-id="3793c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3793c-127">-ResourceId</span></span>
<span data-ttu-id="3793c-128">ID risorsa KeyVault</span><span class="sxs-lookup"><span data-stu-id="3793c-128">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="3793c-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3793c-129">-VaultName</span></span>
<span data-ttu-id="3793c-130">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="3793c-130">Vault name.</span></span>
<span data-ttu-id="3793c-131">Il cmdlet crea l'FQDN di un vault in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="3793c-131">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="3793c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3793c-132">-Confirm</span></span>
<span data-ttu-id="3793c-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3793c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3793c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3793c-134">-WhatIf</span></span>
<span data-ttu-id="3793c-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3793c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3793c-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3793c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3793c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3793c-137">CommonParameters</span></span>
<span data-ttu-id="3793c-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3793c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3793c-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3793c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3793c-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="3793c-140">INPUTS</span></span>

### <span data-ttu-id="3793c-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="3793c-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="3793c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="3793c-142">System.String</span></span>

## <span data-ttu-id="3793c-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3793c-143">OUTPUTS</span></span>

### <span data-ttu-id="3793c-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3793c-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificate</span></span>

## <span data-ttu-id="3793c-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="3793c-145">NOTES</span></span>

## <span data-ttu-id="3793c-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3793c-146">RELATED LINKS</span></span>
