---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultManagedStorageAccountKey.md
ms.openlocfilehash: 94e1b297879e31ff42f9c12c0e4ad4a601e5e163
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520066"
---
# <span data-ttu-id="a6c49-101">Update-AzureKeyVaultManagedStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a6c49-101">Update-AzureKeyVaultManagedStorageAccountKey</span></span>

## <span data-ttu-id="a6c49-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a6c49-102">SYNOPSIS</span></span>
<span data-ttu-id="a6c49-103">Rigenera la chiave specificata dell'account di archiviazione di Azure con chiave Key Vault.</span><span class="sxs-lookup"><span data-stu-id="a6c49-103">Regenerates the specified key of Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6c49-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6c49-104">SYNTAX</span></span>

```
Update-AzureKeyVaultManagedStorageAccountKey [-VaultName] <String> [-AccountName] <String> [-KeyName] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6c49-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a6c49-105">DESCRIPTION</span></span>
<span data-ttu-id="a6c49-106">Rigenera la chiave specificata di un account di archiviazione di Azure con chiave Key Vault e imposta la chiave come chiave attiva.</span><span class="sxs-lookup"><span data-stu-id="a6c49-106">Regenerates the specified key of Key Vault managed Azure Storage Account and sets the key as the active key.</span></span> <span data-ttu-id="a6c49-107">Key Vault inoltra la chiamata a Azure Resource Manager per rigenerare la chiave.</span><span class="sxs-lookup"><span data-stu-id="a6c49-107">Key Vault proxies the call to Azure Resource Manager to regenerate the key.</span></span> <span data-ttu-id="a6c49-108">Il chiamante deve possedere le autorizzazioni per rigenerare le chiavi in un account di archiviazione di Azure specifico.</span><span class="sxs-lookup"><span data-stu-id="a6c49-108">The caller must posses permissions to regenerate keys on given Azure Storage Account.</span></span>

## <span data-ttu-id="a6c49-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6c49-109">EXAMPLES</span></span>

### <span data-ttu-id="a6c49-110">Esempio 1: rigenerare una chiave</span><span class="sxs-lookup"><span data-stu-id="a6c49-110">Example 1: Regenerate a key</span></span>
```
PS C:\> Update-AzureKeyVaultManagedStorageAccountKey -VaultName 'myvault' -AccountName 'mystorageaccount' -KeyName 'key1'
```

<span data-ttu-id="a6c49-111">Rigenera "Key1" dell'account "mystorageaccount" e imposta "Key1" come attivo dell'account di archiviazione di Azure Key.</span><span class="sxs-lookup"><span data-stu-id="a6c49-111">Regenerates 'key1' of account 'mystorageaccount' and sets 'key1' as the active of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="a6c49-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a6c49-112">PARAMETERS</span></span>

### <span data-ttu-id="a6c49-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a6c49-113">-AccountName</span></span>
<span data-ttu-id="a6c49-114">Nome dell'account di archiviazione gestito Key Vault.</span><span class="sxs-lookup"><span data-stu-id="a6c49-114">Key Vault managed storage account name.</span></span> <span data-ttu-id="a6c49-115">Cmdlet crea l'FQDN di un nome di account di archiviazione gestito dal nome del Vault, dall'ambiente selezionato e dal nome dell'account di archiviazione modificato.</span><span class="sxs-lookup"><span data-stu-id="a6c49-115">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6c49-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a6c49-116">-Force</span></span>
<span data-ttu-id="a6c49-117">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="a6c49-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a6c49-118">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="a6c49-118">-KeyName</span></span>
<span data-ttu-id="a6c49-119">Nome della chiave dell'account di archiviazione per rigenerare e rendere attivo.</span><span class="sxs-lookup"><span data-stu-id="a6c49-119">Name of storage account key to regenerate and make active.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6c49-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6c49-120">-PassThru</span></span>
<span data-ttu-id="a6c49-121">Cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a6c49-121">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a6c49-122">Se questa opzione è specificata, cmdlet restituisce l'account di archiviazione gestita che è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="a6c49-122">If this switch is specified, cmdlet returns the managed storage account that was deleted.</span></span>

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

### <span data-ttu-id="a6c49-123">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="a6c49-123">-VaultName</span></span>
<span data-ttu-id="a6c49-124">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="a6c49-124">Vault name.</span></span>
<span data-ttu-id="a6c49-125">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="a6c49-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6c49-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a6c49-126">-Confirm</span></span>
<span data-ttu-id="a6c49-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6c49-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6c49-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6c49-128">-WhatIf</span></span>
<span data-ttu-id="a6c49-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6c49-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6c49-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6c49-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6c49-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6c49-131">-DefaultProfile</span></span>
<span data-ttu-id="a6c49-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a6c49-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6c49-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6c49-133">CommonParameters</span></span>
<span data-ttu-id="a6c49-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6c49-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6c49-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6c49-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6c49-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a6c49-136">INPUTS</span></span>

### <span data-ttu-id="a6c49-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a6c49-137">System.String</span></span>

## <span data-ttu-id="a6c49-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6c49-138">OUTPUTS</span></span>

### <span data-ttu-id="a6c49-139">Microsoft. Azure. Commands. Vault. Models. ManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a6c49-139">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageAccount</span></span>

## <span data-ttu-id="a6c49-140">Note</span><span class="sxs-lookup"><span data-stu-id="a6c49-140">NOTES</span></span>

## <span data-ttu-id="a6c49-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6c49-141">RELATED LINKS</span></span>

[https://msdn.microsoft.com/en-us/library/dn868052.aspx](https://msdn.microsoft.com/en-us/library/dn868052.aspx)

