---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://msdn.microsoft.com/en-us/library/dn868052.aspx
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
ms.openlocfilehash: df29d88fbac1a8d2dc382522e24ff143cf075573
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521204"
---
# <span data-ttu-id="2ece0-101">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="2ece0-101">Undo-AzureKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="2ece0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2ece0-102">SYNOPSIS</span></span>
<span data-ttu-id="2ece0-103">Recuperare una chiave eliminata in un Vault chiave in uno stato attivo.</span><span class="sxs-lookup"><span data-stu-id="2ece0-103">Recovers a deleted key in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ece0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ece0-104">SYNTAX</span></span>

```
Undo-AzureKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ece0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ece0-105">DESCRIPTION</span></span>
<span data-ttu-id="2ece0-106">Il cmdlet **Undo-AzureKeyVaultKeyRemoval** recupererà una chiave eliminata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="2ece0-106">The **Undo-AzureKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="2ece0-107">La chiave recuperata sarà attiva e può essere usata per tutte le operazioni chiave normali.</span><span class="sxs-lookup"><span data-stu-id="2ece0-107">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="2ece0-108">Per eseguire questa operazione, il chiamante deve avere l'autorizzazione "Recupera".</span><span class="sxs-lookup"><span data-stu-id="2ece0-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="2ece0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ece0-109">EXAMPLES</span></span>

### <span data-ttu-id="2ece0-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2ece0-110">Example 1</span></span>
```
PS C:\>Undo-AzureKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="2ece0-111">Questo comando recupererà la chiave "MyKey" eliminata in precedenza in uno stato attivo e utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="2ece0-111">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="2ece0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2ece0-112">PARAMETERS</span></span>

### <span data-ttu-id="2ece0-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="2ece0-113">-Name</span></span>
<span data-ttu-id="2ece0-114">Nome chiave.</span><span class="sxs-lookup"><span data-stu-id="2ece0-114">Key name.</span></span>
<span data-ttu-id="2ece0-115">Cmdlet costruisce il nome di dominio completo di una chiave dal nome del Vault, l'ambiente selezionato e il cognome della chiave.</span><span class="sxs-lookup"><span data-stu-id="2ece0-115">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ece0-116">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="2ece0-116">-VaultName</span></span>
<span data-ttu-id="2ece0-117">Nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="2ece0-117">Vault name.</span></span>
<span data-ttu-id="2ece0-118">Cmdlet costruisce il nome di dominio completo di un Vault in base all'ambiente Name e attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="2ece0-118">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="2ece0-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2ece0-119">-Confirm</span></span>
<span data-ttu-id="2ece0-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ece0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ece0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ece0-121">-WhatIf</span></span>
<span data-ttu-id="2ece0-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ece0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ece0-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2ece0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ece0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ece0-124">-DefaultProfile</span></span>
<span data-ttu-id="2ece0-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2ece0-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ece0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ece0-126">CommonParameters</span></span>
<span data-ttu-id="2ece0-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ece0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ece0-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ece0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ece0-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2ece0-129">INPUTS</span></span>

### <span data-ttu-id="2ece0-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2ece0-130">System.String</span></span>

## <span data-ttu-id="2ece0-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ece0-131">OUTPUTS</span></span>

### <span data-ttu-id="2ece0-132">Microsoft. Azure. Commands. Vault. Models. bundle</span><span class="sxs-lookup"><span data-stu-id="2ece0-132">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="2ece0-133">Note</span><span class="sxs-lookup"><span data-stu-id="2ece0-133">NOTES</span></span>

## <span data-ttu-id="2ece0-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ece0-134">RELATED LINKS</span></span>

[<span data-ttu-id="2ece0-135">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2ece0-135">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="2ece0-136">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2ece0-136">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="2ece0-137">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2ece0-137">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

