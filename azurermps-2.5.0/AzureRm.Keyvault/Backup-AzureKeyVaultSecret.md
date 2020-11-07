---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultsecret
schema: 2.0.0
ms.openlocfilehash: cd83d61c64e4111faf7fc6149107e172d0cf0c9f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865810"
---
# <span data-ttu-id="34e1f-101">Backup-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="34e1f-101">Backup-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="34e1f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="34e1f-102">SYNOPSIS</span></span>
<span data-ttu-id="34e1f-103">Eseguire il backup di un segreto in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="34e1f-103">Backs up a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34e1f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34e1f-104">SYNTAX</span></span>

### <span data-ttu-id="34e1f-105">BySecretName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="34e1f-105">BySecretName (Default)</span></span>
```
Backup-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34e1f-106">BySecret</span><span class="sxs-lookup"><span data-stu-id="34e1f-106">BySecret</span></span>
```
Backup-AzureKeyVaultSecret [-Secret] <Secret> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34e1f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34e1f-107">DESCRIPTION</span></span>
<span data-ttu-id="34e1f-108">Il cmdlet **backup-AzureKeyVaultSecret** consente di eseguire il backup di un segreto specificato in un caveau chiave, scaricarlo e archiviarlo in un file.</span><span class="sxs-lookup"><span data-stu-id="34e1f-108">The **Backup-AzureKeyVaultSecret** cmdlet backs up a specified secret in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="34e1f-109">Se sono presenti più versioni del segreto, tutte le versioni sono incluse nel backup.</span><span class="sxs-lookup"><span data-stu-id="34e1f-109">If there are multiple versions of the secret, all versions are included in the backup.</span></span>
<span data-ttu-id="34e1f-110">Poiché il contenuto scaricato è crittografato, non può essere usato all'esterno dell'archivio di chiavi di Azure.</span><span class="sxs-lookup"><span data-stu-id="34e1f-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="34e1f-111">È possibile ripristinare un segreto di backup in qualsiasi volta chiave nell'abbonamento a cui è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="34e1f-111">You can restore a backed-up secret to any key vault in the subscription that it was backed up from.</span></span>

<span data-ttu-id="34e1f-112">I motivi tipici per usare questo cmdlet sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="34e1f-112">Typical reasons to use this cmdlet are:</span></span>

- <span data-ttu-id="34e1f-113">Si vuole depositare una copia del segreto, in modo da avere una copia offline nel caso in cui si elimini accidentalmente il segreto nel caveau della chiave.</span><span class="sxs-lookup"><span data-stu-id="34e1f-113">You want to escrow a copy of your secret, so that you have an offline copy in case you accidentally delete your secret in your key vault.</span></span>
- <span data-ttu-id="34e1f-114">È stato aggiunto un segreto a un Vault chiave e ora si vuole clonare il segreto in un'area di Azure diversa, in modo da poterlo usare in tutte le istanze dell'applicazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="34e1f-114">You added a secret to a key vault and now want to clone the secret into a different Azure region, so that you can use it from all instances of your distributed application.</span></span> <span data-ttu-id="34e1f-115">Usa il cmdlet Backup-AzureKeyVaultSecret per recuperare il segreto in formato crittografato e quindi usa il cmdlet Restore-AzureKeyVaultSecret e specifica un Vault chiave nella seconda area.</span><span class="sxs-lookup"><span data-stu-id="34e1f-115">Use the Backup-AzureKeyVaultSecret cmdlet to retrieve the secret in encrypted format and then use the Restore-AzureKeyVaultSecret cmdlet and specify a key vault in the second region.</span></span> <span data-ttu-id="34e1f-116">Tieni presente che le aree geografiche devono appartenere alla stessa geografia.</span><span class="sxs-lookup"><span data-stu-id="34e1f-116">(Note that the regions must belong to the same geography.)</span></span>

## <span data-ttu-id="34e1f-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34e1f-117">EXAMPLES</span></span>

### <span data-ttu-id="34e1f-118">Esempio 1: eseguire il backup di un segreto con un nome file generato automaticamente</span><span class="sxs-lookup"><span data-stu-id="34e1f-118">Example 1: Back up a secret with an automatically generated file name</span></span>
```
PS C:\>Backup-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="34e1f-119">Questo comando Recupera il segreto di nome segreto dal caveau della chiave denominato MyKeyVault e salva una copia di backup di tale segreto in un file denominato automaticamente e visualizza il nome del file.</span><span class="sxs-lookup"><span data-stu-id="34e1f-119">This command retrieves the secret named MySecret from the key vault named MyKeyVault and saves a backup of that secret to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="34e1f-120">Esempio 2: eseguire il backup di un segreto in un nome file specificato, sovrascrivendo il file esistente senza richiedere conferma</span><span class="sxs-lookup"><span data-stu-id="34e1f-120">Example 2: Back up a secret to a specified file name, overwriting the existing file without prompting</span></span>
```
PS C:\>Backup-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force
```

<span data-ttu-id="34e1f-121">Questo comando Recupera il segreto di nome segreto dalla chiave vaultnamed MyKeyVault e salva una copia di backup di tale segreto in un file denominato backup. blob.</span><span class="sxs-lookup"><span data-stu-id="34e1f-121">This command retrieves the secret named MySecret from the key vaultnamed MyKeyVault and saves a backup of that secret to a file named Backup.blob.</span></span>

### <span data-ttu-id="34e1f-122">Esempio 3: eseguire il backup di un segreto recuperato in precedenza in un nome file specificato</span><span class="sxs-lookup"><span data-stu-id="34e1f-122">Example 3: Back up a secret previously retrieved to a specified file name</span></span>
```
PS C:\>$secret = Get-AzureKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\>Backup-AzureKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'
```

<span data-ttu-id="34e1f-123">Questo comando usa il nome e il nome del Vault dell'oggetto $secret per recuperare il segreto e salva il backup in un file denominato backup. blob.</span><span class="sxs-lookup"><span data-stu-id="34e1f-123">This command uses the $secret object's vault name and name to retrieves the secret and saves its backup to a file named Backup.blob.</span></span>

## <span data-ttu-id="34e1f-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="34e1f-124">PARAMETERS</span></span>

### <span data-ttu-id="34e1f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34e1f-125">-DefaultProfile</span></span>
<span data-ttu-id="34e1f-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="34e1f-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34e1f-127">-Force</span><span class="sxs-lookup"><span data-stu-id="34e1f-127">-Force</span></span>
<span data-ttu-id="34e1f-128">Richiede la conferma prima di sovrascrivere il file di output, se esistente.</span><span class="sxs-lookup"><span data-stu-id="34e1f-128">Prompts you for confirmation before overwriting the output file, if that exists.</span></span>

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

### <span data-ttu-id="34e1f-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="34e1f-129">-Name</span></span>
<span data-ttu-id="34e1f-130">Specifica il nome del segreto a cui eseguire il backup.</span><span class="sxs-lookup"><span data-stu-id="34e1f-130">Specifies the name of the secret to back up.</span></span>

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

### <span data-ttu-id="34e1f-131">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="34e1f-131">-OutputFile</span></span>
<span data-ttu-id="34e1f-132">Specifica il file di output in cui è archiviato il BLOB di backup.</span><span class="sxs-lookup"><span data-stu-id="34e1f-132">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="34e1f-133">Se non specifichi questo parametro, questo cmdlet genera un nome file.</span><span class="sxs-lookup"><span data-stu-id="34e1f-133">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="34e1f-134">Se specifichi il nome di un file di output esistente, l'operazione non verrà completata e restituirà un messaggio di errore che indica che il file di backup esiste già.</span><span class="sxs-lookup"><span data-stu-id="34e1f-134">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="34e1f-135">-Segreto</span><span class="sxs-lookup"><span data-stu-id="34e1f-135">-Secret</span></span>
<span data-ttu-id="34e1f-136">Specifica l'oggetto di cui deve essere usato il nome e il Vault per l'operazione di backup.</span><span class="sxs-lookup"><span data-stu-id="34e1f-136">Specifies the object whose name and vault should be used for the backup operation.</span></span>

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

### <span data-ttu-id="34e1f-137">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="34e1f-137">-VaultName</span></span>
<span data-ttu-id="34e1f-138">Specifica il nome del Vault chiave che contiene il segreto di cui eseguire il backup.</span><span class="sxs-lookup"><span data-stu-id="34e1f-138">Specifies the name of the key vault that contains the secret to back up.</span></span>

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

### <span data-ttu-id="34e1f-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="34e1f-139">-Confirm</span></span>
<span data-ttu-id="34e1f-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34e1f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34e1f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34e1f-141">-WhatIf</span></span>
<span data-ttu-id="34e1f-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34e1f-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34e1f-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34e1f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34e1f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34e1f-144">CommonParameters</span></span>
<span data-ttu-id="34e1f-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34e1f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34e1f-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34e1f-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34e1f-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="34e1f-147">INPUTS</span></span>

## <span data-ttu-id="34e1f-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34e1f-148">OUTPUTS</span></span>

### <span data-ttu-id="34e1f-149">Stringa</span><span class="sxs-lookup"><span data-stu-id="34e1f-149">String</span></span>
<span data-ttu-id="34e1f-150">Il cmdlet restituisce il percorso del file di output contenente il backup della chiave.</span><span class="sxs-lookup"><span data-stu-id="34e1f-150">The cmdlet returns the path of the output file containing the backup of the key.</span></span>

## <span data-ttu-id="34e1f-151">Note</span><span class="sxs-lookup"><span data-stu-id="34e1f-151">NOTES</span></span>

## <span data-ttu-id="34e1f-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34e1f-152">RELATED LINKS</span></span>

[<span data-ttu-id="34e1f-153">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="34e1f-153">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="34e1f-154">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="34e1f-154">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="34e1f-155">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="34e1f-155">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="34e1f-156">Ripristinare-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="34e1f-156">Restore-AzureKeyVaultSecret</span></span>](./Restore-AzureKeyVaultSecret.md)

