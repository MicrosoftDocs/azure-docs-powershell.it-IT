---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
ms.openlocfilehash: ff4682a7c97f721dac9fb53f375c2a96f4bb33b2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674095"
---
# <span data-ttu-id="57050-101">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="57050-101">Undo-AzKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="57050-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="57050-102">SYNOPSIS</span></span>
<span data-ttu-id="57050-103">Recuperare una chiave eliminata in un Vault chiave in uno stato attivo.</span><span class="sxs-lookup"><span data-stu-id="57050-103">Recovers a deleted key in a key vault into an active state.</span></span>

## <span data-ttu-id="57050-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="57050-104">SYNTAX</span></span>

### <span data-ttu-id="57050-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="57050-105">Default (Default)</span></span>
```
Undo-AzKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57050-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="57050-106">InputObject</span></span>
```
Undo-AzKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57050-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57050-107">DESCRIPTION</span></span>
<span data-ttu-id="57050-108">Il cmdlet **Undo-AzKeyVaultKeyRemoval** recupererà una chiave eliminata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="57050-108">The **Undo-AzKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="57050-109">La chiave recuperata sarà attiva e può essere usata per tutte le operazioni chiave normali.</span><span class="sxs-lookup"><span data-stu-id="57050-109">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="57050-110">Per eseguire questa operazione, il chiamante deve avere l'autorizzazione "Recupera".</span><span class="sxs-lookup"><span data-stu-id="57050-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="57050-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="57050-111">EXAMPLES</span></span>

### <span data-ttu-id="57050-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="57050-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'

Vault Name     : MyKeyVault
Name           : MyKey
Version        : 1af807cc331a49d0b52b7c75e1b2366e
Id             : https://mykeybault.vault.azure.net:443/keys/mykey/1af807cc331a49d0b52b7c75e1b2366e
Enabled        : True
Expires        :
Not Before     :
Created        : 5/24/2018 8:32:27 PM
Updated        : 5/24/2018 8:32:27 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="57050-113">Questo comando recupererà la chiave "MyKey" eliminata in precedenza in uno stato attivo e utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="57050-113">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="57050-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="57050-114">PARAMETERS</span></span>

### <span data-ttu-id="57050-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57050-115">-DefaultProfile</span></span>
<span data-ttu-id="57050-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="57050-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57050-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57050-117">-InputObject</span></span>
<span data-ttu-id="57050-118">Oggetto chiave eliminata</span><span class="sxs-lookup"><span data-stu-id="57050-118">Deleted key object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57050-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="57050-119">-Name</span></span>
<span data-ttu-id="57050-120">Nome chiave.</span><span class="sxs-lookup"><span data-stu-id="57050-120">Key name.</span></span>
<span data-ttu-id="57050-121">Cmdlet costruisce il nome di dominio completo di una chiave dal nome del Vault, l'ambiente selezionato e il cognome della chiave.</span><span class="sxs-lookup"><span data-stu-id="57050-121">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57050-122">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="57050-122">-VaultName</span></span>
<span data-ttu-id="57050-123">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="57050-123">Vault name.</span></span>
<span data-ttu-id="57050-124">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="57050-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57050-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="57050-125">-Confirm</span></span>
<span data-ttu-id="57050-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57050-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57050-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57050-127">-WhatIf</span></span>
<span data-ttu-id="57050-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="57050-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57050-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="57050-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57050-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57050-130">CommonParameters</span></span>
<span data-ttu-id="57050-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57050-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57050-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57050-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57050-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="57050-133">INPUTS</span></span>

### <span data-ttu-id="57050-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="57050-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="57050-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="57050-135">OUTPUTS</span></span>

### <span data-ttu-id="57050-136">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="57050-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="57050-137">Note</span><span class="sxs-lookup"><span data-stu-id="57050-137">NOTES</span></span>

## <span data-ttu-id="57050-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="57050-138">RELATED LINKS</span></span>

[<span data-ttu-id="57050-139">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="57050-139">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="57050-140">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="57050-140">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="57050-141">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="57050-141">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

