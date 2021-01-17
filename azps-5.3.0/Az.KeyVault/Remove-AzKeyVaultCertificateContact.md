---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 12fe8cdc0e8e7210a2db7c7c6ccab1a0fcceeba3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476188"
---
# <span data-ttu-id="cf9dc-101">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="cf9dc-101">Remove-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="cf9dc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cf9dc-102">SYNOPSIS</span></span>
<span data-ttu-id="cf9dc-103">Elimina un contatto registrato per le notifiche di certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="cf9dc-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="cf9dc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cf9dc-104">SYNTAX</span></span>

### <span data-ttu-id="cf9dc-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cf9dc-105">ByName (Default)</span></span>
```
Remove-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf9dc-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="cf9dc-106">ByObject</span></span>
```
Remove-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf9dc-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cf9dc-107">ByResourceId</span></span>
```
Remove-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf9dc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf9dc-108">DESCRIPTION</span></span>
<span data-ttu-id="cf9dc-109">Il cmdlet **Remove-AzKeyVaultCertificateContact** Elimina un contatto registrato per le notifiche di certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="cf9dc-109">The **Remove-AzKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="cf9dc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cf9dc-110">EXAMPLES</span></span>

### <span data-ttu-id="cf9dc-111">Esempio 1: rimuovere un contatto del certificato</span><span class="sxs-lookup"><span data-stu-id="cf9dc-111">Example 1: Remove a certificate contact</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email               VaultName
-----               ---------
user1@microsoft.com mvault2
user2@microsoft.com mvault2
user3@microsoft.com mvault2
user4@microsoft.com mvault2
```

<span data-ttu-id="cf9dc-112">Questo comando rimuove Patti Fuller come contatto di certificato per il Vault della chiave Contoso01.</span><span class="sxs-lookup"><span data-stu-id="cf9dc-112">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>  <span data-ttu-id="cf9dc-113">Se si specifica PassThru, il cmdlet restituisce l'elenco dei contatti del certificato rimanente.</span><span class="sxs-lookup"><span data-stu-id="cf9dc-113">If PassThru is specified, the cmdlet returns the list of remaining certificate contacts.</span></span>

## <span data-ttu-id="cf9dc-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cf9dc-114">PARAMETERS</span></span>

### <span data-ttu-id="cf9dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf9dc-115">-DefaultProfile</span></span>
<span data-ttu-id="cf9dc-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="cf9dc-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf9dc-117">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="cf9dc-117">-EmailAddress</span></span>
<span data-ttu-id="cf9dc-118">Specifica l'indirizzo di posta elettronica del contatto da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="cf9dc-118">Specifies the email address of the contact to remove.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf9dc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf9dc-119">-InputObject</span></span>
<span data-ttu-id="cf9dc-120">Oggetto di Vault.</span><span class="sxs-lookup"><span data-stu-id="cf9dc-120">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cf9dc-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cf9dc-121">-PassThru</span></span>
<span data-ttu-id="cf9dc-122">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="cf9dc-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cf9dc-123">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="cf9dc-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cf9dc-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf9dc-124">-ResourceId</span></span>
<span data-ttu-id="cf9dc-125">ID risorsa di un Vault.</span><span class="sxs-lookup"><span data-stu-id="cf9dc-125">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="cf9dc-126">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="cf9dc-126">-VaultName</span></span>
<span data-ttu-id="cf9dc-127">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="cf9dc-127">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf9dc-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cf9dc-128">-Confirm</span></span>
<span data-ttu-id="cf9dc-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf9dc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf9dc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf9dc-130">-WhatIf</span></span>
<span data-ttu-id="cf9dc-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf9dc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf9dc-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf9dc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf9dc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf9dc-133">CommonParameters</span></span>
<span data-ttu-id="cf9dc-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf9dc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf9dc-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf9dc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf9dc-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cf9dc-136">INPUTS</span></span>

### <span data-ttu-id="cf9dc-137">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="cf9dc-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="cf9dc-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cf9dc-138">System.String</span></span>

## <span data-ttu-id="cf9dc-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cf9dc-139">OUTPUTS</span></span>

### <span data-ttu-id="cf9dc-140">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="cf9dc-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="cf9dc-141">Note</span><span class="sxs-lookup"><span data-stu-id="cf9dc-141">NOTES</span></span>

## <span data-ttu-id="cf9dc-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cf9dc-142">RELATED LINKS</span></span>

[<span data-ttu-id="cf9dc-143">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="cf9dc-143">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="cf9dc-144">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="cf9dc-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

