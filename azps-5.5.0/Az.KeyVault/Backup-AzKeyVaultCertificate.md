---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
ms.openlocfilehash: 51d322ea738a56e4b1fa24cccdb7bb59a6cd0d21
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180471"
---
# <span data-ttu-id="58aef-101">Backup-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="58aef-101">Backup-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="58aef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58aef-102">SYNOPSIS</span></span>
<span data-ttu-id="58aef-103">Backup di un certificato in un vault chiave.</span><span class="sxs-lookup"><span data-stu-id="58aef-103">Backs up a certificate in a key vault.</span></span>

## <span data-ttu-id="58aef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58aef-104">SYNTAX</span></span>

### <span data-ttu-id="58aef-105">ByCertificateName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="58aef-105">ByCertificateName (Default)</span></span>
```
Backup-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58aef-106">ByCertificate</span><span class="sxs-lookup"><span data-stu-id="58aef-106">ByCertificate</span></span>
```
Backup-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58aef-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="58aef-107">DESCRIPTION</span></span>
<span data-ttu-id="58aef-108">Il **cmdlet Backup-AzKeyVaultCertificate** consente di eseguire il backup di un certificato specificato in un vault delle chiavi scaricarlo e archiviarlo in un file.</span><span class="sxs-lookup"><span data-stu-id="58aef-108">The **Backup-AzKeyVaultCertificate** cmdlet backs up a specified certificate in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="58aef-109">Se il certificato ha più versioni, nel backup verranno incluse tutte le relative versioni.</span><span class="sxs-lookup"><span data-stu-id="58aef-109">If the certificate has multiple versions, all its versions will be included in the backup.</span></span>
<span data-ttu-id="58aef-110">Poiché il contenuto scaricato è crittografato, non può essere usato all'esterno del Vault delle chiavi di Azure.</span><span class="sxs-lookup"><span data-stu-id="58aef-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="58aef-111">È possibile ripristinare un certificato di cui è stato eseguito il backup in qualsiasi vault chiave nell'abbonamento da cui è stato eseguito il backup, purché il vault si trova nella stessa area geografica di Azure.</span><span class="sxs-lookup"><span data-stu-id="58aef-111">You can restore a backed-up certificate to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="58aef-112">I motivi tipici per usare questo cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="58aef-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="58aef-113">Si vuole conservare una copia offline del certificato nel caso in cui si elimini accidentalmente l'originale dal Vault.</span><span class="sxs-lookup"><span data-stu-id="58aef-113">You want to retain an offline copy of the certificate in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="58aef-114">È stato creato un certificato con il Vault delle chiavi e ora si vuole clonare l'oggetto in un'area di Azure diversa, in modo da poterlo usare da tutte le istanze dell'applicazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="58aef-114">You created a certificate using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="58aef-115">Usare il cmdlet **Backup-AzKeyVaultCertificate** per recuperare il certificato in formato crittografato e quindi usare il cmdlet **Restore-AzKeyVaultCertificate** e specificare un vault delle chiavi nella seconda area geografica.</span><span class="sxs-lookup"><span data-stu-id="58aef-115">Use the **Backup-AzKeyVaultCertificate** cmdlet to retrieve the certificate in encrypted format and then use the **Restore-AzKeyVaultCertificate** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="58aef-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58aef-116">EXAMPLES</span></span>

### <span data-ttu-id="58aef-117">Esempio 1: Eseguire il backup di un certificato con un nome file generato automaticamente</span><span class="sxs-lookup"><span data-stu-id="58aef-117">Example 1: Back up a certificate with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

<span data-ttu-id="58aef-118">Questo comando recupera il certificato denominato MyCert dal vault delle chiavi denominato MyKeyVault e salva una copia di backup del certificato in un file denominato automaticamente e visualizza il nome del file.</span><span class="sxs-lookup"><span data-stu-id="58aef-118">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="58aef-119">Esempio 2: Eseguire il backup di un certificato con un nome file specificato</span><span class="sxs-lookup"><span data-stu-id="58aef-119">Example 2: Back up a certificate to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="58aef-120">Questo comando recupera il certificato denominato MyCert dal vault delle chiavi denominato MyKeyVault e salva una copia di backup del certificato in un file denominato Backup.BLOB.</span><span class="sxs-lookup"><span data-stu-id="58aef-120">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file named Backup.blob.</span></span>

### <span data-ttu-id="58aef-121">Esempio 3: Eseguire il backup di un certificato recuperato in precedenza con un nome file specificato sovrascrivendo il file di destinazione senza chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="58aef-121">Example 3: Back up a previously retrieved certificate to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $cert = Get-AzKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="58aef-122">Questo comando crea una copia di backup del certificato denominato $cert. Nome nel vault denominato $cert. VaultName in un file denominato Backup.BLOB, sovrascrivendo automaticamente il file, se esistente.</span><span class="sxs-lookup"><span data-stu-id="58aef-122">This command creates a backup of the certificate named $cert.Name in the vault named $cert.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="58aef-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58aef-123">PARAMETERS</span></span>

### <span data-ttu-id="58aef-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58aef-124">-DefaultProfile</span></span>
<span data-ttu-id="58aef-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="58aef-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58aef-126">-Force</span><span class="sxs-lookup"><span data-stu-id="58aef-126">-Force</span></span>
<span data-ttu-id="58aef-127">Sovrascrivere il file specificato, se esistente</span><span class="sxs-lookup"><span data-stu-id="58aef-127">Overwrite the given file if it exists</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58aef-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58aef-128">-InputObject</span></span>
<span data-ttu-id="58aef-129">Segreto di cui eseguire il backup, pipelined in seguito all'output di una chiamata di recupero.</span><span class="sxs-lookup"><span data-stu-id="58aef-129">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByCertificate
Aliases: Certificate

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58aef-130">-Name</span><span class="sxs-lookup"><span data-stu-id="58aef-130">-Name</span></span>
<span data-ttu-id="58aef-131">Nome segreto.</span><span class="sxs-lookup"><span data-stu-id="58aef-131">Secret name.</span></span>
<span data-ttu-id="58aef-132">Il cmdlet crea l'FQDN di un segreto dal nome del vault, l'ambiente attualmente selezionato e il nome del segreto.</span><span class="sxs-lookup"><span data-stu-id="58aef-132">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58aef-133">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="58aef-133">-OutputFile</span></span>
<span data-ttu-id="58aef-134">File di output.</span><span class="sxs-lookup"><span data-stu-id="58aef-134">Output file.</span></span>
<span data-ttu-id="58aef-135">Il file di output per archiviare il backup del certificato.</span><span class="sxs-lookup"><span data-stu-id="58aef-135">The output file to store the backup of the certificate.</span></span>
<span data-ttu-id="58aef-136">Se non viene specificato, verrà generato un nome file predefinito.</span><span class="sxs-lookup"><span data-stu-id="58aef-136">If not specified, a default filename will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58aef-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="58aef-137">-VaultName</span></span>
<span data-ttu-id="58aef-138">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="58aef-138">Vault name.</span></span>
<span data-ttu-id="58aef-139">Il cmdlet crea l'FQDN di un vault in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="58aef-139">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58aef-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58aef-140">-Confirm</span></span>
<span data-ttu-id="58aef-141">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58aef-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58aef-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58aef-142">-WhatIf</span></span>
<span data-ttu-id="58aef-143">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="58aef-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58aef-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="58aef-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58aef-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58aef-145">CommonParameters</span></span>
<span data-ttu-id="58aef-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58aef-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58aef-147">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="58aef-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58aef-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="58aef-148">INPUTS</span></span>

### <span data-ttu-id="58aef-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="58aef-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="58aef-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58aef-150">OUTPUTS</span></span>

### <span data-ttu-id="58aef-151">System.String</span><span class="sxs-lookup"><span data-stu-id="58aef-151">System.String</span></span>

## <span data-ttu-id="58aef-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="58aef-152">NOTES</span></span>

## <span data-ttu-id="58aef-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58aef-153">RELATED LINKS</span></span>
