---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 375cc5493bd3b3cac31f4318df57e155eda918c3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863069"
---
# <span data-ttu-id="00fa4-101">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="00fa4-101">Add-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="00fa4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="00fa4-102">SYNOPSIS</span></span>
<span data-ttu-id="00fa4-103">Aggiunge un contatto per le notifiche dei certificati.</span><span class="sxs-lookup"><span data-stu-id="00fa4-103">Adds a contact for certificate notifications.</span></span>

## <span data-ttu-id="00fa4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="00fa4-104">SYNTAX</span></span>

```
Add-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00fa4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00fa4-105">DESCRIPTION</span></span>
<span data-ttu-id="00fa4-106">Il cmdlet **Add-AzKeyVaultCertificateContact** aggiunge un contatto per un Vault chiave per le notifiche dei certificati in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="00fa4-106">The **Add-AzKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="00fa4-107">Il contatto riceve gli aggiornamenti sugli eventi, ad esempio un certificato vicino alla scadenza, un certificato rinnovato e così via.</span><span class="sxs-lookup"><span data-stu-id="00fa4-107">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="00fa4-108">Questi eventi sono determinati dal criterio del certificato.</span><span class="sxs-lookup"><span data-stu-id="00fa4-108">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="00fa4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="00fa4-109">EXAMPLES</span></span>

### <span data-ttu-id="00fa4-110">Esempio 1: aggiungere un contatto Key Vault certificate</span><span class="sxs-lookup"><span data-stu-id="00fa4-110">Example 1: Add a key vault certificate contact</span></span>
```
PS C:\>Add-AzKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru
```

<span data-ttu-id="00fa4-111">Questo comando aggiunge Patti Fuller come contatto di certificato per il Vault della chiave ContosoKV01 e restituisce l'oggetto **KeyVaultCertificateContact** .</span><span class="sxs-lookup"><span data-stu-id="00fa4-111">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the **KeyVaultCertificateContact** object.</span></span>

## <span data-ttu-id="00fa4-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="00fa4-112">PARAMETERS</span></span>

### <span data-ttu-id="00fa4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00fa4-113">-DefaultProfile</span></span>
<span data-ttu-id="00fa4-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="00fa4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00fa4-115">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="00fa4-115">-EmailAddress</span></span>
<span data-ttu-id="00fa4-116">Specifica l'indirizzo di posta elettronica del contatto.</span><span class="sxs-lookup"><span data-stu-id="00fa4-116">Specifies the email address of the contact.</span></span>

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

### <span data-ttu-id="00fa4-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00fa4-117">-PassThru</span></span>
<span data-ttu-id="00fa4-118">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="00fa4-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="00fa4-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="00fa4-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="00fa4-120">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="00fa4-120">-VaultName</span></span>
<span data-ttu-id="00fa4-121">Specifica il nome del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="00fa4-121">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="00fa4-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="00fa4-122">-Confirm</span></span>
<span data-ttu-id="00fa4-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00fa4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00fa4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00fa4-124">-WhatIf</span></span>
<span data-ttu-id="00fa4-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="00fa4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00fa4-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="00fa4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00fa4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00fa4-127">CommonParameters</span></span>
<span data-ttu-id="00fa4-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00fa4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00fa4-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00fa4-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00fa4-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="00fa4-130">INPUTS</span></span>

### <span data-ttu-id="00fa4-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="00fa4-131">None</span></span>
<span data-ttu-id="00fa4-132">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="00fa4-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="00fa4-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="00fa4-133">OUTPUTS</span></span>

### <span data-ttu-id="00fa4-134">Elenco<Microsoft. Azure. Commands. Vault. Models. KeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="00fa4-134">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="00fa4-135">Note</span><span class="sxs-lookup"><span data-stu-id="00fa4-135">NOTES</span></span>

## <span data-ttu-id="00fa4-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="00fa4-136">RELATED LINKS</span></span>

[<span data-ttu-id="00fa4-137">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="00fa4-137">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="00fa4-138">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="00fa4-138">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

