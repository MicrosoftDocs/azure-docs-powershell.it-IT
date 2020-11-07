---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: cd5e869b1f1d367002b33c5976434f16b22744e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674169"
---
# <span data-ttu-id="23f77-101">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="23f77-101">Backup-AzKeyVaultKey</span></span>

## <span data-ttu-id="23f77-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="23f77-102">SYNOPSIS</span></span>
<span data-ttu-id="23f77-103">Eseguire il backup di una chiave in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="23f77-103">Backs up a key in a key vault.</span></span>

## <span data-ttu-id="23f77-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="23f77-104">SYNTAX</span></span>

### <span data-ttu-id="23f77-105">ByKeyName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="23f77-105">ByKeyName (Default)</span></span>
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23f77-106">ByKey</span><span class="sxs-lookup"><span data-stu-id="23f77-106">ByKey</span></span>
```
Backup-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23f77-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23f77-107">DESCRIPTION</span></span>
<span data-ttu-id="23f77-108">Il cmdlet **backup-AzKeyVaultKey** consente di eseguire il download di una chiave specificata in un Vault chiave e di archiviarla in un file.</span><span class="sxs-lookup"><span data-stu-id="23f77-108">The **Backup-AzKeyVaultKey** cmdlet backs up a specified key in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="23f77-109">Se sono presenti più versioni della chiave, tutte le versioni verranno incluse nel backup.</span><span class="sxs-lookup"><span data-stu-id="23f77-109">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="23f77-110">Poiché il contenuto scaricato è crittografato, non può essere usato all'esterno dell'archivio di chiavi di Azure.</span><span class="sxs-lookup"><span data-stu-id="23f77-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="23f77-111">È possibile ripristinare una chiave di backup in qualsiasi volta chiave nell'abbonamento a cui è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="23f77-111">You can restore a backed-up key to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="23f77-112">I motivi tipici per usare questo cmdlet sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="23f77-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="23f77-113">Si vuole depositare una copia della chiave, in modo da avere una copia offline nel caso in cui si elimini accidentalmente la chiave in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="23f77-113">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your key vault.</span></span>
 
- <span data-ttu-id="23f77-114">È stata creata una chiave con Key Vault e ora si vuole clonare la chiave in un'altra area di Azure, in modo da poterla usare in tutte le istanze dell'applicazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="23f77-114">You created a key using Key Vault and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="23f77-115">Usa il cmdlet **backup-AzKeyVaultKey** per recuperare la chiave in formato crittografato e quindi usa il cmdlet Restore-AzKeyVaultKey e specifica un Vault chiave nella seconda area geografica.</span><span class="sxs-lookup"><span data-stu-id="23f77-115">Use the **Backup-AzKeyVaultKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzKeyVaultKey cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="23f77-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="23f77-116">EXAMPLES</span></span>

### <span data-ttu-id="23f77-117">Esempio 1: eseguire il backup di una chiave con un nome file generato automaticamente</span><span class="sxs-lookup"><span data-stu-id="23f77-117">Example 1: Back up a key with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'

C:\Users\username\mykeyvault-mykey-1527029447.01191
```

<span data-ttu-id="23f77-118">Questo comando Recupera la chiave denominata MyKey dal Vault chiave denominata MyKeyVault e salva una copia di backup di tale chiave in un file denominato automaticamente e visualizza il nome del file.</span><span class="sxs-lookup"><span data-stu-id="23f77-118">This command retrieves the key named MyKey from the key vault named MyKeyVault and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="23f77-119">Esempio 2: eseguire il backup di una chiave in un nome file specificato</span><span class="sxs-lookup"><span data-stu-id="23f77-119">Example 2: Back up a key to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="23f77-120">Questo comando Recupera la chiave denominata MyKey dalla chiave vaultnamed MyKeyVault e salva una copia di backup di tale chiave in un file denominato backup. blob.</span><span class="sxs-lookup"><span data-stu-id="23f77-120">This command retrieves the key named MyKey from the key vaultnamed MyKeyVault and saves a backup of that key to a file named Backup.blob.</span></span>

### <span data-ttu-id="23f77-121">Esempio 3: eseguire il backup di una chiave recuperata in precedenza in un nome file specificato, sovrascrivendo il file di destinazione senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="23f77-121">Example 3: Back up a previously retrieved key to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\> Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="23f77-122">Questo comando crea una copia di backup della chiave denominata $key. Nome nel Vault denominato $key. VAULTNAME in un file denominato backup. blob, sovrascrivendo automaticamente il file se esiste già.</span><span class="sxs-lookup"><span data-stu-id="23f77-122">This command creates a backup of the key named $key.Name in the vault named $key.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="23f77-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="23f77-123">PARAMETERS</span></span>

### <span data-ttu-id="23f77-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23f77-124">-DefaultProfile</span></span>
<span data-ttu-id="23f77-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="23f77-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23f77-126">-Force</span><span class="sxs-lookup"><span data-stu-id="23f77-126">-Force</span></span>
<span data-ttu-id="23f77-127">Sovrascrivere il file assegnato se esiste</span><span class="sxs-lookup"><span data-stu-id="23f77-127">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="23f77-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23f77-128">-InputObject</span></span>
<span data-ttu-id="23f77-129">Bundle chiave per eseguire il backup, tramite pipeline nell'output di una chiamata di recupero.</span><span class="sxs-lookup"><span data-stu-id="23f77-129">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByKey
Aliases: Key

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23f77-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="23f77-130">-Name</span></span>
<span data-ttu-id="23f77-131">Specifica il nome della chiave a cui eseguire il backup.</span><span class="sxs-lookup"><span data-stu-id="23f77-131">Specifies the name of the key to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23f77-132">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="23f77-132">-OutputFile</span></span>
<span data-ttu-id="23f77-133">Specifica il file di output in cui è archiviato il BLOB di backup.</span><span class="sxs-lookup"><span data-stu-id="23f77-133">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="23f77-134">Se non specifichi questo parametro, questo cmdlet genera un nome file.</span><span class="sxs-lookup"><span data-stu-id="23f77-134">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="23f77-135">Se specifichi il nome di un file di output esistente, l'operazione non verrà completata e restituirà un messaggio di errore che indica che il file di backup esiste già.</span><span class="sxs-lookup"><span data-stu-id="23f77-135">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="23f77-136">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="23f77-136">-VaultName</span></span>
<span data-ttu-id="23f77-137">Specifica il nome del Vault chiave che contiene la chiave per eseguire il backup.</span><span class="sxs-lookup"><span data-stu-id="23f77-137">Specifies the name of the key vault that contains the key to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23f77-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="23f77-138">-Confirm</span></span>
<span data-ttu-id="23f77-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23f77-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23f77-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23f77-140">-WhatIf</span></span>
<span data-ttu-id="23f77-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="23f77-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23f77-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="23f77-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23f77-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23f77-143">CommonParameters</span></span>
<span data-ttu-id="23f77-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23f77-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23f77-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23f77-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23f77-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="23f77-146">INPUTS</span></span>

### <span data-ttu-id="23f77-147">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="23f77-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="23f77-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="23f77-148">OUTPUTS</span></span>

### <span data-ttu-id="23f77-149">System. String</span><span class="sxs-lookup"><span data-stu-id="23f77-149">System.String</span></span>

## <span data-ttu-id="23f77-150">Note</span><span class="sxs-lookup"><span data-stu-id="23f77-150">NOTES</span></span>

## <span data-ttu-id="23f77-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="23f77-151">RELATED LINKS</span></span>

[<span data-ttu-id="23f77-152">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="23f77-152">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="23f77-153">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="23f77-153">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="23f77-154">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="23f77-154">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="23f77-155">Ripristinare-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="23f77-155">Restore-AzKeyVaultKey</span></span>](./Restore-AzKeyVaultKey.md)

