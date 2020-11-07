---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificatecontact
schema: 2.0.0
ms.openlocfilehash: 9bfb62388ce4a7a8994f4a618a4c1a00ac5868d6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865803"
---
# <span data-ttu-id="21ee4-101">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="21ee4-101">Remove-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="21ee4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="21ee4-102">SYNOPSIS</span></span>
<span data-ttu-id="21ee4-103">Elimina un contatto registrato per le notifiche di certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="21ee4-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21ee4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="21ee4-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21ee4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="21ee4-105">DESCRIPTION</span></span>
<span data-ttu-id="21ee4-106">Il cmdlet **Remove-AzureKeyVaultCertificateContact** Elimina un contatto registrato per le notifiche di certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="21ee4-106">The **Remove-AzureKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="21ee4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="21ee4-107">EXAMPLES</span></span>

### <span data-ttu-id="21ee4-108">Esempio 1: rimuovere un contatto del certificato</span><span class="sxs-lookup"><span data-stu-id="21ee4-108">Example 1: Remove a certificate contact</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com"
```

<span data-ttu-id="21ee4-109">Questo comando rimuove Patti Fuller come contatto di certificato per il Vault della chiave Contoso01.</span><span class="sxs-lookup"><span data-stu-id="21ee4-109">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>

## <span data-ttu-id="21ee4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="21ee4-110">PARAMETERS</span></span>

### <span data-ttu-id="21ee4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21ee4-111">-DefaultProfile</span></span>
<span data-ttu-id="21ee4-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="21ee4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21ee4-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="21ee4-113">-EmailAddress</span></span>
<span data-ttu-id="21ee4-114">Specifica l'indirizzo di posta elettronica del contatto da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="21ee4-114">Specifies the email address of the contact to remove.</span></span>

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

### <span data-ttu-id="21ee4-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="21ee4-115">-PassThru</span></span>
<span data-ttu-id="21ee4-116">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="21ee4-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="21ee4-117">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="21ee4-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="21ee4-118">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="21ee4-118">-VaultName</span></span>
<span data-ttu-id="21ee4-119">Specifica il nome di un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="21ee4-119">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="21ee4-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="21ee4-120">-Confirm</span></span>
<span data-ttu-id="21ee4-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21ee4-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21ee4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21ee4-122">-WhatIf</span></span>
<span data-ttu-id="21ee4-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21ee4-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21ee4-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21ee4-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21ee4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21ee4-125">CommonParameters</span></span>
<span data-ttu-id="21ee4-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21ee4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21ee4-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21ee4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21ee4-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="21ee4-128">INPUTS</span></span>

## <span data-ttu-id="21ee4-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="21ee4-129">OUTPUTS</span></span>

### <span data-ttu-id="21ee4-130">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. Vault. Models. KeyVaultCertificateContact]</span><span class="sxs-lookup"><span data-stu-id="21ee4-130">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact]</span></span>

## <span data-ttu-id="21ee4-131">Note</span><span class="sxs-lookup"><span data-stu-id="21ee4-131">NOTES</span></span>

## <span data-ttu-id="21ee4-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="21ee4-132">RELATED LINKS</span></span>

[<span data-ttu-id="21ee4-133">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="21ee4-133">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="21ee4-134">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="21ee4-134">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

