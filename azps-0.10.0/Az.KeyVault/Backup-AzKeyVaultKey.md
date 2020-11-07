---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/backup-AzKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: d5fce3a4c70593b9478c0efa8afef29021797bb3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861326"
---
# <span data-ttu-id="bbfd3-101">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bbfd3-101">Backup-AzKeyVaultKey</span></span>

## <span data-ttu-id="bbfd3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bbfd3-102">SYNOPSIS</span></span>
<span data-ttu-id="bbfd3-103">Eseguire il backup di una chiave in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="bbfd3-103">Backs up a key in a key vault.</span></span>

## <span data-ttu-id="bbfd3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bbfd3-104">SYNTAX</span></span>

### <span data-ttu-id="bbfd3-105">ByKeyName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bbfd3-105">ByKeyName (Default)</span></span>
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbfd3-106">ByKey</span><span class="sxs-lookup"><span data-stu-id="bbfd3-106">ByKey</span></span>
```
Backup-AzKeyVaultKey [-Key] <KeyBundle> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbfd3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bbfd3-107">DESCRIPTION</span></span>
<span data-ttu-id="bbfd3-108">Il cmdlet **backup-AzKeyVaultKey** consente di eseguire il download di una chiave specificata in un Vault chiave e di archiviarla in un file.</span><span class="sxs-lookup"><span data-stu-id="bbfd3-108">The **Backup-AzKeyVaultKey** cmdlet backs up a specified key in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="bbfd3-109">Se sono presenti più versioni della chiave, tutte le versioni verranno incluse nel backup.</span><span class="sxs-lookup"><span data-stu-id="bbfd3-109">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="bbfd3-110">Poiché il contenuto scaricato è crittografato, non può essere usato all'esterno dell'archivio di chiavi di Azure.</span><span class="sxs-lookup"><span data-stu-id="bbfd3-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="bbfd3-111">È possibile ripristinare una chiave di backup in qualsiasi volta chiave nell'abbonamento a cui è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="bbfd3-111">You can restore a backed-up key to any key vault in the subscription that it was backed up from.</span></span>

<span data-ttu-id="bbfd3-112">I motivi tipici per usare questo cmdlet sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="bbfd3-112">Typical reasons to use this cmdlet are:</span></span> 

- <span data-ttu-id="bbfd3-113">Si vuole depositare una copia della chiave, in modo da avere una copia offline nel caso in cui si elimini accidentalmente la chiave in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="bbfd3-113">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your key vault.</span></span>
 
- <span data-ttu-id="bbfd3-114">È stata creata una chiave con Key Vault e ora si vuole clonare la chiave in un'altra area di Azure, in modo da poterla usare in tutte le istanze dell'applicazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="bbfd3-114">You created a key using Key Vault and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="bbfd3-115">Usa il cmdlet **backup-AzKeyVaultKey** per recuperare la chiave in formato crittografato e quindi usa il cmdlet Restore-AzKeyVaultKey e specifica un Vault chiave nella seconda area geografica.</span><span class="sxs-lookup"><span data-stu-id="bbfd3-115">Use the **Backup-AzKeyVaultKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzKeyVaultKey cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="bbfd3-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bbfd3-116">EXAMPLES</span></span>

### <span data-ttu-id="bbfd3-117">Esempio 1: eseguire il backup di una chiave con un nome file generato automaticamente</span><span class="sxs-lookup"><span data-stu-id="bbfd3-117">Example 1: Back up a key with an automatically generated file name</span></span>
```
PS C:\>Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="bbfd3-118">Questo comando Recupera la chiave denominata MyKey dal Vault chiave denominata MyKeyVault e salva una copia di backup di tale chiave in un file denominato automaticamente e visualizza il nome del file.</span><span class="sxs-lookup"><span data-stu-id="bbfd3-118">This command retrieves the key named MyKey from the key vault named MyKeyVault and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="bbfd3-119">Esempio 2: eseguire il backup di una chiave in un nome file specificato</span><span class="sxs-lookup"><span data-stu-id="bbfd3-119">Example 2: Back up a key to a specified file name</span></span>
```
PS C:\>Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'
```

<span data-ttu-id="bbfd3-120">Questo comando Recupera la chiave denominata MyKey dalla chiave vaultnamed MyKeyVault e salva una copia di backup di tale chiave in un file denominato backup. blob.</span><span class="sxs-lookup"><span data-stu-id="bbfd3-120">This command retrieves the key named MyKey from the key vaultnamed MyKeyVault and saves a backup of that key to a file named Backup.blob.</span></span>

### <span data-ttu-id="bbfd3-121">Esempio 3: eseguire il backup di una chiave recuperata in precedenza in un nome file specificato, sovrascrivendo il file di destinazione senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="bbfd3-121">Example 3: Back up a previously retrieved key to a specified file name, overwriting the destination file without prompting.</span></span>
```
PS C:\>$key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\>Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force
```

<span data-ttu-id="bbfd3-122">Questo comando crea una copia di backup della chiave denominata $key. Nome nel Vault denominato $key. VAULTNAME in un file denominato backup. blob, sovrascrivendo automaticamente il file se esiste già.</span><span class="sxs-lookup"><span data-stu-id="bbfd3-122">This command creates a backup of the key named $key.Name in the vault named $key.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="bbfd3-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bbfd3-123">PARAMETERS</span></span>

### <span data-ttu-id="bbfd3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbfd3-124">-DefaultProfile</span></span>
<span data-ttu-id="bbfd3-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="bbfd3-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bbfd3-126">-Force</span><span class="sxs-lookup"><span data-stu-id="bbfd3-126">-Force</span></span>
<span data-ttu-id="bbfd3-127">Sovrascrivere il file assegnato se esiste</span><span class="sxs-lookup"><span data-stu-id="bbfd3-127">Overwrite the given file if it exists</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbfd3-128">-Key</span><span class="sxs-lookup"><span data-stu-id="bbfd3-128">-Key</span></span>
<span data-ttu-id="bbfd3-129">Specifica una chiave recuperata in precedenza di cui eseguire il backup.</span><span class="sxs-lookup"><span data-stu-id="bbfd3-129">Specifies a previously retrieved key which is to be backed up.</span></span>

```yaml
Type: KeyBundle
Parameter Sets: ByKey
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbfd3-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="bbfd3-130">-Name</span></span>
<span data-ttu-id="bbfd3-131">Specifica il nome della chiave a cui eseguire il backup.</span><span class="sxs-lookup"><span data-stu-id="bbfd3-131">Specifies the name of the key to back up.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbfd3-132">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="bbfd3-132">-OutputFile</span></span>
<span data-ttu-id="bbfd3-133">Specifica il file di output in cui è archiviato il BLOB di backup.</span><span class="sxs-lookup"><span data-stu-id="bbfd3-133">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="bbfd3-134">Se non specifichi questo parametro, questo cmdlet genera un nome file.</span><span class="sxs-lookup"><span data-stu-id="bbfd3-134">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="bbfd3-135">Se specifichi il nome di un file di output esistente, l'operazione non verrà completata e restituirà un messaggio di errore che indica che il file di backup esiste già.</span><span class="sxs-lookup"><span data-stu-id="bbfd3-135">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="bbfd3-136">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="bbfd3-136">-VaultName</span></span>
<span data-ttu-id="bbfd3-137">Specifica il nome del Vault chiave che contiene la chiave per eseguire il backup.</span><span class="sxs-lookup"><span data-stu-id="bbfd3-137">Specifies the name of the key vault that contains the key to back up.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bbfd3-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bbfd3-138">-Confirm</span></span>
<span data-ttu-id="bbfd3-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bbfd3-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbfd3-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbfd3-140">-WhatIf</span></span>
<span data-ttu-id="bbfd3-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bbfd3-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbfd3-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bbfd3-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbfd3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbfd3-143">CommonParameters</span></span>
<span data-ttu-id="bbfd3-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbfd3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbfd3-145">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbfd3-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbfd3-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bbfd3-146">INPUTS</span></span>

### <span data-ttu-id="bbfd3-147">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bbfd3-147">None</span></span>
<span data-ttu-id="bbfd3-148">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="bbfd3-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bbfd3-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bbfd3-149">OUTPUTS</span></span>

### <span data-ttu-id="bbfd3-150">Stringa</span><span class="sxs-lookup"><span data-stu-id="bbfd3-150">String</span></span>
<span data-ttu-id="bbfd3-151">Il cmdlet restituisce il percorso del file di output contenente il backup della chiave.</span><span class="sxs-lookup"><span data-stu-id="bbfd3-151">The cmdlet returns the path of the output file containing the backup of the key.</span></span>

## <span data-ttu-id="bbfd3-152">Note</span><span class="sxs-lookup"><span data-stu-id="bbfd3-152">NOTES</span></span>

## <span data-ttu-id="bbfd3-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bbfd3-153">RELATED LINKS</span></span>

[<span data-ttu-id="bbfd3-154">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bbfd3-154">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="bbfd3-155">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bbfd3-155">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="bbfd3-156">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bbfd3-156">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="bbfd3-157">Ripristinare-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="bbfd3-157">Restore-AzKeyVaultKey</span></span>](./Restore-AzKeyVaultKey.md)

