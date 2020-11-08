---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsmKey.md
ms.openlocfilehash: 38e0dbf124643a7d669c1787314790166e88f6a9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203663"
---
# <span data-ttu-id="08d95-101">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="08d95-101">Restore-AzManagedHsmKey</span></span>

## <span data-ttu-id="08d95-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="08d95-102">SYNOPSIS</span></span>
<span data-ttu-id="08d95-103">Crea una chiave in un HSM gestito da un tasto di backup.</span><span class="sxs-lookup"><span data-stu-id="08d95-103">Creates a key in a managed HSM from a backed-up key.</span></span>

## <span data-ttu-id="08d95-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="08d95-104">SYNTAX</span></span>

### <span data-ttu-id="08d95-105">ByHsmName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="08d95-105">ByHsmName (Default)</span></span>
```
Restore-AzManagedHsmKey [-HsmName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08d95-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="08d95-106">ByInputObject</span></span>
```
Restore-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08d95-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="08d95-107">ByResourceId</span></span>
```
Restore-AzManagedHsmKey [-ResourceId] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08d95-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08d95-108">DESCRIPTION</span></span>
<span data-ttu-id="08d95-109">Il cmdlet **Restore-AzManagedHsmKey** crea una chiave nell'HSM gestito specificato.</span><span class="sxs-lookup"><span data-stu-id="08d95-109">The **Restore-AzManagedHsmKey** cmdlet creates a key in the specified managed HSM.</span></span>
<span data-ttu-id="08d95-110">Questa chiave è una replica della chiave di backup nel file di input e ha lo stesso nome della chiave originale.</span><span class="sxs-lookup"><span data-stu-id="08d95-110">This key is a replica of the backed-up key in the input file and has the same name as the original key.</span></span>
<span data-ttu-id="08d95-111">Se l'HSM gestito ha già una chiave con lo stesso nome, questo cmdlet non riesce invece di sovrascrivere la chiave originale.</span><span class="sxs-lookup"><span data-stu-id="08d95-111">If the managed HSM already has a key by the same name, this cmdlet fails instead of overwriting the original key.</span></span>
<span data-ttu-id="08d95-112">Se il backup contiene più versioni di una chiave, tutte le versioni verranno ripristinate.</span><span class="sxs-lookup"><span data-stu-id="08d95-112">If the backup contains multiple versions of a key, all versions are restored.</span></span>
<span data-ttu-id="08d95-113">L'HSM gestito in cui ripristinare la chiave può essere diverso dall'HSM gestito a cui è stato eseguito il backup della chiave.</span><span class="sxs-lookup"><span data-stu-id="08d95-113">The managed HSM that you restore the key into can be different from the managed HSM that you backed up the key from.</span></span>
<span data-ttu-id="08d95-114">Tuttavia, l'HSM gestito deve usare lo stesso abbonamento ed essere in un'area di Azure nella stessa geografia (ad esempio, Nord America).</span><span class="sxs-lookup"><span data-stu-id="08d95-114">However, the managed HSM must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="08d95-115">Vedere il Centro protezione di Microsoft Azure ( https://azure.microsoft.com/support/trust-center/) per il mapping delle aree di Azure alle geografie.</span><span class="sxs-lookup"><span data-stu-id="08d95-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="08d95-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="08d95-116">EXAMPLES</span></span>

### <span data-ttu-id="08d95-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="08d95-117">Example 1</span></span>
```powershell
PS C:\> Restore-AzManagedHsmKey -HsmName testmhsm -InputFile "C:\Backup.blob"

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 7cff8510da04433b98144a3e33ad2bae
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/7cff8510da04433b98144a3e33ad2bae
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 10:13:03 AM
Updated        : 10/14/2020 10:13:03 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="08d95-118">Questo comando Ripristina una chiave, incluse tutte le relative versioni, dal file di backup denominato backup. blob nell'HSM gestito denominato testmhsm.</span><span class="sxs-lookup"><span data-stu-id="08d95-118">This command restores a key, including all of its versions, from the backup file named Backup.blob into the managed HSM named testmhsm.</span></span>

## <span data-ttu-id="08d95-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="08d95-119">PARAMETERS</span></span>

### <span data-ttu-id="08d95-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08d95-120">-DefaultProfile</span></span>
<span data-ttu-id="08d95-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="08d95-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08d95-122">-HsmName</span><span class="sxs-lookup"><span data-stu-id="08d95-122">-HsmName</span></span>
<span data-ttu-id="08d95-123">Nome HSM.</span><span class="sxs-lookup"><span data-stu-id="08d95-123">HSM name.</span></span> <span data-ttu-id="08d95-124">Cmdlet costruisce l'FQDN di un HSM gestito in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="08d95-124">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHsmName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08d95-125">-InputFile</span><span class="sxs-lookup"><span data-stu-id="08d95-125">-InputFile</span></span>
<span data-ttu-id="08d95-126">File di input.</span><span class="sxs-lookup"><span data-stu-id="08d95-126">Input file.</span></span>
<span data-ttu-id="08d95-127">File di input contenente il BLOB di cui è stato eseguito il backup</span><span class="sxs-lookup"><span data-stu-id="08d95-127">The input file containing the backed-up blob</span></span>

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

### <span data-ttu-id="08d95-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08d95-128">-InputObject</span></span>
<span data-ttu-id="08d95-129">Oggetto HSM</span><span class="sxs-lookup"><span data-stu-id="08d95-129">HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08d95-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08d95-130">-ResourceId</span></span>
<span data-ttu-id="08d95-131">ID risorsa HSM</span><span class="sxs-lookup"><span data-stu-id="08d95-131">HSM Resource Id</span></span>

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

### <span data-ttu-id="08d95-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="08d95-132">-Confirm</span></span>
<span data-ttu-id="08d95-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08d95-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08d95-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08d95-134">-WhatIf</span></span>
<span data-ttu-id="08d95-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="08d95-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08d95-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="08d95-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08d95-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08d95-137">CommonParameters</span></span>
<span data-ttu-id="08d95-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08d95-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08d95-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08d95-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08d95-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="08d95-140">INPUTS</span></span>

### <span data-ttu-id="08d95-141">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="08d95-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="08d95-142">System. String</span><span class="sxs-lookup"><span data-stu-id="08d95-142">System.String</span></span>

## <span data-ttu-id="08d95-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="08d95-143">OUTPUTS</span></span>

### <span data-ttu-id="08d95-144">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="08d95-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="08d95-145">Note</span><span class="sxs-lookup"><span data-stu-id="08d95-145">NOTES</span></span>

## <span data-ttu-id="08d95-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="08d95-146">RELATED LINKS</span></span>

[<span data-ttu-id="08d95-147">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="08d95-147">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="08d95-148">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="08d95-148">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="08d95-149">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="08d95-149">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="08d95-150">Undo-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="08d95-150">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="08d95-151">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="08d95-151">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="08d95-152">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="08d95-152">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)