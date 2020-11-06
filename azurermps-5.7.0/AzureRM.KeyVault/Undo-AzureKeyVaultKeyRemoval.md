---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
ms.openlocfilehash: 29a7c2d3bb2060b77871cea0c088c50a59197cb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509851"
---
# <span data-ttu-id="c8a4e-101">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="c8a4e-101">Undo-AzureKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="c8a4e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c8a4e-102">SYNOPSIS</span></span>
<span data-ttu-id="c8a4e-103">Recuperare una chiave eliminata in un Vault chiave in uno stato attivo.</span><span class="sxs-lookup"><span data-stu-id="c8a4e-103">Recovers a deleted key in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8a4e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8a4e-104">SYNTAX</span></span>

### <span data-ttu-id="c8a4e-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c8a4e-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8a4e-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c8a4e-106">InputObject</span></span>
```
Undo-AzureKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8a4e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8a4e-107">DESCRIPTION</span></span>
<span data-ttu-id="c8a4e-108">Il cmdlet **Undo-AzureKeyVaultKeyRemoval** recupererà una chiave eliminata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="c8a4e-108">The **Undo-AzureKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="c8a4e-109">La chiave recuperata sarà attiva e può essere usata per tutte le operazioni chiave normali.</span><span class="sxs-lookup"><span data-stu-id="c8a4e-109">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="c8a4e-110">Per eseguire questa operazione, il chiamante deve avere l'autorizzazione "Recupera".</span><span class="sxs-lookup"><span data-stu-id="c8a4e-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="c8a4e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8a4e-111">EXAMPLES</span></span>

### <span data-ttu-id="c8a4e-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c8a4e-112">Example 1</span></span>
```
PS C:\>Undo-AzureKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="c8a4e-113">Questo comando recupererà la chiave "MyKey" eliminata in precedenza in uno stato attivo e utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="c8a4e-113">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="c8a4e-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c8a4e-114">PARAMETERS</span></span>

### <span data-ttu-id="c8a4e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8a4e-115">-DefaultProfile</span></span>
<span data-ttu-id="c8a4e-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c8a4e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8a4e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8a4e-117">-InputObject</span></span>
<span data-ttu-id="c8a4e-118">Oggetto chiave eliminata</span><span class="sxs-lookup"><span data-stu-id="c8a4e-118">Deleted key object</span></span>

```yaml
Type: PSDeletedKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a4e-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c8a4e-119">-Name</span></span>
<span data-ttu-id="c8a4e-120">Nome chiave.</span><span class="sxs-lookup"><span data-stu-id="c8a4e-120">Key name.</span></span>
<span data-ttu-id="c8a4e-121">Cmdlet costruisce il nome di dominio completo di una chiave dal nome del Vault, l'ambiente selezionato e il cognome della chiave.</span><span class="sxs-lookup"><span data-stu-id="c8a4e-121">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a4e-122">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="c8a4e-122">-VaultName</span></span>
<span data-ttu-id="c8a4e-123">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="c8a4e-123">Vault name.</span></span>
<span data-ttu-id="c8a4e-124">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="c8a4e-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="c8a4e-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c8a4e-125">-Confirm</span></span>
<span data-ttu-id="c8a4e-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8a4e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8a4e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8a4e-127">-WhatIf</span></span>
<span data-ttu-id="c8a4e-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8a4e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8a4e-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8a4e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8a4e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8a4e-130">CommonParameters</span></span>
<span data-ttu-id="c8a4e-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8a4e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8a4e-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8a4e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8a4e-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c8a4e-133">INPUTS</span></span>

### <span data-ttu-id="c8a4e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c8a4e-134">System.String</span></span>

## <span data-ttu-id="c8a4e-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8a4e-135">OUTPUTS</span></span>

### <span data-ttu-id="c8a4e-136">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c8a4e-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="c8a4e-137">Note</span><span class="sxs-lookup"><span data-stu-id="c8a4e-137">NOTES</span></span>

## <span data-ttu-id="c8a4e-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8a4e-138">RELATED LINKS</span></span>

[<span data-ttu-id="c8a4e-139">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c8a4e-139">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="c8a4e-140">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c8a4e-140">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="c8a4e-141">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c8a4e-141">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

