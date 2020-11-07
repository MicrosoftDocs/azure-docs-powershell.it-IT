---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurermkeyvaultremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
ms.openlocfilehash: 83737a7643c78ef4ec41d84e153690b3a53a8d5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687911"
---
# <span data-ttu-id="789c2-101">Undo-AzureRmKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="789c2-101">Undo-AzureRmKeyVaultRemoval</span></span>

## <span data-ttu-id="789c2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="789c2-102">SYNOPSIS</span></span>
<span data-ttu-id="789c2-103">Ripristina un Vault di chiave eliminata in uno stato attivo.</span><span class="sxs-lookup"><span data-stu-id="789c2-103">Recovers a deleted key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="789c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="789c2-104">SYNTAX</span></span>

### <span data-ttu-id="789c2-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="789c2-105">Default (Default)</span></span>
```
Undo-AzureRmKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="789c2-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="789c2-106">InputObject</span></span>
```
Undo-AzureRmKeyVaultRemoval [-InputObject] <PSDeletedKeyVault> [-ResourceGroupName] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="789c2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="789c2-107">DESCRIPTION</span></span>
<span data-ttu-id="789c2-108">Il cmdlet **Undo-AzureRmKeyVaultRemoval** recupererà un Vault chiave eliminata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="789c2-108">The **Undo-AzureRmKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="789c2-109">Il Vault recuperato sarà attivo dopo il ripristino</span><span class="sxs-lookup"><span data-stu-id="789c2-109">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="789c2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="789c2-110">EXAMPLES</span></span>

### <span data-ttu-id="789c2-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="789c2-111">Example 1</span></span>
```
PS C:\> Undo-AzureRmKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}
```

<span data-ttu-id="789c2-112">Questo comando recupererà il Vault Key "MyKeyVault" eliminato in precedenza da eastus2 Region e il gruppo di risorse "MyResourceGroup" in uno stato attivo e utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="789c2-112">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="789c2-113">Sostituisce anche i tag con il nuovo tag.</span><span class="sxs-lookup"><span data-stu-id="789c2-113">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="789c2-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="789c2-114">PARAMETERS</span></span>

### <span data-ttu-id="789c2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="789c2-115">-DefaultProfile</span></span>
<span data-ttu-id="789c2-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="789c2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="789c2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="789c2-117">-InputObject</span></span>
<span data-ttu-id="789c2-118">Oggetto Vault eliminato</span><span class="sxs-lookup"><span data-stu-id="789c2-118">Deleted vault object</span></span>

```yaml
Type: PSDeletedKeyVault
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="789c2-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="789c2-119">-Location</span></span>
<span data-ttu-id="789c2-120">Specifica l'area di Azure originale del Vault eliminata.</span><span class="sxs-lookup"><span data-stu-id="789c2-120">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="789c2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="789c2-121">-ResourceGroupName</span></span>
<span data-ttu-id="789c2-122">Specifica il nome di un gruppo di risorse esistente in cui creare il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="789c2-122">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="789c2-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="789c2-123">-Tag</span></span>
<span data-ttu-id="789c2-124">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="789c2-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="789c2-125">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="789c2-125">For example:</span></span>

<span data-ttu-id="789c2-126">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="789c2-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="789c2-127">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="789c2-127">-VaultName</span></span>
<span data-ttu-id="789c2-128">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="789c2-128">Vault name.</span></span>
<span data-ttu-id="789c2-129">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="789c2-129">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="789c2-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="789c2-130">-Confirm</span></span>
<span data-ttu-id="789c2-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="789c2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="789c2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="789c2-132">-WhatIf</span></span>
<span data-ttu-id="789c2-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="789c2-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="789c2-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="789c2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="789c2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="789c2-135">CommonParameters</span></span>
<span data-ttu-id="789c2-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="789c2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="789c2-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="789c2-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="789c2-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="789c2-138">INPUTS</span></span>

### <span data-ttu-id="789c2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="789c2-139">System.String</span></span>
<span data-ttu-id="789c2-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="789c2-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="789c2-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="789c2-141">OUTPUTS</span></span>

### <span data-ttu-id="789c2-142">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="789c2-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="789c2-143">Note</span><span class="sxs-lookup"><span data-stu-id="789c2-143">NOTES</span></span>

## <span data-ttu-id="789c2-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="789c2-144">RELATED LINKS</span></span>

[<span data-ttu-id="789c2-145">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="789c2-145">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)

[<span data-ttu-id="789c2-146">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="789c2-146">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="789c2-147">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="789c2-147">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)
