---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: aee18adf3530976af4b17ffa15f94624248a7db7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515223"
---
# <span data-ttu-id="dcf87-101">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="dcf87-101">Remove-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="dcf87-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dcf87-102">SYNOPSIS</span></span>
<span data-ttu-id="dcf87-103">Elimina un contatto registrato per le notifiche di certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="dcf87-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcf87-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dcf87-104">SYNTAX</span></span>

### <span data-ttu-id="dcf87-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dcf87-105">ByName (Default)</span></span>
```
Remove-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcf87-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="dcf87-106">ByObject</span></span>
```
Remove-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dcf87-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="dcf87-107">ByResourceId</span></span>
```
Remove-AzureKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcf87-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dcf87-108">DESCRIPTION</span></span>
<span data-ttu-id="dcf87-109">Il cmdlet **Remove-AzureKeyVaultCertificateContact** Elimina un contatto registrato per le notifiche di certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="dcf87-109">The **Remove-AzureKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="dcf87-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dcf87-110">EXAMPLES</span></span>

### <span data-ttu-id="dcf87-111">Esempio 1: rimuovere un contatto del certificato</span><span class="sxs-lookup"><span data-stu-id="dcf87-111">Example 1: Remove a certificate contact</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email               VaultName
-----               ---------
user1@microsoft.com mvault2
user2@microsoft.com mvault2
user3@microsoft.com mvault2
user4@microsoft.com mvault2
```

<span data-ttu-id="dcf87-112">Questo comando rimuove Patti Fuller come contatto di certificato per il Vault della chiave Contoso01.</span><span class="sxs-lookup"><span data-stu-id="dcf87-112">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>  <span data-ttu-id="dcf87-113">Se si specifica PassThru, il cmdlet restituisce l'elenco dei contatti del certificato rimanente.</span><span class="sxs-lookup"><span data-stu-id="dcf87-113">If PassThru is specified, the cmdlet returns the list of remaining certificate contacts.</span></span>

## <span data-ttu-id="dcf87-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dcf87-114">PARAMETERS</span></span>

### <span data-ttu-id="dcf87-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcf87-115">-DefaultProfile</span></span>
<span data-ttu-id="dcf87-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="dcf87-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dcf87-117">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="dcf87-117">-EmailAddress</span></span>
<span data-ttu-id="dcf87-118">Specifica l'indirizzo di posta elettronica del contatto da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="dcf87-118">Specifies the email address of the contact to remove.</span></span>

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

### <span data-ttu-id="dcf87-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dcf87-119">-InputObject</span></span>
<span data-ttu-id="dcf87-120">Oggetto di Vault.</span><span class="sxs-lookup"><span data-stu-id="dcf87-120">KeyVault object.</span></span>

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

### <span data-ttu-id="dcf87-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dcf87-121">-PassThru</span></span>
<span data-ttu-id="dcf87-122">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="dcf87-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dcf87-123">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="dcf87-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dcf87-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcf87-124">-ResourceId</span></span>
<span data-ttu-id="dcf87-125">ID risorsa di un Vault.</span><span class="sxs-lookup"><span data-stu-id="dcf87-125">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="dcf87-126">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="dcf87-126">-VaultName</span></span>
<span data-ttu-id="dcf87-127">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="dcf87-127">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="dcf87-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dcf87-128">-Confirm</span></span>
<span data-ttu-id="dcf87-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcf87-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dcf87-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcf87-130">-WhatIf</span></span>
<span data-ttu-id="dcf87-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dcf87-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcf87-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dcf87-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dcf87-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcf87-133">CommonParameters</span></span>
<span data-ttu-id="dcf87-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcf87-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcf87-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcf87-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcf87-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dcf87-136">INPUTS</span></span>

### <span data-ttu-id="dcf87-137">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="dcf87-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="dcf87-138">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="dcf87-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="dcf87-139">System. String</span><span class="sxs-lookup"><span data-stu-id="dcf87-139">System.String</span></span>

## <span data-ttu-id="dcf87-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dcf87-140">OUTPUTS</span></span>

### <span data-ttu-id="dcf87-141">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="dcf87-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="dcf87-142">Note</span><span class="sxs-lookup"><span data-stu-id="dcf87-142">NOTES</span></span>

## <span data-ttu-id="dcf87-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dcf87-143">RELATED LINKS</span></span>

[<span data-ttu-id="dcf87-144">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="dcf87-144">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="dcf87-145">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="dcf87-145">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

