---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: c91aa7e43a36e1218f304c3675f1d3c9635002c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520443"
---
# <span data-ttu-id="214dd-101">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="214dd-101">Remove-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="214dd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="214dd-102">SYNOPSIS</span></span>
<span data-ttu-id="214dd-103">Elimina un contatto registrato per le notifiche di certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="214dd-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="214dd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="214dd-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="214dd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="214dd-105">DESCRIPTION</span></span>
<span data-ttu-id="214dd-106">Il cmdlet **Remove-AzureKeyVaultCertificateContact** Elimina un contatto registrato per le notifiche di certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="214dd-106">The **Remove-AzureKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="214dd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="214dd-107">EXAMPLES</span></span>

### <span data-ttu-id="214dd-108">Esempio 1: rimuovere un contatto del certificato</span><span class="sxs-lookup"><span data-stu-id="214dd-108">Example 1: Remove a certificate contact</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com"
```

<span data-ttu-id="214dd-109">Questo comando rimuove Patti Fuller come contatto di certificato per il Vault della chiave Contoso01.</span><span class="sxs-lookup"><span data-stu-id="214dd-109">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>

## <span data-ttu-id="214dd-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="214dd-110">PARAMETERS</span></span>

### <span data-ttu-id="214dd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="214dd-111">-DefaultProfile</span></span>
<span data-ttu-id="214dd-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="214dd-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="214dd-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="214dd-113">-EmailAddress</span></span>
<span data-ttu-id="214dd-114">Specifica l'indirizzo di posta elettronica del contatto da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="214dd-114">Specifies the email address of the contact to remove.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="214dd-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="214dd-115">-PassThru</span></span>
<span data-ttu-id="214dd-116">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="214dd-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="214dd-117">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="214dd-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="214dd-118">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="214dd-118">-VaultName</span></span>
<span data-ttu-id="214dd-119">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="214dd-119">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="214dd-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="214dd-120">-Confirm</span></span>
<span data-ttu-id="214dd-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="214dd-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="214dd-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="214dd-122">-WhatIf</span></span>
<span data-ttu-id="214dd-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="214dd-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="214dd-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="214dd-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="214dd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="214dd-125">CommonParameters</span></span>
<span data-ttu-id="214dd-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="214dd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="214dd-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="214dd-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="214dd-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="214dd-128">INPUTS</span></span>

### <span data-ttu-id="214dd-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="214dd-129">None</span></span>
<span data-ttu-id="214dd-130">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="214dd-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="214dd-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="214dd-131">OUTPUTS</span></span>

### <span data-ttu-id="214dd-132">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateContact]</span><span class="sxs-lookup"><span data-stu-id="214dd-132">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact]</span></span>

## <span data-ttu-id="214dd-133">Note</span><span class="sxs-lookup"><span data-stu-id="214dd-133">NOTES</span></span>

## <span data-ttu-id="214dd-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="214dd-134">RELATED LINKS</span></span>

[<span data-ttu-id="214dd-135">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="214dd-135">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="214dd-136">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="214dd-136">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

