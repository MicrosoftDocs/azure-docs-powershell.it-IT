---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: 88decaffa736f015b8e65aa1217eab4899b07c7c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351931"
---
# <span data-ttu-id="34bb0-101">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="34bb0-101">Backup-AzKeyVaultKey</span></span>

## <span data-ttu-id="34bb0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="34bb0-102">SYNOPSIS</span></span>
<span data-ttu-id="34bb0-103">Eseguire il backup di una chiave in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="34bb0-103">Backs up a key in a key vault.</span></span>

## <span data-ttu-id="34bb0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34bb0-104">SYNTAX</span></span>

### <span data-ttu-id="34bb0-105">ByKeyName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="34bb0-105">ByKeyName (Default)</span></span>
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34bb0-106">HsmByKeyName</span><span class="sxs-lookup"><span data-stu-id="34bb0-106">HsmByKeyName</span></span>
```
Backup-AzKeyVaultKey -HsmName <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34bb0-107">ByKey</span><span class="sxs-lookup"><span data-stu-id="34bb0-107">ByKey</span></span>
```
Backup-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34bb0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34bb0-108">DESCRIPTION</span></span>
<span data-ttu-id="34bb0-109">Il cmdlet **backup-AzKeyVaultKey** consente di eseguire il download di una chiave specificata in un Vault chiave e di archiviarla in un file.</span><span class="sxs-lookup"><span data-stu-id="34bb0-109">The **Backup-AzKeyVaultKey** cmdlet backs up a specified key in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="34bb0-110">Se sono presenti più versioni della chiave, tutte le versioni verranno incluse nel backup.</span><span class="sxs-lookup"><span data-stu-id="34bb0-110">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="34bb0-111">Poiché il contenuto scaricato è crittografato, non può essere usato all'esterno dell'archivio di chiavi di Azure.</span><span class="sxs-lookup"><span data-stu-id="34bb0-111">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="34bb0-112">È possibile ripristinare una chiave di backup in qualsiasi volta chiave nell'abbonamento a cui è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="34bb0-112">You can restore a backed-up key to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="34bb0-113">I motivi tipici per usare questo cmdlet sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="34bb0-113">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="34bb0-114">Si vuole depositare una copia della chiave, in modo da avere una copia offline nel caso in cui si elimini accidentalmente la chiave in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="34bb0-114">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your key vault.</span></span>
 
- <span data-ttu-id="34bb0-115">È stata creata una chiave con Key Vault e ora si vuole clonare la chiave in un'altra area di Azure, in modo da poterla usare in tutte le istanze dell'applicazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="34bb0-115">You created a key using Key Vault and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="34bb0-116">Usa il cmdlet **backup-AzKeyVaultKey** per recuperare la chiave in formato crittografato e quindi usa il cmdlet Restore-AzKeyVaultKey e specifica un Vault chiave nella seconda area geografica.</span><span class="sxs-lookup"><span data-stu-id="34bb0-116">Use the **Backup-AzKeyVaultKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzKeyVaultKey cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="34bb0-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34bb0-117">EXAMPLES</span></span>

### <span data-ttu-id="34bb0-118">Esempio 1: eseguire il backup di una chiave con un nome file generato automaticamente</span><span class="sxs-lookup"><span data-stu-id="34bb0-118">Example 1: Back up a key with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'

C:\Users\username\mykeyvault-mykey-1527029447.01191
```

<span data-ttu-id="34bb0-119">Questo comando Recupera la chiave denominata MyKey dal Vault chiave denominata MyKeyVault e salva una copia di backup di tale chiave in un file denominato automaticamente e visualizza il nome del file.</span><span class="sxs-lookup"><span data-stu-id="34bb0-119">This command retrieves the key named MyKey from the key vault named MyKeyVault and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="34bb0-120">Esempio 2: eseguire il backup di una chiave in un nome file specificato</span><span class="sxs-lookup"><span data-stu-id="34bb0-120">Example 2: Back up a key to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="34bb0-121">Questo comando Recupera la chiave denominata MyKey dalla chiave vaultnamed MyKeyVault e salva una copia di backup di tale chiave in un file denominato backup. blob.</span><span class="sxs-lookup"><span data-stu-id="34bb0-121">This command retrieves the key named MyKey from the key vaultnamed MyKeyVault and saves a backup of that key to a file named Backup.blob.</span></span>

### <span data-ttu-id="34bb0-122">Esempio 3: eseguire il backup di una chiave recuperata in precedenza in un nome file specificato, sovrascrivendo il file di destinazione senza richiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="34bb0-122">Example 3: Back up a previously retrieved key to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\> Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="34bb0-123">Questo comando crea una copia di backup della chiave denominata $key. Nome nel Vault denominato $key. VAULTNAME in un file denominato backup. blob, sovrascrivendo automaticamente il file se esiste già.</span><span class="sxs-lookup"><span data-stu-id="34bb0-123">This command creates a backup of the key named $key.Name in the vault named $key.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="34bb0-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="34bb0-124">PARAMETERS</span></span>

### <span data-ttu-id="34bb0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34bb0-125">-DefaultProfile</span></span>
<span data-ttu-id="34bb0-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="34bb0-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34bb0-127">-Force</span><span class="sxs-lookup"><span data-stu-id="34bb0-127">-Force</span></span>
<span data-ttu-id="34bb0-128">Sovrascrivere il file assegnato se esiste</span><span class="sxs-lookup"><span data-stu-id="34bb0-128">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="34bb0-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="34bb0-129">-HsmName</span></span>
<span data-ttu-id="34bb0-130">Nome HSM.</span><span class="sxs-lookup"><span data-stu-id="34bb0-130">HSM name.</span></span> <span data-ttu-id="34bb0-131">Cmdlet costruisce l'FQDN di un HSM gestito in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="34bb0-131">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByKeyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34bb0-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34bb0-132">-InputObject</span></span>
<span data-ttu-id="34bb0-133">Bundle chiave per eseguire il backup, tramite pipeline nell'output di una chiamata di recupero.</span><span class="sxs-lookup"><span data-stu-id="34bb0-133">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="34bb0-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="34bb0-134">-Name</span></span>
<span data-ttu-id="34bb0-135">Specifica il nome della chiave a cui eseguire il backup.</span><span class="sxs-lookup"><span data-stu-id="34bb0-135">Specifies the name of the key to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, HsmByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34bb0-136">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="34bb0-136">-OutputFile</span></span>
<span data-ttu-id="34bb0-137">Specifica il file di output in cui è archiviato il BLOB di backup.</span><span class="sxs-lookup"><span data-stu-id="34bb0-137">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="34bb0-138">Se non specifichi questo parametro, questo cmdlet genera un nome file.</span><span class="sxs-lookup"><span data-stu-id="34bb0-138">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="34bb0-139">Se specifichi il nome di un file di output esistente, l'operazione non verrà completata e restituirà un messaggio di errore che indica che il file di backup esiste già.</span><span class="sxs-lookup"><span data-stu-id="34bb0-139">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="34bb0-140">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="34bb0-140">-VaultName</span></span>
<span data-ttu-id="34bb0-141">Specifica il nome del Vault chiave che contiene la chiave per eseguire il backup.</span><span class="sxs-lookup"><span data-stu-id="34bb0-141">Specifies the name of the key vault that contains the key to back up.</span></span>

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

### <span data-ttu-id="34bb0-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="34bb0-142">-Confirm</span></span>
<span data-ttu-id="34bb0-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34bb0-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34bb0-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34bb0-144">-WhatIf</span></span>
<span data-ttu-id="34bb0-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34bb0-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34bb0-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34bb0-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34bb0-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34bb0-147">CommonParameters</span></span>
<span data-ttu-id="34bb0-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34bb0-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34bb0-149">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34bb0-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34bb0-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="34bb0-150">INPUTS</span></span>

### <span data-ttu-id="34bb0-151">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="34bb0-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="34bb0-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34bb0-152">OUTPUTS</span></span>

### <span data-ttu-id="34bb0-153">System. String</span><span class="sxs-lookup"><span data-stu-id="34bb0-153">System.String</span></span>

## <span data-ttu-id="34bb0-154">Note</span><span class="sxs-lookup"><span data-stu-id="34bb0-154">NOTES</span></span>

## <span data-ttu-id="34bb0-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34bb0-155">RELATED LINKS</span></span>

[<span data-ttu-id="34bb0-156">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="34bb0-156">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="34bb0-157">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="34bb0-157">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="34bb0-158">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="34bb0-158">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="34bb0-159">Ripristinare-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="34bb0-159">Restore-AzKeyVaultKey</span></span>](./Restore-AzKeyVaultKey.md)

