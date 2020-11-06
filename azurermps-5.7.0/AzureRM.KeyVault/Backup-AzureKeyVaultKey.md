---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultKey.md
ms.openlocfilehash: 2eecb6d4bb069b1578b3080c04de4c9df1e42f09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512576"
---
# <span data-ttu-id="ae5af-101">Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ae5af-101">Backup-AzureKeyVaultKey</span></span>

## <span data-ttu-id="ae5af-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ae5af-102">SYNOPSIS</span></span>
<span data-ttu-id="ae5af-103">Eseguire il backup di una chiave in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="ae5af-103">Backs up a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae5af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae5af-104">SYNTAX</span></span>

### <span data-ttu-id="ae5af-105">ByKeyName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ae5af-105">ByKeyName (Default)</span></span>
```
Backup-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae5af-106">ByKey</span><span class="sxs-lookup"><span data-stu-id="ae5af-106">ByKey</span></span>
```
Backup-AzureKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae5af-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae5af-107">DESCRIPTION</span></span>
<span data-ttu-id="ae5af-108">Il cmdlet **backup-AzureKeyVaultKey** consente di eseguire il download di una chiave specificata in un Vault chiave e di archiviarla in un file.</span><span class="sxs-lookup"><span data-stu-id="ae5af-108">The **Backup-AzureKeyVaultKey** cmdlet backs up a specified key in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="ae5af-109">Se sono presenti più versioni della chiave, tutte le versioni verranno incluse nel backup.</span><span class="sxs-lookup"><span data-stu-id="ae5af-109">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="ae5af-110">Poiché il contenuto scaricato è crittografato, non può essere usato all'esterno dell'archivio di chiavi di Azure.</span><span class="sxs-lookup"><span data-stu-id="ae5af-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="ae5af-111">È possibile ripristinare una chiave di backup in qualsiasi volta chiave nell'abbonamento a cui è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="ae5af-111">You can restore a backed-up key to any key vault in the subscription that it was backed up from.</span></span>

<span data-ttu-id="ae5af-112">I motivi tipici per usare questo cmdlet sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ae5af-112">Typical reasons to use this cmdlet are:</span></span> 

- <span data-ttu-id="ae5af-113">Si vuole depositare una copia della chiave, in modo da avere una copia offline nel caso in cui si elimini accidentalmente la chiave in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="ae5af-113">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your key vault.</span></span>
 
- <span data-ttu-id="ae5af-114">È stata creata una chiave con Key Vault e ora si vuole clonare la chiave in un'altra area di Azure, in modo da poterla usare in tutte le istanze dell'applicazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="ae5af-114">You created a key using Key Vault and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="ae5af-115">Usa il cmdlet **backup-AzureKeyVaultKey** per recuperare la chiave in formato crittografato e quindi usa il cmdlet Restore-AzureKeyVaultKey e specifica un Vault chiave nella seconda area geografica.</span><span class="sxs-lookup"><span data-stu-id="ae5af-115">Use the **Backup-AzureKeyVaultKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzureKeyVaultKey cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="ae5af-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae5af-116">EXAMPLES</span></span>

### <span data-ttu-id="ae5af-117">Esempio 1: eseguire il backup di una chiave con un nome file generato automaticamente</span><span class="sxs-lookup"><span data-stu-id="ae5af-117">Example 1: Back up a key with an automatically generated file name</span></span>
```
PS C:\>Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="ae5af-118">Questo comando Recupera la chiave denominata MyKey dal Vault chiave denominata MyKeyVault e salva una copia di backup di tale chiave in un file denominato automaticamente e visualizza il nome del file.</span><span class="sxs-lookup"><span data-stu-id="ae5af-118">This command retrieves the key named MyKey from the key vault named MyKeyVault and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="ae5af-119">Esempio 2: eseguire il backup di una chiave in un nome file specificato</span><span class="sxs-lookup"><span data-stu-id="ae5af-119">Example 2: Back up a key to a specified file name</span></span>
```
PS C:\>Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'
```

<span data-ttu-id="ae5af-120">Questo comando Recupera la chiave denominata MyKey dalla chiave vaultnamed MyKeyVault e salva una copia di backup di tale chiave in un file denominato backup. blob.</span><span class="sxs-lookup"><span data-stu-id="ae5af-120">This command retrieves the key named MyKey from the key vaultnamed MyKeyVault and saves a backup of that key to a file named Backup.blob.</span></span>

### <span data-ttu-id="ae5af-121">Esempio 3: eseguire il backup di una chiave recuperata in precedenza in un nome file specificato, sovrascrivendo il file di destinazione senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="ae5af-121">Example 3: Back up a previously retrieved key to a specified file name, overwriting the destination file without prompting.</span></span>
```
PS C:\>$key = Get-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\>Backup-AzureKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force
```

<span data-ttu-id="ae5af-122">Questo comando crea una copia di backup della chiave denominata $key. Nome nel Vault denominato $key. VAULTNAME in un file denominato backup. blob, sovrascrivendo automaticamente il file se esiste già.</span><span class="sxs-lookup"><span data-stu-id="ae5af-122">This command creates a backup of the key named $key.Name in the vault named $key.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="ae5af-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ae5af-123">PARAMETERS</span></span>

### <span data-ttu-id="ae5af-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae5af-124">-DefaultProfile</span></span>
<span data-ttu-id="ae5af-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ae5af-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae5af-126">-Force</span><span class="sxs-lookup"><span data-stu-id="ae5af-126">-Force</span></span>
<span data-ttu-id="ae5af-127">Sovrascrivere il file assegnato se esiste</span><span class="sxs-lookup"><span data-stu-id="ae5af-127">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="ae5af-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae5af-128">-InputObject</span></span>
<span data-ttu-id="ae5af-129">Bundle chiave per eseguire il backup, tramite pipeline nell'output di una chiamata di recupero.</span><span class="sxs-lookup"><span data-stu-id="ae5af-129">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: PSKeyVaultKeyIdentityItem
Parameter Sets: ByKey
Aliases: Key

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae5af-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae5af-130">-Name</span></span>
<span data-ttu-id="ae5af-131">Specifica il nome della chiave a cui eseguire il backup.</span><span class="sxs-lookup"><span data-stu-id="ae5af-131">Specifies the name of the key to back up.</span></span>

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

### <span data-ttu-id="ae5af-132">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="ae5af-132">-OutputFile</span></span>
<span data-ttu-id="ae5af-133">Specifica il file di output in cui è archiviato il BLOB di backup.</span><span class="sxs-lookup"><span data-stu-id="ae5af-133">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="ae5af-134">Se non specifichi questo parametro, questo cmdlet genera un nome file.</span><span class="sxs-lookup"><span data-stu-id="ae5af-134">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="ae5af-135">Se specifichi il nome di un file di output esistente, l'operazione non verrà completata e restituirà un messaggio di errore che indica che il file di backup esiste già.</span><span class="sxs-lookup"><span data-stu-id="ae5af-135">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="ae5af-136">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="ae5af-136">-VaultName</span></span>
<span data-ttu-id="ae5af-137">Specifica il nome del Vault chiave che contiene la chiave per eseguire il backup.</span><span class="sxs-lookup"><span data-stu-id="ae5af-137">Specifies the name of the key vault that contains the key to back up.</span></span>

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

### <span data-ttu-id="ae5af-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ae5af-138">-Confirm</span></span>
<span data-ttu-id="ae5af-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae5af-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae5af-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae5af-140">-WhatIf</span></span>
<span data-ttu-id="ae5af-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae5af-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae5af-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae5af-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae5af-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae5af-143">CommonParameters</span></span>
<span data-ttu-id="ae5af-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae5af-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae5af-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae5af-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae5af-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ae5af-146">INPUTS</span></span>

### <span data-ttu-id="ae5af-147">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ae5af-147">None</span></span>
<span data-ttu-id="ae5af-148">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="ae5af-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ae5af-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae5af-149">OUTPUTS</span></span>

### <span data-ttu-id="ae5af-150">Stringa</span><span class="sxs-lookup"><span data-stu-id="ae5af-150">String</span></span>
<span data-ttu-id="ae5af-151">Il cmdlet restituisce il percorso del file di output contenente il backup della chiave.</span><span class="sxs-lookup"><span data-stu-id="ae5af-151">The cmdlet returns the path of the output file containing the backup of the key.</span></span>

## <span data-ttu-id="ae5af-152">Note</span><span class="sxs-lookup"><span data-stu-id="ae5af-152">NOTES</span></span>

## <span data-ttu-id="ae5af-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae5af-153">RELATED LINKS</span></span>

[<span data-ttu-id="ae5af-154">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ae5af-154">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="ae5af-155">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ae5af-155">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="ae5af-156">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ae5af-156">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="ae5af-157">Ripristinare-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ae5af-157">Restore-AzureKeyVaultKey</span></span>](./Restore-AzureKeyVaultKey.md)
