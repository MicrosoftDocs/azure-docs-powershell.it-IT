---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 6a59b49da2ae283af50487bec21da6c1d2457878
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687522"
---
# <span data-ttu-id="55aef-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="55aef-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="55aef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="55aef-102">SYNOPSIS</span></span>
<span data-ttu-id="55aef-103">Ottiene i contatti registrati per le notifiche dei certificati per un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="55aef-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55aef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="55aef-104">SYNTAX</span></span>

```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="55aef-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55aef-105">DESCRIPTION</span></span>
<span data-ttu-id="55aef-106">Il cmdlet **Get-AzureKeyVaultCertificateContact** ottiene i contatti registrati per le notifiche dei certificati per un Vault chiave in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="55aef-106">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="55aef-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="55aef-107">EXAMPLES</span></span>

### <span data-ttu-id="55aef-108">Esempio 1: ottenere tutti i contatti dei certificati</span><span class="sxs-lookup"><span data-stu-id="55aef-108">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="55aef-109">Questo comando consente di ottenere tutti i contatti per gli oggetti certificato nel caveau della chiave Contoso e quindi di archiviarli nella variabile $Contacts.</span><span class="sxs-lookup"><span data-stu-id="55aef-109">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="55aef-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="55aef-110">PARAMETERS</span></span>

### <span data-ttu-id="55aef-111">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="55aef-111">-VaultName</span></span>
<span data-ttu-id="55aef-112">Specifica il nome del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="55aef-112">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="55aef-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55aef-113">-DefaultProfile</span></span>
<span data-ttu-id="55aef-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="55aef-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55aef-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55aef-115">CommonParameters</span></span>
<span data-ttu-id="55aef-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55aef-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55aef-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55aef-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55aef-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="55aef-118">INPUTS</span></span>

## <span data-ttu-id="55aef-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="55aef-119">OUTPUTS</span></span>

### <span data-ttu-id="55aef-120">Elenco<Microsoft. Azure. Commands. Vault. Models. KeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="55aef-120">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="55aef-121">Note</span><span class="sxs-lookup"><span data-stu-id="55aef-121">NOTES</span></span>

## <span data-ttu-id="55aef-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="55aef-122">RELATED LINKS</span></span>

[<span data-ttu-id="55aef-123">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="55aef-123">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="55aef-124">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="55aef-124">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

