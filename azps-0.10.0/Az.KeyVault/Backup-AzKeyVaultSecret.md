---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/backup-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
ms.openlocfilehash: b1f26123579589c15ac4eff6b577706270a7e15a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861325"
---
# <span data-ttu-id="84859-101">Backup-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="84859-101">Backup-AzKeyVaultSecret</span></span>

## <span data-ttu-id="84859-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="84859-102">SYNOPSIS</span></span>
<span data-ttu-id="84859-103">Eseguire il backup di un segreto in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="84859-103">Backs up a secret in a key vault.</span></span>

## <span data-ttu-id="84859-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84859-104">SYNTAX</span></span>

### <span data-ttu-id="84859-105">BySecretName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="84859-105">BySecretName (Default)</span></span>
```
Backup-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84859-106">BySecret</span><span class="sxs-lookup"><span data-stu-id="84859-106">BySecret</span></span>
```
Backup-AzKeyVaultSecret [-Secret] <Secret> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84859-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84859-107">DESCRIPTION</span></span>
<span data-ttu-id="84859-108">Il cmdlet **backup-AzKeyVaultSecret** consente di eseguire il backup di un segreto specificato in un caveau chiave, scaricarlo e archiviarlo in un file.</span><span class="sxs-lookup"><span data-stu-id="84859-108">The **Backup-AzKeyVaultSecret** cmdlet backs up a specified secret in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="84859-109">Se sono presenti più versioni del segreto, tutte le versioni sono incluse nel backup.</span><span class="sxs-lookup"><span data-stu-id="84859-109">If there are multiple versions of the secret, all versions are included in the backup.</span></span>
<span data-ttu-id="84859-110">Poiché il contenuto scaricato è crittografato, non può essere usato all'esterno dell'archivio di chiavi di Azure.</span><span class="sxs-lookup"><span data-stu-id="84859-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="84859-111">È possibile ripristinare un segreto di backup in qualsiasi volta chiave nell'abbonamento a cui è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="84859-111">You can restore a backed-up secret to any key vault in the subscription that it was backed up from.</span></span>

<span data-ttu-id="84859-112">I motivi tipici per usare questo cmdlet sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="84859-112">Typical reasons to use this cmdlet are:</span></span>

- <span data-ttu-id="84859-113">Si vuole depositare una copia del segreto, in modo da avere una copia offline nel caso in cui si elimini accidentalmente il segreto nel caveau della chiave.</span><span class="sxs-lookup"><span data-stu-id="84859-113">You want to escrow a copy of your secret, so that you have an offline copy in case you accidentally delete your secret in your key vault.</span></span>
- <span data-ttu-id="84859-114">È stato aggiunto un segreto a un Vault chiave e ora si vuole clonare il segreto in un'area di Azure diversa, in modo da poterlo usare in tutte le istanze dell'applicazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="84859-114">You added a secret to a key vault and now want to clone the secret into a different Azure region, so that you can use it from all instances of your distributed application.</span></span> <span data-ttu-id="84859-115">Usa il cmdlet Backup-AzKeyVaultSecret per recuperare il segreto in formato crittografato e quindi usa il cmdlet Restore-AzKeyVaultSecret e specifica un Vault chiave nella seconda area.</span><span class="sxs-lookup"><span data-stu-id="84859-115">Use the Backup-AzKeyVaultSecret cmdlet to retrieve the secret in encrypted format and then use the Restore-AzKeyVaultSecret cmdlet and specify a key vault in the second region.</span></span> <span data-ttu-id="84859-116">Tieni presente che le aree geografiche devono appartenere alla stessa geografia.</span><span class="sxs-lookup"><span data-stu-id="84859-116">(Note that the regions must belong to the same geography.)</span></span>

## <span data-ttu-id="84859-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84859-117">EXAMPLES</span></span>

### <span data-ttu-id="84859-118">Esempio 1: eseguire il backup di un segreto con un nome file generato automaticamente</span><span class="sxs-lookup"><span data-stu-id="84859-118">Example 1: Back up a secret with an automatically generated file name</span></span>
```
PS C:\>Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="84859-119">Questo comando Recupera il segreto di nome segreto dal caveau della chiave denominato MyKeyVault e salva una copia di backup di tale segreto in un file denominato automaticamente e visualizza il nome del file.</span><span class="sxs-lookup"><span data-stu-id="84859-119">This command retrieves the secret named MySecret from the key vault named MyKeyVault and saves a backup of that secret to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="84859-120">Esempio 2: eseguire il backup di un segreto in un nome file specificato, sovrascrivendo il file esistente senza richiedere conferma</span><span class="sxs-lookup"><span data-stu-id="84859-120">Example 2: Back up a secret to a specified file name, overwriting the existing file without prompting</span></span>
```
PS C:\>Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force
```

<span data-ttu-id="84859-121">Questo comando Recupera il segreto di nome segreto dalla chiave vaultnamed MyKeyVault e salva una copia di backup di tale segreto in un file denominato backup. blob.</span><span class="sxs-lookup"><span data-stu-id="84859-121">This command retrieves the secret named MySecret from the key vaultnamed MyKeyVault and saves a backup of that secret to a file named Backup.blob.</span></span>

### <span data-ttu-id="84859-122">Esempio 3: eseguire il backup di un segreto recuperato in precedenza in un nome file specificato</span><span class="sxs-lookup"><span data-stu-id="84859-122">Example 3: Back up a secret previously retrieved to a specified file name</span></span>
```
PS C:\>$secret = Get-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\>Backup-AzKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'
```

<span data-ttu-id="84859-123">Questo comando usa il nome e il nome del Vault dell'oggetto $secret per recuperare il segreto e salva il backup in un file denominato backup. blob.</span><span class="sxs-lookup"><span data-stu-id="84859-123">This command uses the $secret object's vault name and name to retrieves the secret and saves its backup to a file named Backup.blob.</span></span>

## <span data-ttu-id="84859-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="84859-124">PARAMETERS</span></span>

### <span data-ttu-id="84859-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84859-125">-DefaultProfile</span></span>
<span data-ttu-id="84859-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="84859-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84859-127">-Force</span><span class="sxs-lookup"><span data-stu-id="84859-127">-Force</span></span>
<span data-ttu-id="84859-128">Richiede la conferma prima di sovrascrivere il file di output, se esistente.</span><span class="sxs-lookup"><span data-stu-id="84859-128">Prompts you for confirmation before overwriting the output file, if that exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84859-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="84859-129">-Name</span></span>
<span data-ttu-id="84859-130">Specifica il nome del segreto a cui eseguire il backup.</span><span class="sxs-lookup"><span data-stu-id="84859-130">Specifies the name of the secret to back up.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84859-131">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="84859-131">-OutputFile</span></span>
<span data-ttu-id="84859-132">Specifica il file di output in cui è archiviato il BLOB di backup.</span><span class="sxs-lookup"><span data-stu-id="84859-132">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="84859-133">Se non specifichi questo parametro, questo cmdlet genera un nome file.</span><span class="sxs-lookup"><span data-stu-id="84859-133">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="84859-134">Se specifichi il nome di un file di output esistente, l'operazione non verrà completata e restituirà un messaggio di errore che indica che il file di backup esiste già.</span><span class="sxs-lookup"><span data-stu-id="84859-134">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84859-135">-Segreto</span><span class="sxs-lookup"><span data-stu-id="84859-135">-Secret</span></span>
<span data-ttu-id="84859-136">Specifica l'oggetto di cui deve essere usato il nome e il Vault per l'operazione di backup.</span><span class="sxs-lookup"><span data-stu-id="84859-136">Specifies the object whose name and vault should be used for the backup operation.</span></span>

```yaml
Type: Secret
Parameter Sets: BySecret
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84859-137">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="84859-137">-VaultName</span></span>
<span data-ttu-id="84859-138">Specifica il nome del Vault chiave che contiene il segreto di cui eseguire il backup.</span><span class="sxs-lookup"><span data-stu-id="84859-138">Specifies the name of the key vault that contains the secret to back up.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84859-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="84859-139">-Confirm</span></span>
<span data-ttu-id="84859-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84859-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84859-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84859-141">-WhatIf</span></span>
<span data-ttu-id="84859-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84859-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84859-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="84859-143">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84859-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84859-144">CommonParameters</span></span>
<span data-ttu-id="84859-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84859-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84859-146">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84859-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84859-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="84859-147">INPUTS</span></span>

### <span data-ttu-id="84859-148">Nessuno</span><span class="sxs-lookup"><span data-stu-id="84859-148">None</span></span>
<span data-ttu-id="84859-149">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="84859-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="84859-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84859-150">OUTPUTS</span></span>

### <span data-ttu-id="84859-151">Stringa</span><span class="sxs-lookup"><span data-stu-id="84859-151">String</span></span>
<span data-ttu-id="84859-152">Il cmdlet restituisce il percorso del file di output contenente il backup della chiave.</span><span class="sxs-lookup"><span data-stu-id="84859-152">The cmdlet returns the path of the output file containing the backup of the key.</span></span>

## <span data-ttu-id="84859-153">Note</span><span class="sxs-lookup"><span data-stu-id="84859-153">NOTES</span></span>

## <span data-ttu-id="84859-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84859-154">RELATED LINKS</span></span>

[<span data-ttu-id="84859-155">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="84859-155">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="84859-156">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="84859-156">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="84859-157">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="84859-157">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="84859-158">Ripristinare-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="84859-158">Restore-AzKeyVaultSecret</span></span>](./Restore-AzKeyVaultSecret.md)

