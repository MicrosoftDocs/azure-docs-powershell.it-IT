---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: C4E7ACDF-22FB-4D49-93B3-69E787B7E0CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultKey.md
ms.openlocfilehash: 958aeb36ba047284085d471f73aadad78b756839
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328644"
---
# <span data-ttu-id="cae05-101">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cae05-101">Restore-AzKeyVaultKey</span></span>

## <span data-ttu-id="cae05-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cae05-102">SYNOPSIS</span></span>
<span data-ttu-id="cae05-103">Crea una chiave in un Vault chiave da un tasto di backup.</span><span class="sxs-lookup"><span data-stu-id="cae05-103">Creates a key in a key vault from a backed-up key.</span></span>

## <span data-ttu-id="cae05-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cae05-104">SYNTAX</span></span>

### <span data-ttu-id="cae05-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cae05-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultKey [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cae05-106">HsmByVaultName</span><span class="sxs-lookup"><span data-stu-id="cae05-106">HsmByVaultName</span></span>
```
Restore-AzKeyVaultKey -HsmName <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cae05-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cae05-107">ByInputObject</span></span>
```
Restore-AzKeyVaultKey [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cae05-108">HsmByInputObject</span><span class="sxs-lookup"><span data-stu-id="cae05-108">HsmByInputObject</span></span>
```
Restore-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cae05-109">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cae05-109">ByResourceId</span></span>
```
Restore-AzKeyVaultKey [-ResourceId] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cae05-110">HsmByResourceId</span><span class="sxs-lookup"><span data-stu-id="cae05-110">HsmByResourceId</span></span>
```
Restore-AzKeyVaultKey -HsmResourceId <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cae05-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cae05-111">DESCRIPTION</span></span>
<span data-ttu-id="cae05-112">Il cmdlet **Restore-AzKeyVaultKey** crea una chiave nell'archivio chiavi specificato.</span><span class="sxs-lookup"><span data-stu-id="cae05-112">The **Restore-AzKeyVaultKey** cmdlet creates a key in the specified key vault.</span></span>
<span data-ttu-id="cae05-113">Questa chiave è una replica della chiave di backup nel file di input e ha lo stesso nome della chiave originale.</span><span class="sxs-lookup"><span data-stu-id="cae05-113">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="cae05-114">Se il Vault chiave ha già una chiave con lo stesso nome, questo cmdlet non riesce invece di sovrascrivere la chiave originale.</span><span class="sxs-lookup"><span data-stu-id="cae05-114">If the key vault already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="cae05-115">Se il backup contiene più versioni di una chiave, tutte le versioni verranno ripristinate.</span><span class="sxs-lookup"><span data-stu-id="cae05-115">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="cae05-116">Il Vault chiave in cui ripristinare la chiave può essere diverso da quello della chiave a cui è stato eseguito il backup della chiave.</span><span class="sxs-lookup"><span data-stu-id="cae05-116">The key vault that you restore the key into can be different from the key vault that you backed up the key from.</span></span>
<span data-ttu-id="cae05-117">Tuttavia, il Vault della chiave deve usare lo stesso abbonamento ed essere in un'area di Azure nella stessa geografia (ad esempio, Nord America).</span><span class="sxs-lookup"><span data-stu-id="cae05-117">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="cae05-118">Vedere il Centro protezione di Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) per il mapping delle aree di Azure alle geografie.</span><span class="sxs-lookup"><span data-stu-id="cae05-118">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="cae05-119">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cae05-119">EXAMPLES</span></span>

### <span data-ttu-id="cae05-120">Esempio 1: ripristinare un tasto di backup</span><span class="sxs-lookup"><span data-stu-id="cae05-120">Example 1: Restore a backed-up key</span></span>
```powershell
PS C:\> Restore-AzKeyVaultKey -VaultName 'MyKeyVault' -InputFile "C:\Backup.blob"

Vault Name     : MyKeyVault
Name           : key1
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://mykeyvault.vault.azure.net:443/keys/key1/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        :
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 4/6/2018 11:35:04 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="cae05-121">Questo comando Ripristina una chiave, incluse tutte le relative versioni, dal file di backup denominato backup. BLOB nel caveau della chiave denominato MyKeyVault.</span><span class="sxs-lookup"><span data-stu-id="cae05-121">This command restores a key, including all of its versions, from the backup file named Backup.blob into the key vault named MyKeyVault.</span></span>

## <span data-ttu-id="cae05-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cae05-122">PARAMETERS</span></span>

### <span data-ttu-id="cae05-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cae05-123">-DefaultProfile</span></span>
<span data-ttu-id="cae05-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="cae05-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cae05-125">-HsmName</span><span class="sxs-lookup"><span data-stu-id="cae05-125">-HsmName</span></span>
<span data-ttu-id="cae05-126">Nome HSM.</span><span class="sxs-lookup"><span data-stu-id="cae05-126">HSM name.</span></span> <span data-ttu-id="cae05-127">Cmdlet costruisce l'FQDN di un HSM gestito in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="cae05-127">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cae05-128">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="cae05-128">-HsmObject</span></span>
<span data-ttu-id="cae05-129">Oggetto HSM</span><span class="sxs-lookup"><span data-stu-id="cae05-129">HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: HsmByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cae05-130">-HsmResourceId</span><span class="sxs-lookup"><span data-stu-id="cae05-130">-HsmResourceId</span></span>
<span data-ttu-id="cae05-131">ID risorsa HSM</span><span class="sxs-lookup"><span data-stu-id="cae05-131">Hsm Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cae05-132">-InputFile</span><span class="sxs-lookup"><span data-stu-id="cae05-132">-InputFile</span></span>
<span data-ttu-id="cae05-133">Specifica il file di input che contiene il backup della chiave da ripristinare.</span><span class="sxs-lookup"><span data-stu-id="cae05-133">Specifies the input file that contains the backup of the key to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cae05-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cae05-134">-InputObject</span></span>
<span data-ttu-id="cae05-135">Oggetto Vault</span><span class="sxs-lookup"><span data-stu-id="cae05-135">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cae05-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cae05-136">-ResourceId</span></span>
<span data-ttu-id="cae05-137">ID risorsa di un Vault</span><span class="sxs-lookup"><span data-stu-id="cae05-137">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cae05-138">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="cae05-138">-VaultName</span></span>
<span data-ttu-id="cae05-139">Specifica il nome del Vault chiave in cui ripristinare la chiave.</span><span class="sxs-lookup"><span data-stu-id="cae05-139">Specifies the name of the key vault into which to restore the key.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cae05-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cae05-140">-Confirm</span></span>
<span data-ttu-id="cae05-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cae05-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cae05-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cae05-142">-WhatIf</span></span>
<span data-ttu-id="cae05-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cae05-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cae05-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cae05-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cae05-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cae05-145">CommonParameters</span></span>
<span data-ttu-id="cae05-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cae05-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cae05-147">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cae05-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cae05-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cae05-148">INPUTS</span></span>

### <span data-ttu-id="cae05-149">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="cae05-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="cae05-150">System. String</span><span class="sxs-lookup"><span data-stu-id="cae05-150">System.String</span></span>

## <span data-ttu-id="cae05-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cae05-151">OUTPUTS</span></span>

### <span data-ttu-id="cae05-152">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cae05-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="cae05-153">Note</span><span class="sxs-lookup"><span data-stu-id="cae05-153">NOTES</span></span>

## <span data-ttu-id="cae05-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cae05-154">RELATED LINKS</span></span>

[<span data-ttu-id="cae05-155">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cae05-155">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="cae05-156">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cae05-156">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="cae05-157">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cae05-157">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="cae05-158">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cae05-158">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

