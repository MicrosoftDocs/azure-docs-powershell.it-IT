---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 5b6661bada9b63485f937a0401064de2c33e3336
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189699"
---
# <span data-ttu-id="e47c8-101">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e47c8-101">Add-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="e47c8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e47c8-102">SYNOPSIS</span></span>
<span data-ttu-id="e47c8-103">Aggiunge un contatto per le notifiche dei certificati.</span><span class="sxs-lookup"><span data-stu-id="e47c8-103">Adds a contact for certificate notifications.</span></span>

## <span data-ttu-id="e47c8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e47c8-104">SYNTAX</span></span>

### <span data-ttu-id="e47c8-105">Interattivo (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e47c8-105">Interactive (Default)</span></span>
```
Add-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e47c8-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="e47c8-106">ByObject</span></span>
```
Add-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e47c8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e47c8-107">ByResourceId</span></span>
```
Add-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e47c8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e47c8-108">DESCRIPTION</span></span>
<span data-ttu-id="e47c8-109">Il cmdlet **Add-AzKeyVaultCertificateContact** aggiunge un contatto per un Vault chiave per le notifiche dei certificati in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="e47c8-109">The **Add-AzKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="e47c8-110">Il contatto riceve gli aggiornamenti sugli eventi, ad esempio un certificato vicino alla scadenza, un certificato rinnovato e così via.</span><span class="sxs-lookup"><span data-stu-id="e47c8-110">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="e47c8-111">Questi eventi sono determinati dal criterio del certificato.</span><span class="sxs-lookup"><span data-stu-id="e47c8-111">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="e47c8-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e47c8-112">EXAMPLES</span></span>

### <span data-ttu-id="e47c8-113">Esempio 1: aggiungere un contatto Key Vault certificate</span><span class="sxs-lookup"><span data-stu-id="e47c8-113">Example 1: Add a key vault certificate contact</span></span>
```powershell
PS C:\> Add-AzKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email                    VaultName
-----                    ---------
patti.fuller@contoso.com ContosoKV01
```

<span data-ttu-id="e47c8-114">Questo comando aggiunge Patti Fuller come contatto di certificato per il Vault Key di ContosoKV01 e restituisce l'elenco dei contatti per il Vault "ContosoKV01".</span><span class="sxs-lookup"><span data-stu-id="e47c8-114">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the list of contacts for the "ContosoKV01" vault.</span></span>

## <span data-ttu-id="e47c8-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e47c8-115">PARAMETERS</span></span>

### <span data-ttu-id="e47c8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e47c8-116">-DefaultProfile</span></span>
<span data-ttu-id="e47c8-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e47c8-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e47c8-118">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="e47c8-118">-EmailAddress</span></span>
<span data-ttu-id="e47c8-119">Specifica l'indirizzo di posta elettronica del contatto.</span><span class="sxs-lookup"><span data-stu-id="e47c8-119">Specifies the email address of the contact.</span></span>

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

### <span data-ttu-id="e47c8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e47c8-120">-InputObject</span></span>
<span data-ttu-id="e47c8-121">Oggetto di Vault.</span><span class="sxs-lookup"><span data-stu-id="e47c8-121">KeyVault object.</span></span>

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

### <span data-ttu-id="e47c8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e47c8-122">-PassThru</span></span>
<span data-ttu-id="e47c8-123">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="e47c8-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e47c8-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="e47c8-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e47c8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e47c8-125">-ResourceId</span></span>
<span data-ttu-id="e47c8-126">ID risorsa di un Vault.</span><span class="sxs-lookup"><span data-stu-id="e47c8-126">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="e47c8-127">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="e47c8-127">-VaultName</span></span>
<span data-ttu-id="e47c8-128">Specifica il nome del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="e47c8-128">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="e47c8-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e47c8-129">-Confirm</span></span>
<span data-ttu-id="e47c8-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e47c8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e47c8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e47c8-131">-WhatIf</span></span>
<span data-ttu-id="e47c8-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e47c8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e47c8-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e47c8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e47c8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e47c8-134">CommonParameters</span></span>
<span data-ttu-id="e47c8-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e47c8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e47c8-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e47c8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e47c8-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e47c8-137">INPUTS</span></span>

### <span data-ttu-id="e47c8-138">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="e47c8-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="e47c8-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e47c8-139">System.String</span></span>

## <span data-ttu-id="e47c8-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e47c8-140">OUTPUTS</span></span>

### <span data-ttu-id="e47c8-141">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e47c8-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="e47c8-142">Note</span><span class="sxs-lookup"><span data-stu-id="e47c8-142">NOTES</span></span>

## <span data-ttu-id="e47c8-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e47c8-143">RELATED LINKS</span></span>

[<span data-ttu-id="e47c8-144">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e47c8-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="e47c8-145">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e47c8-145">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)
