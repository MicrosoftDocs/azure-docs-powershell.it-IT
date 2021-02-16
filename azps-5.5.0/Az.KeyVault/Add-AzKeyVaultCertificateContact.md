---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 5b6661bada9b63485f937a0401064de2c33e3336
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203869"
---
# <span data-ttu-id="99bbc-101">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="99bbc-101">Add-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="99bbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99bbc-102">SYNOPSIS</span></span>
<span data-ttu-id="99bbc-103">Aggiunge un contatto per le notifiche di certificato.</span><span class="sxs-lookup"><span data-stu-id="99bbc-103">Adds a contact for certificate notifications.</span></span>

## <span data-ttu-id="99bbc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99bbc-104">SYNTAX</span></span>

### <span data-ttu-id="99bbc-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="99bbc-105">Interactive (Default)</span></span>
```
Add-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99bbc-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="99bbc-106">ByObject</span></span>
```
Add-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99bbc-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="99bbc-107">ByResourceId</span></span>
```
Add-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99bbc-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="99bbc-108">DESCRIPTION</span></span>
<span data-ttu-id="99bbc-109">Il cmdlet **Add-AzKeyVaultCertificateContact** aggiunge un contatto per un vault delle chiavi per le notifiche sui certificati nel Vault delle chiavi di Azure.</span><span class="sxs-lookup"><span data-stu-id="99bbc-109">The **Add-AzKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="99bbc-110">Il contatto riceve gli aggiornamenti su eventi come la scadenza del certificato, il certificato rinnovato e così via.</span><span class="sxs-lookup"><span data-stu-id="99bbc-110">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="99bbc-111">Questi eventi sono determinati dal criterio di certificato.</span><span class="sxs-lookup"><span data-stu-id="99bbc-111">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="99bbc-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99bbc-112">EXAMPLES</span></span>

### <span data-ttu-id="99bbc-113">Esempio 1: Aggiungere un contatto con certificato vault chiave</span><span class="sxs-lookup"><span data-stu-id="99bbc-113">Example 1: Add a key vault certificate contact</span></span>
```powershell
PS C:\> Add-AzKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email                    VaultName
-----                    ---------
patti.fuller@contoso.com ContosoKV01
```

<span data-ttu-id="99bbc-114">Questo comando aggiunge Patti Fuller come contatto certificato per il vault della chiave ContosoKV01 e restituisce l'elenco di contatti per il vault "ContosoKV01".</span><span class="sxs-lookup"><span data-stu-id="99bbc-114">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the list of contacts for the "ContosoKV01" vault.</span></span>

## <span data-ttu-id="99bbc-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99bbc-115">PARAMETERS</span></span>

### <span data-ttu-id="99bbc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99bbc-116">-DefaultProfile</span></span>
<span data-ttu-id="99bbc-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="99bbc-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99bbc-118">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="99bbc-118">-EmailAddress</span></span>
<span data-ttu-id="99bbc-119">Specifica l'indirizzo di posta elettronica del contatto.</span><span class="sxs-lookup"><span data-stu-id="99bbc-119">Specifies the email address of the contact.</span></span>

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

### <span data-ttu-id="99bbc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99bbc-120">-InputObject</span></span>
<span data-ttu-id="99bbc-121">Oggetto KeyVault.</span><span class="sxs-lookup"><span data-stu-id="99bbc-121">KeyVault object.</span></span>

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

### <span data-ttu-id="99bbc-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99bbc-122">-PassThru</span></span>
<span data-ttu-id="99bbc-123">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="99bbc-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="99bbc-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="99bbc-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="99bbc-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99bbc-125">-ResourceId</span></span>
<span data-ttu-id="99bbc-126">ID risorsa KeyVault.</span><span class="sxs-lookup"><span data-stu-id="99bbc-126">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="99bbc-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="99bbc-127">-VaultName</span></span>
<span data-ttu-id="99bbc-128">Specifica il nome del vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="99bbc-128">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="99bbc-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="99bbc-129">-Confirm</span></span>
<span data-ttu-id="99bbc-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99bbc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99bbc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99bbc-131">-WhatIf</span></span>
<span data-ttu-id="99bbc-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99bbc-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99bbc-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="99bbc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99bbc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99bbc-134">CommonParameters</span></span>
<span data-ttu-id="99bbc-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99bbc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99bbc-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="99bbc-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99bbc-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="99bbc-137">INPUTS</span></span>

### <span data-ttu-id="99bbc-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="99bbc-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="99bbc-139">System.String</span><span class="sxs-lookup"><span data-stu-id="99bbc-139">System.String</span></span>

## <span data-ttu-id="99bbc-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99bbc-140">OUTPUTS</span></span>

### <span data-ttu-id="99bbc-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="99bbc-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="99bbc-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="99bbc-142">NOTES</span></span>

## <span data-ttu-id="99bbc-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99bbc-143">RELATED LINKS</span></span>

[<span data-ttu-id="99bbc-144">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="99bbc-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="99bbc-145">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="99bbc-145">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

