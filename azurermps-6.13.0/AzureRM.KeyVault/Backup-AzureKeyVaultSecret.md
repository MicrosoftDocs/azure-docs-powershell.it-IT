---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultSecret.md
ms.openlocfilehash: 6021e9c4c3be3ac4eb2721684b9f94463e1b69af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688412"
---
# <span data-ttu-id="19b44-101">Backup-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="19b44-101">Backup-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="19b44-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="19b44-102">SYNOPSIS</span></span>
<span data-ttu-id="19b44-103">Eseguire il backup di un segreto in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="19b44-103">Backs up a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19b44-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="19b44-104">SYNTAX</span></span>

### <span data-ttu-id="19b44-105">BySecretName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="19b44-105">BySecretName (Default)</span></span>
```
Backup-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19b44-106">BySecret</span><span class="sxs-lookup"><span data-stu-id="19b44-106">BySecret</span></span>
```
Backup-AzureKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19b44-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19b44-107">DESCRIPTION</span></span>
<span data-ttu-id="19b44-108">Il cmdlet **backup-AzureKeyVaultSecret** consente di eseguire il backup di un segreto specificato in un caveau chiave, scaricarlo e archiviarlo in un file.</span><span class="sxs-lookup"><span data-stu-id="19b44-108">The **Backup-AzureKeyVaultSecret** cmdlet backs up a specified secret in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="19b44-109">Se sono presenti più versioni del segreto, tutte le versioni sono incluse nel backup.</span><span class="sxs-lookup"><span data-stu-id="19b44-109">If there are multiple versions of the secret, all versions are included in the backup.</span></span>
<span data-ttu-id="19b44-110">Poiché il contenuto scaricato è crittografato, non può essere usato all'esterno dell'archivio di chiavi di Azure.</span><span class="sxs-lookup"><span data-stu-id="19b44-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="19b44-111">È possibile ripristinare un segreto di backup in qualsiasi volta chiave nell'abbonamento a cui è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="19b44-111">You can restore a backed-up secret to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="19b44-112">I motivi tipici per usare questo cmdlet sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="19b44-112">Typical reasons to use this cmdlet are:</span></span>
- <span data-ttu-id="19b44-113">Si vuole depositare una copia del segreto, in modo da avere una copia offline nel caso in cui si elimini accidentalmente il segreto nel caveau della chiave.</span><span class="sxs-lookup"><span data-stu-id="19b44-113">You want to escrow a copy of your secret, so that you have an offline copy in case you accidentally delete your secret in your key vault.</span></span>
- <span data-ttu-id="19b44-114">È stato aggiunto un segreto a un Vault chiave e ora si vuole clonare il segreto in un'area di Azure diversa, in modo da poterlo usare in tutte le istanze dell'applicazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="19b44-114">You added a secret to a key vault and now want to clone the secret into a different Azure region, so that you can use it from all instances of your distributed application.</span></span> <span data-ttu-id="19b44-115">Usa il cmdlet Backup-AzureKeyVaultSecret per recuperare il segreto in formato crittografato e quindi usa il cmdlet Restore-AzureKeyVaultSecret e specifica un Vault chiave nella seconda area.</span><span class="sxs-lookup"><span data-stu-id="19b44-115">Use the Backup-AzureKeyVaultSecret cmdlet to retrieve the secret in encrypted format and then use the Restore-AzureKeyVaultSecret cmdlet and specify a key vault in the second region.</span></span> <span data-ttu-id="19b44-116">Tieni presente che le aree geografiche devono appartenere alla stessa geografia.</span><span class="sxs-lookup"><span data-stu-id="19b44-116">(Note that the regions must belong to the same geography.)</span></span>

## <span data-ttu-id="19b44-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="19b44-117">EXAMPLES</span></span>

### <span data-ttu-id="19b44-118">Esempio 1: eseguire il backup di un segreto con un nome file generato automaticamente</span><span class="sxs-lookup"><span data-stu-id="19b44-118">Example 1: Back up a secret with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'

C:\Users\username\mykeyvault-mysecret-1527029447.01191
```

<span data-ttu-id="19b44-119">Questo comando Recupera il segreto di nome segreto dal caveau della chiave denominato MyKeyVault e salva una copia di backup di tale segreto in un file denominato automaticamente e visualizza il nome del file.</span><span class="sxs-lookup"><span data-stu-id="19b44-119">This command retrieves the secret named MySecret from the key vault named MyKeyVault and saves a backup of that secret to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="19b44-120">Esempio 2: eseguire il backup di un segreto in un nome file specificato, sovrascrivendo il file esistente senza richiedere conferma</span><span class="sxs-lookup"><span data-stu-id="19b44-120">Example 2: Back up a secret to a specified file name, overwriting the existing file without prompting</span></span>
```powershell
PS C:\> Backup-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="19b44-121">Questo comando Recupera il segreto di nome segreto dalla chiave vaultnamed MyKeyVault e salva una copia di backup di tale segreto in un file denominato backup. blob.</span><span class="sxs-lookup"><span data-stu-id="19b44-121">This command retrieves the secret named MySecret from the key vaultnamed MyKeyVault and saves a backup of that secret to a file named Backup.blob.</span></span>

### <span data-ttu-id="19b44-122">Esempio 3: eseguire il backup di un segreto recuperato in precedenza in un nome file specificato</span><span class="sxs-lookup"><span data-stu-id="19b44-122">Example 3: Back up a secret previously retrieved to a specified file name</span></span>
```powershell
PS C:\> $secret = Get-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\> Backup-AzureKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="19b44-123">Questo comando usa il nome e il nome del Vault dell'oggetto $secret per recuperare il segreto e salva il backup in un file denominato backup. blob.</span><span class="sxs-lookup"><span data-stu-id="19b44-123">This command uses the $secret object's vault name and name to retrieves the secret and saves its backup to a file named Backup.blob.</span></span>

## <span data-ttu-id="19b44-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="19b44-124">PARAMETERS</span></span>

### <span data-ttu-id="19b44-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19b44-125">-DefaultProfile</span></span>
<span data-ttu-id="19b44-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="19b44-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19b44-127">-Force</span><span class="sxs-lookup"><span data-stu-id="19b44-127">-Force</span></span>
<span data-ttu-id="19b44-128">Richiede la conferma prima di sovrascrivere il file di output, se esistente.</span><span class="sxs-lookup"><span data-stu-id="19b44-128">Prompts you for confirmation before overwriting the output file, if that exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19b44-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19b44-129">-InputObject</span></span>
<span data-ttu-id="19b44-130">Segreto di cui eseguire il backup, tramite pipeline nell'output di una chiamata di recupero.</span><span class="sxs-lookup"><span data-stu-id="19b44-130">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: BySecret
Aliases: Secret

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19b44-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="19b44-131">-Name</span></span>
<span data-ttu-id="19b44-132">Specifica il nome del segreto a cui eseguire il backup.</span><span class="sxs-lookup"><span data-stu-id="19b44-132">Specifies the name of the secret to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19b44-133">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="19b44-133">-OutputFile</span></span>
<span data-ttu-id="19b44-134">Specifica il file di output in cui è archiviato il BLOB di backup.</span><span class="sxs-lookup"><span data-stu-id="19b44-134">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="19b44-135">Se non specifichi questo parametro, questo cmdlet genera un nome file.</span><span class="sxs-lookup"><span data-stu-id="19b44-135">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="19b44-136">Se specifichi il nome di un file di output esistente, l'operazione non verrà completata e restituirà un messaggio di errore che indica che il file di backup esiste già.</span><span class="sxs-lookup"><span data-stu-id="19b44-136">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="19b44-137">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="19b44-137">-VaultName</span></span>
<span data-ttu-id="19b44-138">Specifica il nome del Vault chiave che contiene il segreto di cui eseguire il backup.</span><span class="sxs-lookup"><span data-stu-id="19b44-138">Specifies the name of the key vault that contains the secret to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19b44-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="19b44-139">-Confirm</span></span>
<span data-ttu-id="19b44-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19b44-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19b44-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19b44-141">-WhatIf</span></span>
<span data-ttu-id="19b44-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19b44-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19b44-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19b44-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19b44-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19b44-144">CommonParameters</span></span>
<span data-ttu-id="19b44-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19b44-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19b44-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19b44-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19b44-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="19b44-147">INPUTS</span></span>

### <span data-ttu-id="19b44-148">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="19b44-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>
<span data-ttu-id="19b44-149">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="19b44-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="19b44-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="19b44-150">OUTPUTS</span></span>

### <span data-ttu-id="19b44-151">System. String</span><span class="sxs-lookup"><span data-stu-id="19b44-151">System.String</span></span>

## <span data-ttu-id="19b44-152">Note</span><span class="sxs-lookup"><span data-stu-id="19b44-152">NOTES</span></span>

## <span data-ttu-id="19b44-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="19b44-153">RELATED LINKS</span></span>

[<span data-ttu-id="19b44-154">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="19b44-154">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="19b44-155">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="19b44-155">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="19b44-156">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="19b44-156">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="19b44-157">Ripristinare-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="19b44-157">Restore-AzureKeyVaultSecret</span></span>](./Restore-AzureKeyVaultSecret.md)

