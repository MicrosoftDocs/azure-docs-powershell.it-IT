---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultCertificate.md
ms.openlocfilehash: 7f75f07ee8f53a57cdb2e359fb4addb51b1d7f76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510975"
---
# <span data-ttu-id="c306d-101">Backup-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="c306d-101">Backup-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="c306d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c306d-102">SYNOPSIS</span></span>
<span data-ttu-id="c306d-103">Eseguire il backup di un certificato in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="c306d-103">Backs up a certificate in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c306d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c306d-104">SYNTAX</span></span>

### <span data-ttu-id="c306d-105">ByCertificateName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c306d-105">ByCertificateName (Default)</span></span>
```
Backup-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c306d-106">ByCertificate</span><span class="sxs-lookup"><span data-stu-id="c306d-106">ByCertificate</span></span>
```
Backup-AzureKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c306d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c306d-107">DESCRIPTION</span></span>
<span data-ttu-id="c306d-108">Il cmdlet **backup-AzureKeyVaultCertificate** consente di eseguire il backup di un certificato specificato in un Vault chiave, scaricarlo e archiviarlo in un file.</span><span class="sxs-lookup"><span data-stu-id="c306d-108">The **Backup-AzureKeyVaultCertificate** cmdlet backs up a specified certificate in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="c306d-109">Se il certificato include più versioni, tutte le sue versioni verranno incluse nel backup.</span><span class="sxs-lookup"><span data-stu-id="c306d-109">If the certificate has multiple versions, all its versions will be included in the backup.</span></span>
<span data-ttu-id="c306d-110">Poiché il contenuto scaricato è crittografato, non può essere usato all'esterno dell'archivio di chiavi di Azure.</span><span class="sxs-lookup"><span data-stu-id="c306d-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="c306d-111">È possibile ripristinare un certificato di backup in qualsiasi volta chiave nell'abbonamento a cui è stato eseguito il backup, purché il Vault si trovi nella stessa geografia di Azure.</span><span class="sxs-lookup"><span data-stu-id="c306d-111">You can restore a backed-up certificate to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="c306d-112">I motivi tipici per usare questo cmdlet sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="c306d-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="c306d-113">Si vuole mantenere una copia offline del certificato nel caso in cui si elimini accidentalmente l'originale dall'archivio.</span><span class="sxs-lookup"><span data-stu-id="c306d-113">You want to retain an offline copy of the certificate in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="c306d-114">È stato creato un certificato usando Key Vault e ora si vuole clonare l'oggetto in un'area di Azure diversa, in modo da poterlo usare in tutte le istanze dell'applicazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="c306d-114">You created a certificate using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="c306d-115">Usa il cmdlet **backup-AzureKeyVaultCertificate** per recuperare il certificato in formato crittografato e quindi usa il cmdlet **Restore-AzureKeyVaultCertificate** e specifica un Vault chiave nella seconda area.</span><span class="sxs-lookup"><span data-stu-id="c306d-115">Use the **Backup-AzureKeyVaultCertificate** cmdlet to retrieve the certificate in encrypted format and then use the **Restore-AzureKeyVaultCertificate** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="c306d-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c306d-116">EXAMPLES</span></span>

### <span data-ttu-id="c306d-117">Esempio 1: eseguire il backup di un certificato con un nome file generato automaticamente</span><span class="sxs-lookup"><span data-stu-id="c306d-117">Example 1: Back up a certificate with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzureKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

<span data-ttu-id="c306d-118">Questo comando Recupera il certificato denominato cert dal Vault chiave denominato MyKeyVault e salva una copia di backup di tale certificato in un file denominato automaticamente e visualizza il nome del file.</span><span class="sxs-lookup"><span data-stu-id="c306d-118">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="c306d-119">Esempio 2: eseguire il backup di un certificato in un nome file specificato</span><span class="sxs-lookup"><span data-stu-id="c306d-119">Example 2: Back up a certificate to a specified file name</span></span>
```powershell
PS C:\> Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="c306d-120">Questo comando Recupera il certificato denominato cert dal Vault chiave denominato MyKeyVault e salva una copia di backup di tale certificato in un file denominato backup. blob.</span><span class="sxs-lookup"><span data-stu-id="c306d-120">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file named Backup.blob.</span></span>

### <span data-ttu-id="c306d-121">Esempio 3: eseguire il backup di un certificato recuperato in precedenza in un nome file specificato, sovrascrivendo il file di destinazione senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="c306d-121">Example 3: Back up a previously retrieved certificate to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $cert = Get-AzureKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzureKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="c306d-122">Questo comando crea una copia di backup del certificato denominato $cert. Nome nel Vault denominato $cert. VAULTNAME in un file denominato backup. blob, sovrascrivendo automaticamente il file se esiste già.</span><span class="sxs-lookup"><span data-stu-id="c306d-122">This command creates a backup of the certificate named $cert.Name in the vault named $cert.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="c306d-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c306d-123">PARAMETERS</span></span>

### <span data-ttu-id="c306d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c306d-124">-DefaultProfile</span></span>
<span data-ttu-id="c306d-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c306d-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c306d-126">-Force</span><span class="sxs-lookup"><span data-stu-id="c306d-126">-Force</span></span>
<span data-ttu-id="c306d-127">Sovrascrivere il file assegnato se esiste</span><span class="sxs-lookup"><span data-stu-id="c306d-127">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="c306d-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c306d-128">-InputObject</span></span>
<span data-ttu-id="c306d-129">Segreto di cui eseguire il backup, tramite pipeline nell'output di una chiamata di recupero.</span><span class="sxs-lookup"><span data-stu-id="c306d-129">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="c306d-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="c306d-130">-Name</span></span>
<span data-ttu-id="c306d-131">Nome segreto.</span><span class="sxs-lookup"><span data-stu-id="c306d-131">Secret name.</span></span>
<span data-ttu-id="c306d-132">Cmdlet costruisce il nome di dominio completo di un segreto dal nome della volta, dall'ambiente selezionato e da quello segreto.</span><span class="sxs-lookup"><span data-stu-id="c306d-132">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="c306d-133">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="c306d-133">-OutputFile</span></span>
<span data-ttu-id="c306d-134">File di output.</span><span class="sxs-lookup"><span data-stu-id="c306d-134">Output file.</span></span>
<span data-ttu-id="c306d-135">File di output per archiviare il backup del certificato.</span><span class="sxs-lookup"><span data-stu-id="c306d-135">The output file to store the backup of the certificate.</span></span>
<span data-ttu-id="c306d-136">Se non specificato, verrà generato un nome file predefinito.</span><span class="sxs-lookup"><span data-stu-id="c306d-136">If not specified, a default filename will be generated.</span></span>

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

### <span data-ttu-id="c306d-137">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="c306d-137">-VaultName</span></span>
<span data-ttu-id="c306d-138">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="c306d-138">Vault name.</span></span>
<span data-ttu-id="c306d-139">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="c306d-139">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="c306d-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c306d-140">-Confirm</span></span>
<span data-ttu-id="c306d-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c306d-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c306d-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c306d-142">-WhatIf</span></span>
<span data-ttu-id="c306d-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c306d-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c306d-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c306d-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c306d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c306d-145">CommonParameters</span></span>
<span data-ttu-id="c306d-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c306d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c306d-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c306d-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c306d-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c306d-148">INPUTS</span></span>

### <span data-ttu-id="c306d-149">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="c306d-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>
<span data-ttu-id="c306d-150">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c306d-150">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="c306d-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c306d-151">OUTPUTS</span></span>

### <span data-ttu-id="c306d-152">System. String</span><span class="sxs-lookup"><span data-stu-id="c306d-152">System.String</span></span>

## <span data-ttu-id="c306d-153">Note</span><span class="sxs-lookup"><span data-stu-id="c306d-153">NOTES</span></span>

## <span data-ttu-id="c306d-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c306d-154">RELATED LINKS</span></span>