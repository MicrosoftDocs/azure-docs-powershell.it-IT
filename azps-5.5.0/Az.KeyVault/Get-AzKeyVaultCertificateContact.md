---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultCertificateContact.md
ms.openlocfilehash: ca7f0f87ebcbad3d613939f2e73a743763b134c9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188190"
---
# <span data-ttu-id="5e1ea-101">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="5e1ea-101">Get-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="5e1ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e1ea-102">SYNOPSIS</span></span>
<span data-ttu-id="5e1ea-103">Recupera i contatti registrati per le notifiche sui certificati per un vault chiave.</span><span class="sxs-lookup"><span data-stu-id="5e1ea-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

## <span data-ttu-id="5e1ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e1ea-104">SYNTAX</span></span>

### <span data-ttu-id="5e1ea-105">VaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5e1ea-105">VaultName (Default)</span></span>
```
Get-AzKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5e1ea-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5e1ea-106">ByInputObject</span></span>
```
Get-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5e1ea-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5e1ea-107">ByResourceId</span></span>
```
Get-AzKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e1ea-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5e1ea-108">DESCRIPTION</span></span>
<span data-ttu-id="5e1ea-109">Il cmdlet **Get-AzKeyVaultCertificateContact** ottiene i contatti registrati per le notifiche sui certificati per un vault chiave nel Vault delle chiavi di Azure.</span><span class="sxs-lookup"><span data-stu-id="5e1ea-109">The **Get-AzKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="5e1ea-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e1ea-110">EXAMPLES</span></span>

### <span data-ttu-id="5e1ea-111">Esempio 1: Recuperare tutti i contatti dei certificati</span><span class="sxs-lookup"><span data-stu-id="5e1ea-111">Example 1: Get all certificate contacts</span></span>
```powershell
PS C:\> $Contacts = Get-AzKeyVaultCertificateContact -VaultName "Contoso"

Email                   VaultName
-----                   ---------
username@microsoft.com  Contoso
username1@microsoft.com Contoso
```

<span data-ttu-id="5e1ea-112">Questo comando recupera tutti i contatti per gli oggetti certificato nel vault della chiave Contoso e quindi li archivia nella variabile $Contacts certificato.</span><span class="sxs-lookup"><span data-stu-id="5e1ea-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="5e1ea-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e1ea-113">PARAMETERS</span></span>

### <span data-ttu-id="5e1ea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e1ea-114">-DefaultProfile</span></span>
<span data-ttu-id="5e1ea-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="5e1ea-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e1ea-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e1ea-116">-InputObject</span></span>
<span data-ttu-id="5e1ea-117">Oggetto KeyVault.</span><span class="sxs-lookup"><span data-stu-id="5e1ea-117">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e1ea-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e1ea-118">-ResourceId</span></span>
<span data-ttu-id="5e1ea-119">Id KeyVault.</span><span class="sxs-lookup"><span data-stu-id="5e1ea-119">KeyVault Id.</span></span>

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

### <span data-ttu-id="5e1ea-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5e1ea-120">-VaultName</span></span>
<span data-ttu-id="5e1ea-121">Specifica il nome del vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="5e1ea-121">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: VaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e1ea-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e1ea-122">CommonParameters</span></span>
<span data-ttu-id="5e1ea-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e1ea-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e1ea-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5e1ea-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e1ea-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="5e1ea-125">INPUTS</span></span>

### <span data-ttu-id="5e1ea-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="5e1ea-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="5e1ea-127">System.String</span><span class="sxs-lookup"><span data-stu-id="5e1ea-127">System.String</span></span>

## <span data-ttu-id="5e1ea-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e1ea-128">OUTPUTS</span></span>

### <span data-ttu-id="5e1ea-129">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="5e1ea-129">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="5e1ea-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="5e1ea-130">NOTES</span></span>

## <span data-ttu-id="5e1ea-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e1ea-131">RELATED LINKS</span></span>

[<span data-ttu-id="5e1ea-132">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="5e1ea-132">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="5e1ea-133">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="5e1ea-133">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

