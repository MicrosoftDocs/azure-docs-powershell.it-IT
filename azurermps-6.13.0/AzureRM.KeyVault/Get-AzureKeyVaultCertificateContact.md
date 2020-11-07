---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 31619366c1d2a1a025cb7ff563a04b166abb2a46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687315"
---
# <span data-ttu-id="ab8ae-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="ab8ae-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="ab8ae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ab8ae-102">SYNOPSIS</span></span>
<span data-ttu-id="ab8ae-103">Ottiene i contatti registrati per le notifiche dei certificati per un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="ab8ae-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab8ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab8ae-104">SYNTAX</span></span>

### <span data-ttu-id="ab8ae-105">VAULTNAME (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ab8ae-105">VaultName (Default)</span></span>
```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ab8ae-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ab8ae-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ab8ae-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ab8ae-107">ByResourceId</span></span>
```
Get-AzureKeyVaultCertificateContact [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ab8ae-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab8ae-108">DESCRIPTION</span></span>
<span data-ttu-id="ab8ae-109">Il cmdlet **Get-AzureKeyVaultCertificateContact** ottiene i contatti registrati per le notifiche dei certificati per un Vault chiave in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="ab8ae-109">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="ab8ae-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab8ae-110">EXAMPLES</span></span>

### <span data-ttu-id="ab8ae-111">Esempio 1: ottenere tutti i contatti dei certificati</span><span class="sxs-lookup"><span data-stu-id="ab8ae-111">Example 1: Get all certificate contacts</span></span>
```powershell
PS C:\> $Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"

Email                   VaultName
-----                   ---------
username@microsoft.com  Contoso
username1@microsoft.com Contoso
```

<span data-ttu-id="ab8ae-112">Questo comando consente di ottenere tutti i contatti per gli oggetti certificato nel caveau della chiave Contoso e quindi di archiviarli nella variabile $Contacts.</span><span class="sxs-lookup"><span data-stu-id="ab8ae-112">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="ab8ae-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ab8ae-113">PARAMETERS</span></span>

### <span data-ttu-id="ab8ae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab8ae-114">-DefaultProfile</span></span>
<span data-ttu-id="ab8ae-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ab8ae-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab8ae-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab8ae-116">-InputObject</span></span>
<span data-ttu-id="ab8ae-117">Oggetto di Vault.</span><span class="sxs-lookup"><span data-stu-id="ab8ae-117">KeyVault object.</span></span>

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

### <span data-ttu-id="ab8ae-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab8ae-118">-ResourceId</span></span>
<span data-ttu-id="ab8ae-119">ID del Vault.</span><span class="sxs-lookup"><span data-stu-id="ab8ae-119">KeyVault Id.</span></span>

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

### <span data-ttu-id="ab8ae-120">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="ab8ae-120">-VaultName</span></span>
<span data-ttu-id="ab8ae-121">Specifica il nome del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="ab8ae-121">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="ab8ae-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab8ae-122">CommonParameters</span></span>
<span data-ttu-id="ab8ae-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab8ae-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab8ae-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab8ae-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab8ae-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ab8ae-125">INPUTS</span></span>

### <span data-ttu-id="ab8ae-126">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="ab8ae-126">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="ab8ae-127">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ab8ae-127">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="ab8ae-128">System. String</span><span class="sxs-lookup"><span data-stu-id="ab8ae-128">System.String</span></span>

## <span data-ttu-id="ab8ae-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab8ae-129">OUTPUTS</span></span>

### <span data-ttu-id="ab8ae-130">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="ab8ae-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="ab8ae-131">Note</span><span class="sxs-lookup"><span data-stu-id="ab8ae-131">NOTES</span></span>

## <span data-ttu-id="ab8ae-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab8ae-132">RELATED LINKS</span></span>

[<span data-ttu-id="ab8ae-133">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="ab8ae-133">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="ab8ae-134">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="ab8ae-134">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

