---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
ms.openlocfilehash: 0c92dbea0127db82a1b1f4605cd581f31c872a57
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674174"
---
# <span data-ttu-id="3e9da-101">Backup-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3e9da-101">Backup-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="3e9da-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3e9da-102">SYNOPSIS</span></span>
<span data-ttu-id="3e9da-103">Eseguire il backup di un certificato in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="3e9da-103">Backs up a certificate in a key vault.</span></span>

## <span data-ttu-id="3e9da-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e9da-104">SYNTAX</span></span>

### <span data-ttu-id="3e9da-105">ByCertificateName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3e9da-105">ByCertificateName (Default)</span></span>
```
Backup-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e9da-106">ByCertificate</span><span class="sxs-lookup"><span data-stu-id="3e9da-106">ByCertificate</span></span>
```
Backup-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e9da-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e9da-107">DESCRIPTION</span></span>
<span data-ttu-id="3e9da-108">Il cmdlet **backup-AzKeyVaultCertificate** consente di eseguire il backup di un certificato specificato in un Vault chiave, scaricarlo e archiviarlo in un file.</span><span class="sxs-lookup"><span data-stu-id="3e9da-108">The **Backup-AzKeyVaultCertificate** cmdlet backs up a specified certificate in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="3e9da-109">Se il certificato include più versioni, tutte le sue versioni verranno incluse nel backup.</span><span class="sxs-lookup"><span data-stu-id="3e9da-109">If the certificate has multiple versions, all its versions will be included in the backup.</span></span>
<span data-ttu-id="3e9da-110">Poiché il contenuto scaricato è crittografato, non può essere usato all'esterno dell'archivio di chiavi di Azure.</span><span class="sxs-lookup"><span data-stu-id="3e9da-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="3e9da-111">È possibile ripristinare un certificato di backup in qualsiasi volta chiave nell'abbonamento a cui è stato eseguito il backup, purché il Vault si trovi nella stessa geografia di Azure.</span><span class="sxs-lookup"><span data-stu-id="3e9da-111">You can restore a backed-up certificate to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="3e9da-112">I motivi tipici per usare questo cmdlet sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3e9da-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="3e9da-113">Si vuole mantenere una copia offline del certificato nel caso in cui si elimini accidentalmente l'originale dall'archivio.</span><span class="sxs-lookup"><span data-stu-id="3e9da-113">You want to retain an offline copy of the certificate in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="3e9da-114">È stato creato un certificato usando Key Vault e ora si vuole clonare l'oggetto in un'area di Azure diversa, in modo da poterlo usare in tutte le istanze dell'applicazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="3e9da-114">You created a certificate using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="3e9da-115">Usa il cmdlet **backup-AzKeyVaultCertificate** per recuperare il certificato in formato crittografato e quindi usa il cmdlet **Restore-AzKeyVaultCertificate** e specifica un Vault chiave nella seconda area.</span><span class="sxs-lookup"><span data-stu-id="3e9da-115">Use the **Backup-AzKeyVaultCertificate** cmdlet to retrieve the certificate in encrypted format and then use the **Restore-AzKeyVaultCertificate** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="3e9da-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e9da-116">EXAMPLES</span></span>

### <span data-ttu-id="3e9da-117">Esempio 1: eseguire il backup di un certificato con un nome file generato automaticamente</span><span class="sxs-lookup"><span data-stu-id="3e9da-117">Example 1: Back up a certificate with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

<span data-ttu-id="3e9da-118">Questo comando Recupera il certificato denominato cert dal Vault chiave denominato MyKeyVault e salva una copia di backup di tale certificato in un file denominato automaticamente e visualizza il nome del file.</span><span class="sxs-lookup"><span data-stu-id="3e9da-118">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="3e9da-119">Esempio 2: eseguire il backup di un certificato in un nome file specificato</span><span class="sxs-lookup"><span data-stu-id="3e9da-119">Example 2: Back up a certificate to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="3e9da-120">Questo comando Recupera il certificato denominato cert dal Vault chiave denominato MyKeyVault e salva una copia di backup di tale certificato in un file denominato backup. blob.</span><span class="sxs-lookup"><span data-stu-id="3e9da-120">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file named Backup.blob.</span></span>

### <span data-ttu-id="3e9da-121">Esempio 3: eseguire il backup di un certificato recuperato in precedenza in un nome file specificato, sovrascrivendo il file di destinazione senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="3e9da-121">Example 3: Back up a previously retrieved certificate to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $cert = Get-AzKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="3e9da-122">Questo comando crea una copia di backup del certificato denominato $cert. Nome nel Vault denominato $cert. VAULTNAME in un file denominato backup. blob, sovrascrivendo automaticamente il file se esiste già.</span><span class="sxs-lookup"><span data-stu-id="3e9da-122">This command creates a backup of the certificate named $cert.Name in the vault named $cert.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="3e9da-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3e9da-123">PARAMETERS</span></span>

### <span data-ttu-id="3e9da-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e9da-124">-DefaultProfile</span></span>
<span data-ttu-id="3e9da-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3e9da-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e9da-126">-Force</span><span class="sxs-lookup"><span data-stu-id="3e9da-126">-Force</span></span>
<span data-ttu-id="3e9da-127">Sovrascrivere il file assegnato se esiste</span><span class="sxs-lookup"><span data-stu-id="3e9da-127">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="3e9da-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e9da-128">-InputObject</span></span>
<span data-ttu-id="3e9da-129">Segreto di cui eseguire il backup, tramite pipeline nell'output di una chiamata di recupero.</span><span class="sxs-lookup"><span data-stu-id="3e9da-129">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="3e9da-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e9da-130">-Name</span></span>
<span data-ttu-id="3e9da-131">Nome segreto.</span><span class="sxs-lookup"><span data-stu-id="3e9da-131">Secret name.</span></span>
<span data-ttu-id="3e9da-132">Cmdlet costruisce il nome di dominio completo di un segreto dal nome della volta, dall'ambiente selezionato e da quello segreto.</span><span class="sxs-lookup"><span data-stu-id="3e9da-132">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="3e9da-133">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="3e9da-133">-OutputFile</span></span>
<span data-ttu-id="3e9da-134">File di output.</span><span class="sxs-lookup"><span data-stu-id="3e9da-134">Output file.</span></span>
<span data-ttu-id="3e9da-135">File di output per archiviare il backup del certificato.</span><span class="sxs-lookup"><span data-stu-id="3e9da-135">The output file to store the backup of the certificate.</span></span>
<span data-ttu-id="3e9da-136">Se non specificato, verrà generato un nome file predefinito.</span><span class="sxs-lookup"><span data-stu-id="3e9da-136">If not specified, a default filename will be generated.</span></span>

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

### <span data-ttu-id="3e9da-137">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="3e9da-137">-VaultName</span></span>
<span data-ttu-id="3e9da-138">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="3e9da-138">Vault name.</span></span>
<span data-ttu-id="3e9da-139">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="3e9da-139">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="3e9da-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3e9da-140">-Confirm</span></span>
<span data-ttu-id="3e9da-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e9da-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e9da-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e9da-142">-WhatIf</span></span>
<span data-ttu-id="3e9da-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e9da-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e9da-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e9da-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e9da-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e9da-145">CommonParameters</span></span>
<span data-ttu-id="3e9da-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e9da-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e9da-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e9da-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e9da-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3e9da-148">INPUTS</span></span>

### <span data-ttu-id="3e9da-149">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="3e9da-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="3e9da-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e9da-150">OUTPUTS</span></span>

### <span data-ttu-id="3e9da-151">System. String</span><span class="sxs-lookup"><span data-stu-id="3e9da-151">System.String</span></span>

## <span data-ttu-id="3e9da-152">Note</span><span class="sxs-lookup"><span data-stu-id="3e9da-152">NOTES</span></span>

## <span data-ttu-id="3e9da-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e9da-153">RELATED LINKS</span></span>
