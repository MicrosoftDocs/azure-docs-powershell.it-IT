---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/powershell/module/az.keyvault/backup-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
ms.openlocfilehash: ae60c2d10c8b186db22fb9fc9cd0a1e66aa1c07d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962013"
---
# <span data-ttu-id="9b5d3-101">Backup-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="9b5d3-101">Backup-AzKeyVaultSecret</span></span>

## <span data-ttu-id="9b5d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b5d3-102">SYNOPSIS</span></span>
<span data-ttu-id="9b5d3-103">Backup di un segreto in un vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-103">Backs up a secret in a key vault.</span></span>

## <span data-ttu-id="9b5d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9b5d3-104">SYNTAX</span></span>

### <span data-ttu-id="9b5d3-105">BySecretName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9b5d3-105">BySecretName (Default)</span></span>
```
Backup-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b5d3-106">BySecret</span><span class="sxs-lookup"><span data-stu-id="9b5d3-106">BySecret</span></span>
```
Backup-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b5d3-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9b5d3-107">DESCRIPTION</span></span>
<span data-ttu-id="9b5d3-108">Il cmdlet **Backup-AzKeyVaultSecret** consente di eseguire il backup di un segreto specificato in un vault delle chiavi scaricarlo e archiviarlo in un file.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-108">The **Backup-AzKeyVaultSecret** cmdlet backs up a specified secret in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="9b5d3-109">Se sono presenti più versioni del segreto, tutte le versioni sono incluse nel backup.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-109">If there are multiple versions of the secret, all versions are included in the backup.</span></span>
<span data-ttu-id="9b5d3-110">Poiché il contenuto scaricato è crittografato, non può essere usato all'esterno del Vault delle chiavi di Azure.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="9b5d3-111">È possibile ripristinare un segreto di cui è stato eseguito il backup in qualsiasi vault della chiave nell'abbonamento da cui è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-111">You can restore a backed-up secret to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="9b5d3-112">I motivi tipici per usare questo cmdlet sono:</span><span class="sxs-lookup"><span data-stu-id="9b5d3-112">Typical reasons to use this cmdlet are:</span></span>
- <span data-ttu-id="9b5d3-113">Si vuole eliminare una copia del segreto, in modo da avere una copia offline nel caso in cui si elimini accidentalmente il segreto nel vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-113">You want to escrow a copy of your secret, so that you have an offline copy in case you accidentally delete your secret in your key vault.</span></span>
- <span data-ttu-id="9b5d3-114">È stato aggiunto un segreto a un vault delle chiavi e ora si vuole clonare il segreto in un'area di Azure diversa, in modo da poterlo usare da tutte le istanze dell'applicazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-114">You added a secret to a key vault and now want to clone the secret into a different Azure region, so that you can use it from all instances of your distributed application.</span></span> <span data-ttu-id="9b5d3-115">Usare il cmdlet Backup-AzKeyVaultSecret per recuperare il segreto in formato crittografato e quindi usare il cmdlet Restore-AzKeyVaultSecret e specificare un vault delle chiavi nella seconda area geografica.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-115">Use the Backup-AzKeyVaultSecret cmdlet to retrieve the secret in encrypted format and then use the Restore-AzKeyVaultSecret cmdlet and specify a key vault in the second region.</span></span> <span data-ttu-id="9b5d3-116">Si noti che le aree geografiche devono appartenere alla stessa area geografica.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-116">(Note that the regions must belong to the same geography.)</span></span>

## <span data-ttu-id="9b5d3-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9b5d3-117">EXAMPLES</span></span>

### <span data-ttu-id="9b5d3-118">Esempio 1: Eseguire il backup di un segreto con un nome file generato automaticamente</span><span class="sxs-lookup"><span data-stu-id="9b5d3-118">Example 1: Back up a secret with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'

C:\Users\username\mykeyvault-mysecret-1527029447.01191
```

<span data-ttu-id="9b5d3-119">Questo comando recupera il segreto denominato MySecret dal vault della chiave denominato MyKeyVault e salva una copia di backup del segreto in un file denominato automaticamente e visualizza il nome del file.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-119">This command retrieves the secret named MySecret from the key vault named MyKeyVault and saves a backup of that secret to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="9b5d3-120">Esempio 2: Eseguire il backup di un segreto con un nome file specificato sovrascrivendo il file esistente senza chiedere conferma</span><span class="sxs-lookup"><span data-stu-id="9b5d3-120">Example 2: Back up a secret to a specified file name, overwriting the existing file without prompting</span></span>
```powershell
PS C:\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="9b5d3-121">Questo comando recupera il segreto denominato MySecret dalla chiave vault denominata MyKeyVault e salva una copia di backup del segreto in un file denominato Backup.BLOB.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-121">This command retrieves the secret named MySecret from the key vaultnamed MyKeyVault and saves a backup of that secret to a file named Backup.blob.</span></span>

### <span data-ttu-id="9b5d3-122">Esempio 3: Eseguire il backup di un segreto recuperato in precedenza con un nome file specificato</span><span class="sxs-lookup"><span data-stu-id="9b5d3-122">Example 3: Back up a secret previously retrieved to a specified file name</span></span>
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\> Backup-AzKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="9b5d3-123">Questo comando usa il nome $secret vault e il nome dell'oggetto per recuperare il segreto e salva il backup in un file denominato Backup.BLOB.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-123">This command uses the $secret object's vault name and name to retrieves the secret and saves its backup to a file named Backup.blob.</span></span>

## <span data-ttu-id="9b5d3-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b5d3-124">PARAMETERS</span></span>

### <span data-ttu-id="9b5d3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b5d3-125">-DefaultProfile</span></span>
<span data-ttu-id="9b5d3-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9b5d3-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9b5d3-127">-Force</span><span class="sxs-lookup"><span data-stu-id="9b5d3-127">-Force</span></span>
<span data-ttu-id="9b5d3-128">Chiede conferma prima di sovrascrivere il file di output, se presente.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-128">Prompts you for confirmation before overwriting the output file, if that exists.</span></span>

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

### <span data-ttu-id="9b5d3-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b5d3-129">-InputObject</span></span>
<span data-ttu-id="9b5d3-130">Segreto di cui eseguire il backup, pipelined in seguito all'output di una chiamata di recupero.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-130">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="9b5d3-131">-Name</span><span class="sxs-lookup"><span data-stu-id="9b5d3-131">-Name</span></span>
<span data-ttu-id="9b5d3-132">Specifica il nome del segreto di cui eseguire il backup.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-132">Specifies the name of the secret to back up.</span></span>

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

### <span data-ttu-id="9b5d3-133">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="9b5d3-133">-OutputFile</span></span>
<span data-ttu-id="9b5d3-134">Specifica il file di output in cui è archiviato il BLOB di backup.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-134">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="9b5d3-135">Se non si specifica questo parametro, questo cmdlet genera automaticamente un nome file.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-135">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="9b5d3-136">Se si specifica il nome di un file di output esistente, l'operazione non verrà completata e verrà restituito un messaggio di errore che indica che il file di backup esiste già.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-136">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="9b5d3-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9b5d3-137">-VaultName</span></span>
<span data-ttu-id="9b5d3-138">Specifica il nome del vault delle chiavi che contiene il segreto di cui eseguire il backup.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-138">Specifies the name of the key vault that contains the secret to back up.</span></span>

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

### <span data-ttu-id="9b5d3-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b5d3-139">-Confirm</span></span>
<span data-ttu-id="9b5d3-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b5d3-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b5d3-141">-WhatIf</span></span>
<span data-ttu-id="9b5d3-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b5d3-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b5d3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b5d3-144">CommonParameters</span></span>
<span data-ttu-id="9b5d3-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b5d3-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9b5d3-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b5d3-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="9b5d3-147">INPUTS</span></span>

### <span data-ttu-id="9b5d3-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="9b5d3-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="9b5d3-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9b5d3-149">OUTPUTS</span></span>

### <span data-ttu-id="9b5d3-150">System.String</span><span class="sxs-lookup"><span data-stu-id="9b5d3-150">System.String</span></span>

## <span data-ttu-id="9b5d3-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="9b5d3-151">NOTES</span></span>

## <span data-ttu-id="9b5d3-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9b5d3-152">RELATED LINKS</span></span>

[<span data-ttu-id="9b5d3-153">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="9b5d3-153">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="9b5d3-154">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="9b5d3-154">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="9b5d3-155">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="9b5d3-155">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="9b5d3-156">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="9b5d3-156">Restore-AzKeyVaultSecret</span></span>](./Restore-AzKeyVaultSecret.md)

