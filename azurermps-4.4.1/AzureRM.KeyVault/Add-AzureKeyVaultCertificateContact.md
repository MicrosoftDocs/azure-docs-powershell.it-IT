---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: af66ad82d37c29d1dcd455cb3ccf7ae11676828c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521221"
---
# <span data-ttu-id="33b27-101">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="33b27-101">Add-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="33b27-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="33b27-102">SYNOPSIS</span></span>
<span data-ttu-id="33b27-103">Aggiunge un contatto per le notifiche dei certificati.</span><span class="sxs-lookup"><span data-stu-id="33b27-103">Adds a contact for certificate notifications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33b27-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="33b27-104">SYNTAX</span></span>

```
Add-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33b27-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33b27-105">DESCRIPTION</span></span>
<span data-ttu-id="33b27-106">Il cmdlet **Add-AzureKeyVaultCertificateContact** aggiunge un contatto per un Vault chiave per le notifiche dei certificati in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="33b27-106">The **Add-AzureKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="33b27-107">Il contatto riceve gli aggiornamenti sugli eventi, ad esempio un certificato vicino alla scadenza, un certificato rinnovato e così via.</span><span class="sxs-lookup"><span data-stu-id="33b27-107">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="33b27-108">Questi eventi sono determinati dal criterio del certificato.</span><span class="sxs-lookup"><span data-stu-id="33b27-108">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="33b27-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="33b27-109">EXAMPLES</span></span>

### <span data-ttu-id="33b27-110">Esempio 1: aggiungere un contatto Key Vault certificate</span><span class="sxs-lookup"><span data-stu-id="33b27-110">Example 1: Add a key vault certificate contact</span></span>
```
PS C:\>Add-AzureKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru
```

<span data-ttu-id="33b27-111">Questo comando aggiunge Patti Fuller come contatto di certificato per il Vault della chiave ContosoKV01 e restituisce l'oggetto **KeyVaultCertificateContact** .</span><span class="sxs-lookup"><span data-stu-id="33b27-111">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the **KeyVaultCertificateContact** object.</span></span>

## <span data-ttu-id="33b27-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="33b27-112">PARAMETERS</span></span>

### <span data-ttu-id="33b27-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="33b27-113">-EmailAddress</span></span>
<span data-ttu-id="33b27-114">Specifica l'indirizzo di posta elettronica del contatto.</span><span class="sxs-lookup"><span data-stu-id="33b27-114">Specifies the email address of the contact.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b27-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33b27-115">-PassThru</span></span>
<span data-ttu-id="33b27-116">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="33b27-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="33b27-117">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="33b27-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="33b27-118">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="33b27-118">-VaultName</span></span>
<span data-ttu-id="33b27-119">Specifica il nome del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="33b27-119">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33b27-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="33b27-120">-Confirm</span></span>
<span data-ttu-id="33b27-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33b27-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33b27-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33b27-122">-WhatIf</span></span>
<span data-ttu-id="33b27-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="33b27-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33b27-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="33b27-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33b27-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33b27-125">-DefaultProfile</span></span>
<span data-ttu-id="33b27-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="33b27-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33b27-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33b27-127">CommonParameters</span></span>
<span data-ttu-id="33b27-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33b27-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33b27-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33b27-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33b27-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="33b27-130">INPUTS</span></span>

## <span data-ttu-id="33b27-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="33b27-131">OUTPUTS</span></span>

### <span data-ttu-id="33b27-132">Elenco<Microsoft. Azure. Commands. Vault. Models. KeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="33b27-132">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="33b27-133">Note</span><span class="sxs-lookup"><span data-stu-id="33b27-133">NOTES</span></span>

## <span data-ttu-id="33b27-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="33b27-134">RELATED LINKS</span></span>

[<span data-ttu-id="33b27-135">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="33b27-135">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="33b27-136">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="33b27-136">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

