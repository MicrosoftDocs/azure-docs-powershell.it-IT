---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultkeyremoval
schema: 2.0.0
ms.openlocfilehash: 831bcdb76a0f24a2935f2ffd2ed0bf7df1c10042
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866330"
---
# <span data-ttu-id="3e45e-101">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="3e45e-101">Undo-AzureKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="3e45e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3e45e-102">SYNOPSIS</span></span>
<span data-ttu-id="3e45e-103">Recuperare una chiave eliminata in un Vault chiave in uno stato attivo.</span><span class="sxs-lookup"><span data-stu-id="3e45e-103">Recovers a deleted key in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e45e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e45e-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e45e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e45e-105">DESCRIPTION</span></span>
<span data-ttu-id="3e45e-106">Il cmdlet **Undo-AzureKeyVaultKeyRemoval** recupererà una chiave eliminata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="3e45e-106">The **Undo-AzureKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="3e45e-107">La chiave recuperata sarà attiva e può essere usata per tutte le operazioni chiave normali.</span><span class="sxs-lookup"><span data-stu-id="3e45e-107">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="3e45e-108">Per eseguire questa operazione, il chiamante deve avere l'autorizzazione "Recupera".</span><span class="sxs-lookup"><span data-stu-id="3e45e-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="3e45e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e45e-109">EXAMPLES</span></span>

### <span data-ttu-id="3e45e-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3e45e-110">Example 1</span></span>
```
PS C:\>Undo-AzureKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="3e45e-111">Questo comando recupererà la chiave "MyKey" eliminata in precedenza in uno stato attivo e utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="3e45e-111">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="3e45e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3e45e-112">PARAMETERS</span></span>

### <span data-ttu-id="3e45e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e45e-113">-DefaultProfile</span></span>
<span data-ttu-id="3e45e-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3e45e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e45e-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e45e-115">-Name</span></span>
<span data-ttu-id="3e45e-116">Nome chiave.</span><span class="sxs-lookup"><span data-stu-id="3e45e-116">Key name.</span></span>
<span data-ttu-id="3e45e-117">Cmdlet costruisce il nome di dominio completo di una chiave dal nome del Vault, l'ambiente selezionato e il cognome della chiave.</span><span class="sxs-lookup"><span data-stu-id="3e45e-117">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e45e-118">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="3e45e-118">-VaultName</span></span>
<span data-ttu-id="3e45e-119">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="3e45e-119">Vault name.</span></span>
<span data-ttu-id="3e45e-120">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="3e45e-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e45e-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3e45e-121">-Confirm</span></span>
<span data-ttu-id="3e45e-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e45e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e45e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e45e-123">-WhatIf</span></span>
<span data-ttu-id="3e45e-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e45e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e45e-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e45e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e45e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e45e-126">CommonParameters</span></span>
<span data-ttu-id="3e45e-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e45e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e45e-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e45e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e45e-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3e45e-129">INPUTS</span></span>

### <span data-ttu-id="3e45e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3e45e-130">System.String</span></span>

## <span data-ttu-id="3e45e-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e45e-131">OUTPUTS</span></span>

### <span data-ttu-id="3e45e-132">Microsoft. Azure. Commands. Vault. Models. bundle</span><span class="sxs-lookup"><span data-stu-id="3e45e-132">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="3e45e-133">Note</span><span class="sxs-lookup"><span data-stu-id="3e45e-133">NOTES</span></span>

## <span data-ttu-id="3e45e-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e45e-134">RELATED LINKS</span></span>

[<span data-ttu-id="3e45e-135">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3e45e-135">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="3e45e-136">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3e45e-136">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="3e45e-137">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3e45e-137">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

