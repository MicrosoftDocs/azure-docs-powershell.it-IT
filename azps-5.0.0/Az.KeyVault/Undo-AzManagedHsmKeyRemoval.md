---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azmanagedhsmkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzManagedHsmKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzManagedHsmKeyRemoval.md
ms.openlocfilehash: be1713584a1d0ce897c1c728f6aa7ae8b6ca3255
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193238"
---
# <span data-ttu-id="137c2-101">Undo-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="137c2-101">Undo-AzManagedHsmKeyRemoval</span></span>

## <span data-ttu-id="137c2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="137c2-102">SYNOPSIS</span></span>
<span data-ttu-id="137c2-103">Ripristina una chiave eliminata in un HSM gestito in uno stato attivo.</span><span class="sxs-lookup"><span data-stu-id="137c2-103">Recovers a deleted key in a managed HSM into an active state.</span></span>

## <span data-ttu-id="137c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="137c2-104">SYNTAX</span></span>

### <span data-ttu-id="137c2-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="137c2-105">Default (Default)</span></span>
```
Undo-AzManagedHsmKeyRemoval [-HsmName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="137c2-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="137c2-106">InputObject</span></span>
```
Undo-AzManagedHsmKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="137c2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="137c2-107">DESCRIPTION</span></span>
<span data-ttu-id="137c2-108">Il cmdlet **Undo-AzManagedHsmKeyRemoval** recupererà una chiave eliminata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="137c2-108">The **Undo-AzManagedHsmKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="137c2-109">La chiave recuperata sarà attiva e può essere usata per tutte le operazioni chiave normali.</span><span class="sxs-lookup"><span data-stu-id="137c2-109">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="137c2-110">Per eseguire questa operazione, il chiamante deve avere l'autorizzazione "Recupera".</span><span class="sxs-lookup"><span data-stu-id="137c2-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="137c2-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="137c2-111">EXAMPLES</span></span>

### <span data-ttu-id="137c2-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="137c2-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzManagedHsmKeyRemoval -HsmName testmhsm -Name testkey001

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

<span data-ttu-id="137c2-113">Questo comando recupererà la chiave "testkey001" eliminata in precedenza in uno stato attivo e utilizzabile.</span><span class="sxs-lookup"><span data-stu-id="137c2-113">This command will recover the key 'testkey001' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="137c2-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="137c2-114">PARAMETERS</span></span>

### <span data-ttu-id="137c2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="137c2-115">-DefaultProfile</span></span>
<span data-ttu-id="137c2-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="137c2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="137c2-117">-HsmName</span><span class="sxs-lookup"><span data-stu-id="137c2-117">-HsmName</span></span>
<span data-ttu-id="137c2-118">Nome HSM.</span><span class="sxs-lookup"><span data-stu-id="137c2-118">HSM name.</span></span> <span data-ttu-id="137c2-119">Cmdlet costruisce l'FQDN di un HSM gestito in base al nome e all'ambiente attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="137c2-119">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="137c2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="137c2-120">-InputObject</span></span>
<span data-ttu-id="137c2-121">Oggetto chiave eliminata</span><span class="sxs-lookup"><span data-stu-id="137c2-121">Deleted key object</span></span>

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

### <span data-ttu-id="137c2-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="137c2-122">-Name</span></span>
<span data-ttu-id="137c2-123">Nome chiave.</span><span class="sxs-lookup"><span data-stu-id="137c2-123">Key name.</span></span>
<span data-ttu-id="137c2-124">Cmdlet costruisce il nome di dominio completo di una chiave dal nome di HSM gestito, dall'ambiente selezionato e dalla chiave.</span><span class="sxs-lookup"><span data-stu-id="137c2-124">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="137c2-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="137c2-125">-Confirm</span></span>
<span data-ttu-id="137c2-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="137c2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="137c2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="137c2-127">-WhatIf</span></span>
<span data-ttu-id="137c2-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="137c2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="137c2-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="137c2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="137c2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="137c2-130">CommonParameters</span></span>
<span data-ttu-id="137c2-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="137c2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="137c2-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="137c2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="137c2-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="137c2-133">INPUTS</span></span>

### <span data-ttu-id="137c2-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="137c2-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="137c2-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="137c2-135">OUTPUTS</span></span>

### <span data-ttu-id="137c2-136">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="137c2-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="137c2-137">Note</span><span class="sxs-lookup"><span data-stu-id="137c2-137">NOTES</span></span>

## <span data-ttu-id="137c2-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="137c2-138">RELATED LINKS</span></span>

[<span data-ttu-id="137c2-139">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="137c2-139">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="137c2-140">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="137c2-140">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="137c2-141">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="137c2-141">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="137c2-142">Ripristinare-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="137c2-142">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)

[<span data-ttu-id="137c2-143">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="137c2-143">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="137c2-144">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="137c2-144">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)