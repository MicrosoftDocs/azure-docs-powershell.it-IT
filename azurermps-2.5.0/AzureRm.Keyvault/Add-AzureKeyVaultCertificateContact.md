---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultcertificatecontact
schema: 2.0.0
ms.openlocfilehash: 9f52889f044ba6bf497b57a53f3e2daaea0dbf3b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865813"
---
# <span data-ttu-id="7d262-101">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="7d262-101">Add-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="7d262-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7d262-102">SYNOPSIS</span></span>
<span data-ttu-id="7d262-103">Aggiunge un contatto per le notifiche dei certificati.</span><span class="sxs-lookup"><span data-stu-id="7d262-103">Adds a contact for certificate notifications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d262-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d262-104">SYNTAX</span></span>

```
Add-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d262-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d262-105">DESCRIPTION</span></span>
<span data-ttu-id="7d262-106">Il cmdlet **Add-AzureKeyVaultCertificateContact** aggiunge un contatto per un Vault chiave per le notifiche dei certificati in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="7d262-106">The **Add-AzureKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="7d262-107">Il contatto riceve gli aggiornamenti sugli eventi, ad esempio un certificato vicino alla scadenza, un certificato rinnovato e così via.</span><span class="sxs-lookup"><span data-stu-id="7d262-107">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="7d262-108">Questi eventi sono determinati dal criterio del certificato.</span><span class="sxs-lookup"><span data-stu-id="7d262-108">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="7d262-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d262-109">EXAMPLES</span></span>

### <span data-ttu-id="7d262-110">Esempio 1: aggiungere un contatto Key Vault certificate</span><span class="sxs-lookup"><span data-stu-id="7d262-110">Example 1: Add a key vault certificate contact</span></span>
```
PS C:\>Add-AzureKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru
```

<span data-ttu-id="7d262-111">Questo comando aggiunge Patti Fuller come contatto di certificato per il Vault della chiave ContosoKV01 e restituisce l'oggetto **KeyVaultCertificateContact** .</span><span class="sxs-lookup"><span data-stu-id="7d262-111">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the **KeyVaultCertificateContact** object.</span></span>

## <span data-ttu-id="7d262-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7d262-112">PARAMETERS</span></span>

### <span data-ttu-id="7d262-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d262-113">-DefaultProfile</span></span>
<span data-ttu-id="7d262-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7d262-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d262-115">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="7d262-115">-EmailAddress</span></span>
<span data-ttu-id="7d262-116">Specifica l'indirizzo di posta elettronica del contatto.</span><span class="sxs-lookup"><span data-stu-id="7d262-116">Specifies the email address of the contact.</span></span>

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

### <span data-ttu-id="7d262-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d262-117">-PassThru</span></span>
<span data-ttu-id="7d262-118">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="7d262-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7d262-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="7d262-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7d262-120">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="7d262-120">-VaultName</span></span>
<span data-ttu-id="7d262-121">Specifica il nome del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="7d262-121">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="7d262-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7d262-122">-Confirm</span></span>
<span data-ttu-id="7d262-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d262-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d262-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d262-124">-WhatIf</span></span>
<span data-ttu-id="7d262-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d262-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d262-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d262-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d262-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d262-127">CommonParameters</span></span>
<span data-ttu-id="7d262-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d262-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d262-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d262-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d262-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7d262-130">INPUTS</span></span>

## <span data-ttu-id="7d262-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d262-131">OUTPUTS</span></span>

### <span data-ttu-id="7d262-132">Elenco<Microsoft. Azure. Commands. Vault. Models. KeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="7d262-132">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="7d262-133">Note</span><span class="sxs-lookup"><span data-stu-id="7d262-133">NOTES</span></span>

## <span data-ttu-id="7d262-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d262-134">RELATED LINKS</span></span>

[<span data-ttu-id="7d262-135">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="7d262-135">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="7d262-136">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="7d262-136">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

