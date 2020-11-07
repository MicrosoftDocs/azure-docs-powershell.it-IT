---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 200C68A3-A79C-4517-8E5D-8128F6C73A5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificatecontact
schema: 2.0.0
ms.openlocfilehash: d6d2070afcb4a5b9b0b13af1fa54dc93621c5a97
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866332"
---
# <span data-ttu-id="34450-101">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="34450-101">Get-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="34450-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="34450-102">SYNOPSIS</span></span>
<span data-ttu-id="34450-103">Ottiene i contatti registrati per le notifiche dei certificati per un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="34450-103">Gets contacts that are registered for certificate notifications for a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34450-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34450-104">SYNTAX</span></span>

```
Get-AzureKeyVaultCertificateContact [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="34450-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34450-105">DESCRIPTION</span></span>
<span data-ttu-id="34450-106">Il cmdlet **Get-AzureKeyVaultCertificateContact** ottiene i contatti registrati per le notifiche dei certificati per un Vault chiave in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="34450-106">The **Get-AzureKeyVaultCertificateContact** cmdlet gets contacts that are registered for certificate notifications for a key vault in Azure Key Vault.</span></span>

## <span data-ttu-id="34450-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34450-107">EXAMPLES</span></span>

### <span data-ttu-id="34450-108">Esempio 1: ottenere tutti i contatti dei certificati</span><span class="sxs-lookup"><span data-stu-id="34450-108">Example 1: Get all certificate contacts</span></span>
```
PS C:\>$Contacts = Get-AzureKeyVaultCertificateContact -VaultName "Contoso"
```

<span data-ttu-id="34450-109">Questo comando consente di ottenere tutti i contatti per gli oggetti certificato nel caveau della chiave Contoso e quindi di archiviarli nella variabile $Contacts.</span><span class="sxs-lookup"><span data-stu-id="34450-109">This command gets all of the contacts for the certificate objects in the Contoso key vault, and then stores them in the $Contacts variable.</span></span>

## <span data-ttu-id="34450-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="34450-110">PARAMETERS</span></span>

### <span data-ttu-id="34450-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34450-111">-DefaultProfile</span></span>
<span data-ttu-id="34450-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="34450-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34450-113">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="34450-113">-VaultName</span></span>
<span data-ttu-id="34450-114">Specifica il nome del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="34450-114">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="34450-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34450-115">CommonParameters</span></span>
<span data-ttu-id="34450-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34450-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34450-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34450-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34450-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="34450-118">INPUTS</span></span>

## <span data-ttu-id="34450-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34450-119">OUTPUTS</span></span>

### <span data-ttu-id="34450-120">Elenco<Microsoft. Azure. Commands. Vault. Models. KeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="34450-120">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="34450-121">Note</span><span class="sxs-lookup"><span data-stu-id="34450-121">NOTES</span></span>

## <span data-ttu-id="34450-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34450-122">RELATED LINKS</span></span>

[<span data-ttu-id="34450-123">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="34450-123">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="34450-124">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="34450-124">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

