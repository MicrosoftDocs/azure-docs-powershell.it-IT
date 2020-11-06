---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 96f793c763a3e9a710c7e401c29880ccc0136b38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521035"
---
# <span data-ttu-id="71028-101">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="71028-101">Add-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="71028-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="71028-102">SYNOPSIS</span></span>
<span data-ttu-id="71028-103">Aggiunge un contatto per le notifiche dei certificati.</span><span class="sxs-lookup"><span data-stu-id="71028-103">Adds a contact for certificate notifications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71028-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71028-104">SYNTAX</span></span>

### <span data-ttu-id="71028-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="71028-105">Interactive (Default)</span></span>
```
Add-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71028-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="71028-106">ByObject</span></span>
```
Add-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71028-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71028-107">DESCRIPTION</span></span>
<span data-ttu-id="71028-108">Il cmdlet **Add-AzureKeyVaultCertificateContact** aggiunge un contatto per un Vault chiave per le notifiche dei certificati in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="71028-108">The **Add-AzureKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="71028-109">Il contatto riceve gli aggiornamenti sugli eventi, ad esempio un certificato vicino alla scadenza, un certificato rinnovato e così via.</span><span class="sxs-lookup"><span data-stu-id="71028-109">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="71028-110">Questi eventi sono determinati dal criterio del certificato.</span><span class="sxs-lookup"><span data-stu-id="71028-110">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="71028-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71028-111">EXAMPLES</span></span>

### <span data-ttu-id="71028-112">Esempio 1: aggiungere un contatto Key Vault certificate</span><span class="sxs-lookup"><span data-stu-id="71028-112">Example 1: Add a key vault certificate contact</span></span>
```
PS C:\>Add-AzureKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru
```

<span data-ttu-id="71028-113">Questo comando aggiunge Patti Fuller come contatto di certificato per il Vault della chiave ContosoKV01 e restituisce l'oggetto **KeyVaultCertificateContact** .</span><span class="sxs-lookup"><span data-stu-id="71028-113">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the **KeyVaultCertificateContact** object.</span></span>

## <span data-ttu-id="71028-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="71028-114">PARAMETERS</span></span>

### <span data-ttu-id="71028-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71028-115">-DefaultProfile</span></span>
<span data-ttu-id="71028-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="71028-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71028-117">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="71028-117">-EmailAddress</span></span>
<span data-ttu-id="71028-118">Specifica l'indirizzo di posta elettronica del contatto.</span><span class="sxs-lookup"><span data-stu-id="71028-118">Specifies the email address of the contact.</span></span>

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

### <span data-ttu-id="71028-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71028-119">-InputObject</span></span>
<span data-ttu-id="71028-120">Oggetto di Vault.</span><span class="sxs-lookup"><span data-stu-id="71028-120">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71028-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71028-121">-PassThru</span></span>
<span data-ttu-id="71028-122">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="71028-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="71028-123">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="71028-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="71028-124">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="71028-124">-VaultName</span></span>
<span data-ttu-id="71028-125">Specifica il nome del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="71028-125">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71028-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="71028-126">-Confirm</span></span>
<span data-ttu-id="71028-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71028-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71028-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71028-128">-WhatIf</span></span>
<span data-ttu-id="71028-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71028-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71028-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71028-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71028-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71028-131">CommonParameters</span></span>
<span data-ttu-id="71028-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71028-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71028-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71028-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71028-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="71028-134">INPUTS</span></span>

### <span data-ttu-id="71028-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="71028-135">None</span></span>
<span data-ttu-id="71028-136">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="71028-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="71028-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71028-137">OUTPUTS</span></span>

### <span data-ttu-id="71028-138">Elenco<Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="71028-138">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact></span></span>

## <span data-ttu-id="71028-139">Note</span><span class="sxs-lookup"><span data-stu-id="71028-139">NOTES</span></span>

## <span data-ttu-id="71028-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71028-140">RELATED LINKS</span></span>

[<span data-ttu-id="71028-141">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="71028-141">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="71028-142">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="71028-142">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

