---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: c56dad380d1e5a43b3f4dafdc0e0e964e6264ef3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521368"
---
# <span data-ttu-id="8013d-101">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8013d-101">Add-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="8013d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8013d-102">SYNOPSIS</span></span>
<span data-ttu-id="8013d-103">Aggiunge un contatto per le notifiche dei certificati.</span><span class="sxs-lookup"><span data-stu-id="8013d-103">Adds a contact for certificate notifications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8013d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8013d-104">SYNTAX</span></span>

### <span data-ttu-id="8013d-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8013d-105">Interactive (Default)</span></span>
```
Add-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8013d-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="8013d-106">ByObject</span></span>
```
Add-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8013d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8013d-107">ByResourceId</span></span>
```
Add-AzureKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8013d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8013d-108">DESCRIPTION</span></span>
<span data-ttu-id="8013d-109">Il cmdlet **Add-AzureKeyVaultCertificateContact** aggiunge un contatto per un Vault chiave per le notifiche dei certificati in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="8013d-109">The **Add-AzureKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="8013d-110">Il contatto riceve gli aggiornamenti sugli eventi, ad esempio un certificato vicino alla scadenza, un certificato rinnovato e così via.</span><span class="sxs-lookup"><span data-stu-id="8013d-110">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="8013d-111">Questi eventi sono determinati dal criterio del certificato.</span><span class="sxs-lookup"><span data-stu-id="8013d-111">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="8013d-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8013d-112">EXAMPLES</span></span>

### <span data-ttu-id="8013d-113">Esempio 1: aggiungere un contatto Key Vault certificate</span><span class="sxs-lookup"><span data-stu-id="8013d-113">Example 1: Add a key vault certificate contact</span></span>
```powershell
PS C:\> Add-AzureKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email                    VaultName
-----                    ---------
patti.fuller@contoso.com ContosoKV01
```

<span data-ttu-id="8013d-114">Questo comando aggiunge Patti Fuller come contatto di certificato per il Vault Key di ContosoKV01 e restituisce l'elenco dei contatti per il Vault "ContosoKV01".</span><span class="sxs-lookup"><span data-stu-id="8013d-114">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the list of contacts for the "ContosoKV01" vault.</span></span>

## <span data-ttu-id="8013d-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8013d-115">PARAMETERS</span></span>

### <span data-ttu-id="8013d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8013d-116">-DefaultProfile</span></span>
<span data-ttu-id="8013d-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8013d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8013d-118">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="8013d-118">-EmailAddress</span></span>
<span data-ttu-id="8013d-119">Specifica l'indirizzo di posta elettronica del contatto.</span><span class="sxs-lookup"><span data-stu-id="8013d-119">Specifies the email address of the contact.</span></span>

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

### <span data-ttu-id="8013d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8013d-120">-InputObject</span></span>
<span data-ttu-id="8013d-121">Oggetto di Vault.</span><span class="sxs-lookup"><span data-stu-id="8013d-121">KeyVault object.</span></span>

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

### <span data-ttu-id="8013d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8013d-122">-PassThru</span></span>
<span data-ttu-id="8013d-123">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="8013d-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8013d-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="8013d-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8013d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8013d-125">-ResourceId</span></span>
<span data-ttu-id="8013d-126">ID risorsa di un Vault.</span><span class="sxs-lookup"><span data-stu-id="8013d-126">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="8013d-127">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="8013d-127">-VaultName</span></span>
<span data-ttu-id="8013d-128">Specifica il nome del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="8013d-128">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8013d-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8013d-129">-Confirm</span></span>
<span data-ttu-id="8013d-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8013d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8013d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8013d-131">-WhatIf</span></span>
<span data-ttu-id="8013d-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8013d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8013d-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8013d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8013d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8013d-134">CommonParameters</span></span>
<span data-ttu-id="8013d-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8013d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8013d-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8013d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8013d-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8013d-137">INPUTS</span></span>

### <span data-ttu-id="8013d-138">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="8013d-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="8013d-139">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8013d-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="8013d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="8013d-140">System.String</span></span>

## <span data-ttu-id="8013d-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8013d-141">OUTPUTS</span></span>

### <span data-ttu-id="8013d-142">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8013d-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="8013d-143">Note</span><span class="sxs-lookup"><span data-stu-id="8013d-143">NOTES</span></span>

## <span data-ttu-id="8013d-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8013d-144">RELATED LINKS</span></span>

[<span data-ttu-id="8013d-145">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8013d-145">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="8013d-146">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8013d-146">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

