---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmKey.md
ms.openlocfilehash: 9e75b6de483f0103103434518d31b472660f4a70
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296874"
---
# <span data-ttu-id="0d2a3-101">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="0d2a3-101">Backup-AzManagedHsmKey</span></span>

## <span data-ttu-id="0d2a3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0d2a3-102">SYNOPSIS</span></span>
<span data-ttu-id="0d2a3-103">Eseguire il backup di una chiave in un HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="0d2a3-103">Backs up a key in a managed HSM.</span></span>

## <span data-ttu-id="0d2a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0d2a3-104">SYNTAX</span></span>

### <span data-ttu-id="0d2a3-105">ByKeyName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0d2a3-105">ByKeyName (Default)</span></span>
```
Backup-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d2a3-106">ByKey</span><span class="sxs-lookup"><span data-stu-id="0d2a3-106">ByKey</span></span>
```
Backup-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d2a3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d2a3-107">DESCRIPTION</span></span>
<span data-ttu-id="0d2a3-108">Il cmdlet **backup-AzManagedHsmKey** salva una chiave specificata in un HSM gestito tramite il download e l'archiviazione in un file.</span><span class="sxs-lookup"><span data-stu-id="0d2a3-108">The **Backup-AzManagedHsmKey** cmdlet backs up a specified key in a managed HSM by downloading it and storing it in a file.</span></span>
<span data-ttu-id="0d2a3-109">Se sono presenti più versioni della chiave, tutte le versioni verranno incluse nel backup.</span><span class="sxs-lookup"><span data-stu-id="0d2a3-109">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="0d2a3-110">Dato che il contenuto scaricato è crittografato, non può essere usato all'esterno dell'HSM gestito da Azure.</span><span class="sxs-lookup"><span data-stu-id="0d2a3-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Managed HSM.</span></span>
<span data-ttu-id="0d2a3-111">È possibile ripristinare una chiave di backup in qualsiasi HSM gestito nell'abbonamento a cui è stato eseguito il backup.</span><span class="sxs-lookup"><span data-stu-id="0d2a3-111">You can restore a backed-up key to any managed HSM in the subscription that it was backed up from.</span></span>
<span data-ttu-id="0d2a3-112">I motivi tipici per usare questo cmdlet sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="0d2a3-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="0d2a3-113">Si vuole ottenere una copia della chiave a garanzia, in modo da avere una copia offline nel caso in cui si elimini accidentalmente la chiave nell'HSM gestito.</span><span class="sxs-lookup"><span data-stu-id="0d2a3-113">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your managed HSM.</span></span>
 
- <span data-ttu-id="0d2a3-114">È stata creata una chiave usando l'HSM gestito e ora si vuole clonare la chiave in un'altra area di Azure, in modo da poterla usare in tutte le istanze dell'applicazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="0d2a3-114">You created a key using Managed HSM and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="0d2a3-115">Usa il cmdlet **backup-AzManagedHsmKey** per recuperare la chiave in formato crittografato e quindi usa il cmdlet Restore-AzManagedHsmKey e specifica un HSM gestito nella seconda area geografica.</span><span class="sxs-lookup"><span data-stu-id="0d2a3-115">Use the **Backup-AzManagedHsmKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzManagedHsmKey cmdlet and specify a managed HSM in the second region.</span></span>

## <span data-ttu-id="0d2a3-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0d2a3-116">EXAMPLES</span></span>

### <span data-ttu-id="0d2a3-117">Esempio 1: eseguire il backup di una chiave con un nome file generato automaticamente</span><span class="sxs-lookup"><span data-stu-id="0d2a3-117">Example 1: Back up a key with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzManagedHsmKey -HsmName testmhsm -Name testkey

C:\Users\username\testmhsm-testkey-1602664728.7106073
```

<span data-ttu-id="0d2a3-118">Questo comando Recupera la chiave denominata TestKey dall'HSM gestito denominato testmhsm e salva una copia di backup di tale chiave in un file denominato automaticamente e visualizza il nome del file.</span><span class="sxs-lookup"><span data-stu-id="0d2a3-118">This command retrieves the key named testkey from the managed HSM named testmhsm and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

## <span data-ttu-id="0d2a3-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0d2a3-119">PARAMETERS</span></span>

### <span data-ttu-id="0d2a3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d2a3-120">-DefaultProfile</span></span>
<span data-ttu-id="0d2a3-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0d2a3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d2a3-122">-Force</span><span class="sxs-lookup"><span data-stu-id="0d2a3-122">-Force</span></span>
<span data-ttu-id="0d2a3-123">Sovrascrivere il file assegnato se esiste</span><span class="sxs-lookup"><span data-stu-id="0d2a3-123">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="0d2a3-124">-HsmName</span><span class="sxs-lookup"><span data-stu-id="0d2a3-124">-HsmName</span></span>
<span data-ttu-id="0d2a3-125">Nome HSM.</span><span class="sxs-lookup"><span data-stu-id="0d2a3-125">HSM name.</span></span> <span data-ttu-id="0d2a3-126">Cmdlet costruisce l'FQDN di un HSM gestito in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="0d2a3-126">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="0d2a3-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d2a3-127">-InputObject</span></span>
<span data-ttu-id="0d2a3-128">Bundle chiave per eseguire il backup, tramite pipeline nell'output di una chiamata di recupero.</span><span class="sxs-lookup"><span data-stu-id="0d2a3-128">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="0d2a3-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="0d2a3-129">-Name</span></span>
<span data-ttu-id="0d2a3-130">Nome chiave.</span><span class="sxs-lookup"><span data-stu-id="0d2a3-130">Key name.</span></span>
<span data-ttu-id="0d2a3-131">Cmdlet costruisce il nome di dominio completo di una chiave dal nome di HSM gestito, dall'ambiente selezionato e dalla chiave.</span><span class="sxs-lookup"><span data-stu-id="0d2a3-131">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="0d2a3-132">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="0d2a3-132">-OutputFile</span></span>
<span data-ttu-id="0d2a3-133">File di output.</span><span class="sxs-lookup"><span data-stu-id="0d2a3-133">Output file.</span></span>
<span data-ttu-id="0d2a3-134">File di output in cui archiviare il BLOB della chiave di backup.</span><span class="sxs-lookup"><span data-stu-id="0d2a3-134">The output file to store the backed up key blob in.</span></span>
<span data-ttu-id="0d2a3-135">Se non è presente, viene scelto un nome file predefinito.</span><span class="sxs-lookup"><span data-stu-id="0d2a3-135">If not present, a default filename is chosen.</span></span>

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

### <span data-ttu-id="0d2a3-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0d2a3-136">-Confirm</span></span>
<span data-ttu-id="0d2a3-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d2a3-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d2a3-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d2a3-138">-WhatIf</span></span>
<span data-ttu-id="0d2a3-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0d2a3-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d2a3-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0d2a3-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d2a3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d2a3-141">CommonParameters</span></span>
<span data-ttu-id="0d2a3-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d2a3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d2a3-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d2a3-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d2a3-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0d2a3-144">INPUTS</span></span>

### <span data-ttu-id="0d2a3-145">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="0d2a3-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="0d2a3-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0d2a3-146">OUTPUTS</span></span>

### <span data-ttu-id="0d2a3-147">System. String</span><span class="sxs-lookup"><span data-stu-id="0d2a3-147">System.String</span></span>

## <span data-ttu-id="0d2a3-148">Note</span><span class="sxs-lookup"><span data-stu-id="0d2a3-148">NOTES</span></span>

## <span data-ttu-id="0d2a3-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0d2a3-149">RELATED LINKS</span></span>

[<span data-ttu-id="0d2a3-150">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="0d2a3-150">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="0d2a3-151">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="0d2a3-151">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="0d2a3-152">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="0d2a3-152">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="0d2a3-153">Undo-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="0d2a3-153">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="0d2a3-154">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="0d2a3-154">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="0d2a3-155">Ripristinare-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="0d2a3-155">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)